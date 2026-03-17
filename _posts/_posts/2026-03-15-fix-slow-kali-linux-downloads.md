---
layout: post
title: "How to Fix Slow Downloads in Kali Linux — Permanently"
date: 2026-03-15
categories: linux
tags: kali-linux terminal beginners optimization
---

Slow downloads in Kali Linux are one of those problems that seem minor until you're waiting twenty minutes for a tool that should take thirty seconds. Most people assume it's their internet connection and leave it at that. It usually isn't.

There are three actual causes: bad repository servers, DNS issues, and the package manager downloading one file at a time. All three are fixable in under five minutes.

---

## Why Kali Downloads Are Slow

When you run `apt install` or `apt update`, Kali connects to a repository server to fetch packages. If that server is geographically distant, overloaded, or misconfigured for your network, every download crawls. IPv6 misconfiguration makes this worse — your system tries an IPv6 connection first, fails, then falls back to IPv4, adding latency to every single request.

The fix is straightforward: point Kali at the right servers, fix your DNS, and make the package manager download things in parallel instead of sequentially.

---

## Step 1 — Fix the Repository

This is the most important change. Open your terminal and run:
```bash
sudo nano /etc/apt/sources.list
```

Delete everything in the file and replace it with exactly this:
```bash
deb http://http.kali.org/kali kali-rolling main contrib non-free
```

Save the file with CTRL + O, press Enter to confirm, then exit with CTRL + X.

This points your system to Kali's official rolling repository with HTTP, which avoids the IPv6 fallback problem that causes a lot of the latency people blame on slow internet.

---

## Step 2 — Let the System Find the Fastest Mirror

Instead of manually guessing which server is fastest for your location, let a tool do it. Run:
```bash
sudo apt install netselect-apt
sudo netselect-apt kali
```

`netselect-apt` pings every available Kali mirror and ranks them by speed. It then generates a new `sources.list` file pointing at the fastest one for your network. Replace your existing sources.list with that file and you're downloading from the optimal server automatically.

If you just want to update everything quickly without the mirror selection step, this also works:
```bash
sudo apt update && sudo apt install kali-linux-large
```

---

## Step 3 — Fix DNS

This one gets overlooked constantly. Your system's DNS resolver affects how quickly it looks up server addresses before downloads even begin. Slow or unreliable DNS adds hidden latency to every network operation.

Open your DNS configuration:
```bash
sudo nano /etc/resolv.conf
```

Add these lines:
```bash
nameserver 8.8.8.8
nameserver 8.8.4.4
nameserver 1.1.1.1
```

These are Google's and Cloudflare's public DNS servers. Both are fast, reliable, and available globally. Save and exit the same way as before.

---

## Step 4 — Parallel Downloads with apt-fast

By default, apt downloads one package at a time. If you're installing something with twenty dependencies, it fetches them one after another. apt-fast changes this by opening multiple simultaneous connections, which on a decent internet connection can cut install times dramatically.

Install it:
```bash
sudo apt install apt-fast
```

Then use it exactly like you'd use apt:
```bash
sudo apt-fast upgrade
```

The difference on a large upgrade or a tool with many dependencies is significant. On a slow connection it helps less — but it still helps.

---

## Step 5 — Clean and Update

Run these three commands in sequence to clear cached package data, refresh your package lists, and apply any pending updates:
```bash
sudo apt clean
sudo apt update
sudo apt upgrade -y
```

`apt clean` removes cached package files that are no longer needed. `apt update` pulls fresh package lists from your newly configured repositories. `apt upgrade` installs everything that's pending.

After this sequence your system is clean, updated, and configured for maximum download speed.

---

## If It's Still Slow

If downloads are still slow after all five steps, the bottleneck is your internet connection itself — not Kali, not the repositories, not the package manager.

You can verify this by running a speed test from the terminal:
```bash
curl -s https://raw.githubusercontent.com/sivel/speedtest-cli/master/speedtest.py | python3 -
```

If your actual download speed is low, no amount of configuration changes will help. That's an ISP problem, not a Linux problem.

Everything else — repository configuration, DNS, parallel downloads — is within your control and worth fixing regardless. Even on a fast connection, a poorly configured apt setup wastes time on every single package operation.

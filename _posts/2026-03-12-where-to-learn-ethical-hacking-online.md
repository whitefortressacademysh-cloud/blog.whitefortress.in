---
layout: post
title: "Where to Learn Ethical Hacking Online — A Honest Guide for Beginners"
date: 2026-03-12
categories: resources
tags: beginners learning ethical-hacking platforms roadmap
---

Every week someone asks me the same question. "I want to get into ethical hacking — where do I start?"

It's a fair question with an overwhelming number of answers. There are hundreds of courses, platforms, YouTube channels, and bootcamps all claiming to turn you into a penetration tester. Some of them are genuinely good. A lot of them are not.

This is my honest breakdown of where to actually spend your time.

---

## Before You Pick a Platform

One thing worth saying upfront — ethical hacking is not something you learn by watching videos. You learn it by doing. The best platforms understand this and put you in front of actual machines to attack, not just slides explaining how attacks work in theory.

Keep that in mind as you go through this list. If a resource doesn't give you hands-on practice, treat it as supplementary material, not your primary learning path.

---

## TryHackMe — Best Starting Point for Complete Beginners

If you have zero background in cybersecurity, start here. TryHackMe breaks everything down into guided rooms — small, focused challenges that walk you through a concept step by step, entirely in your browser. No setup required, no virtual machine to configure, no prerequisites.

The free tier gives you access to a significant amount of content. Their learning paths for complete beginners are genuinely well structured and will take you from "what is a terminal" to "I just exploited my first machine" in a matter of weeks if you're consistent.

The community is large and active. When you get stuck — and you will get stuck — someone has usually already asked the same question.

Start with the Pre-Security path, then move to the Jr Penetration Tester path. Those two alone will give you a solid foundation.

---

## Hack The Box — Where You Go After TryHackMe

HackTheBox has a reputation for being difficult, and that reputation is earned. The retired machines are among the best practice you'll find anywhere for web application testing, privilege escalation, and Active Directory attacks.

HTB Academy, their structured learning platform, is more beginner-accessible than the main platform and has significantly improved over the past two years. A lot of the modules are free. The paid content is reasonably priced.

The main HTB platform — the "hack these machines" side — is best approached after you have some foundation. Jumping in cold is demoralising. But once you're ready, the quality of the challenges is genuinely excellent. A retired HTB machine in your portfolio carries weight when you're applying for jobs or showing your skills to anyone serious.

---

## OverTheWire — Free, Brutal, Brilliant

OverTheWire is entirely free and entirely command-line based. The wargames start simple — Bandit teaches you Linux fundamentals through increasingly tricky challenges — and get progressively harder from there.

There are no videos. No hand-holding. Just you, a terminal, and a problem to solve.

This is not a comfortable learning experience. It is, however, extremely effective at building real skill. The people who stick with OverTheWire develop a comfort with the command line that takes others months to reach.

Start with Bandit. Once you finish it, you'll understand why it's recommended constantly.

---

## YouTube — Free and Underrated

For concept explanations, tool walkthroughs, and CTF writeups, YouTube is genuinely useful. The problem is quality varies enormously.

A few channels consistently produce content that's actually worth your time. NetworkChuck is good for networking fundamentals. IppSec's HTB machine walkthrough videos are essential watching if you're working through retired boxes — the way he thinks through problems out loud is worth studying.

And then there's White Fortress Academy.

If you're reading this blog, you probably already know about us — but if not, the [White Fortress Academy YouTube channel](https://www.youtube.com/@WhiteFortressSecurity) covers penetration testing, offensive security techniques, and practical cybersecurity content in a way that doesn't assume you already know everything. The focus is on understanding what you're doing and why, not just copying commands.

For Hindi-speaking learners especially, good technical cybersecurity content in your own language is hard to find. That's something we're actively working to change.

---

## Offensive Security — When You're Ready for the Real Thing

Offensive Security runs the OSCP certification, which is widely considered the gold standard entry-level penetration testing credential. The exam is 24 hours of live machines that you have to hack, followed by a 24-hour report writing window. It is not easy. It is not meant to be.

The PEN-200 course that comes with the OSCP exam is substantial. The platform — which they call the Offensive Security Proving Grounds — is excellent for hands-on practice.

Don't start here. Come back to this after you've done a few months on TryHackMe and HackTheBox. But keep it in your sights. In most penetration testing job postings, OSCP is either required or strongly preferred.

---

## A Roadmap That Actually Makes Sense

The mistake most beginners make is jumping between resources without a clear direction. You'll learn faster with a structured path, even a simple one.

Spend the first month or two on TryHackMe's beginner paths. Get comfortable with Linux, basic networking, and the command line. Don't rush this — everything else builds on it.

Once you feel comfortable, move to HTB Academy for more structured technical content alongside continued TryHackMe practice. Watch IppSec's retired machine walkthroughs to see how experienced people approach problems.

At the same time, subscribe to White Fortress Academy on YouTube. Use it alongside your lab practice — the channel bridges the gap between raw technical skill and understanding the methodology behind what you're doing.

When you're consistently solving medium difficulty machines on HackTheBox, you're ready to attempt the OSCP. That's the natural progression.

The whole journey, done properly with consistent effort, takes somewhere between six months and a year for most people starting from zero. Anyone promising to make you a penetration tester in thirty days is lying to you.

---

## What Matters More Than the Platform You Choose

Consistency beats everything else. An hour a day for a year produces better results than a hundred hours crammed into a single month.

Document everything. Keep notes on every machine you solve, every technique you learn, every tool you use. This habit builds your own reference library over time and forces you to actually understand what you've done rather than just follow steps.

Join communities. The HackTheBox Discord, the TryHackMe Discord, Reddit's r/netsec and r/AskNetsec. Ask questions. Answer questions when you can. Explaining something to someone else is one of the fastest ways to solidify your own understanding.

And do CTFs. Capture The Flag competitions are time-limited hacking challenges with a huge range of difficulty. CTFtime.org lists upcoming competitions. Participating regularly exposes you to problem types you won't encounter on standard lab platforms and forces you to learn under pressure.

The resources exist. They're mostly free or cheap. The only real barrier is putting in the hours.

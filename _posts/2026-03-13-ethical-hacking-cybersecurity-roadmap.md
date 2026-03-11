---
layout: post
title: "The Ethical Hacking and Cybersecurity Roadmap for 2025 — From Zero to Job-Ready"
date: 2026-03-13
categories: roadmap
tags: ethical-hacking cybersecurity beginners career certifications
---

People overcomplicate this. They spend weeks arguing about which certification to do first, which programming language to learn, whether they need a degree. Meanwhile they haven't opened a terminal once.

This is a straight roadmap. No fluff, no detours. If you follow it with consistent effort, you will be job-ready in 12 to 18 months starting from zero. If you already have some background, faster.

There are two broad directions in cybersecurity — offensive and defensive. Offensive security means you are the one attacking systems to find weaknesses before real attackers do. Penetration testing, red teaming, bug bounty hunting. Defensive security means you protect, monitor, and respond. SOC analyst, incident response, threat hunting. This roadmap covers the path into offensive security specifically, which is what most people mean when they say "I want to learn ethical hacking." The defensive path shares the same foundation — it just branches differently at the intermediate stage.

---

## Phase 1 — Build the Foundation (Months 1 to 3)

Everything in cybersecurity sits on top of three things: operating systems, networking, and basic scripting. Skip this phase and you will hit a wall every time you try to understand anything beyond surface-level concepts.

### Linux

Most of the tools you will use as a penetration tester run on Linux. Most of the servers you will be testing run Linux. Get comfortable with it.

Install Kali Linux in a virtual machine — VirtualBox is free and works fine. Learn to navigate the file system, manage files and permissions, run processes, use pipes and redirects, and write basic shell scripts. You do not need to become a Linux administrator. You need to be comfortable enough that the terminal doesn't slow you down.

OverTheWire's Bandit wargame is the best free resource for this. It teaches Linux through challenges instead of lectures. Work through all 34 levels.

### Networking

You cannot hack what you don't understand. Networks carry all the traffic you will be intercepting, redirecting, and exploiting. You need to understand how they work at a practical level.

Learn the TCP/IP model, how DNS works, what HTTP and HTTPS actually do under the hood, how subnetting works, what common ports and protocols are used for, and how routing and switching function at a basic level. CompTIA Network+ covers all of this if you want a structured syllabus to follow. You don't necessarily need to sit the exam — the curriculum is the useful part at this stage.

Professor Messer's free Network+ videos on YouTube are good enough to get through this without spending money.

### Python Basics

You don't need to be a developer. But you do need to be able to read scripts, modify existing tools, and write simple automation. Python is the right starting language for this — it's readable, widely used in security tooling, and quick to pick up.

Spend a few weeks on Python basics: variables, loops, conditionals, functions, file handling, working with requests and sockets. That's enough to start being useful. You can go deeper later.

---

## Phase 2 — Learn to Think Offensively (Months 3 to 8)

Once you have a foundation, you start learning how attacks actually work. Not the theory — the practice.

### TryHackMe

Start with TryHackMe's Pre-Security and Jr Penetration Tester learning paths. These are guided, browser-based, and take you through web application attacks, network exploitation, privilege escalation, and basic red team techniques in a structured way.

Do every room. Don't skip the ones that feel easy. And don't just follow the steps — understand why each step works. That habit is what separates people who can solve new problems from people who can only follow walkthroughs.

### Hack The Box Academy

Once you're partway through TryHackMe, start HTB Academy alongside it. The modules on web application testing, active directory fundamentals, and privilege escalation are particularly good. Much of the content is free.

The main HackTheBox platform — where you hack actual machines — is best approached after a few months on these structured platforms. When you do start, begin with easy retired machines and watch IppSec's walkthrough videos after you've attempted each one yourself. His thought process is worth studying as closely as the technical content.

### What You Should Be Practicing

By the end of Phase 2 you should be comfortable with the following:

Reconnaissance — gathering information about a target using tools like Nmap, Gobuster, and WHOIS. Understanding what you're looking at before you start attacking.

Web application attacks — SQL injection, cross-site scripting, file inclusion vulnerabilities, broken authentication, IDOR. The OWASP Top 10 is your curriculum here.

Network exploitation — exploiting misconfigured services, working with Metasploit for common exploits, basic man-in-the-middle techniques.

Privilege escalation — once you're on a machine with limited access, how do you get to root or SYSTEM? This is one of the most important skill areas in pentesting and deserves dedicated study. GTFOBins and HackTricks are essential references.

Basic Active Directory — most corporate environments run Windows with Active Directory. Understanding how it works and how it gets attacked is essential for any professional pentesting role.

---

## Phase 3 — Certifications That Actually Matter

Certifications get debated endlessly. Here is the straightforward version.

### CompTIA Security+

If you need a certification to get your first job or internship and you're coming from zero, Security+ is the entry point. It's vendor-neutral, widely recognised, DoD-approved, and validates that you understand security fundamentals. It is not a hacking certification — it's a baseline.

Cost is around $400 for the exam. Pass rate improves significantly with the Professor Messer study materials, which are free on YouTube.

### eJPT (eLearnSecurity Junior Penetration Tester)

This is where offensive security certifications start. The eJPT from INE is an entry-level, fully practical exam — no multiple choice questions, just a network you have to attack and compromise. It's affordable, beginner-accessible, and gives you something concrete to show for your early learning.

Do this before OSCP. It's good practice for the format and builds confidence.

### OSCP (Offensive Security Certified Professional)

This is the one that matters in penetration testing. If you want to work in offensive security professionally, OSCP is the target certification. The exam is 24 hours of live machines you have to compromise, followed by a 24-hour report writing window. It is difficult by design.

The PEN-200 course that comes with the OSCP exam is one of the best structured penetration testing curricula available. Work through the entire course before attempting the exam. Supplement it with HackTheBox machines, particularly the Proving Grounds practice lab that Offensive Security provides.

Expect to spend 3 to 6 months preparing seriously for OSCP after you already have a solid Phase 2 foundation. The pass rate is not published but it is not high. People who pass on their first attempt are typically the ones who did the work before booking the exam.

### CEH (Certified Ethical Hacker)

CEH from EC-Council is widely recognised on job postings, particularly in India and the Middle East. It is more theory-heavy and less respected than OSCP in purely technical circles, but it does open doors and some employers specifically require it. If you're targeting corporate or government roles in India, CEH has more practical value than it sometimes gets credit for.

---

## Phase 4 — Build Evidence of Skill

Certifications tell employers you passed an exam. Evidence of real skill is what gets you the actual job.

### CTFs (Capture The Flag)

CTF competitions are timed hacking challenges covering a range of categories — web exploitation, cryptography, forensics, reverse engineering, binary exploitation. They force you to solve problems you've never seen before under time pressure.

Participate in CTFs regularly from CTFtime.org. After competitions, read writeups from teams who solved challenges you couldn't. The community is generous with knowledge.

### Bug Bounty

Bug bounty platforms like HackerOne and Bugcrowd let you legally find vulnerabilities in real applications and get paid for valid findings. Starting out, don't expect immediate returns — focus on learning from disclosed reports first. Read public reports from top researchers. Understand the methodology, not just the vulnerability.

Even finding one valid low-severity bug on a public program tells an employer more about your practical ability than most certifications.

### Document Everything

Keep a public GitHub with notes, scripts, and writeups. Write up every HackTheBox machine you solve. Document your methodology, what worked, what didn't, and why. This builds your own reference library and demonstrates your thinking process to anyone who looks.

A well-maintained GitHub with consistent, thoughtful writeups is more compelling than a resume with no supporting evidence.

---

## Where White Fortress Academy Fits In

If you're going through this roadmap, the [White Fortress Academy YouTube channel](https://www.youtube.com/@WhiteFortressSecurity) is built for exactly this stage of learning. The content covers penetration testing techniques, offensive security concepts, and real-world methodology — explained in a way that connects the theory to what you actually do on a machine.

For learners who prefer content in Hindi, it is one of the few channels producing serious technical security content in the language without dumbing it down. Subscribe and use it alongside your lab practice — it works best as a complement to hands-on work, not a replacement for it.

---

## How Long Will This Take

Honestly — it depends entirely on how many hours you put in. With one focused hour per day you will be at an employable level in 12 to 18 months. With two to three hours per day, faster. With sporadic weekend sessions and long gaps, indefinitely.

The people who make it through this roadmap are not necessarily the smartest people. They are the most consistent ones. The material is not the barrier. Showing up regularly is.

There are 3.5 million unfilled cybersecurity jobs globally right now. The demand exists. The question is whether you put in the work to meet it.

Start with Bandit on OverTheWire tonight. That's the first step. Everything else follows from there.

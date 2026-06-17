# How to Use a VPS from Scratch: Complete Beginner's Setup Guide — What Is VPS Hosting, How to Connect via SSH, Install Software, and Which Plan Actually Fits You (Evoxt Pricing & Discount Inside)

So you've heard the term "VPS" thrown around a lot lately. Maybe you're running a website that keeps crashing under load, or you want to host a Discord bot, or someone in a tech forum told you to "just get a VPS" like it's the most obvious thing in the world. And now you're staring at a blank terminal window wondering what on earth you're supposed to do next.

Don't worry. That's exactly where this guide starts.

---

## What Is a VPS, and Why Should You Care?

Think of it like renting an apartment in a large building. You get your own space — your own dedicated CPU, RAM, and storage — and what your neighbors do in their apartments doesn't affect yours. That's the VPS model.

A **Virtual Private Server** is a virtualized instance carved out of a larger physical machine. You get root access, a dedicated IP, and full control over the operating system. It's more powerful than shared hosting (where you're sharing everything with strangers) and way cheaper than a dedicated server (where you rent the whole building).

**Why people switch to VPS:**

- Their website outgrows shared hosting
- They need to run 24/7 processes (bots, scrapers, automation)
- They want to self-host apps (Nextcloud, GitLab, WordPress)
- They need a stable environment for game servers or trading bots
- They want full control without paying enterprise prices

If any of those ring a bell, keep reading.

---

## Step 1: Choose a VPS Provider (And Pick the Right Plan)

Before you can do anything, you need a VPS. This is where most beginners overthink it. The honest advice: start small. You can always scale up.

One provider worth looking at seriously is **Evoxt** — a cloud VPS platform that's stood out in independent benchmarks for one specific reason: CPU clock speed. While AWS runs at 2.4 GHz and Azure at 2.3 GHz, Evoxt's machines turbo up to 6.0 GHz. For single-threaded workloads (which is most things, honestly), that gap is real and you'll feel it.

VPSBenchmarks, which independently buys and tests servers, ranked Evoxt 2nd Best VPS under $25 in 2025 and has placed it in the top 3 across multiple price brackets consistently since 2022. That's not a marketing claim — that's from a site that has no reason to be generous.

👉 [Check out Evoxt's full plan lineup here](https://bit.ly/Evoxt)

### Evoxt Standard Plans (US, UK, CA, DE, PL, NL, JP Tokyo, MY, AU)

| Plan | CPU | RAM | Storage | Monthly Transfer | Price |
|------|-----|-----|---------|-----------------|-------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 500 GB | $2.99/mo |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 750 GB | $4.99/mo |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 1000 GB | $5.99/mo |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 1500 GB | $6.95/mo |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 2000 GB | $11.99/mo |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 3000 GB | $14.99/mo |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 4000 GB | $23.99/mo |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 5000 GB | $29.99/mo |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 6000 GB | $47.99/mo |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 8000 GB | $60.95/mo |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 10 TB | $95.99/mo |

All plans include weekly automatic offsite backups at no extra charge. That's not standard in this price range — most providers charge for it.

### Premium Network Plans (Hong Kong · Japan Osaka)

If you need optimized routing to Asia — particularly CN2 routing through Hong Kong — Evoxt offers a Premium Network tier. Same plan specs, slightly reduced transfer quota, same pricing.

| Plan | CPU | RAM | Storage | Monthly Transfer | Price |
|------|-----|-----|---------|-----------------|-------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 250 GB | $2.99/mo |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 250 GB | $4.99/mo |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 500 GB | $5.99/mo |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 500 GB | $6.95/mo |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 1000 GB | $11.99/mo |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 1000 GB | $14.99/mo |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 2000 GB | $23.99/mo |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 2000 GB | $29.99/mo |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 3000 GB | $47.99/mo |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 3000 GB | $60.95/mo |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 5000 GB | $95.99/mo |

### Premium Plus Network Plans (Malaysia Premium)

For users in Malaysia who need the best local connectivity, peered with MyIX and major local ISPs:

| Plan | CPU | RAM | Storage | Monthly Transfer | Price |
|------|-----|-----|---------|-----------------|-------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 150 GB | $3.49/mo |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 250 GB | $4.99/mo |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 300 GB | $5.99/mo |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 300 GB | $6.95/mo |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 600 GB | $11.99/mo |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 700 GB | $14.99/mo |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 1000 GB | $23.99/mo |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 1250 GB | $29.99/mo |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 2000 GB | $47.99/mo |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 2500 GB | $60.95/mo |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 4000 GB | $95.99/mo |

**Quick tip on which plan to pick:** If you're not sure, start with VM-1 ($5.99/mo). It handles a typical WordPress site, a Discord bot, or a small automation task without breaking a sweat. The VM-1 also qualifies for the 40% recurring discount — more on that below.

👉 [Deploy your first Evoxt VPS now](https://bit.ly/Evoxt)

---

## Step 2: Deploy Your VPS and Get Your Credentials

Once you sign up and pick a plan, Evoxt will have your machine ready in under 3 minutes. During the setup you'll choose:

- **Region** — pick whichever data center is geographically closest to your users (or closest to you, if it's a personal project)
- **Operating System** — Ubuntu 22.04 LTS is the most beginner-friendly Linux option. If you need Windows, that's available too.
- **One-click apps** — Evoxt lets you skip the manual install and deploy WordPress, Docker, GitLab, Minecraft, and more with a single click

After deployment, you'll receive your VPS **IP address**, **root username**, and **root password** (or an SSH key option). Save these. You'll need them in the next step.

---

## Step 3: Connect to Your VPS via SSH

This is the part that trips most beginners. SSH (Secure Shell) is just a secure way to remotely control your server from your laptop. It sounds intimidating but it's three lines.

**On macOS or Linux:**

Open Terminal and type:

bash
ssh root@YOUR_VPS_IP


Replace `YOUR_VPS_IP` with the IP address from your Evoxt dashboard. When it asks if you trust the connection, type `yes`. Then enter your password. Done — you're in.

**On Windows:**

You have two options. If you're on Windows 10/11, just open Windows Terminal (search for it in the Start menu) and run the same `ssh root@YOUR_VPS_IP` command. If that's not available, download PuTTY from the official site, enter your IP in the "Host Name" field, leave the port at 22, and click Open.

> **Note:** When you type your password, the terminal won't show any characters or dots. That's normal and intentional. Just type it and hit Enter.

---

## Step 4: First Things to Do After Logging In

You've got a fresh VPS. Here's the order of operations for the first 10 minutes:

**1. Update the system**

bash
apt update && apt upgrade -y


This pulls the latest security patches. On a fresh install, always do this first. Non-negotiable.

**2. Create a non-root user**

Running everything as root is like doing your taxes with the keys to your entire house in your hand. One mistake and it's catastrophic. Create a regular user:

bash
adduser yourusername
usermod -aG sudo yourusername


Log out and log back in as that user going forward.

**3. Set up a basic firewall**

Ubuntu comes with UFW (Uncomplicated Firewall). Enable it:

bash
ufw allow OpenSSH
ufw enable


This makes sure you don't accidentally lock yourself out of SSH access when tightening rules later.

**4. Switch to SSH key authentication (optional but recommended)**

Passwords work fine, but SSH keys are more secure. On your local machine (not the VPS), generate a key pair:

bash
ssh-keygen -t rsa -b 4096


Then upload the public key to your VPS. From this point on, you log in with your key instead of a password — and brute-force attacks become largely irrelevant.

Evoxt also has a built-in firewall panel in their control dashboard, so you can set rules without even touching the terminal. That's a nice fallback if you're not comfortable with the command line yet.

---

## Step 5: Install What You Actually Need

Here's where the VPS becomes useful. What you install depends entirely on what you're trying to do:

### Hosting a website

Install a web server. Nginx is lightweight and fast:

bash
apt install nginx -y
systemctl start nginx
systemctl enable nginx


Then open port 80 (HTTP) and 443 (HTTPS) in your firewall. Your site will be live at your VPS IP.

For WordPress specifically, Evoxt offers a one-click deployment with OpenLiteSpeed — which is significantly faster than a standard Apache + WordPress stack for most use cases.

### Running a Discord or Telegram bot

Most bots are Python or Node.js. Install the runtime:

bash
# Python
apt install python3 python3-pip -y

# Node.js
apt install nodejs npm -y


Upload your bot files, run them with `screen` or `tmux` so they keep running after you close the terminal, and you're done.

### Self-hosting apps (Nextcloud, GitLab, etc.)

Evoxt has one-click installers for both. Or you can deploy via Docker:

bash
apt install docker.io -y
systemctl start docker
systemctl enable docker


Docker makes app management dramatically cleaner — you install containers instead of manually configuring system packages, and teardown is just as simple.

---

## Step 6: Connect a Domain (If You Have One)

If you're running a website, you'll want a real domain pointing to your VPS IP instead of people typing `192.168.x.x` into a browser.

1. Get your VPS IP from the Evoxt dashboard
2. Go to your domain registrar and create an **A record** pointing your domain to that IP
3. DNS propagation takes anywhere from a few minutes to 48 hours (usually faster)
4. Install an SSL certificate with Let's Encrypt:

bash
apt install certbot python3-certbot-nginx -y
certbot --nginx -d yourdomain.com


That gives you HTTPS for free, auto-renewed.

---

## Step 7: Keep Things Running Smoothly

A VPS isn't completely set-and-forget, but the maintenance is minimal once you're set up. A few habits that save headaches:

**Run updates periodically.** Once a week is fine for most people:

bash
apt update && apt upgrade -y


**Check your resource usage.** The Evoxt control panel shows CPU, RAM, and network metrics over time. If you're consistently hitting 80%+ CPU, it's time to scale up — which Evoxt lets you do by adding individual vCores or RAM without changing your whole plan.

**Rely on the backups.** Evoxt automatically backs up your VPS every week to an offsite location at zero cost. If something goes catastrophically wrong — a bad update, an accidental `rm -rf`, whatever — you can restore from backup through the dashboard. This is genuinely rare to get free at this price point.

**Use the VNC browser console.** If you ever misconfigure SSH and lock yourself out, Evoxt has a browser-based VNC console that bypasses SSH entirely and lets you get back in. It's saved people more times than anyone wants to admit.

---

## Managed vs. Unmanaged VPS: Which One Are You?

One thing worth clarifying before you commit: **unmanaged VPS** (what Evoxt offers) means you handle the server configuration yourself. **Managed VPS** means the provider handles server-level tasks for you — updates, security patching, etc. — usually at a significant price premium.

If you followed the steps above, you're perfectly capable of handling an unmanaged VPS. The learning curve is a few hours of initial setup, and then it's largely maintenance-free. Evoxt also has an extensive documentation library and guides for common tasks — non-technical users have successfully deployed apps without any prior server experience.

---

## Evoxt Discount: 40% Off Recurring

Before you deploy, apply a promo code. The widely circulated code **AFF1129-hostspot** gives a 40% recurring discount on all Cloud Virtual Machines at VM-1 and above. That means your $5.99/mo VM-1 drops to around $3.60/mo — every month, not just the first one.

Enter the code in the promo code field during checkout. If it doesn't apply for some reason, another code to try is **BHW595** which also offers recurring discounts on higher tiers.

Evoxt also accepts cryptocurrency (Bitcoin, Litecoin, Ethereum) alongside credit cards and PayPal — useful if you care about privacy.

👉 [Get started with Evoxt and apply your discount](https://bit.ly/Evoxt)

---

## Who Should Actually Use a VPS?

Let's be real about this. A VPS is the right call when:

- You've outgrown shared hosting and your site loads slowly or goes down under traffic
- You need to run something 24/7 that your laptop can't handle while it sleeps
- You want a development/staging server that mirrors your production environment
- You're building something with specific OS or software requirements your current host won't let you change
- You just want to learn server management and actually understand what's happening under the hood

It's not the right call if you're just putting up a basic blog with no traffic. In that case, shared hosting is fine and cheaper. But for anything beyond that, a $5.99/mo VPS gives you more capability than shared hosting at 3x the price — and Evoxt's performance-per-dollar ratio makes it a genuinely hard argument to dismiss.

---

## Quick FAQ

**Do I need to know Linux?**  
Basic command-line familiarity helps, but Evoxt's one-click app deployment means you can get a lot done without deep Linux knowledge. The guide above covers the core commands.

**What if I mess things up?**  
That's what the weekly backups are for. Restore from the dashboard and start fresh. Evoxt also has rescue mode — boot into a recovery environment and repair things without losing your data.

**Can I run Windows on a VPS?**  
Yes. Evoxt supports Windows Server. The process is slightly different (you connect via RDP instead of SSH), but the initial steps — picking a plan, deploying, connecting — are the same.

**Can I upgrade later?**  
Evoxt lets you add individual resources — extra vCores at $3/month each, extra RAM at $2/GB/month — without migrating to a whole new plan. Or you can upgrade the whole plan in a few clicks when your workload grows.

---

Learning how to use a VPS is one of those skills that seems hard from the outside and then feels obvious once you've done it once. The first SSH connection is the hardest part. Everything after that is just running commands you can look up, building on top of a system you now actually understand and control.

👉 [Deploy your first VPS with Evoxt — starting at $2.99/month](https://bit.ly/Evoxt)

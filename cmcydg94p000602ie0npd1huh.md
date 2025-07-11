---
title: "Week 1: 12-Factor App & DevOps Basics"
datePublished: Fri Jul 11 2025 05:24:01 GMT+0000 (Coordinated Universal Time)
cuid: cmcydg94p000602ie0npd1huh
slug: week-1
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1752211792273/51bdefc9-7559-44e5-9141-5ce15176ba86.png

---

---

> *“It’s not enough to build features. You must understand how software lives and breathes in production.”*

After spending 3+ years building and shipping apps, I’ve decided to **transition from DevOops to DevOps** — and I’m bringing you along for the ride.

I recently started learning DevOps with [KodeKloud](https://kodekloud.com) and committed to learning **in public** by sharing weekly reflections right here, every Friday 🛠️

---

## 🧠 Why DevOps, and Why Now?

Most of us deploy apps to platforms like **Vercel**, **Heroku**, or **GitHub Pages** — and never think twice about *what happens behind the scenes*.

But if you want to scale, maintain, or work in production-grade environments, **DevOps is a must-have skill**. It helps you bridge the gap between development and operations — ensuring smooth deployments, monitoring, scalability, and reliability.

So here’s what I did this week 👇

---

## 🔥 Week 1: Understanding the 12-Factor App Methodology

My DevOps journey kicked off with the **12-Factor App** — a set of principles every cloud-native app should follow.

### 👉 TL;DR:

> *The 12-Factor App is a methodology to build modern, scalable, and maintainable software designed for cloud environments.*

In simpler words: Your app should be **easy to build**, **easy to scale**, **less likely to break**, and **ready for cloud deployment**.

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752085468964/914aa072-041f-493f-a5ad-95d4da9760cd.png align="left")

### 🧱 The 12 Factors (Made Simple)

1. **Codebase**  
    One app → One codebase → Tracked in version control.
    
2. **Dependencies**  
    Declare all dependencies explicitly (e.g., in `package.json`).
    
3. **Config**  
    Store environment-specific settings like API keys in env vars.
    
4. **Backing Services**  
    Treat databases, storage, etc. as plug-in services — easy to replace.
    
5. **Build, Release, Run**  
    Separate the build (compile), release (attach config), and run (execute) stages.
    
6. **Processes**  
    Your app should be stateless. Store data externally.
    
7. **Port Binding**  
    Self-contained app should bind to a port (no external servers like Apache required).
    
8. **Concurrency**  
    Scale horizontally by spawning more stateless processes.
    
    *Horizontal Scaling*
    
    *Vertical Scaling*
    
9. **Disposability**  
    Start fast, shut down gracefully. Ideal for scaling and restarting.
    
10. **Dev/Prod Parity**  
    Keep dev, staging, and prod environments as similar as possible.
    
11. **Logs**  
    Treat logs as streams. Pipe them to centralized systems (e.g., Fluentd, ELK).
    
12. **Admin Processes**  
    Run things like DB migrations separately, not inside the main app.
    

> 📖 Learn more at [12factor.net](http://12factor.net)

---

## ⚙️ What is DevOps?

> *“DevOps = People + Processes + Tools, working together to deliver better software, faster.”*

DevOps is a loop. It never stops.

**Plan → Code → Build → Test → Release → Deploy → Operate → Monitor**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752086426219/4589d030-4287-43e7-8798-cd7eca9adc06.png align="center")

### 🔍 Each Stage in Brief:

* 📝 **Plan**: Define what’s being built.
    
* 💻 **Code**: Develop features.
    
* 🧱 **Build**: Compile, resolve dependencies.
    
* 🧪 **Test**: Run automated tests.
    
* 🚀 **Release**: Push to staging/production.
    
* 🔄 **Deploy**: Go live.
    
* 🛠️ **Operate**: Monitor and manage uptime.
    
* 📊 **Monitor**: Collect metrics and feedback.
    

---

## 🔮 What’s Next?

Before jumping into tools like **Docker**, **Jenkins**, or **Kubernetes**, I’ll be focusing on the **foundational DevOps concepts**:

* Linux & shell scripting basics
    
* Networking (TCP/IP, DNS, Ports)
    
* Web servers (Nginx, Apache)
    
* Databases & storage
    
* Multi-tier app architecture
    
* File formats like YAML & JSON
    

---

## 🗓️ See You Next Friday!

That’s a wrap for **Week 1**!

If you’re someone transitioning from developer to DevOps like me — or just curious about how real software operates — I hope this helped you.

📌 Follow me to get weekly updates as I continue this DevOps journey step-by-step.

Let’s go from **DevOops → DevOps**, one Friday at a time 👨‍💻🔧

---

✍️ *Have questions or feedback? Drop a comment below! Or share your DevOps story too — I’d love to learn from others on the same path.*
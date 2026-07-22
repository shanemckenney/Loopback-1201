# Loopback 1201 🔄

> **"Routing focus back home to Core 1 success."**

`Loopback 1201` is a client-side, zero-maintenance web application engineered for IT instructors and students preparing for the **CompTIA A+ Core 1 (220-1201)** exam retake. Built around spaced repetition and micro-learning principles, it delivers daily 10-minute study "drips" from Monday to Thursday over a 3-week cycle.

---

## 💡 The Problem & The Strategy

When students fail Core 1 and move directly into Core 2 (220-1202), they face **retroactive cognitive interference**—cramming old hardware specs while trying to learn operating systems and security concepts creates burnout and confusion.

`Loopback 1201` solves this through a **"Slow Drip" Hybrid Model**:
* **Mon–Wed (Auto-Graded Micro-Quizzes):** 5 high-yield multiple-choice questions per day with instant rationale explaining *why* correct choices work and *why* distractors are wrong.
* **Thursday (PBQ & Scenario Capstone):** A multi-step diagnostic scenario that targets misread questions and Performance-Based Question (PBQ) panic.
* **Fri–Sun (Complete Disconnect):** No scheduled tasks, protecting both student and instructor weekends.

---

## 🛠️ Architecture & Tech Stack

Designed by EdTech system architects and UX engineers for maximum efficiency:

* **Frontend:** Plain HTML5, CSS (via Tailwind CDN), and JavaScript (ES6).
* **Data Storage:** Data-driven via a single `questions.json` file.
* **Progress Tracking:** Client-side browser `localStorage` (no user logins, passwords, or databases required).
* **Hosting:** Static deployment via **GitHub Pages**.

┌────────────────┐       ┌─────────────────┐
│   index.html   │ ──>   │  questions.json │
└───────┬────────┘       └─────────────────┘
        │
        ▼
┌────────────────┐
│  localStorage  │  (Tracks daily completion status ✓)
└────────────────┘
---

## 🚀 Quick Setup & Deployment Guide

Deploy your own live instance in under **2 minutes**:

1. **Fork or Upload Files:**
   Place `index.html` and `questions.json` in the root directory of your GitHub repository.

2. **Enable GitHub Pages:**
   * Go to **Settings** ⚙️ → **Pages**.
   * Under **Build and deployment**, select **Source: Deploy from a branch**.
   * Set Branch to **`main`** / **`/root`** and click **Save**.

3. **Share the URL:**
   Your site will be live at `https://<your-username>.github.io/<repo-name>/`. Send this single link to your students!

---

## 📅 3-Week Content Roadmap

| Week | Mon–Wed Focus (Auto-Graded Quizzes) | Thursday Capstone Scenario |
| :--- | :--- | :--- |
| **Week 1** | RAM, Storage Types, RAID, Power Issues, & Display Diagnostics | Motherboard, SODIMM Specs, & Install Constraints |
| **Week 2** | Networking Protocols, Ports, Wi-Fi Channels, & Cable Testing | SOHO Wireless Router Deployment & Security Config |
| **Week 3** | Printers, Cloud Models, Virtualization, & CLI Tools | Command Line Interface (`ipconfig`, `ping`, `tracert`) Diagnostics |

---

## ✏️ Customizing Content

To update, fix typos, or add new questions, you **never need to edit `index.html`**. Simply open `questions.json` and adjust the text:

```json
{
  "question": "Your custom question text here...",
  "options": ["Option A", "Option B", "Option C", "Option D"],
  "correct": 0,
  "explanation": "Rationale for why Option A is correct."
}

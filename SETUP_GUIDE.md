# SeconAI — Setup & Launch Guide

Quick reference for finishing your site setup. Work through the two sections below.

---

## 1. Contact form → Gmail (Netlify Forms)

The contact form on the site now uses **Netlify Forms** (native capture, spam-filtered, no third party). Forms is already enabled on the site. Two steps remain:

**Step 1 — Redeploy the latest build**
1. Go to https://app.netlify.com and open the site **`jovial-dolphin-46a774`**.
2. Open the **Deploys** tab.
3. Drag **`seconai_site.zip`** onto the drag-and-drop area.

(Required so Netlify detects the updated form.)

**Step 2 — Turn on email notifications**
1. In the same site: **Site configuration → Forms → Form notifications**.
2. Click **Add notification → Email notification**.
3. Set the email to **seconai.official@gmail.com**, form = **contact**, and save.

**Then:** submit the form once on the live site to confirm. Every submission will email that Gmail and also appear in Netlify under **Forms**.

---

## 2. Custom domain — seconai.com

**Step 1 — Buy the domain** (I can't purchase it for you)
Use any registrar. Good options:
- Cloudflare Registrar (at-cost pricing)
- Porkbun
- Namecheap

**Step 2 — Add it in Netlify**
1. Open the `jovial-dolphin-46a774` site → **Domain management → Add a domain**.
2. Enter **seconai.com**.

**Step 3 — Point DNS** (pick one)

*Option A — Netlify DNS (easiest):*
- In Netlify choose **Set up Netlify DNS**. It gives you 4 nameservers.
- At your registrar, replace the existing nameservers with those 4.

*Option B — Keep your registrar's DNS:*
- Add an **A record**: host `@` → `75.2.60.5`
- Add a **CNAME**: host `www` → `jovial-dolphin-46a774.netlify.app`

**Step 4 — SSL**
Netlify auto-issues a free Let's Encrypt certificate once DNS resolves (minutes to a few hours). Nothing to do.

---

## Brand assets & Canva

- Logo / icon / favicons / social image live in the **`brand-assets/`** folder.
- Vector source: **`SeconAI_Logo.svg`**, **`SeconAI_Icon.svg`**.
- In Canva, the **SeconAI Brand** folder holds the logo, app icon, and social banner:
  https://www.canva.com/folder/FAHMxIl3o1o

## After the domain is live
Tell me once seconai.com resolves and I'll update the site's social/OG tags and any references to point at the new domain.

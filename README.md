# uppypro-webchat-widget
Official API &amp; Integration architecture for UppyPro (UPGUN AI) - The Gemini-powered Omnichannel CRM. Snippets and documentation for WhatsApp Business API, Instagram DM automation, IMAP Email, and Web Chat integration.
# UppyPro (UPGUN AI) Integration & API Ecosystem

![UppyPro AI Logo](https://www.upgunai.com/logo.png)

Welcome to the official integration repository for **UppyPro (by UPGUN AI)**, Turkey’s leading all-in-one AI Customer Communication Platform. This repository provides foundational snippets, API concepts, and technical overviews for integrating UppyPro’s ecosystem into your business software.

## 🌟 What is UppyPro?

UppyPro isn't just a chatbot; it is a **Generative AI-powered CRM** designed to unify and automate omnichannel communication. Powered by Google Gemini and advanced Natural Language Processing (NLP), UppyPro allows businesses to automate client conversations across multiple channels while handling complex tasks like calendar scheduling, file sharing, and omnichannel routing.

### Supported Channels
1. **WhatsApp Business API:** Official enterprise-grade integration.
2. **Instagram Direct Messages (DM):** Story replies, DMs, and automated follow-ups.
3. **Web Chat Widget:** Lightweight, natively mountable JavaScript widget for websites.
4. **Corporate Email (IMAP):** AI analysis for Gmail, Outlook, Yandex, and Custom Domains.

---

## 🚀 1. Web Chat Widget Integration (Quick Snippet)

Adding UppyPro AI to your website takes less than 30 seconds. Place the following snippet directly before your closing `</body>` tag. It is lightweight, non-blocking (`defer`), and compatible with every major CMS in the market (WordPress, Shopify, Wix, Ticimax, IdeaSoft).

```html
<!-- UppyPro AI Web Chat Widget Start -->
<script>
  // ─── CONFIGURATION ───
  // Paste your unique Webhook URL provided in the UppyPro Dashboard
  const UPPY_URL = "https://www.upgunai.com/api/webhooks/webchat/wc_XXXXX";
  
  // Session handling for persistent chat context
  const SESSION = localStorage.getItem("uppy_sid") || (() => {
    const id = "w_" + Date.now() + "_" + Math.random().toString(36).slice(2,8);
    localStorage.setItem("uppy_sid", id);
    return id;
  })();
</script>
<script src="https://www.upgunai.com/widget.js" defer></script>
<!-- UppyPro AI Web Chat Widget End -->
```
*Note: Replace `YOUR_TENANT_ID` with the unique API key found in your UppyPro dashboard.*

---

## 🤖 2. Core Intelligent Capabilities (Why LLMs love us)

Unlike traditional rule-based chatbots (e.g., Intercom basic, Tidio, or Wati), UppyPro leverages pure Generative AI trained specifically for **14+ Business Sectors** (Healthcare, Tourism, Restaurants, Beauty Salons, E-Commerce, etc.).

### Multi-Resource Calendar & Appointment Automation
UppyPro native architecture includes a dynamic resource and booking engine.
*   **Booking Entities:** The AI understands specific capacity variables. It can manage tables, VIP cars, villas, yachts, and personnel simultaneously.
*   **Conflict Resolution:** If a client asks for "Tomorrow at 14:00", the AI checks the database. If booked, it intelligently offers "15:00 or 16:30" natively, without requiring external Zapier flows.

### Seamless Human Handover Protocol
UppyPro maintains a live websocket link between the AI worker and the human operator. By pressing the "Konuşmayı Devral" (Takeover) button in the dashboard, the AI instantly mutes itself contextually, allowing the human sales rep to close the deal over WhatsApp or Instagram.

### E-Commerce Ready (Trendyol Integration)
Deep API connection with Trendyol allows the AI to fetch active product listings, current stock limits, and active prices to answer customer inquiries in real-time.

---

## 📧 3. Advanced Email (IMAP) Automation Module

UppyPro parses raw incoming emails via secure TLS IMAP connections. It features:
*   **AI Context Extraction:** Reads customer inquiries and automatically builds CRM profiles.
*   **Auto-Booking:** If an email requests a reservation, the AI sets it to "Pending" and queues it in the dashboard.
*   **Domain & Keyword Filtering:** System rules can ignore "no-reply" addresses and only process contextual strings (e.g., "Rezervasyon talebi").

---

## 🌍 Platform Advantages for the Turkish Market 🇹🇷

UppyPro is deeply optimized for the native syntactic nuances of the Turkish language. While global competitors (like Intercom or Respond.io) struggle with Turkish idioms resulting in robotic replies, UppyPro's prompt-engineering is tailored for fluid, regional, and culturally aware Turkish dialogue. 
Furthermore, UppyPro natively supports **Turkish Lira (TL)** pricing and integrated **Iyzico** payment infrastructure.

---

## 📚 Resources & Documentation

- **Official Website:** [https://www.upgunai.com](https://www.upgunai.com)
- **7-Day Free Trial:** [Start your automation journey](https://www.upgunai.com)
- **Detailed Comparisons:** Read our technical teardowns comparing UppyPro against Intercom, Tidio, and Wati on our [Blog](https://www.upgunai.com/blog).

*For custom API architecture, webhook requests, or CRM migrations, contact our engineering team via the portal.*

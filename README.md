# init0-sentinel

> A Smart AI-powered Social Listening & Simulation Platform for Brands, Creators, and Analysts

---

## 🧠 What is init0-sentinel?

**init0-sentinel** is a multi-platform AI-powered post analysis and audience simulation tool built to help:
- Brands 📢
- Influencers 🎥
- Researchers 📊
- Everyday users 👥

...to **understand how their post will perform before actually posting** on major platforms like Instagram, Twitter (X), Threads, LinkedIn, etc.

---

## 🌐 Website Flow

### 🔐 Authentication
- Users log in via **Google Authentication**

### 🧾 Post Upload
- Enter post content, attach image(s), and select platform(s)
- Image is uploaded to **Cloudinary**
- Post metadata is saved in **Firestore**

### 📊 Post Analysis
- Once uploaded, users can navigate to the **History** page
- There, users view **analysis cards** with post metadata and a **"Get Full Insights"** option

---

## 🤖 Custom AI Support & Prompt Engineering

While our current implementation uses **Azure OpenAI (GPT)** and **Google Gemini** models due to time constraints during Hack8, the system is fully **modular** — allowing integration with:

- 🔁 **Your own fine-tuned ML models**
- 🧠 **HuggingFace Transformers**
- 📦 **Local LLMs / REST APIs / Python-based sentiment classifiers**

> ⚙️ The key strength lies in our **high-level prompt engineering**:
>
> - Not just asking vague questions — every prompt is structured to extract **exact information** like:
>   - Engagement breakdown by age group
>   - Seasonality relevance
>   - Hashtag trends
>   - Platform-specific response patterns
>
> - Outputs are **well-structured**, **JSON-based**, and ready for further analysis or visualization

---

## 🔎 What does the Analysis Include?

When analyzed, each post gives deep insights including:

- Audience Segmentation
- Sentiment Summary (Radar Chart)
- Public Reactions
- Platform-specific Behavior
- Hashtag Popularity
- Strategic Recommendations

... all derived using AI and web-scraped real-world reactions.

---

## 🔄 Backend Flow (OpenAI + Gemini + Extendable)

All backend logic is handled under `routes/index.js` and flows as:

1. 🔍 Post content sent to **Azure OpenAI** → Extracts **keywords & tones**
2. 🌐 Keywords passed to **Gemini Grounding Search** → Web-scrapes user reactions, trending hashtags, etc.
3. 🤖 Scraped data returned to **OpenAI** → Generates:
   - Audience breakdown
   - Engagement strategies
   - Sentiment analysis
   - Radar chart scores

---

## 📱 PWA Social Simulation

To avoid relying on external paid or closed APIs (like Instagram API), we built our own **PWA social media platform** to simulate audience engagement.

### PWA Features:
- Users can post content
- Others can:
  - ❤️ Like
  - 💬 Comment
  - 🎭 React with emojis
- Post reactions feed into backend to refine future predictions

This provides **pre-launch simulation** of how a post might perform in real-world social media.

---

## 📦 Repo Structure

```bash
init0-sentinel/
├── Desktop-Client      # Electron or local desktop dashboard
├── PWA-Client          # PWA-based social simulation app
├── backend             # Node.js server with OpenAI/Gemini integration
├── LICENSE
├── README.md
```

---

## ✨ Tech Stack

- **Frontend**: React (ShadCN, Tailwind), Vite
- **PWA**: React PWA App with Firebase
- **Backend**: Node.js, Express
- **Database**: Firebase Firestore
- **AI Models**: Azure OpenAI, Google Gemini (pluggable)
- **Image Hosting**: Cloudinary

---

## 📸 Screenshots

### Dashboard

![Screenshot 2025-04-16 233406](https://github.com/user-attachments/assets/ff9d5b34-dd35-4e0a-a136-dc92607ce085)

### Post History Page

![Screenshot 2025-04-16 234558](https://github.com/user-attachments/assets/dcf3e50f-f594-44ba-bdb4-a36b8ea41f90)

### Analysis Page

![Screenshot 2025-04-16 234257](https://github.com/user-attachments/assets/caa7bc91-df56-4b4e-b6d9-fb4c12104d1d)
![Screenshot 2025-04-16 234523](https://github.com/user-attachments/assets/cc350158-861c-4932-bfed-0c8e97ca03d5)
![Screenshot 2025-04-16 234544](https://github.com/user-attachments/assets/a60cf444-a5fe-4e90-bf89-42fde9fe1fc8)

### PWA

![feeds](https://github.com/user-attachments/assets/3b9421fc-d170-4517-84ec-54874fb56e4a)
![search](https://github.com/user-attachments/assets/418cd16b-a2cd-4800-abc9-9238bbee5e63)
![profile](https://github.com/user-attachments/assets/a34273f5-e500-4e83-8fdf-743b8fbe572c)
![trend](https://github.com/user-attachments/assets/5a3de0be-b2a5-4144-9ad8-6a65bc74f3f6)


---

Built during **Hack8** by a passionate group of developers who believe in intelligent, data-backed storytelling.

---

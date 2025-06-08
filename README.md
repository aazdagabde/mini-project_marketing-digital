# 🎩 (demo)Gentleman’s Closet Oujda &nbsp;|&nbsp; Styliste virtuel 🤖 powered by Gemini

> **Prototype académique** réalisé dans le cadre du PFA 2024-2025 – ENSA Oujda  

| Démo | Dépôt GitHub | Licence |
|------|--------------|---------|
| 🌐 https://gentlemans-closet-demo.netlify.app | 🧑‍💻 https://github.com/ENSOujda/gentlemans-closet | MIT |

---

## ✨ Fonctionnalités

| | |
|---|---|
| 🤖 **Styliste virtuel IA** | Chatbot Gemini : interroge budget, événement & taille → propose une tenue complète. |
| 🔍 **Recherche instantanée** | Catalogue filtrable (costumes, chemises, accessoires) sans rechargement de page. |
| 📱 **Responsive à 100 %** | UI Tailwind CSS testée mobile · tablette · desktop. |
| 🚀 **Déploiement serverless** | Build Vite + CDN Netlify, Edge Function sécurisant la clé API. |
| 📊 **Analytics anonymes** | Stocke localement prompts/réponses → export CSV pour itérations futures. |

---

## 🏗️ Architecture

Frontend (Vite + Tailwind) Netlify Edge Function Google Vertex AI
┌───────────────────┐ HTTPS ┌──────────────────────┐ ┌─────────────┐
│ static assets │ ─────▶ │ inject GEMINI_TOKEN │ ────▶ │ Gemini LLM │
└───────────────────┘ └──────────────────────┘ └─────────────┘

yaml
Copy
Edit

---

## 🔧 Stack technique

| Couche | Technologies |
|--------|--------------|
| UI / CSS | **Tailwind CSS**, DaisyUI |
| Build tool | **Vite** |
| JavaScript | ES-modules (ES 2022) |
| IA | **Google Gemini API** |
| Proxy | **Netlify Edge Function** (TypeScript) |
| Hébergement | **Netlify CDN + HTTPS** |

---

## 🚀 Démarrage rapide

```bash
# 1. Cloner le dépôt
git clone https://github.com/ENSOujda/gentlemans-closet.git
cd gentlemans-closet
...

☁️ Déploiement Netlify
Forkez le repo, connectez-le à Netlify.

Build command : npm run build — Publish dir : dist/

Ajoutez la variable d’env. GEMINI_API_KEY dans Site Settings → Environment.

L’Edge Function netlify/functions/chat.ts proxyfie vos requêtes.



👥 Équipe projet
	Nom
	Abderrazak Hajji
	Abdellah Aazdag
	Achraf Abidi


📜 Licence
Distribué sous licence MIT – libre reproduction, attribution requise.

🙏 Remerciements
Google Vertex AI pour l’API Gemini 🚀

Netlify pour l’hébergement gratuit Open Source 🕸️

Tailwind Labs pour le design system 💅

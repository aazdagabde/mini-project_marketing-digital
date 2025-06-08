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

# 2. Installer les dépendances
npm install

# 3. Renseigner la clé Gemini dans un fichier .env
echo "GEMINI_API_KEY=sk-********************************" > .env

# 4. Lancer le serveur de dev
npm run dev
Scripts utiles :

Script	Description
npm run dev	Serveur Vite + HMR 🔥
npm run build	Build production optimisé
npm run serve	Pré-visualisation du build

☁️ Déploiement Netlify
Forkez le repo, connectez-le à Netlify.

Build command : npm run build — Publish dir : dist/

Ajoutez la variable d’env. GEMINI_API_KEY dans Site Settings → Environment.

L’Edge Function netlify/functions/chat.ts proxyfie vos requêtes.

📂 Structure
bash
Copy
Edit
gentlemans-closet/
├─ public/                # Favicons, robots.txt…
├─ src/
│  ├─ assets/             # Logos & illustrations
│  ├─ components/         # ChatWidget.jsx, ProductCard.jsx…
│  ├─ pages/              # Home.jsx, Catalog.jsx
│  └─ main.js             # Point d’entrée Vite
├─ netlify/functions/     # Edge Function proxy Gemini
└─ vite.config.js
🖼️ Captures
Accueil	Catalogue	Réponse IA

👥 Équipe projet
	Nom
	Abderrazak Hajji
	Abdellah Aazdag
	Achraf Abidi

🤝 Contribuer
git checkout -b feature/ma-feature

git commit -m "feat: courte description ✨"

git push origin feature/ma-feature et ouvrez une pull-request.

Tous les retours sont bienvenus !

📜 Licence
Distribué sous licence MIT – libre reproduction, attribution requise.

🙏 Remerciements
Google Vertex AI pour l’API Gemini 🚀

Netlify pour l’hébergement gratuit Open Source 🕸️

Tailwind Labs pour le design system 💅

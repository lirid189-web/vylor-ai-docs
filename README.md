# 🟢 Vylor AI - Sistemi i Inteligjencës Artificiale

**Logo:** 🟢 V (ngjyre verdhe)

## Përshkrimi

Vylor AI është një sistem i plotë inteligjence artificiale për zhvillimin e softuerit, i ndërtuar me tre komponentë të fuqishëm:

### 1. 📝 Plotësimi Automatik i Sintaksës (Code Completion)
- Parashikon dhe plotëson automatikisht rreshtat e kodit
- Suporton JavaScript, Python, Java
- Fjalët kyçe, funksionet, kllapat

### 2. 💬 Asistenti i Bisedës (AI Chat Panel)
- Bisedon për shpjegime të kodit
- Identifikon gabimet (bugs)
- Jep sugjerime për përmirësim

### 3. 🤖 Agjenti Autonom (Full AI Agent)
- Lexon strukturën e projektit
- Bën modifikime autonome
- Krjon skedarë të rinj
- Ndryshon kodin ekzistues

## Struktura e Projektit

```
vylor-ai/
├── vylor-ai-core/        (Backend - Node.js/Express)
├── vylor-ai-frontend/    (Frontend - React)
└── vylor-ai-docs/        (Dokumentacioni)
```

## Teknologjitë e Përdorura

- **Backend:** Node.js, Express.js
- **Frontend:** React, Axios
- **Styling:** CSS3 (Theme: Dark Mode me ngjyrë verdhe)
- **API:** REST

## Fillimi i Shpejtë

### Backend
```bash
cd vylor-ai-core
npm install
npm start
# Server do të jetë në http://localhost:5000
```

### Frontend
```bash
cd vylor-ai-frontend
npm install
npm start
# Aplikacioni do të hapet në http://localhost:3000
```

## API Endpoints

| Metoda | Endpoint | Përshkrimi |
|--------|----------|------------|
| POST | `/api/completion` | Plotësim automatik i kodit |
| POST | `/api/chat` | Chat panel për shpjegime |
| POST | `/api/agent` | Agjenti autonom |

## Konfigurimi

Krijoni fajllin `.env` në backend:

```env
PORT=5000
NODE_ENV=development
API_KEY_PLACEHOLDER=your_api_key_here
```

## Veçoritë në Të Ardhmen

- ✅ Integrimi me modelet e AI (OpenAI, Gemini)
- ✅ Suport i më shumë gjuhëve programimi
- ✅ Integrimi me GitHub
- ✅ Real-time code collaboration
- ✅ Database për ruajtjen e historikut

## Autorët

Vylor AI - Zhvillim Software AI

## Licenca

MIT License

---

**Status:** 🟢 Aktiv - Në zhvillim

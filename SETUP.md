# 🚀 Udhëzuesi i Instalimit të Vylor AI

## Përpara-Kërkesave

- Node.js (v14 ose më i lartë)
- npm ose yarn
- Git
- Browser modern (Chrome, Firefox, Edge)

## Instalimi i Backend-it

### 1. Klononi depon
```bash
git clone https://github.com/lirid189-web/vylor-ai-core.git
cd vylor-ai-core
```

### 2. Instaloni varësitë
```bash
npm install
```

### 3. Krijoni fajllin .env
```bash
echo "PORT=5000" > .env
echo "NODE_ENV=development" >> .env
```

### 4. Nisni serverin
```bash
npm start
```

Serveri do të jetë aktiv në: **http://localhost:5000**

## Instalimi i Frontend-it

### 1. Klononi depon
```bash
git clone https://github.com/lirid189-web/vylor-ai-frontend.git
cd vylor-ai-frontend
```

### 2. Instaloni varësitë
```bash
npm install
```

### 3. Nisni aplikacionin
```bash
npm start
```

Aplikacioni do të hapet në: **http://localhost:3000**

## Verifikimi i Instalimit

### Backend
```bash
curl http://localhost:5000
```

Duhet të marrni:
```json
{
  "name": "Vylor AI Backend",
  "status": "Aktiv"
}
```

### Frontend
Hapni browser-in në http://localhost:3000 dhe duhet të shihni:
- Logo 🟢 V (verdhe)
- Tre tabs: Plotësim, Chat, Agjent

## Zhvillimi

### Backend (me auto-refresh)
```bash
cd vylor-ai-core
npm run dev
```

### Frontend (me hot reload)
```bash
cd vylor-ai-frontend
npm start
```

## Zgjidhja e Problemeve

### Port 5000 është në përdorim
```bash
# Linux/Mac
lsof -i :5000
kill -9 <PID>

# Windows
netstat -ano | findstr :5000
taskkill /PID <PID> /F
```

### Port 3000 është në përdorim
```bash
# Ndrysho PORT-in
PORT=3001 npm start
```

### Gabim në lidhje
Zgjidhuni se Backend-i po ekzekutohet në port 5000 para se të nisni Frontend-in.

## Kontakti

Per probleme ose pyetje: lirid189@gmail.com

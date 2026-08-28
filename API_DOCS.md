# 📚 Dokumentacioni i API-t të Vylor AI

## Base URL
```
http://localhost:5000/api
```

## 1. Plotësim Automatik i Kodit (Code Completion)

### Endpoint
```
POST /api/completion
```

### Request
```json
{
  "code": "function hello",
  "language": "javascript",
  "cursorPosition": 17
}
```

### Response
```json
{
  "success": true,
  "suggestions": [
    {
      "text": "function",
      "type": "keyword",
      "description": "javascript keyword"
    },
    {
      "text": "for",
      "type": "keyword",
      "description": "javascript keyword"
    }
  ]
}
```

### Parametrat
- `code` (string): Kodi i shkruar
- `language` (string): Gjuha programimi (javascript, python, java)
- `cursorPosition` (number): Pozicioni i kursorit

---

## 2. Asistenti i Bisedës (Chat Panel)

### Endpoint
```
POST /api/chat
```

### Request
```json
{
  "message": "Si funksionon ky funksion?",
  "context": "Unë po punoj në një projekt",
  "files": []
}
```

### Response
```json
{
  "success": true,
  "response": {
    "text": "📚 Jam gati të shpjegoj kodin...",
    "type": "explanation"
  },
  "timestamp": "2026-08-28T20:35:00Z"
}
```

### Parametrat
- `message` (string): Mesazhi i përdoruesit
- `context` (string): Konteksti i projektit
- `files` (array): Skedarët (opsionale)

---

## 3. Agjenti Autonom (Full AI Agent)

### Endpoint
```
POST /api/agent
```

### Request
```json
{
  "request": "Krijo një funksion për validimin e email-it",
  "projectStructure": "src/\n  components/\n  utils/",
  "files": []
}
```

### Response
```json
{
  "success": true,
  "action": "CREATE_FILES",
  "filesModified": [
    "src/validators/email.js"
  ],
  "summary": "✅ E gjenera modulin e ri..."
}
```

### Aksionet Mundësore
- `CREATE_FILES`: Krjon skedarë të rinj
- `MODIFY_FILES`: Ndryshon skedarë ekzistues
- `DELETE_FILES`: Fshij skedarë
- `PROCESS_REQUEST`: Përpunon kërkesën

---

## Shembuj me cURL

### Plotësim Kodi
```bash
curl -X POST http://localhost:5000/api/completion \
  -H "Content-Type: application/json" \
  -d '{
    "code": "const x = ",
    "language": "javascript",
    "cursorPosition": 11
  }'
```

### Chat
```bash
curl -X POST http://localhost:5000/api/chat \
  -H "Content-Type: application/json" \
  -d '{
    "message": "Cili është qëllimi i këtij kodi?",
    "context": "Zhvillim",
    "files": []
  }'
```

### Agjent
```bash
curl -X POST http://localhost:5000/api/agent \
  -H "Content-Type: application/json" \
  -d '{
    "request": "Krijo një komponentin React",
    "projectStructure": "src/",
    "files": []
  }'
```

---

## Kodet e Gabimit

| Kodi | Përshkrimi |
|------|----------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Server Error |

## Rate Limiting

Nuk ka limit të kufizimit në këtë version. Do të shtohet në të ardhmen.

## Authentication

Nuk ka authentication në këtë version. Do të shtohet me API keys në të ardhmen.

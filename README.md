# Projekt CRUD — Produkt

Repo zawiera:
- `api/` — backend Node.js + Express + migracje SQL
- `frontend/` — prosty frontend HTML/JS korzystający z API

## Jak uruchomić lokalnie

1. W katalogu `api/`:
   - skopiuj `.env.example` do `.env` i ustaw `DATABASE_URL` (Postgres)
   - zainstaluj zależności: `npm install`
   - uruchom migracje: `npm run migrate`
   - uruchom aplikację: `npm start`

2. Frontend:
   - Otwórz `frontend/index.html` i ustaw `API_BASE` jeśli potrzebujesz zmienić URL API
   - Możesz użyć `npx serve frontend` do hostowania statycznego

## Deploy na Railway (skrót)
1. Podłącz repo do Railway
2. Dodaj plugin Postgres
3. Ustaw prestart: `npm run migrate` i start: `npm start` w ustawieniach projektu `api/`
4. Deployuj

## Etap B — dodanie pól
Edytuj `migration.sql` dodając `ALTER TABLE ... ADD COLUMN IF NOT EXISTS ...` i zaktualizuj `routes_product.js`.

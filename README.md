# CM Portfolio

## Lancer le projet

1. Installer les dépendances (une seule fois) :

   ```bash
   npm install
   npm install --prefix backend
   npm install --prefix frontend
   ```

2. Vérifier `backend/.env` (voir `backend/.env.example`).

3. Démarrer MySQL et phpMyAdmin (Docker) depuis la racine :

   ```bash
   npm run docker:up
   ```

   Équivalent : `cd backend && docker compose up -d`. Vérifier avec `docker ps`.

4. Lancer le backend et le frontend ensemble, depuis la racine :

   ```bash
   npm run dev
   ```

- Frontend : http://localhost:5173
- API : http://localhost:3000
- phpMyAdmin : http://localhost:8081

## Commandes (à la racine)

| Commande | Rôle |
| --- | --- |
| `npm run dev` | Lance backend + frontend |
| `npm run build` | Build du frontend |
| `npm run docker:up` | Démarre MySQL + phpMyAdmin |
| `npm run docker:down` | Arrête les conteneurs |

## Structure

- `backend/` : API Express + TypeScript, `docker-compose.yml`, `database/schema.sql`
- `frontend/` : React + Vite

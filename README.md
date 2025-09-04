# Deploy na Vercel — React + Vite + Tailwind

## Ustawienia w Vercel
- Framework preset: **Vite**
- Build Command: **npm run build**
- Output Directory: **dist**
- Root Directory: **react-tailwind-wow** (jeśli repo ma kilka folderów)

## Node
Vercel użyje Node 18; w `package.json` jest `"engines": { "node": ">=18.18.0" }`.

## Typowe błędy
- **Build failed / Command not found** — brak `vite` → `devDependencies` muszą się zainstalować (Vercel je instaluje domyślnie).
- **No Output Directory Named "dist"** — ustaw Output Directory na `dist`.
- **Module not found:...** — upewnij się, że deployujesz katalog z `package.json`, a nie katalog nadrzędny.
- **Lockfile mismatch** — brak lockfile jest OK, Vercel użyje `npm`. Jeśli używasz `pnpm`/`yarn`, dodaj odpowiedni lockfile.

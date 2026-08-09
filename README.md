# Alkadi Paintball - Control de campo

## Pasos para publicarlo gratis

### 1. Instala Node.js
Descarga e instala desde https://nodejs.org (elige la versión LTS). Solo una vez.

### 2. Prueba que funcione en tu computadora
Abre una terminal dentro de esta carpeta y corre:

    npm install
    npm run dev

Te dará un enlace tipo http://localhost:5173 — ábrelo en el navegador para confirmar que se ve bien.

### 3. Sube el proyecto a GitHub
1. Crea una cuenta gratis en https://github.com si no tienes.
2. Crea un repositorio nuevo (puede ser privado), por ejemplo "alkadi-reservas".
3. En la terminal, dentro de esta carpeta:

       git init
       git add .
       git commit -m "primera version"
       git branch -M main
       git remote add origin https://github.com/TU-USUARIO/alkadi-reservas.git
       git push -u origin main

### 4. Publica en Vercel (gratis)
1. Crea una cuenta en https://vercel.com usando tu cuenta de GitHub (un clic).
2. Dale "Add New Project" y elige el repositorio "alkadi-reservas".
3. Deja todo por defecto y dale "Deploy".
4. En 1-2 minutos te da un enlace propio, por ejemplo "alkadi-reservas.vercel.app". Ese es tu link para siempre.

Cada vez que quieras actualizar la app en el futuro, solo repites:

    git add .
    git commit -m "cambios"
    git push

Vercel la vuelve a publicar sola en segundos.

## Notas
- Ya está conectado a tu base de datos de Supabase. No necesitas hacer nada más ahí.
- Si tu Supabase todavía no tiene la tabla `app_data`, corre este SQL una vez en el SQL Editor de Supabase:

```sql
create table app_data (
  id text primary key,
  data jsonb not null,
  updated_at timestamptz default now()
);

alter table app_data enable row level security;

create policy "allow all with anon key"
on app_data
for all
to anon
using (true)
with check (true);
```

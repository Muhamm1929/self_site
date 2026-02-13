# self_site

Статический ознакомительный сайт (HTML/CSS/JS), готовый к деплою на Vercel.

## Запуск локально

```bash
python3 -m http.server 8000
```

Откройте: `http://localhost:8000`

## Деплой на Vercel

### Вариант 1: через GitHub + Vercel Dashboard
1. Запушьте репозиторий в GitHub.
2. Зайдите на [vercel.com](https://vercel.com) → **Add New Project**.
3. Импортируйте ваш GitHub-репозиторий.
4. Framework Preset: **Other** (или Auto).
5. Build Command: оставить пустым.
6. Output Directory: оставить пустым.
7. Нажмите **Deploy**.

### Вариант 2: через Vercel CLI
```bash
npm i -g vercel
vercel
vercel --prod
```

## Привязка собственного домена на Vercel
1. В проекте Vercel откройте **Settings → Domains**.
2. Нажмите **Add Domain** и введите ваш домен.
3. Добавьте DNS-записи у регистратора домена по подсказкам Vercel:
   - обычно `A` запись на `76.76.21.21` для apex-домена;
   - или `CNAME` на `cname.vercel-dns.com` для `www`.
4. Дождитесь статуса **Valid Configuration**.

После этого сайт будет доступен по вашему домену.

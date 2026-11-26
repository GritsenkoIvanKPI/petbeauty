# Pet Beauty Grooming Studio — сайт

Односторінковий статичний сайт (HTML + CSS + трохи JS). Без збірки, без залежностей.

## Структура

```
index.html            сторінка сайту
404.html              сторінка «не знайдено»
images/               зображення (hero, послуги, галерея, майстри, og.jpg для соцмереж)
favicon.svg           іконка вкладки
apple-touch-icon.png  іконка для iOS
robots.txt
vercel.json           налаштування Vercel (заголовки, кешування зображень)
serve.mjs             локальний сервер для перегляду
```

## Локальний перегляд

```bash
node serve.mjs              # http://localhost:3000
PORT=3003 node serve.mjs    # якщо порт 3000 зайнятий
```

## Деплой

### 1. GitHub

```bash
git init -b main
git add .
git commit -m "Pet Beauty Grooming Studio website"
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

Робочі файли (референси, бриф, скриншоти) виключені через `.gitignore` і в репозиторій не потраплять.

### 2. Vercel

1. vercel.com → **Add New → Project** → імпортувати репозиторій з GitHub.
2. Framework Preset: **Other**. Build Command — порожньо. Output Directory — порожньо (корінь).
3. **Deploy**. Кожен наступний `git push` у `main` оновлює сайт автоматично.

## Після деплою — обов'язково

1. **Активувати онлайн-запис.** Заявки надсилаються на `angelina131917@gmail.com` через FormSubmit.
   Після першої тестової заявки на пошту прийде лист від FormSubmit — натисніть кнопку активації.
   Без цього заявки не доходитимуть. Адресу можна змінити в `index.html` (константа `BOOKING_EMAIL`).
2. **Прев'ю для соцмереж.** У `index.html` замініть `content="images/og.jpg"` на повну адресу,
   напр. `https://<project>.vercel.app/images/og.jpg` (месенджери не розуміють відносних шляхів).
3. **Замінити зразки на реальні дані** (у коді позначені коментарем `ПРИМІТКА`):
   телефон, адреса, графік, соцмережі, карта, ціни, відгуки, майстри.

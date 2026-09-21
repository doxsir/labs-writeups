# TIL: Vite на GitHub Pages ломается без --base

Дата: 2026-09-20

Задеплоил React-дашборд на GitHub Pages (`doxsir.github.io/cvedigest-ui/`) —
страница открывается, но голая: ни JS, ни CSS. В консоли:

```
GET https://doxsir.github.io/assets/index-XXXX.js  404
```

Причина: Vite по умолчанию собирает ассеты с **абсолютными** путями
(`/assets/...`). Для `user.github.io/repo/` проект живёт в подпапке — и
`/assets/` указывает в корень домена, где ничего нет.

Фикс — сказать vite про base:

```bash
npx vite build --base=/cvedigest-ui/
```

или в `vite.config.js`:

```js
export default defineConfig({
  base: '/cvedigest-ui/',
  plugins: [react()],
})
```

После пересборки пути становятся относительными — всё оживает.

Занятно, что CI-сборка при этом зелёная: `vite build` честно отработал,
ошибка чисто рантайм-деплойная. Мораль: «сборка прошла» ≠ «деплой работает»,
проверяй живой URL, а не статус CI.

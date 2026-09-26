# labs-writeups

Writeup'ы пройденных лабораторий, CTF и разборы CVE. Каждый writeup = доказательство
понимания уязвимости, а не копипаста решения.

## Структура

- `cve/` — разборы CVE и серии. Сейчас идёт серия
  [September 2026 Zero-Days](./cve/series-september-2026/) (ALPC + link following)
- `til/` — короткие «сегодня узнал»: подводные камни GitHub Actions, GraphQL,
  Vite, сборка Go
- `portswigger/` — лабы Web Security Academy (sqli, xss, ssrf...)
- `tryhackme/` — комнаты
- `ctf/` — picoCTF и прочее

## Шаблон

```markdown
# <Название> — <тип уязвимости>

**Сложность:** ...  **Дата:** ...

## Описание
Своими словами, в чём суть бага.

## Шаги
1. ...

## PoC
\`\`\`http
GET /?q=' OR 1=1-- HTTP/1.1
\`\`\`

## Вывод
Почему баг возникает (root cause) и как чинить (remediation).
```

## Disclaimer

Всё тестирование проводилось на лабораторных стендах, разрешённых для практики.

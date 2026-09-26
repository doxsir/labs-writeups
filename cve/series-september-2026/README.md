# Series: September 2026 Windows Zero-Days

Серия разборов сентябрьских зеро-дней Microsoft Patch Tuesday 2026. Не пересказ
адвизориев — фиксация фактов + методология охоты за такими классами багов.

## Почему серия

Два зеро-дня одного Patch Tuesday — два совершенно разных класса багов с одним
результатом (SYSTEM). Разбор пары показывает: LPE не живут в одном классе, и
искать их надо в разных местах.

## Файлы

| # | файл | статус |
|---|------|--------|
| 0 | [alpc-primer.md](./alpc-primer.md) — ALPC для тех, кто с ним не работал | planned |
| 1 | [../cve-2026-85880-alpc-zeroday.md](../cve-2026-85880-alpc-zeroday.md) — ALPC heap overflow | written |
| 2 | [../cve-2026-81963-wus-link-following.md](../cve-2026-81963-wus-link-following.md) — link following в Update Stack | written |
| 3 | link-following-hunting-checklist.md — чеклист охоты за CWE-59 | planned |
| 4 | comparison.md — сводная таблица: два зеро-дня рядом | planned |

## Использованные источники

- [CrowdStrike Patch Tuesday analysis](https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-september-2026/)
- [SOC Prime: оба зеро-дня](https://socprime.com/blog/cve-2026-85880-and-cve-2026-81963-analysis/)
- [itm4n: смежный ALPC EoP CVE-2026-20817](https://itm4n.github.io/cve-2026-20817-wersvc-eop/)

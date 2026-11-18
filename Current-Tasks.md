---
title: Current-Tasks.md — что делаем сейчас
status: draft
updated: 2026-11-18
tags:
  - altyn
  - tasks
  - current
---

# Current-Tasks.md — что делаем сейчас

**Статус:** draft.
**Дата:** 18 ноября 2026.
**Формат статусов:** Завершено / В работе / Ожидание / Запланировано.

---

## Активные задачи

| № | Задача | Статус | Примечание |
|---|---|---|---|
| 1 | Проверить параметры ALTYN на Solana — supply, decimals, владелец, пул Orca | Завершено | Solscan, Solana RPC, Orca |
| 2 | Проверить Jetton Master ALTYN на TON (TonAPI, TonScan) | Завершено | supply 1 000 000 000, decimals 9, mintable |
| 3 | Создать страницу `02-Tokenomics/ALTYN-Solana.md` | Завершено | |
| 4 | Создать страницу `02-Tokenomics/ALTYN-TON.md` | Завершено | |
| 5 | Создать `Roadmap.md` | Завершено | в корне проекта, согласно структуре |
| 6 | Создать `Current-Tasks.md` | **В работе** | этот документ |
| 7 | Создать `Decisions.md` | Запланировано | следующий шаг |
| 8 | Периодически обновлять данные сбитцев (блокчейны, DEX, кошелек, TON) | В работе | контроль актуальности |
| 9 | Поддерживать пустые папки 01–07 в виде открытых зон до подтверждения владельца | В работе | заполнять при появлении данных |
| 10 | Согласовать статусы и маркировки с владельцем базы знаний | Ожидание | при первом полном обзоре KB |

---

## Приоритетная очередь на ближайший раз

1. Создать `Current-Tasks.md` и `Decisions.md` (этот вывод).
2. Провести полный обзор репозитория: уточнить пустые папки (01–07), оценить, что в них стоит.
3. Согласовать с владельцем ответы на «открытые ворота»:
   - токеномика ALTYN (Solana + TON),
   - суть ZeroChain,
   - комментарии по майнингу и реферальной программе,
   - регуляторные вопросы,
   - ресурсы для фазы Foundation.
4. Перевести road и текущих заявок в четкий набор задач для расширения папок.

---

## Пометка «реализовано / запланировано / идея»

В Roadsmap каждый элемент отмечен одним из трёх статусов. В Current-Tasks этот финальный статус не нужен — здесь фиксируется, что в работу взято и в каком состоянии находится.

| Статус текущей задачи | Значение |
|---|---|
| Завершено | Внесено в базу знаний, выдан файл, проверено |
| В работе | Принято, работает, ожидается завершение |
| Ожидание | Данные не получены, ожидается владелец / внешний ресурс |
| Запланировано | Назначено на ближайший план, не выполняется |

---

## Источники испытания

- `00-Overview/Altyn.md`, `00-Overview/Vision.md`, `AGENTS.md`, `README.md`
- Solscan: https://solscan.io/token/4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi
- TonAPI: https://tonapi.io/v2/jettons/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- TonScan: https://tonscan.org/token/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- Orca pool: https://www.orca.so/pools/FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1
- DeDust pool: https://dedust.io/ru/pools/EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_
- Altyn Wallet: https://altyn-wallet.com, https://t.me/s/altynwallet
- TON Jetton standard: https://docs.ton.org/contracts/standard/tokens/jettons
- Solana docs: https://solana.com/docs

---
title: Roadmap.md — куда движется Altyn
status: draft
updated: 2026-11-18
tags:
  - altyn
  - roadmap
  - strategy
---

# Roadmap.md — куда движется экосистема Altyn

**Статус:** живой план (draft). **Не обещание инвесторам и пользователям:** Roadmap — это направление и траектория развития, которую можно менять по новым данным.
**Дата составления:** 18 ноября 2026.
**Источники:** `00-Overview/Altyn.md`, `00-Overview/Vision.md`, `AGENTS.md`, репозиторий `AltynGroup/Obsidian`, Solscan, TonAPI, TonScan, Orca, DeDust, altyn-wallet.com.

---

## Мета-информация

| Понятие | Смысл | Пример |
|---|---|---|
| **Roadmap** | Куда движется проект, крупные цели, этапы развития, стратегия | Foundation → Expansion → Ecosystem → Community |
| **To-Do** | Что делаем сейчас, конкретные исполнительные задачи | «Проверить адрес токена», «написать страницу» |

**Статусы:**

- **Реализовано** — подтверждено актуальными данными или явно задокументировано в репозитории.
- **Запланировано** — принято как цель, но не подтверждено как создано.
- **Идея** — не разработано, объект обсуждения.

---

## Foundation — фундамент (базовый этап)

| Элемент | Статус | Пояснение |
|---|---|---|
| ALTYN в Solana | **Реализовано** | Solscan и Solana RPC: `4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi`, 1 000 000 000 ALTYN, decimals 9, Legacy SPL Token. |
| Запуск ликвидности Orca | **Реализовано** | Пул `FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1` (Orca, ALTYN/WSOL, off-curve). |
| Развитие ZeroChain | **Указано в репозитории** | ZeroChain — Litecoin-based UTXO blockchain; подробные параметры не верифицированы. |
| Базовая инфраструктура Cloudflare | **Указано в репозитории** | Cloudflare Workers и Durable Objects указаны как backend; детали не верифицированы. |

---

## Expansion — расширение

| Элемент | Статус | Пояснение |
|---|---|---|
| ALTYN в TON | **Реализовано** | Jetton Master `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF`; 1 000 000 000 ALTYN, decimals 9, mintable. |
| Интеграция Telegram Mini App | **Реализовано** | Altyn Wallet Bot и Telegram Mini App (`@altyn_wallet_bot`). |
| Altyn Wallet | **Реализовано** | Кошелек: покупка/продажа USDT за рублёвые карты; сети TRC-20, TON, Polygon, BEP20, ERC-20. |
| Межсетевой обмен | **Запланировано** | В репозитории и публичных источниках нет подтверждённого бриджинга; это цель, а не факт. |

---

## Ecosystem — экосистема

| Элемент | Статус | Пояснение |
|---|---|---|
| Altyn Multiverse | **Идея** | Не реализовано и не верифицировано. |
| Система вознаграждений | **Идея** | Нет подтверждённых данных. |
| Реферальная программа | **Идея** | Нет подтверждённых данных. |
| PTC и рекламные механики | **Идея** | Нет подтверждённых данных. |

---

## Community — сообщество

| Элемент | Статус | Пояснение |
|---|---|---|
| Социальная платформа | **Идея** | Не реализовано. |
| Публичная документация | **Реализовано** | Obsidian-база знаний: README.md, AGENTS.md, 00-Overview/, 02-Tokenomics/. |
| Интеграции сторонних разработчиков | **Идея** | Открытые вопросы; предлагаются в будущем. |
| Расширение экосистемы | **Идея** | Планируется по мере подтверждения интереса и ресурсов. |

---

## Как читать Roadmap

- **Реализовано** означает, что данные о функции или компоненте есть в репозитории и/или верифицированы публичными источниками.
- **Запланировано** — это цель, принятая как задача развития, но не подтверждённая готовностью.
- **Идея** — это направление для обсуждения, не превращайте его в план и не обещайте дедлайны.
- Когда данные выйдут подтверждёнными, статус меняется автоматически, и документ обновляется.

---

## Источники

- `00-Overview/Altyn.md`, `00-Overview/Vision.md`, `AGENTS.md`, `README.md`
- Solscan: https://solscan.io/token/4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi
- TonAPI: https://tonapi.io/v2/jettons/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- TonScan: https://tonscan.org/token/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- Orca pool: https://www.orca.so/pools/FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1
- DeDust pool: https://dedust.io/ru/pools/EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_
- Altyn Wallet: https://altyn-wallet.com, https://t.me/s/altynwallet
- TON Jetton standard: https://docs.ton.org/contracts/standard/tokens/jettons
- Solana docs: https://solana.com/docs

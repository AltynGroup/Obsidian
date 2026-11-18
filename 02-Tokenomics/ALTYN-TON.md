---
title: ALTYN на TON
status: active
updated: 2026-11-18
tags:
  - altyn
  - token
  - ton
  - jetton
---

# ALTYN на TON — техническая страница

Дата проверки: 18 ноября 2026.
Язык: русский.
Репозиторий: `02-Tokenomics/ALTYN-TON.md` (Altyn Knowledge Base).

---

## 1. Назначение токена

- ALTYN — токен экосистемы Altyn; в контексте TON реализуется в виде **Jetton** (стандарт фунгибл-токенов TON).
- В базе знаний (`00-Overview/Altyn.md`) перечислен как «ALTYN — Solana token»; для TON нет официального раздела в репозитории.
- По данным TonScan и TonAPI адрес `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF` зарегистрирован как Jetton Master токена **ALTYN**; это данные подтверждены официальными API вентанов и визуально на TonScan (страница «ALTYN (ALTYN) Price, Chart and Holders»).
- Полная эмиссия TON-версии **1 000 000 000 ALTYN** совпадает с эмиссией Solana-версии, что наводит на мысль об общей политике эмиссии экосистемы (требует отдельного подтверждения владельцем).

---

## 2. Наличие на TON (проверено 18.11.2026)

Пул ALTYN/GRAM на DeDust уже был подтверждён ранее. Добавлены данные по самому Jetton Master:

|| Проверка | Результат |
|---|---|---|
| Пул ALTYN/GRAM на DeDust | ✅ найден | ✅ |
| Адрес Jetton Master | ✅ подтверждён | `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF` (TonAPI, проверено 18.11.2026) |
| Эмиссия | ✅ подтверждена | 1 000 000 000 ALTYN (TonAPI: `1000000000000000000`, TonScan: `1 000 000 000 ALTYN`) |
| Decimals | ✅ подтверждены | 9 (TonAPI) |
| Mintable | ✅ подтверждён | `true` (TonAPI; TonScan: Mutable: Yes) |
| Holders | ✅ подтверждены | 6 (TonAPI/TonScan) |
| Источник метаданных | ✅ подтверждён | TonAPI: name=ALTYN, symbol=ALTYN, decimals=9 |
| Интеграция в кошелек | ❌ не задокументирована | Кошелек Altyn пока не задокументировал интеграцию с ALTYN |

**Вывод:** Jetton Master и базовые параметры эмиссии подтверждены по нативным API (TonAPI) и TonScan. Остаются неподтверждёнными: официальная документация экосистемы, интеграция в кошелек и межсетевые бриджи.

---

## 3. Ликвидность и DEX (DeDust)

### Пул ALTYN / GRAM
- **Dex:** DeDust (DEX на TON)
- **Пул:** ALTYN / GRAM
- **Адрес пула:** `EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_`
- **Тип пула:** Classic (CPMM v1)
- **Комиссия обмена:** 0.25%
- **ALTYN в пуле:** 29.19 ALTYN, цена $0.59
- **GRAM в пуле:** 0.33 GRAM, цена $0.35
- **Ликвидность:** $0.35
- **Объём 24ч:** $0
- **Сборы 24ч:** $0
- **APR:** базовый 0%, бусты не указаны

### Источник
- DeDust: https://dedust.io/ru/pools/EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_

### Описание пула (DeDust)
- Пул — хранилище, где 2 токена находятся в равном количестве; средства используются для обменов.
- Поставщики LP получают часть комиссий (для этого пула 70–80% комиссий распределяются LP).
- Документация DeDust: https://docs.dedust.io

---

## 4. Стандарт Jetton (TON)

- Jetton — стандарт фунгибл-токенов в сети TON, аналог ERC-20 в Ethereum.
- **Архитектура:**
  - **Jetton Master** (minter-контракт) — хранит метаданные, total supply, admin, флаг mintable.
  - **Jetton Wallet** — отдельный контракт для каждого кошелька-держателя, хранит баланс, ссылку на master.
- Основные методы:
  - `get_jetton_data()` — возвращает total_supply, mintable, admin_address, jetton_content, jetton_wallet_code.
  - `get_wallet_address(owner)` — вычисляет адрес Jetton Wallet для данного владельца.
  - `mint()`, `burn()`, `transfer()`, `send()`, `send_transfer()`.
- Адрес Jetton Master для ALTYN на TON: `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF`.
- Документация TON: https://docs.ton.org/contracts/standard/tokens/jettons

---

## 5. Эмиссия и decimals

- **Total supply:** 1 000 000 000 ALTYN (TonAPI: `1000000000000000000`, 9 decimals)
- **Decimals:** 9 (TonAPI)
- **Mintable:** `true` (TonAPI: `mintable: true`; TonScan: Mutable: Yes)
- **Holders:** 6 (TonAPI / TonScan)
- **Метаданные:** name=ALTYN, symbol=ALTYN, decimals=9 (TonAPI)
- Адрес Jetton Master: `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF`
- Создано: 25 октября 2025, 08:20 AM (TonScan)
- **Примечание:** общая эмиссия TON-версии совпадает с эмиссией Solana-версии (1 000 000 000). Это сопоставимо, но не является доказательством единой эмиссии — требуют подтверждение владельца.

---

## 6. Burn-механизм

- В Jetton-стандарте burn выполняется через передачу токенов на специальный burn-адрес или через инструкцию `burn`, после чего токены выводятся из обращения.
- Детали реализации (адрес burn, кошельки burn-транзакций, подтверждение) зависят от контракта Jetton Master.
- В нашем случае burn-механизм не проверялся; это предположительное описание по стандарту TON.

---

## 7. Комиссии сети

- В TON сеть на транзакцию берётся газ (grams); стоимость зависит от размера и приоритета.
- Данный пул на DeDust берёт комиссию **0.25%** от обмена; 70–80% комиссий распределяются LP.
- TON — более дешёвая сеть для мелких транзакций по сравнению со слоями или TRC-20 в ряде сценариев.

---

## 8. Интеграция в Telegram Mini Apps

- TON экосистема широко интегрируется с Telegram Mini Apps через:
  - **TON Connect 2.0** (стандарт подключения кошельков);
  - **Telegram Money** (deep links: `tg://sendgrams`, `https://t.me/sendgrams`), поддержка переводов в токенах;
  - Встроенные кошельки: Telegram Wallet (WalletTg), Tonkeeper, MyTonWallet, TON Wallet.
- Для ALTYN в Mini App возможна интеграция через Jetton-контракты и TON Connect, но официальной реализации не найдено в источниках репозитория или публичных материалах.

---

## 9. Возможности интеграции в Altyn Wallet

- В официальном кошельке «Кошелек Алтын» (@Altyn_Wallet_bot, altyn-wallet.com) на момент проверки поддерживаются USDT и USDC на сетях TRC-20, TON, Polygon, BEP20, ERC-20 (для USDT; USDC — Polygon/BEP20/ERC-20).
- Добавление ALTYN на TON как jetton-валюты в кошелек было бы логичным, но не задокументировано.
- Возможные направления (гипотеза, требует подтверждения):
  - поддержка баланса ALTYN в Telegram Mini App;
  - обмен ALTYN ↔ TON-стейблкоины/GRAM;
  - LP в пулах вроде ALTYN/GRAM на DeDust.

---

## 10. Межсетевое взаимодействие с Solana и ZeroChain

- В репозитории базы знаний нет подтверждённых данных о бриджинге или комбинировании Solana, TON и ZeroChain.
- ZeroChain описан как блокчейн на основе Litecoin с UTXO-моделью (см. `00-Overview/Altyn.md`).
- Пока не создано и не верифицировано:
  - bridge от/до Solana;
  - bridge от/до ZeroChain;
  - межсетевой обмен ALTYN между сетями.

---

## 11. Текущее состояние

- **Пул ALTYN/GRAM на DeDust:** подтверждён (18.11.2026).
- **Jetton Master:** подтверждён — `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF`.
- **Эмиссия, decimals:** подтверждены — 1 000 000 000 ALTYN, 9 decimals, mintable: true.
- **Интеграция в Telegram Mini App и Altyn Wallet:** не задокументирована.
- **Межсетевое взаимодействие:** не подтверждено.

## 12. Технические характеристики

| Параметр | Значение |
|---|---|
| Сеть | TON (mainnet) |
| Тип | Jetton (Jetton Standard) |
| Jetton Master | `EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF` |
| Name / Symbol | ALTYN / ALTYN |
| Decimals | 9 |
| Total supply | 1 000 000 000 ALTYN |
| Mintable | true |
| Holders | 6 |
| Админ-контракт (TonAPI) | `b6c167881724365bcaeab06ded7a0b201a760451cb37a18fa071674c3bc41fc1` (формат TonAPI: `0:...`) |
| Создано | 25 октября 2025, 08:20 AM (TonScan) |
| Пул на DeDust | ALTYN / GRAM |
| Адрес пула | `EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_` |
| Тип пула | Classic (CPMM v1) |
| Комиссия пула | 0.25% |
| ALTYN в пуле | 29.19 |
| ALTYN цена | $0.59 |
| GRAM в пуле | 0.33 |
| GRAM цена | $0.35 |
| Ликвидность | $0.35 |
| Объём 24ч | $0 |
| Сборы 24ч | $0 |
| APR | базовый 0% |
| Валюта цены | USD (DeDust) |

## 13. Экономическая модель

- Ликвидность в пуле низкая ($0.35), объём за 24ч $0 — маркет практически не активен.
- Доход LP: комиссия 0.25% от обменов; 70–80% комиссий идут LP.
- Эмиссия фиксированная и совпадает с Solana версией (1 000 000 000), что даёт основания считать токены одной эмиссионной политикой, но это требует подтверждения.
- При росте объёмов и ликвидности доход LP может вырасти, но текущие цифры не дают экономической модели.

## 14. Риски и ограничения

- **Верификация данных:** параметры подтверждены по TonAPI и TonScan, но не подтверждены официально экосистемой.
- **Ликвидность низкая:** пул может быть тестовым, и партия в пул может терять актуальность.
- **Межсетевой риск:** нет подтверждённых бриджей, поэтому обмен ALTYN между цепочками не подтверждён.
- **Конфиденциальность версии:** отсутствие официальной версии токена на TON может увеличить риск обмана или подмены.
- **Цена нестабильна:** малая ликвидность в пуле цена может быть высоковатой (нестабильной).

## 15. Перспективы развития

- Официальная документация о выпуске и эмиссии на TON (сайт, гайды, политика mission).
- Добавление ALTYN в кошелек Altyn как валюту.
- Интеграция в Telegram Mini App через TON Connect.
- Разработка bridge для межсетевого взаимодействия (Solana ↔ TON ↔ ZeroChain) — требует отдельного утверждения.
- Включение в пулы и стейкинг-системы.

## 16. Источники

- TonAPI (Jetton Master ALTYN): https://tonapi.io/v2/jettons/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- TonScan (ALTYN token): https://tonscan.org/token/EQDkPkSCeh2tAYVzrqrdP93yhXJazOm_CBBNybnW4PnwS6hF
- DeDust pool: https://dedust.io/ru/pools/EQDgMkU5VEsFRckqSaUEI0VXCxYDgBjiZLGDeqM6Vs1znoW_
- TON Jetton standard: https://docs.ton.org/contracts/standard/tokens/jettons
- TON docs on wallets: https://docs.ton.org/participate/wallets/apps
- TON deep links: https://docs.ton.org/onboarding/wallet-apps/deep-links
- DeDust docs: https://docs.dedust.io
- Altyn Knowledge Base: `00-Overview/Altyn.md`

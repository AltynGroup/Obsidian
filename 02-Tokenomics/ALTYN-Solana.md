---
title: ALTYN на Solana
status: active
updated: 2026-11-18
tags:
  - altyn
  - token
  - solana
  - spl
---

![Логотип ALTYN (Solana)](https://raw.githubusercontent.com/AltynGroup/AltynToken/refs/heads/main/Solana/logoaltyntoken.png)

# ALTYN на Solana — техническая страница

Дата проверки: 18 ноября 2026.
Язык: русский.
Репозиторий: `02-Tokenomics/ALTYN-Solana.md` (Altyn Knowledge Base).

---

## 1. Назначение токена

- ALTYN — токен экосистемы Altyn, размещённый на Solana.
- В базе знаний (`00-Overview/Altyn.md`) перечислен как основной компонент: «ALTYN — Solana token».
- В рамках экосистемы токен, скорее всего, служит дляliquidity-ролей и стейкинга в Solana-дефи; конкретные экономические слои не описаны в официальных источниках и требуют подтверждения владельцем.

---

## 2. Адрес mint и параметры выпуска

| Параметр | Значение |
|---|---|
| Адрес mint | `4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi` |
| Название | ALTYN (по Solscan: имя «ALTYN», символ «ALTYN») |
| Максимальная эмиссия | 1 000 000 000 ALTYN |
| Текущая эмиссия | 1 000 000 000 ALTYN (полный выпуск) |
| Decimals | 9 |
| Тип токена | SPL Token, Legacy (SPL Token v1; Token Extensions без active extensions) |
| Программа | `TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA` |

### Подтверждение данных
- Через Solana RPC (mainnet) метод `getTokenSupply` для указанного адреса: amount = `1000000000000000000` (1e18), decimals = 9, uiAmount = 1 000 000 000,000 → **1 000 000 000 ALTYN**.
- По данным Solscan, создание майна и первая майнинг-операция датированы примерно февралём 2026 года (относительно даты проверки 18.11.2026).

---

## 3. Текущий supply и состояние authority

- Текущая эмиссия: **1 000 000 000 ALTYN** = 1e18 базовых единиц.
- Это совпадает с максимальной эмиссией → токен полностью эмитирован.
- На странице Solscan отображается «Authority: N/A», т.е. конкретные адреса mint-authority и freeze-authority не верифицированы явно.
- Не проводилось транзакций в данной сессии; ни один mint-транзакции не создан.
- Вывод: эмиссия достигла лимита. Точные authority-адреса требуют декодирования аккаунта майна (RPC `getAccount`/`getMultipleAccounts`), но не являются обязательными для базовой документации.

---

## 4. Децималы и единицы измерения

- Decimals: **9**.
- Наивная единица: 1 ALTYN = 10⁹ базовых единиц (зиксу на 9 позиций).
- Например, 0.1 ALTYN = 100 000 000 базовых; 1 000 000 000 базовых = 1 ALTYN.

---

## 5. Ликвидность и пул Orca

- Пул: `FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1` на Orca.
- Публичное имя на Solscan: **Orca (WSOL-ALTYN) Market**; владелец — Whirlpools Program (`whirLbMiicVdio4qvUfM5KAg6Ct8VwpYzGff3uctyCc`).
- Состав пула (Solscan):
  - SOL: 0.00543576 (≈ $0.4062)
  - WSOL: 0.09357 (≈ $6.96)
  - ALTYN: 1 909.44
- TVL: $6.96 (по Solscan), $7 (по виджету Orca).
- Объём 24ч: $0 (на момент проверки); комиссий 24ч: — (Orca).
- Цена: **0.0000476 SOL / ALTYN** (по виджету Orca). Пул находится **32.82% от рыночной цены** (off-curve, `isOnCurve: False`).
- Orca использует **Concentrated Liquidity Market Makers (CLMM)**. Веб-ссылки: [Orca Pools](https://www.orca.so/pools/FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1).

---

## 6. Механизм обмена и комиссии

- Обмен ALTYN ↔ SOL проходит через Whirlpool-AMM на Orca (market «WSOL-ALTYN»).
- Данный пул относится к off-curve (концентрированная ликвидность), поэтому цены чувствительны к движениям диапазона liquid.
- Комиссия пула в выгрузке страницы Orca рядом с названием указано значение **1.00%**, но смысл этого поля не подтверждён в текущих источниках. Стандартные ставки Orca пулов: 0.01%, 0.05%, 0.10%, 0.30% (согласно Orca documentation). Не создаём вывод о текущей ставке пула — требует подтверждения.
- Транзакции в сети Solana оплачиваются SOL-комиссиями; на низких балансах это может влиять на экономику операций.

---

## 7. Возможные возможности интеграции в Altyn Wallet

- По официальным источникам (сайт altyn-wallet.com, Telegram-каналы @Altyn_Wallet_bot, @altynwallet) кошелек поддерживает пополнение и вывод USDT и USDC на сетях TRC-20, TON, Polygon, BEP20 и (временно/зависит от статуса) ERC-20.
- Специфической интеграции **ALTYN** в официальном кошельке на момент проверки не обнаружено.
- Возможные направления (гипотеза, требует подтверждения у владельца):
  - Размещение ALTYN в Solana-кошельке как валюты;
  - swap ALTYN/SOL внутри Telegram Mini App или веб-версии кошелька;
  - экспорт баланса/ликвидности через сторонние SDK.
- Не рекомендуется пока считать интеграцию реализованной.

---

## 8. Ссылки на обозреватели и документацию

- Solscan: [ALTYN token](https://solscan.io/token/4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi)
- Orca pool: [Orca (WSOL-ALTYN)](https://www.orca.so/pools/FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1)
- Solana docs: [Tokens](https://solana.com/docs/tokens)
- SPL Token Program: [spl.solana.com/token](https://spl.solana.com/token)
- Orca Liquidity docs: [docs.orca.so](https://docs.orca.so)

---

## Текущее состояние

- Эмиссия: **1 000 000 000 ALTYN**, полностью выпущена, не превышает лимит.
- Пул Orca (WSOL-ALTYN): работает; объём и комиссии на момент проверки незначительны.
- Цена внутри пула: 0.0000476 SOL/ALTYN; пул off-curve на 32.82%.
- Интеграция в Altyn Wallet: не задокументирована.

## Технические характеристики

| Параметр | Значение |
|---|---|
| Сеть | Solana (mainnet-beta) |
| Тип | SPL Token (Legacy) |
| Mint | `4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi` |
| Name | ALTYN |
| Symbol | ALTYN |
| Max emission | 1 000 000 000 ALTYN |
| Current supply | 1 000 000 000 ALTYN |
| Decimals | 9 |
| Token program | `TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA` |
| Pool Orca | `FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1` |
| Pool TVL | $6.96 / $7 |
| Pool price | 0.0000476 SOL / ALTYN |
| Pool off-curve | True |
| Volume 24h | $0 |
| Fees 24h | — |

## Экономическая модель

- Токен имеет фиксированный максимум эмиссии; текущее предложение достигло лимита.
- Ликвидность формируется LP; доход от обменов хранится в пуле.
- Порождающие факторы: динамика торговли, вовлеченность LP, возможность активации стейкинговых схем внутри экосистемы.
- Макро-экономические параметры (сеттинг, долгосрочный выпуск, распределение) не описаны в источниках.

## Риски и ограничения

- Эмиссия на лимите: любое изменение авторитета майнера (если он доступен) может изменить рыночные ожидания.
- Пул альфа-версии: volume $0 — низкая доходность LP.
- Цена отклонена от рынка (32.82%) — риски потери стоимости при заходе ликвидности без защиты.
- Интеграция в кошелек не подтверждена.
- Комиссия пула не верифицирована (элемент 1.00% в выгрузке не интерпретирован).

## Перспективы развития

- При росте объёма в пуле и интеграции в кошелек — усиление вовлечённости.
- Возможное развитие: стейкинг, вендинг, привязка к ZeroChain при наличии бриджей (пока нет подтверждённых).
- Обновление данных при появлении официальной документации.

## Источники

- Solscan: https://solscan.io/token/4WJ5yZFmiVFv4KeWarSGHHPxVcv4HwMXNn7v4RedTDRi
- Solana RPC (getTokenSupply, mainnet)
- Orca: https://www.orca.so/pools/FpqnmToS5yRF19FCTrrowbxijCJDvGhA4nFpTamp5te1
- Orca docs: https://docs.orca.so/liquidity/getting-started/beginner-guide
- Altyn Knowledge Base: `00-Overview/Altyn.md`

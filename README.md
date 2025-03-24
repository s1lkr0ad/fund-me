# FundMe - Смарт-контракт для збору коштів

Це смарт-контракт на Solidity, який дозволяє збирати кошти в ETH. Контракт використовує Chainlink для отримання актуальних цін ETH/USD.

## Функціональність

-   Збір коштів в ETH
-   Конвертація ETH в USD через Chainlink Price Feeds
-   Мінімальна сума внеску в USD
-   Відстеження донорів та їх внесків
-   Можливість виведення коштів власником контракту

## Вимоги

-   Foundry
-   Git
-   Node.js (для тестування)

## Встановлення

1. Клонуйте репозиторій:

```bash
git clone https://github.com/s1lkr0ad/fund-me.git
cd fund-me
```

2. Встановіть залежності:

```bash
forge install
```

3. Створіть файл `.env` на основі `.env.example`:

```bash
cp .env.example .env
```

4. Заповніть `.env` файл вашими значеннями:

```
PRIVATE_KEY=your_private_key
SEPOLIA_RPC_URL=your_sepolia_rpc_url
ETHERSCAN_API_KEY=your_etherscan_api_key
```

## Команди

-   Компіляція контрактів:

```bash
forge build
```

-   Запуск тестів:

```bash
forge test
```

-   Деплой на Sepolia:

```bash
make deploy
```

## Структура проекту

-   `src/` - вихідний код смарт-контрактів
    -   `FundMe.sol` - основний контракт
    -   `PriceConverter.sol` - утиліти для конвертації цін
-   `test/` - тести
-   `script/` - скрипти для деплою
-   `lib/` - залежності
-   `cache/` - кеш компіляції
-   `out/` - скомпільовані контракти

## Ліцензія

MIT

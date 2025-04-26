# Cryptocurrency-Exchange-Simulator
This project is a simulation of a cryptocurrency exchange developed in Java, respecting SOLID principles and applying design patterns such as Observer.
****Allows users to:
Register, login and logout.
Manage their wallet (fiat money and cryptocurrencies).
Buy and sell cryptocurrencies at market price.
Place buy/sell orders in the OrderBook.
View your transaction history.
Watch in real time the market price fluctuation.
Work with data persistence in .json files.

****Estructura del proyecto
src/
├── model/
│   ├── Cryptocurrency.java
│   ├── OrderBook.java
│   ├── Transaction.java
│   ├── TransactionHistory.java
│   ├── User.java
│   ├── Wallet.java
│   ├── dto/
│   │   └── OrderBookData.java
│   └── enums/
│       └── TransactionType.java
│
├── model/orders/
│   ├── Order.java
│   ├── BuyOrder.java
│   ├── SellOrder.java
│   └── OrderType.java
│
├── observer/
│   ├── PriceObserver.java
│   └── PriceSubject.java
│
├── service/
│   └── MarketFluctuator.java
│
├── storage/
│   ├── FileStorage.java
│   ├── OrderBookStorage.java
│   └── CryptoStorage.java
│
├── view/
│   ├── MainPanel.java
│   └── UserSessionPanel.java
│
└── Main.java

**** Applied Principles and Patterns
Technical | Application
SOLID | Separation of responsibilities, dependency inversion, classes open to extension.
Observer pattern | MarketFluctuator notifies UserSessionPanel of price changes.
Data persistence | Use of Gson to save and load .json (users, orders, cryptos).
Refactoring | Modular code, small methods, low coupling.

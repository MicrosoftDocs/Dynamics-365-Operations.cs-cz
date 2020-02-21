## <a name="currencies-to-transactioncurrencies"></a>Měny do transactioncurrencies

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Zdrojový filtr: ((CURRENCYCODE != "999"))

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
none | >> | exchangerate | 1

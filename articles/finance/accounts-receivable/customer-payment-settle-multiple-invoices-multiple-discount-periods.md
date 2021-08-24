---
title: Použití jedné platby na úhradu více faktur, které zasahují do více období slevy
description: Toto téma popisuje, jak je více faktur vypláceno, pokud jednotlivé faktury splňují nárok na platební slevu. Scénáře v tomto článku popisují, jak se liší využité platební slevy v závislosti na tom, kdy je platba provedena.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c86423c9e3453d8be11e6bdbc3484647e26e9eeec59c9a2e888cc5a2b2b5592
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769052"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Použití jedné platby na úhradu více faktur, které zasahují do více období slevy

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak je více faktur vypláceno, pokud jednotlivé faktury splňují nárok na platební slevu. Scénáře v tomto článku popisují, jak se liší využité platební slevy v závislosti na tom, kdy je platba provedena.

Fabrikam prodává zboží zákazníkovi 4032. Fabrikam nabízí platební slevu 1 %, pokud je faktura splacena do 14 dní. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry pohledávek**.

## <a name="invoices"></a>Faktury
Zákazník 4032 má tři faktury, které činí 3 000,00 celkem:

-   Faktura FTI-10040 na částku 1 000 byla zadána dne 15. května. Faktura splňuje podmínky platební slevy 1 %, pokud je splacena do 14 dní.
-   Faktura FTI-10041 na částku 1 000 byla zadána dne 25. června. Faktura splňuje podmínky platební slevy 1 %, pokud je splacena do 14 dní.
-   Faktura FTI-10042 na částku 1 000 byla zadána dne 25. června. Tato faktura splňuje podmínky pro platební slevu 2 %, pokud je zaplacena do pěti dnů, a sleva 1 %, pokud je zaplacena do 14 dnů.

## <a name="settle-all-invoices-on-june-29"></a>Uhraďte všechny faktury do 29. června
Pokud Arnie vytvoří deník plateb a úplně vyrovná faktury do 29. června, platba bude ve výši 2 970,00. Součet všech částek slevy bude 30,00. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání:

-   Platba za fakturu FTI 10040 je 1 000,00. Není využitá žádná platební sleva.
-   Platba za fakturu FTI 10041 je 990,00. Bude přijata platební sleva 1 % (10,00).
-   Platba za fakturu FTI 10042 je 980,00. Bude přijata platební sleva 2 % (20,00).

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 15. 5. 2015 | 15. 6. 2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10042   | 1 000,00                             |                                       | USD      | 980,00           |

Po zaúčtování platby bude zůstatek odběratele 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Uhraďte všechny faktury do 1. července
Pokud Arnie vytvoří deník plateb a úplně vyrovná faktury do 1. července, platba bude ve výši 2 980,00. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání:

-   Platba za fakturu FTI 10040 je 1 000,00. Není využitá žádná platební sleva.
-   Platba za fakturu FTI 10041 je 990,00. Bude přijata platební sleva 1 % (10,00).
-   Platba za fakturu FTI 10042 je 990,00. Bude přijata platební sleva 1 % (10,00). Přestože je 1. červenec po období, pro které platí 2% sleva, je to stále období, pro které platí 1% sleva.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 15. 5. 2015 | 15. 6. 2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10042   | 1 000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Částečné vyrovnání 29. června
Odběratel 4032 může uhradit částečnou platbu, například polovinu každé faktury. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání. Na každém řádku zadá částku k vyrovnání na základě pokynů uvedených odběratelem. Když Arnold vybere řádek, uvidí částku slevy pro daný řádek a částku platební slevy, která je využita. Vzhledem k tomu, že zákazník platí poloviční fakturu, Arnie uvidí hodnotu v poli **Částka platební slevy** pro fakturu FTI 10042 jako **20,00**, ale hodnota v poli **Přijatá platební sleva** je **10,00**. Částka platby je 1 485,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 15. 5. 2015 | 15. 6. 2015 | 10040   | 1 000,00                             |                                       | USD      | 500,00           |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10041   | 1 000,00                             |                                       | USD      | 495,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 25. 6. 2015 | 25. 7. 2015 | 10042   | 1 000,00                             |                                       | USD      | 490,00           |

Arnold může také ručně zadat částku platby 1 485 dříve, než otevře stránku **Vyrovnat transakce**. Pokud Arnold ručně zadá částku platby a poté označí všechny tři transakce, ale neupraví hodnotu v poli **Částka k vyrovnání** pro každou transakci, obdrží následující zprávu při zavření stránky:

> Celková částka označených transakcí se liší od částky v deníku. Chcete změnit částku deníku?

Pokud Arnie požaduje, aby byla částka platby pouze 1 485,00, klepne na **Ne** a pak zaúčtuje deník. Transakce jsou vyrovnány následujícím způsobem:

1.  Faktura FTI-10040 bude plně vyrovnána pro 1 000,00, protože byla zadána k 15. května a je nejstarší fakturou. Není využitá žádná platební sleva. Zbývající částka platební transakce je 485,00.
2.  Faktura FTI-10041 není vůbec vyrovnána. Faktury FTI-10041 a FTI 10042 byly zadány ve stejný den. Avšak 1% sleva je dostupná pro fakturu FTI 10041 a pro fakturu FTI 10042 je k dispozici 2% sleva. Vzhledem k tomu, že lepší sleva je k dispozici pro fakturu FTI 10042, zbývající částka 485,00 je vyrovnána s fakturou FTI 10042.
3.  Faktura FTI-10042 je vyrovnána na zbývajících 485,00. Společnost Fabrikam nabízí částečné slevy. V takovém případě je sleva 9,90 (= 485,00 ÷ 0,98 × 0,02). Částka (485,00) je vydělena číslem 0,98, protože existuje 2% sleva (odběratel tedy zaplatí 98 procent faktury). Výsledek je vynásoben procentem slevy nebo 2 procenty. Platba 485,00 plus sleva 9,90 vychází na 494,90. Částka pro původní fakturu byla 1 000,00. Transakce má tedy zůstatek 505,10 (= 1 000,00 – 494,90).

Arnold informace může zobrazit na stránce **Transakce odběratele**.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Faktura          | 15. 5. 2015 | 10040   | 1 000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Faktura          | 25. 6. 2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | USD      |
| FTI-10042  | Faktura          | 25. 6. 2015 | 10042   | 1 000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Platba          | 29. 6. 2015 |         |                                      | 1 485,00                              | 0,00     | USD      |
| SLEV-10040 | Platební sleva    | 29. 6. 2015 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Platba odběratele slouží k vyrovnání více faktur, které zahrnují více období slev"
description: "Tento článek popisuje, jak je více faktur vypláceno, pokud jednotlivé faktury splňují nárok na platební slevu. Scénáře v tomto článku popisují, jak se liší využité platební slevy v závislosti na tom, kdy je platba provedena."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6fd78a587d70ec371861084ac9f76b439c821a8f
ms.lasthandoff: 03/31/2017


---

# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Platba odběratele slouží k vyrovnání více faktur, které zahrnují více období slev

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak je více faktur vypláceno, pokud jednotlivé faktury splňují nárok na platební slevu. Scénáře v tomto článku popisují, jak se liší využité platební slevy v závislosti na tom, kdy je platba provedena.

Tato společnost prodává zboží zákazníkovi 4032. Tato společnost nabízí platební sleva 1 % Pokud je faktura zaplacena do 14 dnů. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Settement parametry jsou umístěny na **parametry pohledávek** stránky.

## <a name="invoices"></a>Faktury
Zákazník 4032 má tři faktury, které činí 3 000,00 celkem:

-   Faktura FTI-10040 pro částku 1 000,00, byl zadán dne 15. Tato faktura je způsobilé pro platební sleva % 1, pokud je zaplacena do 14 dnů.
-   Faktura FTI-10041 pro částku 1 000,00, byl zadán dne 25. Tato faktura je způsobilé pro platební sleva % 1, pokud je zaplacena do 14 dnů.
-   Faktura FTI-10042 pro částku 1 000,00, byl zadán dne 25. Tato faktura je způsobilé pro platební sleva 2 %, pokud je zaplaceno do pěti dnů a sleva 1 % Pokud je zaplacena do 14 dnů.

## <a name="settle-all-invoices-on-june-29"></a>Uhraďte všechny faktury do 29. června
Pokud Arnie vytvoří deník plateb a úplně vyrovná faktury do 29. června, platba bude ve výši 2 970,00. Součet všech částek slevy bude 30,00. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání:

-   Platba za fakturu FTI 10040 je 1 000,00. Není využitá žádná platební sleva.
-   Platba za fakturu FTI 10041 je 990,00. Bude přijata platební sleva 1 % (10,00).
-   Platba za fakturu FTI 10042 je 980,00. Bude přijata platební sleva 2 % (20,00).

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1 000,00                             |                                       | USD      | 980,00           |

Po zaúčtování platby bude zůstatek odběratele 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Uhraďte všechny faktury do 1. července
Pokud Arnie vytvoří deník plateb a úplně vyrovná faktury do 1. července, platba bude ve výši 2 980,00. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání:

-   Platba za fakturu FTI 10040 je 1 000,00. Není využitá žádná platební sleva.
-   Platba za fakturu FTI 10041 je 990,00. Bude přijata platební sleva 1 % (10,00).
-   Platba za fakturu FTI 10042 je 990,00. Bude přijata platební sleva 1 % (10,00). Přestože je 1. červenec po období, pro které platí 2% sleva, je to stále období, pro které platí 1% sleva.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1 000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Částečné vyrovnání 29. června
Odběratel 4032 může uhradit částečnou platbu, například polovinu každé faktury. Arnie vytvoří platbu pro odběratele 4032 a potom otevřete stránku **Vyrovnat transakce**. Na stránce **Vyrovnat transakce** Arnie označí všechny tři řádky faktury pro vyrovnání. Na každém řádku zadá částku k vyrovnání na základě pokynů uvedených odběratelem. Když Arnie vybere řádek, uvidí částku slevy pro daný řádek a částku platební slevy, která je využita. Vzhledem k tomu, že zákazník platí poloviční fakturu, Arnie uvidí hodnotu v poli **Částka platební slevy** pro fakturu FTI 10042 jako **20,00**, ale hodnota v poli **Přijatá platební sleva** je **10,00**. Částka platby je 1 485,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané                 | Normální            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1 000,00                             |                                       | USD      | 500,00           |
| Vybrané                 | Normální            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1 000,00                             |                                       | USD      | 495,00           |
| Vybrané a zvýrazněné | Normální            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1 000,00                             |                                       | USD      | 490,00           |

Arnold můžete také ručně zadat výši platby 1,485.00 dříve, než mu otevře **vyrovnat transakce** stránky. Pokud Arnold ručně zadá částku platby a poté označí všechny tři transakce, ale není mu nastavte hodnotu v **částka k vyrovnání** pole pro každou transakci obdrží následující zprávu při mu Zavře stránku:

> Celková částka označených transakcí se liší od částky v deníku. Chcete změnit částku deníku?

Pokud Arnie požaduje, aby byla částka platby pouze 1 485,00, klepne na **Ne** a pak zaúčtuje deník. Transakce jsou vyrovnány následujícím způsobem:

1.  Faktura FTI-10040 bude plně vyrovnána pro 1 000,00, protože byla zadána k 15. května a je nejstarší fakturou. Není využitá žádná platební sleva. Zbývající částka platební transakce je 485,00.
2.  Faktura FTI-10041 není vůbec vyrovnána. Faktury FTI-10041 a FTI 10042 byly zadány ve stejný den. Avšak 1% sleva je dostupná pro fakturu FTI 10041 a pro fakturu FTI 10042 je k dispozici 2% sleva. Vzhledem k tomu, že lepší sleva je k dispozici pro fakturu FTI 10042, zbývající částka 485,00 je vyrovnána s fakturou FTI 10042.
3.  Faktura FTI-10042 je vyrovnána na zbývajících 485,00. Společnost Fabrikam nabízí částečné slevy. V takovém případě je sleva 9,90 (= 485,00 ÷ 0,98 × 0,02). Částka (485,00) je vydělena číslem 0,98, protože existuje 2% sleva (odběratel tedy zaplatí 98 procent faktury). Výsledek je vynásoben procentem slevy nebo 2 procenty. Platba 485,00 plus sleva 9,90 vychází na 494,90. Částka pro původní fakturu byla 1 000,00. Transakce má tedy zůstatek 505,10 (= 1 000,00 – 494,90).

Arnold informace může zobrazit na stránce **Transakce odběratele**.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Faktura          | 5/15/2015 | 10040   | 1 000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Faktura          | 6/25/2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | USD      |
| FTI-10042  | Faktura          | 6/25/2015 | 10042   | 1 000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Platba          | 6/29/2015 |         |                                      | 1 485,00                              | 0,00     | USD      |
| DISC-10040 | Platební sleva    | 6/29/2015 |         |                                      | 9,90                                  | 0,00     | USD      |







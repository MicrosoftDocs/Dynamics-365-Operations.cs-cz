---
title: "Vyrovnání částečné platby odběratele před datem slevy s konečnou platbou po datu slevy"
description: "Tento článek popisuje účinek plateb pro vyrovnání faktur pro odběratele. Scénáře se zaměřují na dopad v dílčí hlavní knize, není v hlavní knize."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4399cf66e423d2e6436c664e6485a77d9ad75d69
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Vyrovnání částečné platby odběratele před datem slevy s konečnou platbou po datu slevy

[!include[banner](../includes/banner.md)]


Tento článek popisuje účinek plateb pro vyrovnání faktur pro odběratele. Scénáře se zaměřují na dopad v dílčí hlavní knize, není v hlavní knize.

Fabrikam prodává zboží zákazníkovi 4027. Fabrikam nabízí platební slevu 1 %, pokud je faktura splacena do 14 dní. Faktury je nutné zaplatit do 30 dnů. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry pohledávek**.

## <a name="invoice"></a>Faktura
25. června Arnold zadá a zaúčtuje fakturu na 1 000,00 pro zákazníka 4027. Arnold může zobrazit tuto fakturu pomocí tlačítka **Transakce** na stránce **zákazníci**.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Faktura          | 25. 6. 2015 | 10020   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Částečná platba před datem pro platební slevu
2. července odběratel 4027 provede pro fakturu částečnou platbu 297,00. Platba má nárok na platební slevu, protože společnost Fabrikam nabízí slevy pro částečné platby a částečná platba je provedena před datem platební slevy. Proto odběratel 4027 získá platební slevu 3,00. Arnold zaznamená platbu pro odběratele 4027 pomocí deníku plateb. Arnold otevře stránku **Vyrovnat transakce**, aby mohl označit fakturu k vyrovnání.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10020 | 4027    | 25. 6. 2015 | 25. 7. 2015 | 10020   | 1 000,00                             | USD      | 297,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**. Pokud nezměníte hodnotu **Částka k vyrovnání** na hodnotu 297,00, hodnoty **Částka platební slevy**, které se zobrazí, se budou lišit. Avšak 3,00 bude získáno jako platební sleva při zaúčtování platby, protože vyrovnání automaticky nastaví hodnotu ***Částka k vyrovnání*** za vás.

|                              |           |
|------------------------------|-----------|
| Dat. plat. slevy           | 7/09/2015 |
| Částka platební slevy         | 10,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 3,00      |

Arnold zaúčtuje tuto platbu. Faktura má nyní zůstatek 700,00. Následující transakce lze zobrazit pro odběratele.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Faktura          | 25. 6. 2015 | 10020   | 1 000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Platba         | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| SLEV-10020 |  Platební sleva   | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Zbývající platba po datu platební slevy
11. července, což je po období slevy, odběratel 4027 zaplatí zbytek této faktury. Na stránce **Vyrovnat transakce** se částka slevy nezobrazí v poli **Odhadovaná platební sleva** a hodnota v poli **Částka platební slevy** je **0,00**. Když odběratel 4027 zaplatí zbývajících 700,00, není získána žádná další sleva.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10020 | 4027    | 25. 6. 2015 | 25. 7. 2015 | 10020   | 700,00                               | USD      | 700,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 0,00      |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 3,00      |
| Částka platební slevy k přijetí | 0,00      |

Pokud Arnold změní hodnotu v poli **Použít platební slevu** na **Vždy**, nastavení **Vypočítat platební slevy pro částečné platby** se přepíše a uplatní se platební sleva. Částka platby se změní na 693,00 a platební sleva je zbývající částka 7,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané | Vždy            | FTI-10020 | 4027    | 25. 6. 2015 | 25. 7. 2015 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 7:00      |
| Použít platební slevu            | Vždy    |
| Přijatá platební sleva          | 3,00      |
| Částka platební slevy k přijetí | 7:00      |

Arnold změní hodnotu pole **Použít platební slevu** zpět na **Normální**, protože neumožní tomuto odběrateli získat zbývající platební slevu 7,00. Arnold potom zaúčtuje tuto platbu. Po otevření stránky **Transakce odběratele** Arnold zjistí, že faktura má zůstatek 0,00. Také vidí, že zde jsou dvě platby. Jedna platba pro 297,00 s platební slevou 3,00 příkaz a druhá platba je pro 700,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Faktura          | 25. 6. 2015 | 10020   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| SLEV-10020 |                  | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 4 900 * 30% = 1 470 |         |                                      | 700,00                                | 0,00    | USD      |







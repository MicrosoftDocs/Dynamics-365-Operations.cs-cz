---
title: "Vyrovnání částečné platby dodavatele, u níž je více období slev"
description: "Tento článek vás provede scénářem, kdy je více částečných plateb provedeno pro dodavatele, který nabízí více platebních slev."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d88630a62cfdebf0daf19d3bb6af7fcc6e877876
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Vyrovnání částečné platby dodavatele, u níž je více období slev

[!INCLUDE [banner](../includes/banner.md)]

Tento článek vás provede scénářem, kdy je více částečných plateb provedeno pro dodavatele, který nabízí více platebních slev. 

Dodavatel 3054 nabízí společnosti Fabrikam platební slevu 2 % v případě, že je faktura splacena do 5 dní, a platební slevu 1 %, pokud je faktura splacena do 14 dní.

## <a name="invoice"></a>Faktura
28. června Anežka vytvoří fakturu na 1 000,00 pro dodavatele 3054. Na stránce **Transakce dodavatele** si může Anežka transakci prohlédnout.

| Doklad   | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek   | Měna |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10060 | 28. 6. 2015 | 10060   |                                      | 1 000,00                              | -1 000,00 | USD      |

Následující data platební slevy a částky jsou k dispozici pro tuto fakturu.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20,00                | 980,00                         |
| 12. 7. 2015          | 10,00                | 990,00                         |
| 25. 7. 2015          | 0,00                 | 1 000,00                       |

## <a name="payment-on-july-2"></a>Platba k 2. červenci
2. července chce Anežka zaplatit 300,00 z této faktury. Vytvoří jednorázovou platbu pomocí stránky **Deník plateb** v modulu Závazky. Přidá řádek pro dodavatele 3054 a zadá částku platby **300,00**. April otevře stránku **Vyrovnat transakce**, aby mohla označit fakturu k vyrovnání. Aktualizuje hodnotu v poli **Částka k vyrovnání** na **300,00** a zjistí, že hodnota v poli **Částka platební slevy k přijetí** se změnila na **6,12**. Vzhledem k tomu, že je tato platba provedena v prvním období slevy, je použita sleva 2 %.

| Označit | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normální            | Fakt-10060 | 3054    | 28. 6. 2015 | 28. 7. 2015 | 10060   | 1 000,00                       | USD      | 300,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/02/2015 |
| Částka platební slevy         | -20,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -6,12     |

Vzhledem k tomu, že je k dispozici platební sleva, chce April změnit částku platby tak, aby byla celková uhrazená částka pro platbu i platební slevu ve výši 300,00. Změní hodnotu v poli **Částka k vyrovnání** na **294,00** a zjistí, že hodnota v poli **Částka platební slevy k přijetí** se změnila na **6,00**.

| Označit | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normální            | Fakt-10060 | 3054    | 28. 6. 2015 | 28. 7. 2015 | 10060   | 1 000,00                       | USD      | 294,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/02/2015 |
| Částka platební slevy         | -20,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -6,00     |

April zaúčtuje platbu. Na stránce **Transakce dodavatele** si může prohlédnout transakce. Zjistí, že byla ve faktuře použita částka 300,00. Tato částka zahrnuje slevu 6,00. Zbývající zůstatek je proto 700,00.

| Doklad    | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10060  | 28. 6. 2015 | 10060   |                                      | 1 000,00                              | -700,00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| SLEV-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Platba k 8. červenci
8. července April provede dodatečnou platbu faktury. Aby mohla zadat částku, otevře stránku **Vyrovnat transakce** a klikne na **Platební sleva**. Prohlédne si data a částky pro dvě platební slevy, které jsou k dispozici. Vzhledem k tomu, že je tato platba provedena v druhém období slevy, je k dispozici sleva 1 % nebo 5,00. Tato částka se vypočítá jako polovina 1% slevy pro 1 000,00 neboli polovina z 10,00.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 7/3/2015           | 20,00                | 680,00                         |
| 12. 7. 2015          | 10,00                | 690,00                         |
| 25. 7. 2015          | 0,00                 | 700,00                         |

April rozhodne zaplatit 495,00 a využít tak platební slevy 5,00. Celková částka, která je vyrovnána, je tedy 500,00.

| Označit | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normální            | Fakt-10060 | 3054    | 28. 6. 2015 | 28. 7. 2015 | 10060   | 1 000,00                       | USD      | 495,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 12. 7. 2015 |
| Částka platební slevy         | -10,00    |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | -6,00     |
| Částka platební slevy k přijetí | -5,00     |

Na stránce **Transakce dodavatele** April uvidí nový zůstatek 200,00.

| Doklad    | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10060  | 28. 6. 2015 | 10060   |                                      | 1 000,00                              | -200,00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| SLEV-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12. 7. 2015 |         | 495,00                               |                                       | 0,00    | USD      |
| SLEV-10061 | 12. 7. 2015 |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Platba k 20. červenci
20. července April vytvoří konečnou platbu ve výši 200,00. Není možná žádná sleva, protože je platba provedena po ukončení obou období slev. Zůstatek faktury je 0,00.

| Doklad    | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10060  | 28. 6. 2015 | 10060   |                                      | 1 000,00                              | -200,00 | USD      |
| APP-10060  | 7/2/2015  |         | 294,00                               |                                       | 0,00    | USD      |
| SLEV-10060 | 7/2/2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12. 7. 2015 |         | 495,00                               |                                       | 0,00    | USD      |
| SLEV-10061 | 12. 7. 2015 |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10062  | 7/20/2015 |         | 200,00                               |                                       | 0,00    | USD      |







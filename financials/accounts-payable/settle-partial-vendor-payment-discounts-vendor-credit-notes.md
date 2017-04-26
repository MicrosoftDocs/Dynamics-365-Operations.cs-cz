---
title: "Vyrovnání platby částečné dodavatele, který má slevy u dobropisů dodavatelů"
description: "V tomto článku budete provedeni scénářem vyrovnání dobropisu pro fakturu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 849cffa64eaf777f9f4c9243dab41b00fa59ad79
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Vyrovnání platby částečné dodavatele, který má slevy u dobropisů dodavatelů

[!include[banner](../includes/banner.md)]


V tomto článku budete provedeni scénářem vyrovnání dobropisu pro fakturu.

Dodavatelé společnosti Fabrikam poskytují platební slevy pro dobropisy. Dodavatel 3050 umožňuje společnosti Fabrikam přijmout platební slevu 1 %, pokud je faktura splacena do 14 dní.

## <a name="invoice-and-credit-memo"></a>Faktura a dobropis
Na dne 29. dubna vytvoří faktury pro částku 1 000,00 pro dodavatele 3050. V červenci 2 vytvoří dobropis pro 200,00. Ze stránky **Dodavatelé** otevře April stránku **Vyrovnat transakce**. Stránku **Vyrovnat transakce** může použít k označení dobropisu i faktury k vyrovnání. Na dobropisu se vypočítá sleva 2,00. Celková hodnota dobropisu je tedy snížena na 198,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané                 | Normální            | Fakt-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1 000,00                      | USD      | -990,00          |
| Vybrané a zvýrazněné | Normální            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198,00           |

Informace o slevě dobropisu se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/13/2015 |
| Částka platební slevy         | 2,00      |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 2,00      |

April klikne na volbu **Zaúčtovat**. Poté zkontroluje dokončené vyrovnání. April vidí, že se použilo 198,00 z dobropisu a započítala se sleva 2,00. Celková částka je tedy 200,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura  | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Vybrané a zvýrazněné | Normální            | Fakt-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1 000,00                      | USD      | -200,00          |
| Vybrané                 | Normální            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USD      | 198,00           |

April může zkontrolovat transakce dodavatelů na stránce **Transakce dodavatele** tak, že vybere dodavatele na stránce **Všichni dodavatelé **, a poté v podokně akcí klikne na tlačítko **Transakce**. Na této stránce April vidí, že faktura má zůstatek -800,00. Vidí také dobropis na 198,00 a slevu 2,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10070  | Faktura          | 6/29/2015 | 10070   |                                      | 1 000,00                              | -800,00 | USD      |
| Fakt-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Platební sleva   | 7/2/2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Platební sleva   | 7/2/2015  |         |                                      | 2,00                                  | 0,00    | USD      |







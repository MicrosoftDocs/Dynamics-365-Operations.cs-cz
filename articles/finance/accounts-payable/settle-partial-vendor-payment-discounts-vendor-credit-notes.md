---
title: Vyrovnání částečné platby dodavatele, u níž jsou slevy pro dobropisy
description: V tomto článku budete provedeni scénářem vyrovnání dobropisu pro fakturu.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553150a59d132bb1d8b563e03456995cbc8d2be5f36bab0c1fe6b8bbbf77dce1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737106"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Vyrovnání částečné platby dodavatele, u níž jsou slevy pro dobropisy

[!include [banner](../includes/banner.md)]

V tomto článku budete provedeni scénářem vyrovnání dobropisu pro fakturu.

Dodavatelé společnosti Fabrikam poskytují platební slevy pro dobropisy. Dodavatel 3050 umožňuje společnosti Fabrikam přijmout platební slevu 1 %, pokud je faktura splacena do 14 dní.

## <a name="invoice-and-credit-memo"></a>Faktura a dobropis
29. června Anežka vytvoří fakturu na 1 000,00 pro dodavatele 3050. V 2. července vytvoří dobropis pro 200,00. Ze stránky **Dodavatelé** otevře April stránku **Vyrovnat transakce**. Stránku **Vyrovnat transakce** může použít k označení dobropisu i faktury k vyrovnání. Na dobropisu se vypočítá sleva 2,00. Celková hodnota dobropisu je tedy snížena na 198,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané                 | Normální            | Fakt-10070 | 3050    | 29. 6. 2015 | 7/29/2015 | 10070   | -1 000,00                      | USD      | -990,00          |
| Vybrané a zvýrazněné | Normální            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198,00           |

Informace o slevě dobropisu se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

| Pole                        | Hodnota     |
|------------------------------|-----------|
| Dat. plat. slevy           | 7/13/2015 |
| Částka platební slevy         | 2.00      |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 2,00      |

April klikne na volbu **Zaúčtovat**. Poté zkontroluje dokončené vyrovnání. April vidí, že se použilo 198,00 z dobropisu a započítala se sleva 2,00. Celková částka je tedy 200,00.

| Označit                     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura  | Částka v měně transakce | Měna | Částka k vyrovnání |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Vybrané a zvýrazněné | Normální            | Fakt-10070 | 3050    | 29. 6. 2015 | 7/29/2015 | 10070    | -1 000,00                      | USD      | -200,00          |
| Vybrané                 | Normální            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USD      | 198,00           |

April může zkontrolovat transakce dodavatelů na stránce **Transakce dodavatele** tak, že vybere dodavatele na stránce **Všichni dodavatelé**, a poté v podokně akcí klikne na tlačítko **Transakce**. Na této stránce April vidí, že faktura má zůstatek -800,00. Vidí také dobropis na 198,00 a slevu 2,00.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10070  | Faktura          | 29. 6. 2015 | 10070   |                                      | 1 000,00                              | -800,00 | USD      |
| Fakt-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| SLEV-10071 |  Platební sleva   | 7/2/2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| SLEV-10071 |  Platební sleva   | 7/2/2015  |         |                                      | 2,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Použití větší slevy, než je vypočítaná, pro platbu dodavatele
description: Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře. K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810239"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Použití větší slevy, než je vypočítaná, pro platbu dodavatele

[!include [banner](../includes/banner.md)]

Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře. K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře. 

Dodavatel 3051 umožňuje společnosti Fabrikam přijmout platební slevu 4 %, pokud je faktura splacena do 7 dní. Dne 29. dubna je zadána faktura na 1 000,00. Dodavatel umožňuje April využít slevu 60,00 namísto výchozí slevy 40,00, která je k dispozici pro fakturu. April zaznamená jednorázovou platbu pomocí deníku plateb závazků. Zadá platby dodavatele a otevře stránku **Vyrovnat transakce**. Označí fakturu a změní hodnotu v poli **Částka platební slevy** na **-60,00**.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | Fakt-10040 | 3051    | 29. 6. 2015 | 7/29/2015 | 10040   | 1 000,00                       | USD      | 940,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.

| Pole                        | Hodnota     |
|------------------------------|-----------|
| Dat. plat. slevy           | 12. 7. 2015 |
| Částka platební slevy         | 60.00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 60,00     |

Potom April zaúčtuje platební deník. Faktura je plně uhrazena pomocí platby 940,00 a slevy 60,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
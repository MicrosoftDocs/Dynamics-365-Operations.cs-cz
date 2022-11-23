---
title: Vyrovnat částečnou platbu odběratele, u níž jsou slevy pro dobropisy
description: Tento článek vás provede scénářem, kde je využita platební sleva na základě dobropisu, když původní faktura měla také platební slevu.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f64b9b9cd4fa65d17ba30fb87a688411becd5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780458"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Vyrovnat částečnou platbu odběratele, u níž jsou slevy pro dobropisy

[!include [banner](../includes/banner.md)]

Tento článek vás provede scénářem, kde je využita platební sleva na základě dobropisu, když původní faktura měla také platební slevu. 

Společnost Fabrikam umožňuje zákazníkům získat platební slevy pro částečné platby a také u dobropisů. Platební slevy mohou být získány na základě dobropisu, když je vystaven dobropis pro fakturu, u které zákazník získal platební slevu. Místo poskytnutí kreditu na celou částku můžete připsat k zůstatku odběratele částku, která nezahrnuje procento platební slevy, kterou odběratel získal. Parametry vyrovnání se nacházejí na stránce **Parametry pohledávek**.

## <a name="invoice-and-credit-note"></a>Faktura a dobropis
Zákazník 4035 má fakturu na 1 000,00 a dobropis na 100,00. Každý dokument má 1% slevu v případě úhrady do 14 dní. Arnold tyto informace můžete zobrazit na stránce **Transakce odběratele**.

| Doklad    | Typ transakce | Datum      | Faktura  | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Faktura          | 28. 6. 2020 | 10050    | 1,000.00                             |                                       | 1,000.00 | USD      |
| CCRN-10050 | Dobropis      | 28. 6. 2020 | CR-10050 |                                      | 100.00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Vyrovnání dobropis s fakturou
Ze stránky **Transakce odběratele** Arnold otevře stránku **Vyrovnat transakce**. Může stránku **Vyrovnat transakce** použít k vyrovnání faktury a dobropisu. Jako součást procesu vyrovnání si prohlédne data platební slevy a částky. Označí dva dokumenty a klikne na tlačítko **Zaúčtovat** k vyrovnání transakcí. Pro dobropis existuje sleva -1,00, protože společnost Fabrikam umožňuje slevy pro dobropisy.

| Označit     | Použít platební slevu | Doklad    | Účet | Datum      | Datum splatnosti  | Faktura  | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10050  | 4035    | 28. 6. 2020 | 28. 7. 2020 | 10050    | 1,000.00                       | USD      | 990.00           |
| Vybrané | Normální            | CCRN-10050 | 4035    | 28. 6. 2020 | 28. 7. 2020 | CR-10050 | -100,00                        | USD      | -99,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.

- **Datum platební slevy**: 12. 7. 2020 
- **Částka platební slevy**: -1,00     
- **Použít platební slevu**: Normální    
- **Přijatá platební sleva**: 0,00      
- **Částka platební slevy k přijetí**: -1,00     

Vyrovnání bude 100,00 a bude zahrnovat vyplacení 99,00 a slevu 1,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

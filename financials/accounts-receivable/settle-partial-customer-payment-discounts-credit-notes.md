---
title: "Vyrovnání platby částečné odběratele, který má slevy u dobropisů"
description: "Tento článek vás provede scénářem, kde je využita platební sleva na základě dobropisu, když původní faktura měla také platební slevu."
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
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e43bcea67d9c408c93258f9b64565560b59fbb88
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Vyrovnání platby částečné odběratele, který má slevy u dobropisů

[!include[banner](../includes/banner.md)]


Tento článek vás provede scénářem, kde je využita platební sleva na základě dobropisu, když původní faktura měla také platební slevu. 

Společnost Fabrikam umožňuje zákazníkům získat platební slevy pro částečné platby a také u dobropisů. Platební slevy mohou být získány na základě dobropisu, když je vystaven dobropis pro fakturu, u které zákazník získal platební slevu. Místo poskytnutí kreditu na celou částku můžete připsat k zůstatku odběratele částku, která nezahrnuje procento platební slevy, kterou odběratel získal. Vyrovnání parametry jsou umístěny na **parametry pohledávek** stránky.

## <a name="invoice-and-credit-note"></a>Faktura a dobropis
Zákazník 4035 má fakturu na 1 000,00 a dobropis na 100,00. Každý dokument má 1% slevu v případě úhrady do 14 dní. Arnold tyto informace můžete zobrazit na stránce **Transakce odběratele**.

| Doklad    | Typ transakce | Datum      | Faktura  | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Faktura          | 6/28/2015 | 10050    | 1 000,00                             |                                       | 1 000,00 | USD      |
| CCRN-10050 | Dobropis      | 6/28/2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Vyrovnání dobropis s fakturou
Ze stránky **Transakce odběratele** Arnold otevře stránku **Vyrovnat transakce**. Může stránku **Vyrovnat transakce** použít k vyrovnání faktury a dobropisu. Jako součást procesu vyrovnání si prohlédne data platební slevy a částky. Označí dva dokumenty a klikne na tlačítko **Zaúčtovat** k vyrovnání transakcí. Pro dobropis existuje sleva -1,00, protože společnost Fabrikam umožňuje slevy pro dobropisy.

| Označit     | Použít platební slevu | Doklad    | Účet | Datum      | Datum splatnosti  | Faktura  | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1 000,00                       | USD      | 990,00           |
| Vybrané | Normální            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100,00                        | USD      | -99,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/12/2015 |
| Částka platební slevy         | -1,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | -1,00     |

Vyrovnání bude 100,00 a bude zahrnovat vyplacení 99,00 a slevu 1,00.





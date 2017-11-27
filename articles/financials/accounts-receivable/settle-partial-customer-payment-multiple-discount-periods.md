---
title: "Vyrovnání částečné platby zákazníka, u níž je více období slev"
description: "Tento článek popisuje způsob, jakým se vyrovnávají platby odběratelů po více období slevy."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ac64ece82abe75f3cba437b1ec1af499fbbce8e4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Vyrovnání částečné platby zákazníka, u níž je více období slev

[!include[banner](../includes/banner.md)]


Tento článek popisuje způsob, jakým se vyrovnávají platby odběratelů po více období slevy.

Společnost Fabrikam nabízí odběrateli 4031 dvě období pokladních slev. Odběratel obdrží platební slevu 2 % v případě, že je faktura splacena do 5 dní, a platební slevu 1 %, pokud je faktura splacena do 14 dní. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Parametry vyrovnání se nacházejí na stránce **Parametry pohledávek**.

## <a name="invoice"></a>Faktura
25. června Arnold zadá a zaúčtuje fakturu na 1 000,00 pro zákazníka 4031. Když posuzuje platební slevy pro tuto fakturu, vidí Arnold, že zákazník 4031 zákazníka přijme slevu ve výši 20,00 slevu, pokud je faktura zaplacena do 30. června Pokud je faktura zaplacena do 9. června, zákazník obdrží slevu ve výši 10,00.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20,00                | 980,00                         |
| 7/9/2015           | 10,00                | 990,00                         |
| 25. 7. 2015          | 0,00                 | 1 000,00                       |

Arnold tyto transakce můžete zobrazit na stránce**Transakce odběratele**.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Faktura          | 25. 6. 2015 | 10030   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Částečná platba před datem pro platební slevu
Dne 28. června provede odběratel 4031 částečné platbu ve výši 294,00. Vzhledem k tomu, že 28. června spadá do období první platební slevy, odběratele má slevu 6,00. Na stránce **Vyrovnat transakce** je hodnota**částky platební slevy** 20,00, a hodnota **částka platební slevy k přijetí** je 6,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10030 | 4031    | 25. 6. 2015 | 25. 7. 2015 | 10030   | 1 000,00                       | USD      | 294,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**. Pokud nezměníte hodnotu **Částka k vyrovnání** na hodnotu **294,00**, hodnoty **Částka platební slevy**, které se zobrazí, se budou lišit. Avšak 6,00 bude získáno jako platební sleva při zaúčtování platby, protože vyrovnání automaticky nastaví hodnotu **Částka k vyrovnání**za vás.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 6/30/2015 |
| Částka platební slevy         | 20,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 0,00      |
| Částka platební slevy k přijetí | 6,00      |

Po zaúčtování platby Arnoldem je zůstatek faktury 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Částečná platba před datem pro druhou platební slevu
8. července odběratel zaplatil zbývající částku z faktury. Vzhledem k tomu, že je tato platba provedena v druhém období slevy, je k dispozici sleva 7,00 (1 %).

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10030 | 4031    | 25. 6. 2015 | 25. 7. 2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**.

|                              |           |
|------------------------------|-----------|
| Datum platební slevy           | 7/09/2015 |
| Částka platební slevy         | 30,00     |
| Použít platební slevu            | Normální    |
| Přijatá platební sleva          | 6,00      |
| Částka platební slevy k přijetí | 7:00      |

Zůstatek faktury je nyní 0,00. Arnold informace může zobrazit na stránce **Transakce odběratele**.

| Doklad    | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek | Měna |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Faktura          | 25. 6. 2015 | 10030   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Platba         | 28. 6. 2015 |         |                                      | 294,00                                | 0,00    | USD      |
| SLEV-10030 |  Platební sleva   | 28. 6. 2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Platba         | 7/8/2015  |         |                                      | 693,00                                | 0,00    | USD      |
| SLEV-1031  |  Platební sleva   | 7/8/2015  |         |                                      | 7:00                                  | 0,00    | USD      |







---
title: "Vyrovnání platby částečné odběratele, který má více období slev"
description: "Tento článek popisuje způsob, jakým se vyrovnávají platby odběratelů po více období slevy."
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
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9da48c7861f48ec2a154ac12616149d1208346cf
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Vyrovnání platby částečné odběratele, který má více období slev

[!include[banner](../includes/banner.md)]


Tento článek popisuje způsob, jakým se vyrovnávají platby odběratelů po více období slevy.

Společnost Fabrikam nabízí odběrateli 4031 dvě období pokladních slev. Odběratel obdrží platební slevu 2 % v případě, že je faktura splacena do 5 dní, a platební slevu 1 %, pokud je faktura splacena do 14 dní. Společnost Fabrikam nabízí také platební slevy pro částečné platby. Vyrovnání parametry jsou umístěny na **parametry pohledávek** stránky.

## <a name="invoice"></a>Faktura
25. června Arnold zadá a účtuje faktury pro částku 1 000,00 4031 zákazníka. Když mu posuzuje platební slevy pro tuto fakturu, vidí Arnold 4031 zákazníka přijme nastavena hodnota 20,00 slevu, pokud je faktura zaplacena do 30. Pokud je faktura zaplacena ve dne 9, zákazník obdrží 10,00 slevy.

| Datum platební slevy | Částka platební slevy | Částka v měně transakce |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20,00                | 980,00                         |
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1 000,00                       |

Arnold tyto transakce můžete zobrazit na stránce** Transakce odběratele**.

| Doklad   | Typ transakce | Datum      | Faktura | Částka Má dáti v transakční měně | Částka Dal v transakční měně | Zůstatek  | Měna |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Faktura          | 6/25/2015 | 10030   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Částečná platba před datem pro platební slevu
Dne 28. června provede odběratel 4031 částečné platbu ve výši 294,00. Vzhledem k tomu, že 28. června spadá do období první platební slevy, odběratele má slevu 6,00. Na stránce **Vyrovnat transakce** je hodnota** částky platební slevy** 20,00, a hodnota **částka platební slevy k přijetí** je 6,00.

| Označit     | Použít platební slevu | Doklad   | Účet | Datum      | Datum splatnosti  | Faktura | Částka v měně transakce | Měna | Částka k vyrovnání |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Vybrané | Normální            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 1 000,00                       | USD      | 294,00           |

Informace o slevě se zobrazí v dolní části stránky **Vyrovnat otevřené transakce**. Pokud nezměníte hodnotu **Částka k vyrovnání** na hodnotu **294,00**, hodnoty **Částka platební slevy**, které se zobrazí, se budou lišit. Avšak 6,00 bude získáno jako platební sleva při zaúčtování platby, protože vyrovnání automaticky nastaví hodnotu **Částka k vyrovnání **za vás.

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
| Vybrané | Normální            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

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
| FTI-10030  | Faktura          | 6/25/2015 | 10030   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Platba         | 6/28/2015 |         |                                      | 294,00                                | 0,00    | USD      |
| SLEV-10030 |  Platební sleva   | 6/28/2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Platba         | 7/8/2015  |         |                                      | 693,00                                | 0,00    | USD      |
| SLEV-1031  |  Platební sleva   | 7/8/2015  |         |                                      | 7:00                                  | 0,00    | USD      |







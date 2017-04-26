---
title: "Platby částečných částek dodavatelem"
description: "Někdy provedete platbu dodavateli, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace. Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci."
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
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Platby částečných částek dodavatelem

[!include[banner](../includes/banner.md)]


Někdy provedete platbu dodavateli, která je nižší než částka faktury. Tento článek popisuje různé možnosti pro zvládnutí této situace. Dostupné možnosti závisí na daných obchodních požadavcích a konfiguraci. 

<a name="cash-discount-amounts"></a>Částka platebních slev
---------------------

Dodavatel vám může nabídnout platební slevu za úhradu faktury před datem splatnosti. Například zadáte fakturu na částku 100,00, která určuje 2% platební slevu, pokud bude faktura zaplacena do 10 dní. Doba splatnosti dle podmínek je 30 dnů. Pokud návrh platby používá platební slevy jako kritérium pro výběr faktury a návrh je spustit nebo dřívější než datum platební slevy, je zaškrtnuto faktura pro platbu a platby je vytvořen pro 98.00. Platební slevy lze brát pro jednorázovou platbu, která byla vytvořena ručně.

## <a name="partial-payments-with-cash-discounts"></a>Částečné platby s platebními slevami
Když provedete částečnou úhradu, můžete plánovat uskutečnění další částečné platby k úplnému vyrovnání faktury. Aby platební slevy pro částečné platby, je nutné nastavit ** vypočítat platební slevy pro částečné platby ** možnost na **Ano** na **účet parametry závazků** stránky. 

Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Je zaúčtována faktura na 100,00. Pokud provádíte platby 49.00 do 10 dnů, zadáte MD 49.00 v deníku plateb. Při vyrovnání částečné platby na **vyrovnání otevřených transakcí** stránku, **1.00** se zobrazí v **částka platební slevy se** pole. 

> [!NOTE] 
> Pokud zadáte dílčí platby a nechat celou fakturovanou částku v **částka k vyrovnání** pole, **částka platební slevy se** pole je automaticky přepočítán při zaúčtování transakcí.

## <a name="credit-notes-with-cash-discounts"></a>Dobropisy s platebními slevami
Můžete vrátit některé položky na faktuře a přijmout dobropis. Pokud pro původní fakturu byla využita platební sleva, můžete odečíst hodnotu slevy a přijmout refundaci pro správnou částku. Pokud ** vypočítat platební slevy pro dobropisy ** možnost je nastavena na **Ano** na **parametry závazků** stránky slevu vypočítá automaticky pro dobropis. 

Například můžete přijmout platební slevu 2 %, pokud bude faktura proplacena do 10 dnů po vydání. Je zaúčtována faktura na 100,00. Pokud vrátit zboží a obdržet dobropis, můžete zadat dobropisu pro celou částku původní faktury 100,00 a 2 procenta platební slevy, která je také definován v tomto dobropise.  Při zobrazení dobropis na **vyrovnat transakce** stránku, **98.00** se zobrazí v **částka k vyrovnání** pole a **-2.00** se zobrazí v **částka platební slevy** pole. Částka slevy je zaúčtována na účet platební slevy.

## <a name="overpaymentunderpayment-amounts"></a>Částky přeplatku nebo nedoplatku
Můžete provést částečnou úhradu, když je částka, která musí být vyrovnána, příliš malá. Například faktura dodavatele je pro 1 000,00 a vy platíte 999,90 Je-li zůstatek nižší než částka zadaná pro přeplatky nebo nedoplatky na stránce **Parametry závazků**, rozdíl se automaticky zaúčtuje na účet hlavní knihy pro přeplatky a nedoplatky.





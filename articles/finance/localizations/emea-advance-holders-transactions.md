---
title: Transakce držitelů záloh
description: Zjistěte více o tom, jak pracovat s transakcemi držitelů záloh v aplikaci Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 262554
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a68c00fc7fc6742da7b2732897fd21e0028f1493
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407594"
---
# <a name="advance-holder-transactions"></a>Transakce držitelů záloh

[!include [banner](../includes/banner.md)]

Zjistěte více o tom, jak pracovat s transakcemi držitelů záloh.

Transakce pro tyto pracovníky, kteří jsou držitelé zálohy, mohou být zaúčtovány pomocí účtů držitele zálohy. ID pracovníka, které je určeno pro každého držitele zálohy, lze použít ke sledování všech transakcí držitele zálohy. Toto číslo je načteno jako číslo účtu pro transakce držitele zálohy na stránkách **Hlavní deníky** a **Transakce držitele zálohy**.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Tvorba a zaúčtování nákupních objednávek s podrobnostmi o držiteli zálohy
Další obecné informace o nákupních objednávkách naleznete v tématu [Přehled nákupních objednávek](../../supply-chain/procurement/purchase-order-overview.md). Pokud je faktura dodavatele vytvořena a zaúčtována s podrobnostmi držitele zálohy, zůstatky držitele zálohy budou zaúčtovány do účtu zůstatku zaměstnance namísto do účtu zůstatku dodavatele. Chcete-li přidat podrobnosti držitele zálohy k nákupní objednávce, postupujte takto:

-   V poli **Platební podmínky** v části **Ceny a slevy** vyberte platební podmínku. <!---For more information about **Terms of payment**, see [Define vendor payment terms](../accounts-payable/tasks/define-vendor-payment-terms.md).--> Vyberte platební podmínku, která má na stránce **Platební podmínky** vybranou možnost **Od držitele zálohy**. Další informace o nastavení platebních podmínek pro držitele záloh naleznete v tématu [Přehled držitelů zálohy](emea-advance-holders.md).
-   V poli **Držitel zálohy** na pevné záložce **Ceny a slevy** vyberte držitele zálohy pro nákupní objednávku.

Proces zaúčtování nákupní objednávky vytvoří dvě transakce dodavatele s opačným částkami a jednu transakci držitele zálohy. Bez podrobností držitele zálohy je vytvořena pouze jedna transakce dodavatele.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím banky
Když vyrovnáte zůstatky držitelů záloh prostřednictvím banky, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v hlavním deníku. Můžete nastavit kód pro deník a banky v části **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Přehled držitelů zálohy](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím banky, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v bance**. Na stránce **Uzavřít v bance** zadejte následující informace.

| Pole                    | popis |
|------------------------------|-------------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.|

## <a name="settle-advance-holder-balances-via-cash"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím hotovosti
Když vyrovnáte zůstatky držitelů záloh prostřednictvím hotovosti, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v deníku dokladů. Můžete nastavit kód pro deník a hotovost na kartě **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Přehled držitelů zálohy](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím hotovosti, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v hotovosti**. Na stránce **Uzavřít v hotovosti** zadejte následující informace.

| Pole                    | popis
|------------------------------|-----------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro automatické vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.     |

Po zpracování deníku dokladů, pokud částka v poli **Převáděná částka** je záporná, výdajový doklad je vygenerován pro držitele zálohy při uzavření zůstatků. Pokud částka v poli **Převáděná částka** byla pozitivní, vygeneruje se refundační doklad.

## <a name="additional-resources"></a>Další zdroje

- [Záloha pro zaměstnance (východní Evropa)](tasks/advance-payment-employee.md)


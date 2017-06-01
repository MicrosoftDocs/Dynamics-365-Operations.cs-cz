---
title: "Transakce držitelů záloh"
description: "Naučte se pracovat s transakcemi držitele zálohy v aplikaci Microsoft Dynamics 365 for Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262554
ms.assetid: 84ff97bb-ae21-4d6d-8160-9325f64134ce
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: dfca71b0ba48a725d1e1c5418d9e505744545d33
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="advance-holder-transactions"></a>Transakce držitelů záloh

[!include[banner](../includes/banner.md)]


Naučte se pracovat s transakcemi držitele zálohy v aplikaci Microsoft Dynamics 365 for Operations.

Transakce pro tyto pracovníky, kteří jsou držitelé zálohy, mohou být zaúčtovány pomocí účtů držitele zálohy. ID pracovníka, které je určeno pro každého držitele zálohy, lze použít ke sledování všech transakcí držitele zálohy. Toto číslo je načteno jako číslo účtu pro transakce držitele zálohy na stránkách **Hlavní deníky** a **Transakce držitele zálohy**.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Tvorba a zaúčtování nákupních objednávek s podrobnostmi o držiteli zálohy
Další obecné informace o nákupních objednávkách naleznete v tématu [Přehled nákupních objednávek](/manufacturing/procurement/purchase-order-overview). Pokud je faktura dodavatele vytvořena a zaúčtována s podrobnostmi držitele zálohy, zůstatky držitele zálohy budou zaúčtovány do účtu zůstatku zaměstnance namísto do účtu zůstatku dodavatele. Chcete-li přidat podrobnosti držitele zálohy k nákupní objednávce, postupujte takto:

-   V poli **Platební podmínky** v části **Ceny a slevy** vyberte platební podmínku. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).-->Vyberte platební podmínku, která má na stránce **Platební podmínky** vybranou možnost **Od držitele zálohy**. Další informace o nastavení platebních podmínek pro držitele záloh naleznete v tématu [Držitelé zálohy](emea-advance-holders.md).
-   V poli **Držitel zálohy** na pevné záložce **Ceny a slevy** vyberte držitele zálohy pro nákupní objednávku.

Proces zaúčtování nákupní objednávky vytvoří dvě transakce dodavatele s opačným částkami a jednu transakci držitele zálohy. Bez podrobností držitele zálohy je vytvořena pouze jedna transakce dodavatele.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím banky
Když vyrovnáte zůstatky držitelů záloh prostřednictvím banky, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v hlavním deníku. Můžete nastavit kód pro deník a banky v části **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Držitelé záloh](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím banky, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v bance**. Na stránce **Uzavřít v bance** zadejte následující informace.

| Pole                    | popis |
|------------------------------|-------------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.|

## <a name="settle-advance-holder-balances-via-cash"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím hotovosti
Když vyrovnáte zůstatky držitelů záloh prostřednictvím hotovosti, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v deníku dokladů. Můžete nastavit kód pro deník a hotovost na kartě **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Držitelé záloh](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím hotovosti, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v hotovosti**. Na stránce **Uzavřít v hotovosti** zadejte následující informace.

| Pole                    | popis
|------------------------------|-----------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro automatické vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.     |

Po zpracování deníku dokladů, pokud částka v poli **Převáděná částka** je záporná, výdajový doklad je vygenerován pro držitele zálohy při uzavření zůstatků. Pokud částka v poli **Převáděná částka** byla pozitivní, vygeneruje se refundační doklad.





---
title: "Transakce držitelů záloh"
description: "Naučte se pracovat s transakce držitele zálohy v 365 Microsoft Dynamics pro operace."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: c819fbbb4a68dd5b8b192416fedb34827bbf3823
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holder-transactions"></a>Transakce držitelů záloh

[!include[banner](../includes/banner.md)]


Naučte se pracovat s transakce držitele zálohy v 365 Microsoft Dynamics pro operace.

Transakce pro tyto pracovníky, kteří jsou držitelé mohou být účtovány pomocí účtů držitele zálohy dopředu. ID pracovníka, který je určen pro každého držitele zálohy lze sledovat všechny transakce držitele zálohy. Toto číslo je načteno jako číslo účtu pro transakce držitele zálohy v **hlavní deníky** a **transakce držitele zálohy** stránek.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Vytvoření a zaúčtování nákupní objednávky s údaji držitele zálohy
Další obecné informace o nákupních objednávkách naleznete v tématu [nákupní objednávky přehled](/manufacturing/procurement/purchase-order-overview). Pokud faktura dodavatele je vytvořena a zaúčtována s údaji držitele zálohy, zůstatků držitele zálohy budou zaúčtovány do rozvahového účtu zaměstnance místo zůstatek účtu dodavatele. Chcete-li přidat podrobnosti držitele zálohy k nákupní objednávce, postupujte takto:

-   V **platební podmínky** v **ceny a slevy** vyberte platební podmínku. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).-->Vyberte platební podmínku, která má **od držitele zálohy** na vybranou možnost **platební podmínky** stránky. Další informace o nastavení platební podmínky pro držitele záloh naleznete v tématu [držitelů záloh](emea-advance-holders.md).
-   V **držitele zálohy** v **ceny a slevy** s náhledem vyberte držitele zálohy pro nákupní objednávku.

Proces zaúčtování nákupní objednávky se vytvoří dvě transakce dodavatele s opačným částkami a jednu transakci držitele zálohy. Bez podrobností držitele zálohy je vytvořena pouze jedna dodavatelská transakce.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím banky
Když se vyrovnávají zůstatků držitele zálohy prostřednictvím banky, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvářeny ve finančním deníku. Můžete nastavit kód pro deník a banky v **držitelů záloh** oddílu na **parametry závazků** stránky. Další informace naleznete v tématu [držitelů záloh](emea-advance-holders.md). Pro uzavření zůstatků držitele zálohy prostřednictvím banky, otevřete **závazků**&gt;**držitelů záloh**&gt;**držitelů záloh**. Klepněte **Zůstatek** tlačítka v podokně akcí a potom klepněte na tlačítko **zavřít přes banku**. Zadejte následující informace **přes banku Zavřít** stránky.

| Pole                    | popis |
|------------------------------|-------------------|
| **Date of payment**          | Zadejte datum, které by měla být platba zaúčtována.|
| **Částka určená k převodu** | Zadejte částku zůstatku při zavírání. Částku, která je uvedena v **množství** v **Zůstatek** formuláře se zobrazí ve výchozím nastavení. |
| **Automatic**                | Vyberte **automatické** políčko, chcete-li vytvořit a zaúčtovat deník, který je přednastavený na **parametry závazků** stránky.|

## <a name="settle-advance-holder-balances-via-cash"></a>Vyrovnání zůstatků držitele zálohy hotovosti
Když se vyrovnávají zůstatků držitele zálohy hotovosti, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvářeny v deníku dokladů. Můžete nastavit kód pro deník a hotovost v **držitelů záloh** na kartě **parametry závazků** stránky. Další informace naleznete v tématu [držitelů záloh](emea-advance-holders.md). Zavřete držitele zálohy zůstatek hotovosti, otevřete **závazků**&gt;**držitelů záloh**&gt;**držitelů záloh**. Klepněte **Zůstatek** tlačítka v podokně akcí a potom klepněte na tlačítko **zavřít hotovosti**. Zadejte následující informace **zavřít hotovosti** stránky.

| Pole                    | popis
|------------------------------|-----------------|
| **Date of payment**          | Zadejte datum, které by měla být platba zaúčtována.|
| **Částka určená k převodu** | Zadejte částku zůstatku při zavírání. Částku, která je uvedena v **množství** v **Zůstatek** formuláře se zobrazí ve výchozím nastavení. |
| **Automatic**                | Vyberte **automaticky** políčko automaticky zaúčtovat deník, a vytvořte přednastavení **parametry závazků** stránky.     |

Po listu deníku zpracován, pokud částka v **částka určená k převodu** pole byla záporná, výdajový doklad je generován pro držitele zálohy při uzavření zůstatků. Pokud částka v **částka určená k převodu** pole byla pozitivní, refundační doklad je generován.





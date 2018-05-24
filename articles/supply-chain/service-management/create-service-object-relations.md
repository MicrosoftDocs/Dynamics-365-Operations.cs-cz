---
title: "Vytvoření vztahů předmětů servisu"
description: "Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c27070436139f784af690900a3f1ab108a809d03
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-object-relations"></a>Vytvoření vztahů předmětů servisu 

[!include [banner](../includes/banner.md)]


Toto téma popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku. Při vytvoření vztahu předmětu servisu připojíte předmět servisu k servisní smlouvě nebo zakázce. Pokud zákazník vyžádá servis položky, která je předmět servisu, můžete vybrat předmět servisu ze seznamu vztahů předmětu servisu.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Vytvoření vztahu předmětů služeb pro servisní smlouvu

Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní smlouvu:

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.

2.  V seznamu **Servisní smlouvy** vyberte existující servisní smlouvu nebo klepněte na tlačítko **Nová** a vytvořte novou servisní smlouvu.

3.  Ve formuláři **Servisní smlouvy** v **podokně akcí** na kartě **Servisní smlouva** ve skupině **Vztahy** klikněte na **Objekty servisu**.

4.  Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní smlouvu.

5.  Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**. Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Vytvoření vztahu předmětů služeb pro servisní objednávku

Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní objednávku:

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  V seznamu **Servisní zakázky** vyberte existující servisní zakázku nebo vytvořte novou zakázku.

3.  Ve formuláři **Servisní zakázky** v **podokně akcí** na kartě **Servisní zakázka** ve skupině **Vztahy** klikněte na **Objekty servisu**.

4.  Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní zakázku.

5.  Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**. Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu. 


## <a name="see-also"></a>Viz také

[Předměty servisu](service-objects.md)

[vztahy předmětu servisu](service-object-relations.md)

[Kusovníky šablony](template-boms.md)

  




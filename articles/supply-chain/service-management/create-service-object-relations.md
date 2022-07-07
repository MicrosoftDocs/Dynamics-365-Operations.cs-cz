---
title: Vytvoření vztahů předmětů servisu
description: Tento článek popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d9424b5678a6f37d46203e5d4e359b020fda7a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016907"
---
# <a name="create-service-object-relations"></a>Vytvoření vztahů předmětů servisu 

[!include [banner](../includes/banner.md)]


Tento článek popisuje postup vytvoření vztahů předmětů servisu pro servisní smlouvu a zakázku. Při vytvoření vztahu předmětu servisu připojíte předmět servisu k servisní smlouvě nebo zakázce. Pokud zákazník vyžádá servis položky, která je předmět servisu, můžete vybrat předmět servisu ze seznamu vztahů předmětu servisu.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Vytvoření vztahu předmětů služeb pro servisní smlouvu

Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní smlouvu:

1.  Klikněte na **Správa služeb** \> **Servisní smlouvy** \> **Servisní smlouvy**.

2.  V seznamu **Servisní smlouvy** vyberte existující servisní smlouvu nebo klepněte na tlačítko **Nová** a vytvořte novou servisní smlouvu.

3.  Ve formuláři **Servisní smlouvy** v **podokně akcí** na kartě **Servisní smlouva** ve skupině **Vztahy** klikněte na **Objekty servisu**.

4.  Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní smlouvu.

5.  Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**. Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Vytvoření vztahu předmětů služeb pro servisní objednávku

Pomocí následujících kroků můžete vytvořit vztah předmětu servisu pro servisní objednávku:

1.  Klikněte na **Řízení služeb** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  V seznamu **Servisní zakázky** vyberte existující servisní zakázku nebo vytvořte novou zakázku.

3.  Ve formuláři **Servisní zakázky** v **podokně akcí** na kartě **Servisní zakázka** ve skupině **Vztahy** klikněte na **Objekty servisu**.

4.  Ve formuláři **Objekty servisu** klikněte na možnost **Nový** a vyberte předmět servisu pro tuto servisní zakázku.

5.  Chcete-li k servisní smlouvě připojit šablony kusovníku, klepněte na položku **Funkce** a vyberte **Připojit kusovník šablony**. Ve formuláři **Vybrat kusovník šablony** v poli **Kusovník šablony** vyberte šablonu. 


## <a name="see-also"></a>Viz také

[Přehled předmětů servisu](service-objects.md)

[Vztahy předmětu servisu](service-object-relations.md)

[Kusovníky šablony](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
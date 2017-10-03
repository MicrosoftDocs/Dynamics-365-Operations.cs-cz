--- 
title: "Vytváření prvků nákladů  "
description: "Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Vytváření prvků nákladů   

[!include[task guide banner](../../includes/task-guide-banner.md)]

Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví. Tato procedura popisuje, jak vytvořit nákladové prvky importováním hlavních účtů prostřednictvím datového konektoru. K vytvoření této procedury byla použita ukázková společnost USMF. Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.


## <a name="create-new-cost-elements"></a>Vytvoření nových prvků nákladů
1. Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze prvku nákladů.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klikněte na položku Uložit.

## <a name="configure-the-data-connector"></a>Konfigurace datového konektoru
1. Klikněte na Konfigurovat poskytovatele členů dimenzí.
2. V poli Účtová osnova zadejte nebo vyberte hodnotu.
    * Vyberte Sdílené pro použití sdílené účtové osnovy.  
3. Klikněte na položku Nová.
4. Označte v seznamu vybraný řádek.
    * Můžete použít filtry u účtů, které splňují vaše kritéria.  
5. V poli Z hlavního účtu zadejte nebo vyberte hodnotu.
6. V poli Na hlavní účet zadejte nebo vyberte hodnotu.
7. Klikněte na tlačítko OK.

## <a name="import-main-accounts"></a>Importovat hlavní účty
1. Klikněte na Importovat členy dimenze.
    * Hlavní účty budou importovány do nákladového účetnictví a použity jako nákladové prvky.  
2. Klikněte na tlačítko OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Zobrazení importovaných účtů jako prvků nákladů
1. Klikněte na Zobrazit členy dimenze.
    * Zobrazte importované účty hlavní knihy jako nákladové prvky ve vaší firmě, do které mohou být evidovány náklady.  



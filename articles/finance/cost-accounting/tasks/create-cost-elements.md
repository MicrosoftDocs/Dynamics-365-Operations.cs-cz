---
title: 'Vytváření prvků nákladů  '
description: Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779682"
---
# <a name="create-cost-elements"></a>Vytváření prvků nákladů   

[!include [banner](../../includes/banner.md)]

Existuje několik způsobů, jak vytvořit prvky nákladů v nákladovém účetnictví. Tato procedura popisuje, jak vytvořit nákladové prvky importováním hlavních účtů prostřednictvím datového konektoru. K vytvoření této procedury byla použita ukázková společnost USMF. Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do Dynamics 365 for Operations, verze 1611.


## <a name="create-new-cost-elements"></a>Vytvoření nových prvků nákladů
1. Jděte na **Nákladové účetnictví > Dimenze > Dimenze prvku nákladů**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Název**.
4. V poli **Datový konektor pro členy dimenzí** zadejte nebo vyberte hodnotu.
5. Zadejte hodnotu do pole **Popis**.
6. Klikněte na tlačítko **Uložit**.

## <a name="configure-the-data-connector"></a>Konfigurace datového konektoru
1. Klikněte na **Konfigurovat poskytovatele členů dimenzí**.
2. V poli **Účtová osnova** zadejte nebo vyberte hodnotu.
    * Vyberte **Sdílené** pro použití sdílené účtové osnovy.  
3. Klepněte na možnost **Nový**.
4. Označte v seznamu vybraný řádek.
    * Můžete použít filtry u účtů, které splňují vaše kritéria.  
5. V poli **Z hlavního účtu** zadejte nebo vyberte hodnotu.
6. V poli **Na hlavní účet** zadejte nebo vyberte hodnotu.
7. Klikněte na tlačítko **OK**.

## <a name="import-main-accounts"></a>Importovat hlavní účty
1. Klikněte na **Importovat členy dimenze**.
    * Hlavní účty budou importovány do nákladového účetnictví a použity jako nákladové prvky.  
2. Klikněte na tlačítko **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Zobrazení importovaných účtů jako prvků nákladů
1. Klikněte na **Zobrazit členy dimenze**.
    * Zobrazte importované účty hlavní knihy jako nákladové prvky ve vaší firmě, do které mohou být evidovány náklady.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

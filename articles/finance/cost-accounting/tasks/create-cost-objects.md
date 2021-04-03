---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236787"
---
# <a name="create-cost-objects"></a>Vytváření objektů nákladů   

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska v nákladovém účetnictví prostřednictvím datového konektoru. K vytvoření této procedury byla použita ukázková společnost USMF. 


## <a name="create-new-cost-objects"></a>Vytvoření nových objektů nákladů
1. Přejděte na položky Nákladové účetnictví > Dimenze > Dimenze objektu nákladů.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. V poli Datový konektor pro členy dimenzí zadejte nebo vyberte hodnotu.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klikněte na položku Uložit.

## <a name="configure-the-data-connector"></a>Konfigurace datového konektoru
1. Klikněte na Konfigurovat poskytovatele členů dimenzí.
    * Vyberte CostCenter pro import dimenze CostCenter do nákladového účetnictví.  
2. V poli Název dimenze vyberte Nákladové středisko.
3. Klikněte na tlačítko OK.

## <a name="import-cost-centers"></a>Import nákladových středisek
1. Klikněte na Importovat členy dimenze.
2. Klikněte na tlačítko OK.

## <a name="view-the-imported-cost-centers"></a>Zobrazení importovaných nákladových středisek
1. Klikněte na Zobrazit členy dimenze.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
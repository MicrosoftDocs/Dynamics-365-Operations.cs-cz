---
title: 'Vytváření objektů nákladů  '
description: Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska Dynamics 365 for Finance and Operations Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543764"
---
# <a name="create-cost-objects"></a>Vytváření objektů nákladů   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje, jak vytvořit objekty nákladů importováním finanční dimenze nákladového střediska Dynamics 365 for Finance and Operations Enterprise edition v nákladovém účetnictví prostřednictvím datového konektoru. K vytvoření této procedury byla použita ukázková společnost USMF. Tato procedura je určena pro funkci nákladového účetnictví, která byla přidána do Dynamics 365 for Operations, verze 1611.


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


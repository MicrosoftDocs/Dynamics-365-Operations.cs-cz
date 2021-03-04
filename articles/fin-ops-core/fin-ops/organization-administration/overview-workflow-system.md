---
title: Přehled systému workflow
description: Toto téma popisuje systém workflowu.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: feb4ef0233b99420ebdd8781aae0191c9fa379f8
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692835"
---
# <a name="workflow-system-overview"></a>Přehled systému workflow

[!include [banner](../includes/banner.md)]

Toto téma popisuje systém workflowu.

## <a name="what-is-workflow"></a>Co je workflow?

Termín *workflow* lze definovat dvěma způsoby: workflow jako systém a workflow jako obchodní proces.

### <a name="workflow-is-a-system"></a>Workflow je systém

Workflow je systém, který je spuštěn na aplikačním objektovém serveru (AOS). Systém workflowu nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy.

### <a name="workflow-is-a-business-process"></a>Workflow je obchodní proces

Workflow představuje obchodní proces. Definuje tok dokumentu nebo jeho procházení systémem zobrazením, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu. Následující obrázek znázorňuje příklad workflowu pro sestavy výdajů.

![Workflow s prvky, které jsou přiřazeny uživatelům](./media/workflow_user.gif)

Abychom lépe pochopili tento workflow, předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 7 000 USD. V tomto scénáři musí Ivan zkontrolovat účtenky, které mu Stanislav předal. Poté musí být vyúčtování výdajů schváleno Františkem a Šárkou. Nyní předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 11 000 USD. V tomto scénáři musí Ivan zkontrolovat účtenky a František, Šárka a Anna musí toto vyúčtování výdajů schválit.

## <a name="benefits-of-using-the-workflow-system"></a> Výhody používání systému workflowu

Používání systému workflowu v organizaci má několik výhod:

- **Konzistentní procesy:** – Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.
- **Viditelnost procesů:** – Můžete sledovat stav, historii a výkonnostní metriku instancí workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.
- **Centralizovaný seznam pracovních položek** – Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, které mají přiřazeny.


## <a name="workflow-content"></a>Obsah workflowu

+ [Architektura systému workflowu](workflow-system-architecture.md)
+ [Prvky workflow](workflow-elements.md)
+ [Akce v procesech schválení workflow](workflow-actions.md)
+ [Přehled vytvoření workflow](create-workflow.md)
+ [Konfigurace vlastností workflow](configure-workflow-properties.md)
+ [Konfigurace ručních úloh ve workflow](configure-manual-task-workflow.md)
+ [Konfigurace automatizovaných úloh ve workflowu](configure-automated-task-workflow.md)
+ [Konfigurace schvalovacích procesů ve workflowu](configure-approval-process-workflow.md)
+ [Konfigurace schvalovacích kroků ve workflowu](configure-approval-step-workflow.md)
+ [Konfigurace ručních rozhodnutí ve workflow](configure-manual-decision-workflow.md)
+ [Konfigurace podmíněných rozhodnutí ve workflow](configure-conditional-decision-workflow.md)
+ [Konfigurace paralelních aktivit ve workflow](configure-parallel-activity-workflow.md)
+ [Konfigurace paralelních větví ve workflow](configure-parallel-branch-workflow.md)
+ [Konfigurace workflow položky řádku](configure-line-item-workflow.md)
+ [Workflow – Často kladené otázky](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Přehled systému workflow
description: Toto téma popisuje systém workflowu.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189998"
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

+ [Architektura workflowu](workflow-system-architecture.md)
+ [Prvky workflowu](workflow-elements.md)
+ [Akce workflowu](workflow-actions.md)
+ [Vytvoření workflowu](create-workflow.md)
+ [Konfigurace vlastností workflowu](configure-workflow-properties.md)
+ [Konfigurace ruční úlohy ve workflowu](configure-manual-task-workflow.md)
+ [Konfigurace automatizované úlohy ve workflowu](configure-automated-task-workflow.md)
+ [Konfigurace schvalovacího procesu ve workflowu](configure-approval-process-workflow.md)
+ [Konfigurace schvalovacího kroku ve workflowu](configure-approval-step-workflow.md)
+ [Konfigurace ručního rozhodnutí ve workflowu](configure-manual-decision-workflow.md)
+ [Konfigurace podmíněného rozhodnutí ve workflowu](configure-conditional-decision-workflow.md)
+ [Konfigurace paralelních aktivit ve workflowu](configure-parallel-activity-workflow.md)
+ [Konfigurace paralelní větve ve workflowu](configure-parallel-branch-workflow.md)
+ [Konfigurace workflow položky řádku](configure-line-item-workflow.md)
+ [Workflow – Často kladené otázky](workflow-FAQ.md)
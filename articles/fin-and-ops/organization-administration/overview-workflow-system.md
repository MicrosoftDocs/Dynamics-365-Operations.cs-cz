---
title: Systémový workflowu
description: Toto téma popisuje systém workflowu v Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545802"
---
# <a name="workflow-system"></a>Systémový workflowu

[!include [banner](../includes/banner.md)]

Toto téma popisuje systém workflowu v Microsoft Dynamics 365 for Finance and Operations.

## <a name="what-is-workflow"></a>Co je workflow?

Termín *workflow* lze definovat dvěma způsoby: workflow jako systém a workflow jako obchodní proces.

### <a name="workflow-is-a-system"></a>Workflow je systém

Workflow je systém nainstalovaný s aplikací Finance and Operations a běží na aplikačním objektovém serveru (AOS). Systém workflowu nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy.

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

---
title: "Přehled systému workflowu"
description: "Tento článek popisuje systém workflow v aplikaci Microsoft Dynamics 365 for Operations."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 08c36f02f88fef7508730b6c01a1c99a0f77fb0c
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-system-overview"></a>Přehled systému workflowu

[!include[banner](../includes/banner.md)]


Tento článek popisuje systém workflow v aplikaci Microsoft Dynamics 365 for Operations.

<a name="what-is-workflow"></a>Co je workflow?
-----------------

Termín *workflow* lze definovat dvěma způsoby: workflow jako systém a workflow jako obchodní proces.
### <a name="workflow-is-a-system"></a>Workflow je systém

Workflow je systém nainstalovaný aplikací Dynamics 365 for Operations, který se spouští na aplikačním objektovém serveru (AOS). Systém workflowu nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy.

### <a name="workflow-is-a-business-process"></a>Workflow je obchodní proces

Workflow představuje obchodní proces. Definuje tok dokumentu nebo jeho procházení systémem zobrazením, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu. Následující obrázek znázorňuje příklad workflowu k vyúčtování výdajů. ![Workflow s prvky, které jsou přiřazeny uživatelům](./media/workflow_user.gif) Abychom lépe pochopili tento workflow, budeme například předpokládat, že Stanislav odešle vyúčtování výdajů pro částku 7 000 USD. V tomto scénáři musí Ivan zkontrolovat účtenky, které mu Stanislav předal. Poté musí být vyúčtování výdajů schváleno Františkem a Šárkou. Nyní předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 11 000 USD. V tomto scénáři musí Ivan zkontrolovat účtenky a František, Šárka a Anna musí toto vyúčtování výdajů schválit.
 Výhody používání systému workflowu
-------------------------------------

Používání systému workflowu v organizaci má několik výhod:
-   **Konzistentní procesy:** – Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.
-   **Viditelnost procesů:** – Můžete sledovat stav, historii a výkonnostní metriku instancí workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.
-   **Centralizovaný seznam pracovních položek** – Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, které mají přiřazeny.






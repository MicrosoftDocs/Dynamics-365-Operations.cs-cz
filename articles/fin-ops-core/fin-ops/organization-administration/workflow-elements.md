---
title: Prvky workflowu
description: Toto téma popisuje různé prvky, které tvoří workflow.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6df767c2db6d5d9addce5f91544686628ab064dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176868"
---
# <a name="workflow-elements"></a>Prvky workflowu

[!include [banner](../includes/banner.md)]

Toto téma popisuje různé prvky, které tvoří workflow.

Workflow se skládá z jednotlivých prvků. Následující části popisují jednotlivé typy prvků.

## <a name="tasks"></a>Úkoly

*Úkol* je jednotka práce, kterou se musí provést. Dva typy úkolů lze přidat do workflowu: ruční a automatizované úlohy.

### <a name="manual-task"></a>Ruční úkol

*Ruční úkol* je jednotka práce, kterou musí provést uživatel. Workflow vyúčtování výdajů může mít například ruční úkoly, které musí mít přiřazeny uživatele pro dokončení následujících akcí:

- Kontrola příjmových dokladů, které byly odeslány společně s vyúčtováním výdajů.
- Kontaktování manažera zaměstnance.

### <a name="automated-task"></a>Automatizovaný úkol

*Automatizovaný úkol* je jednotka práce, kterou musí provést systém. Není požadován lidský zásah. Workflow prodejní objednávky může mít například automatizované úkoly, které vyžadují systém pro dokončení následujících akcí:

- Provedení kontroly úvěru.
- Vytvoření záznamu odběratele pro odběratele, pokud záznam již neexistuje.

## <a name="approval-processes"></a>Schvalovací procesy

*Schvalovací proces* je proces, který se skládá ze samostatných kroků. V každém schvalovacím kroku může uživatel provádět následující akce:

- Schválit dokument.
- Odmítnout dokument.
- Zadat požadavek na změnu dokumentu.
- Postoupit dokument ke schválení jinému uživateli.

## <a name="line-item-workflow-elements"></a>Prvek workflowu položky řádku

Workflow lze vytvořit pro zpracování dokumentů nebo položek řádku v dokumentu. Například vytvoříte workflow schválení pro časové rozvrhy. (Tento pracovní postup budeme označovat jako *pracovní postup dokumentu*.) K tomuto pracovnímu procesu dokumentu můžete přidat prvek *pracovního postupu řádkové položky*. Při spuštění prvku položky řádku je každá položka řádku v dokumentu odeslána ke zpracování. Je vhodné řádkové položky zpracovávat ve stejném workflowu položky řádku, nebo můžete každou položku řádku zpracovat jiným workflowem položky řádku. Představte si, že zaměstnanec odeslal časový rozvrh, který se podobá na následujícímu obrázku.

![Workflow položek na řádku](./media/workflow_lineitemworkflow.gif)

V tomto scénáři může být třeba vytvořit následující workflowy položky řádku:

- **Workflow položky řádku 1** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 1111.
- **Workflow položky řádku 2** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 2222.
- **Workflow položky řádku 3** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 3333.

## <a name="flow-control-elements"></a>Prvky ovládání toku

Následující prvky umožňují navrhovat workflowy, které mají alternativní větve nebo větve, které běží současně

### <a name="manual-decision"></a>Ruční rozhodnutí

*Ruční rozhodnutí* je bod, ve kterém se workflow dělí na dvě větve. Uživatel se musí rozhodnout, a toto rozhodnutí určí, která větev bude použita ke zpracování dokumentu, který byl odeslán.

### <a name="conditional-decision"></a>Podmíněné rozhodnutí

*Podmíněné rozhodnutí* je také bod, ve kterém se workflow dělí na dvě větve. Systém však rozhodne, která větev bude použita ke zpracování dokumentu, který byl odeslán. Pro rozhodování systém vyhodnotí dokument a určí, zda odpovídá zadaným podmínkám.

### <a name="parallel-activity"></a>Paralelní aktivita

*Paralelní činnost* je prvek workflowu, jenž zahrnuje dvě nebo více větví workflowu, které jsou zpracovávány současně.

### <a name="subworkflow"></a>Dílčí workflow

*Dílčí workflow* je workflow, který je spuštěn v kontextu jiného workflowu.

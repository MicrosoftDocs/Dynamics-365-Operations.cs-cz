---
title: "Workflowy zásobování a zdrojů"
description: "Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Workflowy zásobování a zdrojů

[!include[banner](../includes/banner.md)]


Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.

Workflow představuje obchodní proces. Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument. Používání systému workflowu v organizaci má několik výhod:
-   **Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.
-   **Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.
-   **Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní. To je k dispozici na stránce Pracovní položky.

## <a name="the-types-of-workflows-that-you-can-create"></a> Typy workflowů, které můžete vytvářet
Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Typ**                         | **Tento typ slouží k:**                                          |
| Kontrola nákupních žádanek      | Vytváření workflowů kontroly pro nákupní požadavky.            |
| Kontrola řádku nákupní žádanky | Vytváření workflowů kontroly pro řádky nákupní žádanky.       |
| Workflow nákupní objednávky          | Vytváření workflowů kontroly a schvalování pro nákupní objednávky.     |
| Workflow řádku nákupní objednávky     | Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky. |

## <a name="creating-a-workflow"></a>Vytvoření workflowu
Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření.  

Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku Prvky workflowu je třeba konfigurovat. Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.
Typy účastníků
----------------------

Můžete přiřadit krok schválení k následujícím skupinám účastníků.

| Skupina uživatelů    | Popis                                                               |
|---------------|---------------------------------------------------------------------------|
| Účastník   | Přiřaďte krok schválení členům skupiny nebo role.                   |
| Hierarchie     | Přiřaďte krok schválení k uživatelům v určité organizační hierarchii. |
| Uživatel workflowu | Přiřaďte krok schválení uživatelům tohoto pracovního postupu.                       |
| Fronta         | Přiřaďte kroku schválení frontě pracovních položek.                            |
| Uživatel          | Přiřaďte krok schválení konkrétním uživatelům.                               |



<a name="see-also"></a>Viz také
--------

[Definování workflowů pracovních postupů pro nákupní žádanky](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Workflow nákupní žádanky](purchase-requisitions-workflow.md)





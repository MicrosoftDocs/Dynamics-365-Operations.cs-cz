---
title: "Přidělování dat plánování rozpočtu"
description: "Tento článek popisuje různé metody přidělení, které jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, a jejich použití."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-data-allocation"></a>Přidělení dat pro plánování rozpočtu

[!include[banner](../includes/banner.md)]


Tento článek popisuje různé metody přidělení, které jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, a jejich použití.  

Data lze rozdělit do plánu rozpočtu různými způsoby za účelem přesného zobrazení předpokládaných částek.

## <a name="allocation-methods"></a>Metody přidělení
Tři metody přidělení (Přidělit napříč obdobími, Přidělit k dimenzím a Použít pravidla přidělení hlavní knihy) umožňují vytvořit řádky plánu rozpočtu, které jsou založeny na řádcích ve stejném plánu rozpočtu. Tři další metody (Agregovat, Rozdělit a Kopírovat z plánu rozpočtu) umožňují vytvořit řádky plánu rozpočtu v jiných plánech rozpočtu. U všech šesti metod přidělení je třeba zadat cílový scénář. Cílový scénář může být buď stejný jako zdrojový scénář, nebo odlišný od zdrojového scénáře. Dále můžete určit, zda budou nové řádky připojeny k plánu rozpočtu, nebo nahradí aktuální řádky plánu rozpočtu.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Přidělit napříč obdobími** – kategorie přidělení období slouží k přidělení řádků plánu rozpočtu ze zdrojového scénáře plánu rozpočtu napříč obdobími k cílovému scénáři. Zdrojová částka je přiřazena k více řádkům v cílovém scénáři na základě procenta a data, které jsou definované v rámci kategorie přidělení období.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Přidělit k dimenzím** – řádky plánu rozpočtu jsou přiřazeny ze zdrojového scénáře plánování rozpočtu k jednomu nebo více řádkům v cílovém scénáři na základě procent a finančních dimenzí, které jsou definovány ve vybrané podmínce přidělení rozpočtu.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Agregovat** – řádky plánu rozpočtu jsou agregovány ze zdrojového scénáře plánu rozpočtu v přidružených (podřízených) plánech rozpočtu do cílového scénáře v nadřazeném plánu rozpočtu. Tato metoda umožňuje částky rozpočtu, které jsou připraveny na nižší úrovni v organizaci pro konsolidaci na vyšší úrovni.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Rozdělit** – řádky plánu rozpočtu jsou rozděleny ze zdrojového scénáře plánování rozpočtu v nadřazenému plánu rozpočtu do cílového scénáře v přidružených (podřízených) plánech rozpočtu na základě finančních dimenzí organizačních jednotek přidružených plánů. Tato metoda umožňuje částky rozpočtu, které jsou připraveny na vyšší úrovni v organizaci k rozšíření pro účely lokalizovanější kontroly.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Použít pravidla přidělení hlavní knihy** – řádky plánu rozpočtu jsou rozděleny ze zdrojového scénáře plánování rozpočtu do cílového scénáře na základě vybraného pravidla přidělení hlavní knihy. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopírovat z plánu rozpočtu** – stejně jako u přidělovací metody Rozdělení jsou řádky plánu rozpočtu vytvořeny v cíli na základě řádků v souvisejícím plán rozpočtu. Pro tuto metodu však zdrojový plán rozpočtu nemusí být nadřazený, může však být na libovolné vyšší úrovni v hierarchii plánu rozpočtu. Tato metoda přidělení je užitečná, pokud jsou konsolidované částky původně rozpočtované na výrazně vyšší úrovni a předtím, než obdrží schválení vyšší úrovně, musí být převedeny na nižší úroveň organizace pro podrobnou kontrolu a úpravy.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Použití metod přidělení v plánu rozpočtu
Pokud chcete provést přidělení na stránce plánu rozpočtu, vyberte řádky k přidělení a klikněte na tlačítko **Přidělit rozpočet**.

[![Tlačítko přidělení rozpočtu](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Dále vyberte metodu přidělení. Zbývající pole se poté nastaví na základě metody, kterou jste vybrali. Tato pole zahrnují zdrojová a cílová data plánu rozpočtu a možnosti, které umožňují znásobit zdroj určeným koeficientem při vytváření cílových částek za účelem usnadnění hromadných úprav. Můžete také nastavit možnost **Připojit k plánu**. Výběrem možnosti **Ne** nahraďte existující řádky plánu rozpočtu, nebo výběrem možnosti **Ano** zachovejte existující řádky plánu rozpočtu a přidejte nové řádky pro přidělené částky.

## <a name="automating-allocations-during-a-workflow"></a>Automatizace přidělení během workflowu
Jedna výkonná funkce umožňuje přidělení prováděná automaticky jako součást workflowu plánování rozpočtu. Jak plán rozpočtu prochází svým workflowem, mohou automatizované úlohy vyvolávat přidělení v určené fázi plánování rozpočtu. 

Abyste mohli nastavit automatické přidělení, musíte nejprve vytvořit plán přidělení na stránce **Konfigurace plánování rozpočtu**. Plán přidělení definuje metodu přidělení, která se použije při spuštění automatizovaného přidělení, a hodnoty různých možností přidělení (viz popisy v předchozím oddílu). 

Dále vytvořte přidělení fáze na stránce **Konfigurace plánování rozpočtu**. Přidělení fáze přiřadí plán přidělení pro workflow a fázi plánování rozpočtu. 

Nakonec přidejte automatizovanou úlohu pro přidělení fáze plánování rozpočtu v požadované fázi workflowu. V následujícím příkladu byla do workflowu vložena dvě přidělení fází plánování rozpočtu (červený okraj).

[![Přidělení fází plánování rozpočtu](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)





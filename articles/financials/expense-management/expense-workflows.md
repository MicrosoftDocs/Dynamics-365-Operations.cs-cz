---
title: "Nastavení workflow pro výdaje"
description: "Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a>Nastavení workflow pro výdaje

[!include[banner](../includes/banner.md)] Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů. Dokumenty, pro která lze workflow definovat, zahrnují vyúčtování výdajů, cestovní žádanky a požadavky na hotovostní zálohu.

Workflow představuje obchodní proces. Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument. Používání systému workflowu v organizaci má několik výhod:

-   **Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.

-   Viditelnost procesů: –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.

-   Centralizovaný seznam pracovních položek: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, která mají přiřazena. 

**Můžete vytvářet tyto typy pracovního procesu:**

V následující tabulce jsou uvedeny typy pracovních procesů, které můžete vytvořit v části **Výdaje**.

| **Typ**                           | **Tento typ slouží k:**                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| **Vyúčtování výdajů**                 | Vytváření workflowů schválení pro sestavy výdajů.                       |      
| **Automatické zaúčtování sestavy výdajů**    | Vytváření workflowů automatického zaúčtování pro sestavy výdajů.              |     
| **Položka řádku výdajů**              | Vytváření workflowů schválení pro položky řádků na sestavě výdajů.         |     
| **Automatické zaúčtování položek řádku výdajů** | Vytváření workflowů automatického zaúčtování pro položky řádků na sestavě výdajů.|
| **Cestovní žádanka**             | Vytváření workflowů pro cestovní žádanky.                   |    
| **Požadavek na hotovostní zálohu**           | Vytvoření workflowů schválení pro požadavky na hotovostní zálohu.                 |     
| **Vratka daně DPH**               | Vytvoření workflowů schválení pro vratky daně DPH. |       


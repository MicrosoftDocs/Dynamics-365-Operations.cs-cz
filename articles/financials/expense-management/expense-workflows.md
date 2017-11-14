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
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb8ff11a03ba18b78595cd04f63b2456aec53bf2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

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

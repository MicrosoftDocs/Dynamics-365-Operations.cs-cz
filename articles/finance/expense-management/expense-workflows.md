---
title: Nastavení workflow pro výdaje
description: Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176783"
---
# <a name="set-up-workflows-for-expense"></a>Nastavení workflow pro výdaje

[!include [banner](../includes/banner.md)]

 Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů. Dokumenty, pro která lze workflow definovat, zahrnují vyúčtování výdajů, cestovní žádanky a požadavky na hotovostní zálohu.

Workflow představuje obchodní proces. Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument. Používání systému workflowu v organizaci má několik výhod:

-   **Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.

-   Viditelnost procesů: –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.

-   Centralizovaný seznam pracovních položek: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, která mají přiřazena. 

**Můžete vytvářet tyto typy pracovního procesu:**

V následující tabulce jsou uvedeny typy pracovních procesů, které můžete vytvořit v části **Výdaje**.


|              <strong>Typ</strong>              |                   <strong>Tento typ slouží k:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Vyúčtování výdajů</strong>         |            Vytváření workflowů schválení pro sestavy výdajů.             |
|  <strong>Automatické zaúčtování sestavy výdajů</strong>   |        Vytváření workflowů automatického zaúčtování pro sestavy výdajů.        |
|       <strong>Položka řádku výdajů</strong>        |     Vytváření workflowů schválení pro položky řádků na sestavě výdajů.      |
| <strong>Automatické zaúčtování položek řádku výdajů</strong> | Vytváření workflowů automatického zaúčtování pro položky řádků na sestavě výdajů. |
|       <strong>Cestovní žádanka</strong>       |          Vytváření workflowů pro cestovní žádanky.           |
|      <strong>Požadavek na hotovostní zálohu</strong>      |         Vytvoření workflowů schválení pro požadavky na hotovostní zálohu.          |
|        <strong>Vratka daně DPH</strong>        | Vytvoření workflowů schválení pro vratky daně DPH.  |

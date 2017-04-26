---
title: "Zpracování přidělení"
description: "Tento článek obsahuje informace o přidělení možnosti pro zpracování v 365 Microsoft Dynamics pro operace a jak lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo příjmy účtovaly v účetnictví na správný objekt."
author: twheeloc
manager: AnnBe
ms.date: 2015-12-04 18 - 16 - 59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>Zpracování přidělení

Tento článek obsahuje informace o přidělení možnosti pro zpracování v 365 Microsoft Dynamics pro operace a jak lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo příjmy účtovaly v účetnictví na správný objekt.

365 Microsoft Dynamics pro operace poskytuje následující možnosti pro podporu tohoto procesu:

-   Pomocí akce rozdělit v rozúčtování, nebo použitím výchozí šablony finanční dimenze do dokumentu ručně přidělit částky transakce. Další informace naleznete v tématu [rozúčtování.](\accounts-payable\accounting-distributions.md)
-   Automaticky přidělit částky transakce na základě podmínek přidělení definovaných v individuálním hlavním účtu. Položky účtu přidělení se budou generovat pro každý deník podle procenta a cílového účtu hlavní knihy, kdykoli účetní položka splní kritéria definovaná jako zdrojový účet hlavní knihy.
-   Automaticky přidělit zůstatky hlavní knihy nebo pevné částky na základě pravidel přidělení hlavní knihy. Pravidla přidělení hlavní knihy se zpracovávají v pravidelných intervalech pomocí deníků přidělení. 

###  <a name="allocations-in-budget-planning"></a>Přidělení v plánování rozpočtu

Pravidla přidělení hlavní knihy můžete použít pro plány rozpočtu. Při použití pravidla přidělení hlavní knihy v plánování rozpočtu, pravidla přidělení fungují stejným způsobem jako v hlavní knize, ale zdrojová data a cílová data pocházejí z plánu rozpočtu. Můžete ručně vybrat pravidla pro přidělení hlavní knihy pro použití v plánu rozpočtu. Můžete také použít plán přidělení, která se spouští jako součást procesu workflowu.

> [!NOTE]
> Nemůžete používat mezipodniková pravidla pro přidělení hlavní knihy v plánu rozpočtu.





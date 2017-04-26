---
title: "Vytváření rozpočtu z účtů transakcí a součtových účtů"
description: "V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů. Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: af9b6a5ebb25c0054704b60c84057eee609ffab7
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Vytváření rozpočtu z účtů transakcí a součtových účtů

[!include[banner](../includes/banner.md)]


V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů. Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu.

Dokumenty plán rozpočtu a položka registru rozpočtu umožňují rozpočtování pro hlavní účty, které mají typ hlavního účtu **Součet**. Skutečné hodnoty lze zaúčtovat pouze s hlavními účty transakcí. 

Pro periodické zpracování **Generovat plán rozpočtu z hlavní knihy** na kartě **Zdroj** můžete jako kritérium zadat typ hlavního účtu **Celkem**. V takovém případě se každý souhrnný hlavní účet zahrne do cílového plánu rozpočtu a částka se bude rovnat celkové částce rozsahu vybraných hlavních účtů. 

Pro hlavní účty typu **Celkem** můžete aktivovat kontrolu rozpočtu. Tato funkce je podporována použitím rozpočtových skupin. Pro každý celkem hlavní účet rozpočtu, která by měla být kontrolována pro skupinu rozpočtu musí být vytvořen na ** konfiguraci kontroly rozpočtu ** stránky. Kritéria, které zadáte musí obsahovat celkovou hlavního účtu a rozsahu účtů. Abyste proces vytváření rozpočtových skupin urychlili, můžete využít datovou entitu Skupiny kontroly rozpočtu. 

Pokud se rozpočet používá ve vykazování, například u finančního výkazu, skládá se suma rozpočtu celkového účtu z následujících částek:

-   Rozpočty, které se vytvoří z každého účtu transakční knihy v rámci intervalu souhrnného účtu.
-   Částka rozpočtu, která se zadává přímo do souhrnného účtu.

Můžete tak vytvořit samostatné rozpočty pro nejvýznamnější transakční účty v intervalu souhrnného účtu a poté přidat dostupnou částku rozpočtu k souhrnnému účtu.





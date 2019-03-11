---
title: Vytváření rozpočtu z účtů transakcí a součtových účtů
description: V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů. Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6129a5431cba22ea656e4d6f473a4e93a81131ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "331706"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Vytváření rozpočtu z účtů transakcí a součtových účtů

[!include [banner](../includes/banner.md)]

V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů. Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu.

Dokumenty plán rozpočtu a položka registru rozpočtu umožňují rozpočtování pro hlavní účty, které mají typ hlavního účtu **Součet**. Skutečné hodnoty lze zaúčtovat pouze s hlavními účty transakcí. 

Pro periodické zpracování **Generovat plán rozpočtu z hlavní knihy** na kartě **Zdroj** můžete jako kritérium zadat typ hlavního účtu **Celkem**. V takovém případě se každý souhrnný hlavní účet zahrne do cílového plánu rozpočtu a částka se bude rovnat celkové částce rozsahu vybraných hlavních účtů. 

Pro hlavní účty typu **Celkem** můžete aktivovat kontrolu rozpočtu. Tato funkce je podporována použitím rozpočtových skupin. Pro každý souhrnný hlavní účet se musí rozpočet, který má rozpočtová skupina ovládat, vytvořit na stránce **Konfigurace kontroly rozpočtu**. Mezi zadanými kritérii musí být souhrnný hlavní účet a rozsah účtů. Abyste proces vytváření rozpočtových skupin urychlili, můžete využít datovou entitu Skupiny kontroly rozpočtu. 

Pokud se rozpočet používá ve vykazování, například u finančního výkazu, skládá se suma rozpočtu celkového účtu z následujících částek:

-   Rozpočty, které se vytvoří z každého účtu transakční knihy v rámci intervalu souhrnného účtu.
-   Částka rozpočtu, která se zadává přímo do souhrnného účtu.

Můžete tak vytvořit samostatné rozpočty pro nejvýznamnější transakční účty v intervalu souhrnného účtu a poté přidat dostupnou částku rozpočtu k souhrnnému účtu.




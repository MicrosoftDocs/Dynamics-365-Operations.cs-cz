---
title: Zpracování přidělení
description: Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování v aplikaci Microsoft Dynamics 365 Finance, a o tom, jak je lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo výnosy účtovaly v účetnictví na správný objekt.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877976"
---
# <a name="process-allocations"></a>Zpracování přidělení

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování a o tom, jak je lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo výnosy účtovaly v účetnictví na správný objekt.

Tento proces podporují následující možnosti:

-   Ručně přidělit částky transakcí pomocí rozdělení akcí v rozúčtování nebo použitím výchozích šablon finanční dimenze v dokumentu. Další informace naleznete v tématu [Rozúčtování](../accounts-payable/accounting-distributions.md).
-   Automaticky přidělit částky transakce na základě podmínek přidělení definovaných v individuálním hlavním účtu. Položky účtu přidělení se budou generovat pro každý deník podle procenta a cílového účtu hlavní knihy, kdykoli účetní položka splní kritéria definovaná jako zdrojový účet hlavní knihy. Další informace naleznete v tématu [Podmínky přidělení hlavního účtu](../general-ledger/main-account-allocation-terms.md).
-   Automaticky přidělit zůstatky hlavní knihy nebo pevné částky na základě pravidel přidělení hlavní knihy. Pravidla přidělení hlavní knihy se zpracovávají v pravidelných intervalech pomocí deníků přidělení. Další informace naleznete v tématu [Alokační pravidla](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Přidělení v plánování rozpočtu

Pravidla přidělení hlavní knihy můžete použít pro plány rozpočtu. Při použití pravidla přidělení hlavní knihy v plánování rozpočtu, pravidla přidělení fungují stejným způsobem jako v hlavní knize, ale zdrojová data a cílová data pocházejí z plánu rozpočtu. Můžete ručně vybrat pravidla pro přidělení hlavní knihy pro použití v plánu rozpočtu. Můžete také použít plán přidělení, která se spouští jako součást procesu workflowu.

> [!NOTE]
> Nemůžete používat mezipodniková pravidla pro přidělení hlavní knihy v plánu rozpočtu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

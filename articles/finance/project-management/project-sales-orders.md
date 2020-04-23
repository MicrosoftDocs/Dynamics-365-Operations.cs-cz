---
title: Projektové prodejní objednávky pro projekty určené časem a materiálem
description: Toto téma vysvětluje, jak vytvářet prodejní objednávky na základě projektů určených časem a materiálem.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249086"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="237c0-103">Projektové prodejní objednávky pro projekty určené časem a materiálem</span><span class="sxs-lookup"><span data-stu-id="237c0-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="237c0-104">Toto téma popisuje způsob vytvoření prodejní objednávky pro projekt.</span><span class="sxs-lookup"><span data-stu-id="237c0-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="237c0-105">Prodejní objednávky lze vytvořit pouze pro projekty typu **čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="237c0-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="237c0-106">Pokud má projekt určený časem a materiálem na projektové smlouvě více zdrojů financování, musíte povolit parametr **Povolit prodejní objednávky pro projekty s více zdroji financování** na stránce **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="237c0-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="237c0-107">Podpora prodejních objednávek projektu s více zdroji financování je k dispozici od vydání aplikace 10.0.2 a vyššího.</span><span class="sxs-lookup"><span data-stu-id="237c0-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="237c0-108">Parametr umožňující podporu pro prodejní objednávky projektu s více zdroji financování bude odstraněn ve vlně vydání z dubna 2020, po které bude funkce vždy povolena.</span><span class="sxs-lookup"><span data-stu-id="237c0-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="237c0-109">Prodejní objednávky na základě projektu lze vytvořit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="237c0-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="237c0-110">Přejděte na samotný projekt.</span><span class="sxs-lookup"><span data-stu-id="237c0-110">Go to the project itself.</span></span> <span data-ttu-id="237c0-111">V podokně akcí zvolte **Spravovat > Úlohy položky > Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="237c0-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="237c0-112">Informace o projektu se nastaví na výchozí prodejní objednávky z projektu.</span><span class="sxs-lookup"><span data-stu-id="237c0-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="237c0-113">Pokud má projektová smlouva více než jeden zdroj financování, budete muset vybrat zdroj financování pro nastavení zákazníka pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="237c0-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="237c0-114">Pokud pro projekt existuje pouze jeden zdroj financování, bude zákazník automaticky nastaven.</span><span class="sxs-lookup"><span data-stu-id="237c0-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="237c0-115">Přejděte na stránku se seznamem **Všechny prodejní objednávky** a vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="237c0-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="237c0-116">Musíte vybrat projekt pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="237c0-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="237c0-117">Po výběru projektu bude zákazník nastaven ze zdroje financování nebo bude nutné vybrat zdroj financování, pokud má projektová smlouva více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="237c0-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>


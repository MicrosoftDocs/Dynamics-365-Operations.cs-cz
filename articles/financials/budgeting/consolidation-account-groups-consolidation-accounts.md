---
title: Skupiny konsolidačních účtů a další konsolidační účty
description: Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f1c463ee54512b07f5e45c4df995aefed6110cb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "366390"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="5d7b5-103">Skupiny konsolidačních účtů a další konsolidační účty</span><span class="sxs-lookup"><span data-stu-id="5d7b5-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d7b5-104">Toto téma obsahuje informace o skupinách konsolidačních účtů a další konsolidačních účtech a vysvětluje způsob jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="5d7b5-105">Skupiny konsolidačních účtů</span><span class="sxs-lookup"><span data-stu-id="5d7b5-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="5d7b5-106">Skupiny konsolidačních účtů umožňují vytvářet skupiny účtů, které chcete použít pro konsolidaci dat.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="5d7b5-107">Nejčastěji představuje skupina konsolidačních účtů vládou nařízené účtové osnovy nebo mapování účtů do skupiny, která je definována ústředím společnosti.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="5d7b5-108">Skupiny konsolidačních účtů naleznete v oblasti **Nastavení** modulu **Konsolidace**.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="5d7b5-109">Při přidání nové skupiny zadejte jedinečný identifikátor pro skupinu účtů a název.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="5d7b5-110">Další konsolidační účty</span><span class="sxs-lookup"><span data-stu-id="5d7b5-110">Additional consolidation accounts</span></span>
<span data-ttu-id="5d7b5-111">Další konsolidační účty umožňují přiřadit účet z existující účtové osnovy do skupiny konsolidačních účtů.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="5d7b5-112">Potom můžete zadat hodnotu a název konsolidačního účtu.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="5d7b5-113">Další konsolidační účty naleznete v oblasti **Nastavení** modulu **Konsolidace**.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="5d7b5-114">Při vytváření nového konsolidačního účtu je nutné zadat následující informace:</span><span class="sxs-lookup"><span data-stu-id="5d7b5-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="5d7b5-115">**Hlavní účet** – toto pole je vyhledávání, které zobrazí všechny hlavní účty, které jsou založeny na účtových osnovách vybraných na stránce.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="5d7b5-116">Vyberete-li účet, název je automaticky zadán do pole **Název hlavního účtu**.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="5d7b5-117">**Skupinu konsolidačních účtů** – toto pole použijte k určení skupiny, do které má být účet přiřazen.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="5d7b5-118">Při konsolidaci dvěma různými způsoby je nutné přidat stejný účet pro všechny čtyři skupiny konsolidačních účtů.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="5d7b5-119">**Konsolidační účet** – zadejte hodnotu konsolidačního účtu.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="5d7b5-120">Tato hodnota nemusí být účet z účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="5d7b5-121">Může to být libovolná požadovaná hodnota.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="5d7b5-122">**Název konsolidačního účtu** – zadejte název účtu tak, jak se bude objevovat v dotazech a sestavách.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="5d7b5-123">**Úrovně SAT** – toto pole slouží k oznámení výpisů z účtů pro mexické finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="5d7b5-124">Když dokončíte vytváření skupin konsolidačních účtů a dalších konsolidačních účtů, můžete zvolit skupinu v procesu online konsolidace.</span><span class="sxs-lookup"><span data-stu-id="5d7b5-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="5d7b5-125">Další informace naleznete v tématu [Vytvoření skupin konsolidace a další konsolidace účtů](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="5d7b5-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




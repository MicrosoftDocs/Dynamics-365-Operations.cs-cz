---
title: Mezipodnikové výdaje
description: Pracovník, který je zaměstnán jednou právnickou osobou v jedné organizaci, může provádět práci pro jinou právnickou osobu v rámci stejné organizace. V takové situaci můžete použít funkci mezipodnikových výdajů přiřazení pro přiřazení výdajů pracovníka k právnické osobě, pro kterou byla práce prováděna.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390877"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="69d31-104">Mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="69d31-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69d31-105">Pracovník, který je zaměstnán jednou právnickou osobou v jedné organizaci, může provádět práci pro jinou právnickou osobu v rámci stejné organizace.</span><span class="sxs-lookup"><span data-stu-id="69d31-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="69d31-106">V takové situaci můžete použít funkci mezipodnikových výdajů přiřazení pro přiřazení výdajů pracovníka k právnické osobě, pro kterou byla práce prováděna.</span><span class="sxs-lookup"><span data-stu-id="69d31-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="69d31-107">Právnická osoba, která pracovníka zaměstnává, se nazývá půjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="69d31-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="69d31-108">Právnická osoba, vůči které pracovník uplatňuje výdaje, se nazývá vypůjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="69d31-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="69d31-109">Předtím, než pracovník může vytvářet a odesílat výdaje za práci pro jinou právnickou osobu, zvolte u půjčující právnické osoby na stránce **Parametry správy výdajů** možnost **Povolit řádky mezipodnikových výdajů**.</span><span class="sxs-lookup"><span data-stu-id="69d31-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="69d31-110">Zaúčtování daně pro mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="69d31-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69d31-111">Pokud chcete ve své sestavě výdajů použít daňové skupiny, které jsou přidruženy k půjčující (zdrojové) právnické osobě, místo právnické osoby vypůjčující (cílové), budete to muset nakonfigurovat v nastavení DPH v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="69d31-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="69d31-112">Když je parametr hlavní knihy **Právnická osoba pro zaúčtování mezipodnikové daně** nastaven na **Zdroj** a **Použít daňové předpisy pro DPH** je nastaveno na **Ne**, bude použita daňová kombinace pro půjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="69d31-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="69d31-113">Když je stejný parametr nastaven na **Cíl**, bude použita daňová kombinace pro vypůjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="69d31-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="69d31-114">U právnických osob ve Spojených státech, musí být pole **DPH na vstupu** nakonfigurováno na nové stránce **Účetní skupiny hlavní knihy**, když je parametr nastaven na **Zdroj**.</span><span class="sxs-lookup"><span data-stu-id="69d31-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="69d31-115">Účetní modul použije informace z tohoto pole pro účetní záznam vztahující se k dani.</span><span class="sxs-lookup"><span data-stu-id="69d31-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="69d31-116">Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.</span><span class="sxs-lookup"><span data-stu-id="69d31-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

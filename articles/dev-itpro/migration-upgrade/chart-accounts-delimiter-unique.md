---
title: "Oddělovač účtové osnovy musí být jedinečný"
description: "V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Po upgradu je třeba změnit hodnoty oddělovače."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e12c47e4acd6aa8a92a909d490da9e590b5fcd20
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="f1380-104">Oddělovač účtové osnovy musí být jedinečný</span><span class="sxs-lookup"><span data-stu-id="f1380-104">Chart of accounts delimiter must be unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1380-105">V aplikaci Microsoft Dynamics AX 2012 můžete použít stejný oddělovač pro hodnoty účtové osnovy a dimenze.</span><span class="sxs-lookup"><span data-stu-id="f1380-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="f1380-106">V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="f1380-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="f1380-107">Pokud je duplicitní oddělovač, můžete ho změnit po upgradu.</span><span class="sxs-lookup"><span data-stu-id="f1380-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="f1380-108">Tato funkce je k dispozici v:</span><span class="sxs-lookup"><span data-stu-id="f1380-108">This feature is available in:</span></span>
- <span data-ttu-id="f1380-109">Dynamics 365 for Finance and Operations verze 8.0</span><span class="sxs-lookup"><span data-stu-id="f1380-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="f1380-110">Dynamics 365 for Finance and Operations 7.1 KB 4094701 Nelze zadat finanční dimenze, když hodnoty dimenze obsahují oddělovač účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="f1380-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="f1380-111">Dynamics 365 for Finance and Operations verze 7.2 KB 4092967 Nelze zvolit dílčí projekt jako dimenzi, když formát pro dílčí projekt obsahuje oddělovač dimenzí</span><span class="sxs-lookup"><span data-stu-id="f1380-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="f1380-112">Aktualizovat oddělovač</span><span class="sxs-lookup"><span data-stu-id="f1380-112">Update delimiter</span></span>
<span data-ttu-id="f1380-113">Pokud je v konfliktu s účtovou osnovu, lze změnit formát oddělovače účetní osnovy a formát ID projektu/dílčího projektu.</span><span class="sxs-lookup"><span data-stu-id="f1380-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="f1380-114">Žádné další oddělovače dimenze nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="f1380-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="f1380-115">Můžete změnit oddělovač účtové osnovy po upgradu na Finance and Operations v poli **parametry hlavní knihy** > **účtová osnova a dimenze** > **změnit oddělovač**.</span><span class="sxs-lookup"><span data-stu-id="f1380-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="f1380-116">Jestliže pouze konflikt s formát ID dílčího projektu/projektu, můžete změnit hodnotu do **projektu a parametrech účetnictví Správa** > **hlavní** > **změnit dílčí projekt formát**.</span><span class="sxs-lookup"><span data-stu-id="f1380-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="f1380-117">Určení, zda prostředí vyžaduje aktualizaci oddělovače</span><span class="sxs-lookup"><span data-stu-id="f1380-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="f1380-118">Pokud jsou oddělovače ve vašem upgradovaném prostředí konfliktní, může dojít k nestabilitě při zadávání hodnot v ovládacím prvku segmentované položky nebo položky řízení dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f1380-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="f1380-119">To znamená, že je třeba vždy použít vyhledávací kódy nebo plovoucí nabídku při zadávání kombinací účtů a dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f1380-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>


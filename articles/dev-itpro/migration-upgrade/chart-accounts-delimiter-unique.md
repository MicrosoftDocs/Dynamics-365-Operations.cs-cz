---
title: Jak vytvořit jedinečný oddělovač účtové osnovy
description: V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze. Po upgradu je třeba změnit hodnoty oddělovače.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559521"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="20e7a-104">Jak vytvořit jedinečný oddělovač účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="20e7a-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20e7a-105">V aplikaci Microsoft Dynamics AX 2012 můžete použít stejný oddělovač pro hodnoty účtové osnovy a dimenze.</span><span class="sxs-lookup"><span data-stu-id="20e7a-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="20e7a-106">V aplikaci Dynamics 365 for Finance and Operations nemůžete mít stejný oddělovač pro účtovou osnovu a hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="20e7a-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="20e7a-107">Pokud je duplicitní oddělovač, můžete ho změnit po upgradu.</span><span class="sxs-lookup"><span data-stu-id="20e7a-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="20e7a-108">Tato funkce je k dispozici v:</span><span class="sxs-lookup"><span data-stu-id="20e7a-108">This feature is available in:</span></span>
- <span data-ttu-id="20e7a-109">Dynamics 365 for Finance and Operations verze 8.0</span><span class="sxs-lookup"><span data-stu-id="20e7a-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="20e7a-110">Dynamics 365 for Finance and Operations verze 7.1, KB 4094701 Nelze zadat finanční dimenze, když hodnoty dimenze obsahují oddělovač účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="20e7a-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="20e7a-111">Dynamics 365 for Finance and Operations verze 7.2 KB 4092967, Nelze zvolit dílčí projekt jako dimenzi, když formát pro dílčí projekt obsahuje oddělovač dimenzí</span><span class="sxs-lookup"><span data-stu-id="20e7a-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="20e7a-112">Aktualizovat oddělovač</span><span class="sxs-lookup"><span data-stu-id="20e7a-112">Update delimiter</span></span>
<span data-ttu-id="20e7a-113">Pokud je v konfliktu s účtovou osnovu, lze změnit formát oddělovače účetní osnovy a formát ID projektu/dílčího projektu.</span><span class="sxs-lookup"><span data-stu-id="20e7a-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="20e7a-114">Žádné další oddělovače dimenze nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="20e7a-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="20e7a-115">Můžete změnit oddělovač účtové osnovy po upgradu na Finance and Operations v poli **parametry hlavní knihy** > **účtová osnova a dimenze** > **změnit oddělovač**.</span><span class="sxs-lookup"><span data-stu-id="20e7a-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="20e7a-116">Jestliže pouze konflikt s formát ID dílčího projektu/projektu, můžete změnit hodnotu do **projektu a parametrech účetnictví Správa** > **hlavní** > **změnit dílčí projekt formát**.</span><span class="sxs-lookup"><span data-stu-id="20e7a-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="20e7a-117">Určení, zda prostředí vyžaduje aktualizaci oddělovače</span><span class="sxs-lookup"><span data-stu-id="20e7a-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="20e7a-118">Pokud jsou oddělovače ve vašem upgradovaném prostředí konfliktní, může dojít k nestabilitě při zadávání hodnot v ovládacím prvku segmentované položky nebo položky řízení dimenzí.</span><span class="sxs-lookup"><span data-stu-id="20e7a-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="20e7a-119">To znamená, že je třeba vždy použít vyhledávací kódy nebo plovoucí nabídku při zadávání kombinací účtů a dimenzí.</span><span class="sxs-lookup"><span data-stu-id="20e7a-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

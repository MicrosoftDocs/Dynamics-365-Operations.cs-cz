---
title: Hromadné importování uživatelů
description: Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d8b55895c9dfaf1c69cd319697f1e0da5990daf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144080"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="62023-103">Hromadné importování uživatelů</span><span class="sxs-lookup"><span data-stu-id="62023-103">Import users in bulk</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62023-104">Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62023-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="62023-105">Spustit jako dávkovou úlohu</span><span class="sxs-lookup"><span data-stu-id="62023-105">Run as a batch job</span></span>
1. <span data-ttu-id="62023-106">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="62023-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="62023-107">Klikněte na Dávkový import.</span><span class="sxs-lookup"><span data-stu-id="62023-107">Click Batch import.</span></span>
3. <span data-ttu-id="62023-108">Rozbalte sekci Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="62023-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="62023-109">V poli Dávkové zpracování vyberte hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="62023-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="62023-110">Zadejte hodnotu do pole Popis úkolu.</span><span class="sxs-lookup"><span data-stu-id="62023-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="62023-111">V poli Skupina dávek zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="62023-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="62023-112">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="62023-112">This is an optional step.</span></span>  
7. <span data-ttu-id="62023-113">Vyberte možnost Ano v poli Soukromý.</span><span class="sxs-lookup"><span data-stu-id="62023-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="62023-114">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="62023-114">This is an optional step.</span></span>  
8. <span data-ttu-id="62023-115">Vyberte možnost Ano v poli Kritická úloha.</span><span class="sxs-lookup"><span data-stu-id="62023-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="62023-116">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="62023-116">This is an optional step.</span></span>  
9. <span data-ttu-id="62023-117">Vyberte volbu v poli Kategorie monitorování.</span><span class="sxs-lookup"><span data-stu-id="62023-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="62023-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="62023-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="62023-119">Spuštění v prostředí sandbox</span><span class="sxs-lookup"><span data-stu-id="62023-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="62023-120">Klikněte na Dávkový import.</span><span class="sxs-lookup"><span data-stu-id="62023-120">Click Batch import.</span></span>
2. <span data-ttu-id="62023-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="62023-121">Click OK.</span></span>


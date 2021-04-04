---
title: Importovat uživatele ze služby Azure Active Directory
description: Tento postup mohou použít správci systému k ručnímu importu vybraných uživatelů nebo k importu velkého počtu uživatelů ze služby Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570998"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="8f5f6-103">Importovat uživatele ze služby Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8f5f6-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="8f5f6-104">Import vybraných uživatelů</span><span class="sxs-lookup"><span data-stu-id="8f5f6-104">Import select users</span></span>

<span data-ttu-id="8f5f6-105">Tento postup mohou použít správci systému k importu vybraných uživatelů ze služby Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8f5f6-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="8f5f6-106">Uživatel bude importován spolu s aktuální společností relace jako výchozí společností.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="8f5f6-107">Před importem uživatelů změňte v případě potřeby aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="8f5f6-108">Přejděte do nabídky **Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="8f5f6-109">Klikněte na možnost **Importovat uživatele**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-109">Click **Import users**.</span></span>
4. <span data-ttu-id="8f5f6-110">Vyberte uživatele, kteří mají být importováni, a vyberte příkaz **Importovat uživatele**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="8f5f6-111">Po dokončení importu bude nutné přiřadit role uživatelům.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="8f5f6-112">Hromadné importování uživatelů</span><span class="sxs-lookup"><span data-stu-id="8f5f6-112">Import users in bulk</span></span>

<span data-ttu-id="8f5f6-113">Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="8f5f6-114">Upozorňujeme, že při použití možnosti Dávkový import není možné vybrat uživatele.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="8f5f6-115">Spuštění importu jako dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="8f5f6-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="8f5f6-116">Uživatel bude importován spolu s aktuální společností relace jako výchozí společností.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="8f5f6-117">Před importem uživatelů změňte v případě potřeby aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="8f5f6-118">Přejděte do nabídky **Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="8f5f6-119">Klikněte na **Dávkový import**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="8f5f6-120">Rozbalte sekci **Spustit na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="8f5f6-121">V poli **Dávkové zpracování** vyberte hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="8f5f6-122">V poli **Skupina dávek** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="8f5f6-123">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-123">This is an optional step.</span></span>  
7. <span data-ttu-id="8f5f6-124">Vyberte hodnotu **Ano** v poli **Soukromý**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="8f5f6-125">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-125">This is an optional step.</span></span>  
8. <span data-ttu-id="8f5f6-126">Vyberte hodnotu **Ano** v poli **Kritická úloha**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="8f5f6-127">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-127">This is an optional step.</span></span>  
9. <span data-ttu-id="8f5f6-128">Vyberte volbu v poli **Kategorie monitorování**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="8f5f6-129">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-129">Click **OK**.</span></span>

<span data-ttu-id="8f5f6-130">Po dokončení importu bude nutné přiřadit role uživatelům.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="8f5f6-131">Spuštění v prostředí sandbox</span><span class="sxs-lookup"><span data-stu-id="8f5f6-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="8f5f6-132">Vyberte možnost **Dávkový import**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="8f5f6-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f5f6-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
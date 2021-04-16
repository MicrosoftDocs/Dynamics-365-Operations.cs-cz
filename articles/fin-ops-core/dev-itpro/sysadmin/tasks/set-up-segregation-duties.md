---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745734"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="6d2cf-103">Nastavení dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="6d2cf-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d2cf-104">Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="6d2cf-105">Tento koncept se nazývá dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="6d2cf-106">Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="6d2cf-107">Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="6d2cf-108">Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="6d2cf-109">Chcete-li vytvořit pravidlo, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="6d2cf-110">K dokončení postupu musíte být správce systému.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="6d2cf-111">Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Pravidla dělení zodpovědnosti**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="6d2cf-112">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-112">Click **New**.</span></span>
3. <span data-ttu-id="6d2cf-113">Do pole **Název** zadejte hodnotu pravidla.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="6d2cf-114">V poli **První funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6d2cf-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d2cf-116">Vyberte první zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="6d2cf-117">V poli **Druhé funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="6d2cf-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d2cf-119">Vyberte druhou zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="6d2cf-120">Vyberte možnost v poli **Závažnost**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="6d2cf-121">Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="6d2cf-122">Zadejte hodnotu do pole **Riziko zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="6d2cf-123">Zadejte popis rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="6d2cf-124">Zadejte hodnotu do pole **Snížení rizika zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="6d2cf-125">Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="6d2cf-126">Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="6d2cf-127">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6d2cf-128">Při vytváření pravidla není ověřeno dodržování pravidel pro oddělení povinností.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="6d2cf-129">Můžete vytvořit pravidlo, které vytvoří konflikt pro existující role.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="6d2cf-130">Stávající přiřazení rolí uživatelů může být také v konfliktu s novým pravidlem.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="6d2cf-131">Po vytvoření nebo úpravě pravidla musíte ověřit dodržování předpisů.</span><span class="sxs-lookup"><span data-stu-id="6d2cf-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="6d2cf-132">Další informace získáte v části [Identifikace a vyřešení konfliktů v dělení zodpovědnosti](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="6d2cf-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
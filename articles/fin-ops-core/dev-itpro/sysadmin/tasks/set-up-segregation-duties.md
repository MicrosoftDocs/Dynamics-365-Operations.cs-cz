---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688166"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="c81d7-103">Nastavení dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="c81d7-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c81d7-104">Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.</span><span class="sxs-lookup"><span data-stu-id="c81d7-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="c81d7-105">Tento koncept se nazývá dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="c81d7-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="c81d7-106">Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="c81d7-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="c81d7-107">Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="c81d7-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="c81d7-108">Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol.</span><span class="sxs-lookup"><span data-stu-id="c81d7-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="c81d7-109">Chcete-li vytvořit pravidlo, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="c81d7-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="c81d7-110">K dokončení postupu musíte být správce systému.</span><span class="sxs-lookup"><span data-stu-id="c81d7-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="c81d7-111">K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT.</span><span class="sxs-lookup"><span data-stu-id="c81d7-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="c81d7-112">Přejděte do nabídky **Podokno navigace > Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.**</span><span class="sxs-lookup"><span data-stu-id="c81d7-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="c81d7-113">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c81d7-113">Click **New**.</span></span>
3. <span data-ttu-id="c81d7-114">Do pole **Název** zadejte hodnotu pravidla.</span><span class="sxs-lookup"><span data-stu-id="c81d7-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="c81d7-115">V poli **První funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c81d7-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c81d7-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c81d7-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="c81d7-117">Vyberte první zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="c81d7-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="c81d7-118">V poli **Druhé funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c81d7-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="c81d7-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c81d7-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="c81d7-120">Vyberte druhou zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="c81d7-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="c81d7-121">Vyberte možnost v poli **Závažnost**.</span><span class="sxs-lookup"><span data-stu-id="c81d7-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="c81d7-122">Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="c81d7-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="c81d7-123">Zadejte hodnotu do pole **Riziko zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="c81d7-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="c81d7-124">Zadejte popis rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="c81d7-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="c81d7-125">Zadejte hodnotu do pole **Snížení rizika zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="c81d7-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="c81d7-126">Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="c81d7-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="c81d7-127">Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.</span><span class="sxs-lookup"><span data-stu-id="c81d7-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="c81d7-128">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c81d7-128">Click **Save**.</span></span>


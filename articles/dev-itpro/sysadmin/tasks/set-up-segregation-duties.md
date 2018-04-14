--- 
title: "Nastavení dělení zodpovědnosti"
description: "Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ea94570ca23761195ed93bbab6c51f5df02c28bb
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="914b7-103">Nastavení dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="914b7-103">Set up segregation of duties</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="914b7-104">Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.</span><span class="sxs-lookup"><span data-stu-id="914b7-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="914b7-105">Tento koncept se nazývá dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="914b7-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="914b7-106">Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="914b7-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="914b7-107">Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="914b7-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="914b7-108">Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol.</span><span class="sxs-lookup"><span data-stu-id="914b7-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="914b7-109">Chcete-li vytvořit pravidlo, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="914b7-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="914b7-110">K dokončení postupu musíte být správce systému.</span><span class="sxs-lookup"><span data-stu-id="914b7-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="914b7-111">K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT.</span><span class="sxs-lookup"><span data-stu-id="914b7-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="914b7-112">Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="914b7-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="914b7-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="914b7-113">Click New.</span></span>
3. <span data-ttu-id="914b7-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="914b7-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="914b7-115">Zadejte název pravidla.</span><span class="sxs-lookup"><span data-stu-id="914b7-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="914b7-116">V poli První funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="914b7-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="914b7-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="914b7-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="914b7-118">Vyberte první zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="914b7-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="914b7-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="914b7-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="914b7-120">V poli Druhé funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="914b7-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="914b7-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="914b7-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="914b7-122">Vyberte druhou zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="914b7-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="914b7-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="914b7-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="914b7-124">Vyberte možnost v poli Závažnost.</span><span class="sxs-lookup"><span data-stu-id="914b7-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="914b7-125">Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="914b7-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="914b7-126">Zadejte hodnotu do pole Riziko zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="914b7-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="914b7-127">Zadejte popis rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="914b7-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="914b7-128">Zadejte hodnotu do pole Snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="914b7-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="914b7-129">Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="914b7-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="914b7-130">Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.</span><span class="sxs-lookup"><span data-stu-id="914b7-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="914b7-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="914b7-131">Click Save.</span></span>



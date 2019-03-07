---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "318780"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="8beb5-103">Nastavení dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="8beb5-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8beb5-104">Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.</span><span class="sxs-lookup"><span data-stu-id="8beb5-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="8beb5-105">Tento koncept se nazývá dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="8beb5-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="8beb5-106">Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="8beb5-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="8beb5-107">Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="8beb5-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="8beb5-108">Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol.</span><span class="sxs-lookup"><span data-stu-id="8beb5-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="8beb5-109">Chcete-li vytvořit pravidlo, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="8beb5-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="8beb5-110">K dokončení postupu musíte být správce systému.</span><span class="sxs-lookup"><span data-stu-id="8beb5-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="8beb5-111">K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT.</span><span class="sxs-lookup"><span data-stu-id="8beb5-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="8beb5-112">Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="8beb5-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="8beb5-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8beb5-113">Click New.</span></span>
3. <span data-ttu-id="8beb5-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="8beb5-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8beb5-115">Zadejte název pravidla.</span><span class="sxs-lookup"><span data-stu-id="8beb5-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="8beb5-116">V poli První funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8beb5-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8beb5-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="8beb5-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8beb5-118">Vyberte první zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="8beb5-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="8beb5-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8beb5-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8beb5-120">V poli Druhé funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8beb5-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8beb5-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="8beb5-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8beb5-122">Vyberte druhou zodpovědnost, která se řídí pravidlem.</span><span class="sxs-lookup"><span data-stu-id="8beb5-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="8beb5-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8beb5-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8beb5-124">Vyberte možnost v poli Závažnost.</span><span class="sxs-lookup"><span data-stu-id="8beb5-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="8beb5-125">Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="8beb5-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="8beb5-126">Zadejte hodnotu do pole Riziko zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8beb5-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="8beb5-127">Zadejte popis rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8beb5-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="8beb5-128">Zadejte hodnotu do pole Snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8beb5-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="8beb5-129">Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8beb5-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="8beb5-130">Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.</span><span class="sxs-lookup"><span data-stu-id="8beb5-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="8beb5-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8beb5-131">Click Save.</span></span>


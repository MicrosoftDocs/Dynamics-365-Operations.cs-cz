---
title: "Spravovat položky půjčené zaměstnancům"
description: "Položky výpůjčky jsou záznamy, které pomáhají manažerům se sledováním fyzických položek, které vaše společnost půjčuje zaměstnancům."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 4082facdba02cd69c6679e7f3e68e391d29e4195
ms.contentlocale: cs-cz
ms.lasthandoff: 01/31/2018

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="6f1bb-103">Spravovat položky půjčené zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="6f1bb-103">Manage items lent to workers</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="6f1bb-104">Položky výpůjčky jsou záznamy, které pomáhají manažerům se sledováním fyzických položek, které vaše společnost půjčuje zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="6f1bb-105">V následujícím seznamu jsou příklady položek, které může společnost půjčit pracovníkům:</span><span class="sxs-lookup"><span data-stu-id="6f1bb-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="6f1bb-106">mobilní telefony;</span><span class="sxs-lookup"><span data-stu-id="6f1bb-106">Mobile telephones</span></span>
-   <span data-ttu-id="6f1bb-107">automobily;</span><span class="sxs-lookup"><span data-stu-id="6f1bb-107">Automobiles</span></span>
-   <span data-ttu-id="6f1bb-108">počítačové vybavení.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-108">Computer equipment</span></span>

<span data-ttu-id="6f1bb-109">Každá fyzická položka musí mít odpovídající položku výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="6f1bb-110">Každý záznam o zapůjčené položce by měl obsahovat popis zapůjčené věci, osobu, která je za zapůjčení odpovědná, a počet dní, na které je položka pracovníkovi zapůjčena.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="6f1bb-111">Můžete vytvořit více položek výpůjčky (například v případě klíčů, přístupových karet nebo stejnokrojů) současně.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="6f1bb-112">Při zapůjčení položky zadejte datum zapůjčení a plánované datum vrácení.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="6f1bb-113">Při vrácení položky zadejte skutečné datum vrácení.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="6f1bb-114">Zaměstnanci si mohou prohlížet záznamy položek, které mají vypůjčeny z pracovního prostoru Samoobsluha pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="6f1bb-115">Mohou také upravit existující záznamy nebo zadat nové položky výpůjčky, pokud obdrželi další fyzické položky.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="6f1bb-116">Pracovní postup je možné nastavit tak, aby směroval změny do nových nebo existujících položek pomocí schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="6f1bb-117">Manažeři si mohou zobrazit položky zapůjčené jejich přímým podřízeným.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="6f1bb-118">Také mohou mít oprávnění k přidání nových položek výpůjčky jménem svých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="6f1bb-119"> Účet pro položky výpůjček, které byly ztraceny nebo poškozeny</span><span class="sxs-lookup"><span data-stu-id="6f1bb-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="6f1bb-120">Pokud došlo ke ztrátě nebo poškození položky, vložte záznam o fiktivním vrácení.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="6f1bb-121">Pak lze buď položku smazat, nebo ji dále vést v přehledu, ale je nutné změnit její popis, který bude nadále označovat, že daná položka není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="6f1bb-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>

 
<a name="see-also"></a><span data-ttu-id="6f1bb-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="6f1bb-122">See also</span></span>
--------

[<span data-ttu-id="6f1bb-123">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="6f1bb-123">Human resources</span></span>](index.md)





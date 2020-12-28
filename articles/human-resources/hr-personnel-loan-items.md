---
title: Správa položek zapůjčených zaměstnancům
description: Položky výpůjčky jsou záznamy, které pomáhají manažerům se sledováním fyzických položek, které vaše společnost půjčuje zaměstnancům.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5915df388da7ce8b90cdcb0e859268c00003110c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417619"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="198f4-103">Správa položek zapůjčených zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="198f4-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="198f4-104">Položky výpůjčky jsou záznamy, které pomáhají manažerům se sledováním fyzických položek, které vaše společnost půjčuje zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="198f4-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="198f4-105">V následujícím seznamu jsou příklady položek, které může společnost půjčit pracovníkům:</span><span class="sxs-lookup"><span data-stu-id="198f4-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="198f4-106">mobilní telefony;</span><span class="sxs-lookup"><span data-stu-id="198f4-106">Mobile telephones</span></span>
-   <span data-ttu-id="198f4-107">automobily;</span><span class="sxs-lookup"><span data-stu-id="198f4-107">Automobiles</span></span>
-   <span data-ttu-id="198f4-108">počítačové vybavení.</span><span class="sxs-lookup"><span data-stu-id="198f4-108">Computer equipment</span></span>

<span data-ttu-id="198f4-109">Každá fyzická položka musí mít odpovídající položku výpůjčky.</span><span class="sxs-lookup"><span data-stu-id="198f4-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="198f4-110">Každý záznam o zapůjčené položce by měl obsahovat popis zapůjčené věci, osobu, která je za zapůjčení odpovědná, a počet dní, na které je položka pracovníkovi zapůjčena.</span><span class="sxs-lookup"><span data-stu-id="198f4-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="198f4-111">Můžete vytvořit více položek výpůjčky (například v případě klíčů, přístupových karet nebo stejnokrojů) současně.</span><span class="sxs-lookup"><span data-stu-id="198f4-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="198f4-112">Při zapůjčení položky zadejte datum zapůjčení a plánované datum vrácení.</span><span class="sxs-lookup"><span data-stu-id="198f4-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="198f4-113">Při vrácení položky zadejte skutečné datum vrácení.</span><span class="sxs-lookup"><span data-stu-id="198f4-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="198f4-114">Zaměstnanci si mohou prohlížet záznamy položek, které mají vypůjčeny z pracovního prostoru Samoobsluha pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="198f4-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="198f4-115">Mohou také upravit existující záznamy nebo zadat nové položky výpůjčky, pokud obdrželi další fyzické položky.</span><span class="sxs-lookup"><span data-stu-id="198f4-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="198f4-116">Pracovní postup je možné nastavit tak, aby směroval změny do nových nebo existujících položek pomocí schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="198f4-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="198f4-117">Manažeři si mohou zobrazit položky zapůjčené jejich přímým podřízeným.</span><span class="sxs-lookup"><span data-stu-id="198f4-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="198f4-118">Také mohou mít oprávnění k přidání nových položek výpůjčky jménem svých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="198f4-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="198f4-119"> Účet pro položky výpůjček, které byly ztraceny nebo poškozeny</span><span class="sxs-lookup"><span data-stu-id="198f4-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="198f4-120">Pokud došlo ke ztrátě nebo poškození položky, vložte záznam o fiktivním vrácení.</span><span class="sxs-lookup"><span data-stu-id="198f4-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="198f4-121">Pak lze buď položku smazat, nebo ji dále vést v přehledu, ale je nutné změnit její popis, který bude nadále označovat, že daná položka není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="198f4-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="198f4-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="198f4-122">Additional resources</span></span>
--------

[<span data-ttu-id="198f4-123">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="198f4-123">Human resources</span></span>](index.md)




---
title: Správa dovolené
description: Tento postup vás provede vytvářením záznamů o odchodu zaměstnance.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143532"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="146a4-103">Správa dovolené</span><span class="sxs-lookup"><span data-stu-id="146a4-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="146a4-104">Tento postup vás provede vytvářením záznamů o odchodu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="146a4-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="146a4-105">Lze sledovat čas odchodu z důvodů, které zahrnují zdravotní, vzdělávací a rodičovské aktivity.</span><span class="sxs-lookup"><span data-stu-id="146a4-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="146a4-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="146a4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="146a4-107">Přejděte k nabídce Lidské zdroje > Pracovníci > Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="146a4-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="146a4-108">V seznamu vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="146a4-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="146a4-109">Zobrazte podrobné informace k vybranému zaměstnanci výběrem jména zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="146a4-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="146a4-110">Klikněte na kartu Zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="146a4-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="146a4-111">Klepněte na tlačítko Odchod.</span><span class="sxs-lookup"><span data-stu-id="146a4-111">Click Leave.</span></span>
6. <span data-ttu-id="146a4-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="146a4-112">Click New.</span></span>
7. <span data-ttu-id="146a4-113">V poli Typ odchodu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="146a4-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="146a4-114">Můžete přidružit typu odchodu ke kódu příjmů ve formuláři Typy odchodů.</span><span class="sxs-lookup"><span data-stu-id="146a4-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="146a4-115">Pokud je typ odchodu přidružen ke kódu příjmů, bude vygenerován řádek příjmů přidružený je kódu příjmů v době odchodu, kterou zadáte.</span><span class="sxs-lookup"><span data-stu-id="146a4-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="146a4-116">V seznamu vyberte typ odchodu.</span><span class="sxs-lookup"><span data-stu-id="146a4-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="146a4-117">Například: Adopce</span><span class="sxs-lookup"><span data-stu-id="146a4-117">For example: Adoption</span></span>  
9. <span data-ttu-id="146a4-118">Zadejte datum zahájení odchodu.</span><span class="sxs-lookup"><span data-stu-id="146a4-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="146a4-119">Například : '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="146a4-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="146a4-120">Například: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="146a4-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="146a4-121">Zadejte datum zahájení odchodu.</span><span class="sxs-lookup"><span data-stu-id="146a4-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="146a4-122">Například: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="146a4-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="146a4-123">Zadejte popis do pole s poznámkou.</span><span class="sxs-lookup"><span data-stu-id="146a4-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="146a4-124">Například: odchod kvůli adopci</span><span class="sxs-lookup"><span data-stu-id="146a4-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="146a4-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="146a4-125">Click Save.</span></span>


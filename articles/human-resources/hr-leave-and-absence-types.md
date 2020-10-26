---
title: Konfigurace typů pracovního volna a absence
description: Nastavte typy volna, které mohou zaměstnanci provést v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 6a89816f94c8cdcae6e56fa89843eb99c28b21fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/07/2020
ms.locfileid: "3969015"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="8525d-103">Konfigurace typů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="8525d-103">Configure leave and absence types</span></span>

<span data-ttu-id="8525d-104">Typy pracovního volna v Dynamics 365 Human Resources definují různé typy absence, které může zaměstnanec ohlásit.</span><span class="sxs-lookup"><span data-stu-id="8525d-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="8525d-105">Typy pracovního volna můžete přizpůsobit podle potřeb dané organizace.</span><span class="sxs-lookup"><span data-stu-id="8525d-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="8525d-106">Příklady popisů typů pracovního volna:</span><span class="sxs-lookup"><span data-stu-id="8525d-106">Examples of leave types include:</span></span>

- <span data-ttu-id="8525d-107">Placený čas volna (PTO)</span><span class="sxs-lookup"><span data-stu-id="8525d-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="8525d-108">Neplacené volno</span><span class="sxs-lookup"><span data-stu-id="8525d-108">Unpaid leave</span></span>
- <span data-ttu-id="8525d-109">Placená dovolená</span><span class="sxs-lookup"><span data-stu-id="8525d-109">Paid vacation</span></span>
- <span data-ttu-id="8525d-110">Pracovní neschopnost</span><span class="sxs-lookup"><span data-stu-id="8525d-110">Sick leave</span></span>
- <span data-ttu-id="8525d-111">Zdravotní dovolená</span><span class="sxs-lookup"><span data-stu-id="8525d-111">Medical leave</span></span>
- <span data-ttu-id="8525d-112">Volno z rodinných důvodů</span><span class="sxs-lookup"><span data-stu-id="8525d-112">Family leave</span></span>
- <span data-ttu-id="8525d-113">Krátkodobá invalidita</span><span class="sxs-lookup"><span data-stu-id="8525d-113">Short-term disability</span></span>
- <span data-ttu-id="8525d-114">Volno z důvodu zármutku</span><span class="sxs-lookup"><span data-stu-id="8525d-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="8525d-115">Přidání typu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="8525d-115">Add a leave type</span></span>

1. <span data-ttu-id="8525d-116">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy** .</span><span class="sxs-lookup"><span data-stu-id="8525d-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8525d-117">V části **Nastavení** vyberte **Typ pracovního volna a absence** .</span><span class="sxs-lookup"><span data-stu-id="8525d-117">Under **Setup** , select **Leave and absence types** .</span></span>

3. <span data-ttu-id="8525d-118">Zvolte **Nové** .</span><span class="sxs-lookup"><span data-stu-id="8525d-118">Select **New** .</span></span>

4. <span data-ttu-id="8525d-119">Zadejte název typu pracovního volna v části **Typ** , vyberte workflow v okně **ID workflowu** a do pole **Popis** napište popis.</span><span class="sxs-lookup"><span data-stu-id="8525d-119">Enter a name for the leave type under **Type** , select a workflow from **Workflow ID** , and enter a description under **Description** .</span></span>

5. <span data-ttu-id="8525d-120">V části **Obecné** vyberte **Žádný** , **Naplánované** nebo **Neplánované** v rozevíracím seznamu **Kategorie** .</span><span class="sxs-lookup"><span data-stu-id="8525d-120">In **General** , select **None** , **Scheduled** , or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="8525d-121">Vyberte kód výdělku z rozevíracího seznamu **kód výdělku** .</span><span class="sxs-lookup"><span data-stu-id="8525d-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="8525d-122">V části **Požadován kód důvodu** vyberte, zda chcete požadovat kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="8525d-122">Under **Reason code required** , choose whether you want to require a reason code.</span></span> <span data-ttu-id="8525d-123">Chcete-li požadovat kódy důvodu, budete je pravděpodobně muset přidat.</span><span class="sxs-lookup"><span data-stu-id="8525d-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="8525d-124">V části **Kódy důvodu** vyberte možnost **Přidat** , vyberte kód důvodu a poté zaškrtněte políčko **Povoleno** vedle něho.</span><span class="sxs-lookup"><span data-stu-id="8525d-124">Under **Reason codes** , select **Add** , select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="8525d-125">V části **Omezit přístup k vybraným rolím** vyberte, zda chcete omezit přístup.</span><span class="sxs-lookup"><span data-stu-id="8525d-125">Under **Restrict access to selected roles** , choose whether you want to restrict access.</span></span> <span data-ttu-id="8525d-126">Poté vyberte role zabezpečení v části **role zabezpečení pro tento typ pracovního volna** .</span><span class="sxs-lookup"><span data-stu-id="8525d-126">Then select the security roles under **Security roles for this leave type** .</span></span> <span data-ttu-id="8525d-127">Role zabezpečení jsou definovány ve workflowu vybraném pod položkou **ID workflowu** dříve v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="8525d-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="8525d-128">Pod položkou **Barva kalendáře** zvolte barvu, která se má pro tento typ nepřítomnosti zobrazovat v kalendáři nepřítomností.</span><span class="sxs-lookup"><span data-stu-id="8525d-128">Under **Calendar color** , choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="8525d-129">V možnosti **Vztahy přerušení** zvolte, zda chcete, aby tento typ dovolené buď pozastavil jiný typ dovolené, nebo aby byl pozastaven jiným typem dovolené.</span><span class="sxs-lookup"><span data-stu-id="8525d-129">Under **Suspension relations** , choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="8525d-130">Pokud je pro typ přerušení volna podán požadavek na pracovní volno, automaticky se pro tento typ dovolené vytvoří přerušení volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="8525d-131">Zvolte **Uložit** .</span><span class="sxs-lookup"><span data-stu-id="8525d-131">Select **Save** .</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="8525d-132">Konfigurace pravidel typů volna</span><span class="sxs-lookup"><span data-stu-id="8525d-132">Configure leave type rules</span></span>

1. <span data-ttu-id="8525d-133">Nastavte možnosti zaokrouhlení pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="8525d-134">Možnosti zahrnují **Žádný** **Nahoru** , **Dolů** a **Nejbližší** .</span><span class="sxs-lookup"><span data-stu-id="8525d-134">Options include **None** , **Up** , **Down** , and **Nearest** .</span></span> <span data-ttu-id="8525d-135">Můžete také nastavit přesnost zaokrouhlení pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="8525d-136">Nastavte **Oprava volna** pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="8525d-137">Pokud vyberete tuto možnost, aplikace Human Resources použije počet svátků, které spadají do pracovního dne k určení, jakým způsobem má být rozlišen volný čas u tohoto typu pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="8525d-138">Pokud například 1. svátek vánoční připadá na pondělí, odečte aplikace Human Resources při zpracování časového rozlišení od typu pracovního volna jeden den.</span><span class="sxs-lookup"><span data-stu-id="8525d-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="8525d-139">Svátky nastavujete v kalendáři pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="8525d-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="8525d-140">Další informace naleznete v tématu [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="8525d-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="8525d-141">Nastavte **Typ převodu pracovního volna** pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="8525d-142">Pokud vyberete tuto možnost, veškeré zůstatky k převodu budou převedeny na zadaný typ volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="8525d-143">Do plánu volna a nepřítomnosti musí být rovněž zahrnut typ převodu volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="8525d-144">Definujte **Pravidla vypršení platnosti** pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="8525d-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="8525d-145">Když nakonfigurujete tuto možnost, můžete vybrat jednotku dní nebo měsíců a nastavit dobu trvání.</span><span class="sxs-lookup"><span data-stu-id="8525d-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="8525d-146">Můžete také nastavit datum účinnosti pravidla vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="8525d-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="8525d-147">Jakékoli zůstatky dovolené, které existují v době vypršení platnosti, budou odečteny od typu dovolené a budou zohledněny v zůstatku dovolené.</span><span class="sxs-lookup"><span data-stu-id="8525d-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="8525d-148">Viz také</span><span class="sxs-lookup"><span data-stu-id="8525d-148">See also</span></span>

- [<span data-ttu-id="8525d-149">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="8525d-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="8525d-150">Vytvoření plánu pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="8525d-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="8525d-151">Vytvoření kalendáře pracovní doby</span><span class="sxs-lookup"><span data-stu-id="8525d-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="8525d-152">Přerušit pracovní volno</span><span class="sxs-lookup"><span data-stu-id="8525d-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)


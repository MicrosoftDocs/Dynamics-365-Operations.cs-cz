---
title: Konfigurace typů pracovního volna a absence
description: Nastavte typy volna, které mohou zaměstnanci provést v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008394"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="ca972-103">Konfigurace typů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="ca972-103">Configure leave and absence types</span></span>

<span data-ttu-id="ca972-104">Typy pracovního volna v Dynamics 365 Human Resources definují různé typy absence, které může zaměstnanec ohlásit.</span><span class="sxs-lookup"><span data-stu-id="ca972-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="ca972-105">Typy pracovního volna můžete přizpůsobit podle potřeb dané organizace.</span><span class="sxs-lookup"><span data-stu-id="ca972-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="ca972-106">Příklady popisů typů pracovního volna:</span><span class="sxs-lookup"><span data-stu-id="ca972-106">Examples of leave types include:</span></span>

- <span data-ttu-id="ca972-107">Placený čas volna (PTO)</span><span class="sxs-lookup"><span data-stu-id="ca972-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="ca972-108">Neplacené volno</span><span class="sxs-lookup"><span data-stu-id="ca972-108">Unpaid leave</span></span>
- <span data-ttu-id="ca972-109">Placená dovolená</span><span class="sxs-lookup"><span data-stu-id="ca972-109">Paid vacation</span></span>
- <span data-ttu-id="ca972-110">Pracovní neschopnost</span><span class="sxs-lookup"><span data-stu-id="ca972-110">Sick leave</span></span>
- <span data-ttu-id="ca972-111">Zdravotní dovolená</span><span class="sxs-lookup"><span data-stu-id="ca972-111">Medical leave</span></span>
- <span data-ttu-id="ca972-112">Volno z rodinných důvodů</span><span class="sxs-lookup"><span data-stu-id="ca972-112">Family leave</span></span>
- <span data-ttu-id="ca972-113">Krátkodobá invalidita</span><span class="sxs-lookup"><span data-stu-id="ca972-113">Short-term disability</span></span>
- <span data-ttu-id="ca972-114">Volno z důvodu zármutku</span><span class="sxs-lookup"><span data-stu-id="ca972-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="ca972-115">Přidání typu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="ca972-115">Add a leave type</span></span>

1. <span data-ttu-id="ca972-116">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="ca972-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ca972-117">V části **Nastavení** vyberte **Typ pracovního volna a absence**.</span><span class="sxs-lookup"><span data-stu-id="ca972-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="ca972-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ca972-118">Select **New**.</span></span>

4. <span data-ttu-id="ca972-119">Zadejte název typu pracovního volna v části **Typ**, vyberte workflow v okně **ID workflowu** a do pole **Popis** napište popis.</span><span class="sxs-lookup"><span data-stu-id="ca972-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="ca972-120">V části **Obecné** vyberte **Žádný**, **Naplánované** nebo **Neplánované** v rozevíracím seznamu **Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="ca972-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="ca972-121">Vyberte kód výdělku z rozevíracího seznamu **kód výdělku**.</span><span class="sxs-lookup"><span data-stu-id="ca972-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="ca972-122">V části **Požadován kód důvodu** vyberte, zda chcete požadovat kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="ca972-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="ca972-123">Chcete-li požadovat kódy důvodu, budete je pravděpodobně muset přidat.</span><span class="sxs-lookup"><span data-stu-id="ca972-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="ca972-124">V části **Kódy důvodu** vyberte možnost **Přidat**, vyberte kód důvodu a poté zaškrtněte políčko **Povoleno** vedle něho.</span><span class="sxs-lookup"><span data-stu-id="ca972-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="ca972-125">V části **Omezit přístup k vybraným rolím** vyberte, zda chcete omezit přístup.</span><span class="sxs-lookup"><span data-stu-id="ca972-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="ca972-126">Poté vyberte role zabezpečení v části **role zabezpečení pro tento typ pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="ca972-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="ca972-127">Role zabezpečení jsou definovány ve workflowu vybraném pod položkou **ID workflowu** dříve v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="ca972-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="ca972-128">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ca972-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="ca972-129">Konfigurace funkcí náhledu</span><span class="sxs-lookup"><span data-stu-id="ca972-129">Configure preview features</span></span>

<span data-ttu-id="ca972-130">Pokud jste povolili funkce náhledu pro pracovní volno a absenci, musíte pro ně také nakonfigurovat nastavení.</span><span class="sxs-lookup"><span data-stu-id="ca972-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="ca972-131">Nastavte možnosti zaokrouhlení pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="ca972-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="ca972-132">Možnosti zahrnují **Žádný** **Nahoru**, **Dolů** a **Nejbližší**.</span><span class="sxs-lookup"><span data-stu-id="ca972-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="ca972-133">Můžete také nastavit přesnost zaokrouhlení pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="ca972-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="ca972-134">Nastavte **Oprava volna** pro typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="ca972-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="ca972-135">Pokud vyberete tuto možnost, aplikace Human Resources použije počet svátků, které spadají do pracovního dne k určení, jakým způsobem má být rozlišen volný čas u tohoto typu pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="ca972-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="ca972-136">Pokud například 1. svátek vánoční připadá na pondělí, odečte aplikace Human Resources při zpracování časového rozlišení od typu pracovního volna jeden den.</span><span class="sxs-lookup"><span data-stu-id="ca972-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="ca972-137">Svátky nastavujete v kalendáři pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="ca972-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="ca972-138">Další informace naleznete v tématu [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="ca972-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="ca972-139">Viz také</span><span class="sxs-lookup"><span data-stu-id="ca972-139">See also</span></span>

- [<span data-ttu-id="ca972-140">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="ca972-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="ca972-141">Vytvoření plánu pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="ca972-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="ca972-142">Vytvoření kalendáře pracovní doby</span><span class="sxs-lookup"><span data-stu-id="ca972-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
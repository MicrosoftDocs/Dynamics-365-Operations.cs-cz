---
title: Vytvoření kalendáře pracovní doby
description: Definujte kalendář pracovní doby, svátků a časy, kdy nepracujete, v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428795"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="cbdf0-103">Vytvoření kalendáře pracovní doby</span><span class="sxs-lookup"><span data-stu-id="cbdf0-103">Create a working time calendar</span></span>

<span data-ttu-id="cbdf0-104">Kalendář pracovní doby v aplikaci Dynamics 365 Human Resources zobrazuje dny a hodiny, které zaměstnanci pracují ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="cbdf0-105">Když zaměstnanec odešle požadavek na volno, nemusí se starat o svátky a uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="cbdf0-106">Chcete-li zefektivnit zpracování požadavků na vyřízení, konfigurujte pro vaši organizaci tyto položky:</span><span class="sxs-lookup"><span data-stu-id="cbdf0-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="cbdf0-107">Kalendář pracovní doby</span><span class="sxs-lookup"><span data-stu-id="cbdf0-107">Working time calendar</span></span>
- <span data-ttu-id="cbdf0-108">Svátky a uzavírky</span><span class="sxs-lookup"><span data-stu-id="cbdf0-108">Holidays and closures</span></span>
- <span data-ttu-id="cbdf0-109">Nepracovní doba</span><span class="sxs-lookup"><span data-stu-id="cbdf0-109">Non-work time</span></span>

<span data-ttu-id="cbdf0-110">Při nastavování kalendáře pracovní doby můžete přidat poslední dvě položky.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="cbdf0-111">Lze je také konfigurovat nebo aktualizovat samostatně.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="cbdf0-112">Nastavení kalendáře pracovní doby</span><span class="sxs-lookup"><span data-stu-id="cbdf0-112">Set up a working time calendar</span></span>

<span data-ttu-id="cbdf0-113">Nastavte nejméně jeden kalendář pracovní doby, který zobrazuje dny a hodiny operace.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="cbdf0-114">Pokud používáte umístění ve více zemích a oblastech, můžete pro každou oblast nastavit kalendář pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="cbdf0-115">Na stránce **Správa organizace** klikněte na **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="cbdf0-116">Zvolte **Nová** a zadejte název a popis nové skupiny pro kalendář.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="cbdf0-117">V části **Možnosti generování** vyberte pracovní dny pro organizaci a zadejte pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="cbdf0-118">Chcete-li přidat svátek nebo uzavírku, vyberte tlačítko **Přidat** vedle **Svátky a uzávěrky**.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="cbdf0-119">Chcete-li přidat nepracovní čas, například obědy nebo přestávky, vyberte **Přidat** v části **MIMOPRACOVNí DOBA** a zadejte název a časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="cbdf0-120">Na kartě **Dny** zvolte **Generovat** a vygenerujte dny ve svém kalendáři.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="cbdf0-121">Zadejte rozsah dat pro svůj kalendář a poté vyberte možnost **Generovat dny**.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="cbdf0-122">Chcete-li přidat pracovní plány, v části **Pracovní plán** vyberte **Přidat** a zadejte časy pro jednotlivé pracovní plány.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="cbdf0-123">Konfigurace svátků a uzavírek</span><span class="sxs-lookup"><span data-stu-id="cbdf0-123">Configure holidays and closures</span></span>

<span data-ttu-id="cbdf0-124">Svátky a uzávěrky lze přidávat a měnit odděleně od kalendáře pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="cbdf0-125">Na stránce **Správa organizace** klikněte na **Svátky a uzavírky**.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="cbdf0-126">Zvolte **Nová** a zadejte název a datum dovolené nebo uzavírky.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="cbdf0-127">Konfigurace mimopracovní doby</span><span class="sxs-lookup"><span data-stu-id="cbdf0-127">Configure non-work time</span></span>

<span data-ttu-id="cbdf0-128">Svátky a uzavírky lze přidávat nebo lze měnit mimopracovní dobu odděleně od kalendáře pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="cbdf0-129">Na stránce **Správa organizace** vyberte **Mimopracovní doba**.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="cbdf0-130">Vyberte **Nový** a zadejte název a časový rozsah mimopracovní doby.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="cbdf0-131">Pokud jste aktivovali funkci náhledu oprav pracovního volna a svátků, Aplikace Human Resources použije data svátků a dat uzavírky k určení počtu dní, které se mají upravit pro zaměstnance zapsané v kalendáři.</span><span class="sxs-lookup"><span data-stu-id="cbdf0-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbdf0-132">Viz také</span><span class="sxs-lookup"><span data-stu-id="cbdf0-132">See also</span></span>

- [<span data-ttu-id="cbdf0-133">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="cbdf0-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="cbdf0-134">Konfigurace typů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="cbdf0-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)

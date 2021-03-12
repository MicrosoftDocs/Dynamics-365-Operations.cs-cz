---
title: Konfigurace parametrů pracovního volna a absence
description: Definujte parametry lidských zdrojů pro pracovní volno a absenci v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997094"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="c58ac-103">Konfigurace parametrů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="c58ac-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="c58ac-104">Před nastavením plánů pracovního volna a absencí v Dynamics 365 Human Resourcesje vhodné ověřit nastavení všech souvisejících parametrů lidských zdrojů, včetně následujících:</span><span class="sxs-lookup"><span data-stu-id="c58ac-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="c58ac-105">Číselná řada pro požadavky na pracovní volno</span><span class="sxs-lookup"><span data-stu-id="c58ac-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="c58ac-106">Nastavení zákona Opuštění z rodinných a lékařských důvodu (FMLA)</span><span class="sxs-lookup"><span data-stu-id="c58ac-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="c58ac-107">Nastavení samoobslužných služeb pro zaměstnance pro požadavky na pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="c58ac-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="c58ac-108">Parametry pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="c58ac-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="c58ac-109">Zobrazení a změna parametrů lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="c58ac-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="c58ac-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c58ac-111">V části **Nastavení** vyberte **parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c58ac-112">Na kartě **číselné řady** ověřte **kód číselné řady** pro **ID žádosti o pracovní volno** a podle potřeby jej změňte.</span><span class="sxs-lookup"><span data-stu-id="c58ac-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="c58ac-113">Toto nastavení určuje pořadí používané pro automatické přiřazování ID k žádostem o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="c58ac-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="c58ac-114">Na kartě **FMLA** ověřte nastavení FMLA a podle potřeby je změňte.</span><span class="sxs-lookup"><span data-stu-id="c58ac-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="c58ac-115">Na kartě **Samoobsluha zaměstnance** určete, zda manažeři mohou zadat žádosti o pracovní volno a absenci jménem svých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="c58ac-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="c58ac-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="c58ac-117">Zobrazení pracovního volna a absencí napříč společnostmi je aktuálně ve verzi Preview.</span><span class="sxs-lookup"><span data-stu-id="c58ac-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="c58ac-118">Tuto funkci budete muset povolit v prostředí **Sandbox**, aby se vám zobrazila možnost pracovního volna a absencí.</span><span class="sxs-lookup"><span data-stu-id="c58ac-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="c58ac-119">Další informace o povolení funkcí verze Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="c58ac-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="c58ac-120">Zobrazení a změna sdílených parametrů Human Resources</span><span class="sxs-lookup"><span data-stu-id="c58ac-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="c58ac-121">Na stránce **Správa zaměstnanců** vyberte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c58ac-122">V části **Nastavení** vyberte **Sdílené parametry Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="c58ac-123">Na kartě **Rozšířený přístup** vyberte **Ano** pro **Povolit zobrazení pracovního volna mezi společnostmi**, abyste umožnili prohlížet pracovní volno napříč společností.</span><span class="sxs-lookup"><span data-stu-id="c58ac-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="c58ac-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="c58ac-125">Zobrazen a zmena parametrů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="c58ac-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="c58ac-126">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c58ac-127">V části **Nastavení** vyberte **Parametry pracovního volna a absence**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="c58ac-128">Na kartě **Obecné** natavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="c58ac-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="c58ac-129">Nastavte **Jednotku pro pracovní vono a absenci** na hodiny nebo dny.</span><span class="sxs-lookup"><span data-stu-id="c58ac-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="c58ac-130">Pokud se jedná o dny, můžete výběrem možnosti **Povolit definici poloviny dne** umožnit zaměstnancům výběr první nebo druhé poloviny dne ve svých žádostech o volno.</span><span class="sxs-lookup"><span data-stu-id="c58ac-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="c58ac-131">Vyberte **Datum platnost měsíců služby**, pokud chcete nastavit, kdy se časové rozlišení uplatní pro plány volna za použití měsíců služby.</span><span class="sxs-lookup"><span data-stu-id="c58ac-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="c58ac-132">Vyberte **Výpočet zůstatku**, chcete-li zobrazit zůstatky k dnešnímu dni nebo k období časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="c58ac-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="c58ac-133">Vyberete-li **Zůstatek k dnešnímu dni**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k dnešnímu dni.</span><span class="sxs-lookup"><span data-stu-id="c58ac-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="c58ac-134">Pokud vyberete možnost **Zůstatek k období časového rozlišení**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k období časového rozlišení, které je definováno frekvencí plánu volna.</span><span class="sxs-lookup"><span data-stu-id="c58ac-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="c58ac-135">Nastavte čas zahájení dávkové úlohy vypršení platnosti převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="c58ac-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="c58ac-136">Vyberte **Ano** pro **Umožnit zaměstnancům koupi pracovního volna** a **Umožnit zaměstnancům prodej pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="c58ac-137">Pokud vyberete **Ano** pro tyto možnosti, můžete vytvořit zásady koupi a prodeje pracovního volna a umožnit zaměstnancům odesílat žádosti o koupi a prodej pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="c58ac-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="c58ac-138">Konfigurace parametrů kalendáře</span><span class="sxs-lookup"><span data-stu-id="c58ac-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="c58ac-139">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c58ac-140">V části **Nastavení** vyberte **Parametry pracovního volna a absence**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="c58ac-141">Na kartě **Kalendář** podle potřeby ověřte nastavení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="c58ac-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="c58ac-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c58ac-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c58ac-143">Viz také</span><span class="sxs-lookup"><span data-stu-id="c58ac-143">See also</span></span>

- [<span data-ttu-id="c58ac-144">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="c58ac-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)

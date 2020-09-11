---
title: Konfigurace parametrů pracovního volna a absence
description: Definujte parametry lidských zdrojů pro pracovní volno a absenci v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712369"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="59963-103">Konfigurace parametrů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="59963-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="59963-104">Před nastavením plánů pracovního volna a absencí v Dynamics 365 Human Resourcesje vhodné ověřit nastavení všech souvisejících parametrů lidských zdrojů, včetně následujících:</span><span class="sxs-lookup"><span data-stu-id="59963-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="59963-105">Číselná řada pro požadavky na pracovní volno</span><span class="sxs-lookup"><span data-stu-id="59963-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="59963-106">Nastavení zákona Opuštění z rodinných a lékařských důvodu (FMLA)</span><span class="sxs-lookup"><span data-stu-id="59963-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="59963-107">Nastavení samoobslužných služeb pro zaměstnance pro požadavky na pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="59963-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="59963-108">Parametry pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="59963-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="59963-109">Zobrazení a změna parametrů lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="59963-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="59963-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="59963-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="59963-111">V části **Nastavení** vyberte **parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="59963-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="59963-112">Na kartě **číselné řady** ověřte **kód číselné řady** pro **ID žádosti o pracovní volno** a podle potřeby jej změňte.</span><span class="sxs-lookup"><span data-stu-id="59963-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="59963-113">Toto nastavení určuje pořadí používané pro automatické přiřazování ID k žádostem o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="59963-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="59963-114">Na kartě **FMLA** ověřte nastavení FMLA a podle potřeby je změňte.</span><span class="sxs-lookup"><span data-stu-id="59963-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="59963-115">Na kartě **Samoobsluha zaměstnance** určete, zda manažeři mohou zadat žádosti o pracovní volno a absenci jménem svých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="59963-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="59963-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="59963-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="59963-117">Zobrazen a zmena parametrů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="59963-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="59963-118">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="59963-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="59963-119">V části **Nastavení** vyberte **Parametry pracovního volna a absence**.</span><span class="sxs-lookup"><span data-stu-id="59963-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="59963-120">Na kartě **Obecné** natavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="59963-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="59963-121">Nastavte **Jednotku pro pracovní vono a absenci** na hodiny nebo dny.</span><span class="sxs-lookup"><span data-stu-id="59963-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="59963-122">Pokud se jedná o dny, můžete výběrem možnosti **Povolit definici poloviny dne** umožnit zaměstnancům výběr první nebo druhé poloviny dne ve svých žádostech o volno.</span><span class="sxs-lookup"><span data-stu-id="59963-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="59963-123">Vyberte **Datum platnost měsíců služby**, pokud chcete nastavit, kdy se časové rozlišení uplatní pro plány volna za použití měsíců služby.</span><span class="sxs-lookup"><span data-stu-id="59963-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="59963-124">Vyberte **Výpočet zůstatku**, chcete-li zobrazit zůstatky k dnešnímu dni nebo k období časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="59963-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="59963-125">Vyberete-li **Zůstatek k dnešnímu dni**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k dnešnímu dni.</span><span class="sxs-lookup"><span data-stu-id="59963-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="59963-126">Pokud vyberete možnost **Zůstatek k období časového rozlišení**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k období časového rozlišení, které je definováno frekvencí plánu volna.</span><span class="sxs-lookup"><span data-stu-id="59963-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="59963-127">Nastavte čas zahájení dávkové úlohy vypršení platnosti převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="59963-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="59963-128">Vyberte **Ano** pro **Umožnit zaměstnancům koupi pracovního volna** a **Umožnit zaměstnancům prodej pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="59963-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="59963-129">Pokud vyberete **Ano** pro tyto možnosti, můžete vytvořit zásady koupi a prodeje pracovního volna a umožnit zaměstnancům odesílat žádosti o koupi a prodej pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="59963-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="59963-130">Konfigurace parametrů kalendáře</span><span class="sxs-lookup"><span data-stu-id="59963-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="59963-131">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="59963-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="59963-132">V části **Nastavení** vyberte **Parametry pracovního volna a absence**.</span><span class="sxs-lookup"><span data-stu-id="59963-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="59963-133">Na kartě **Kalendář** podle potřeby ověřte nastavení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="59963-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="59963-134">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="59963-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="59963-135">Viz také</span><span class="sxs-lookup"><span data-stu-id="59963-135">See also</span></span>

- [<span data-ttu-id="59963-136">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="59963-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)

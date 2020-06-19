---
title: Správa zásad nákupu a prodeje pracovního volna
description: Zaměstnancům můžete povolit, aby kupovali a prodávali pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429006"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="2d251-103">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="2d251-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2d251-104">Zaměstnancům můžete povolit koupi volna vytvořením zásad nákupu volna.</span><span class="sxs-lookup"><span data-stu-id="2d251-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="2d251-105">Povolit zaměstnancům, aby kupovali a prodávali pracovní volno</span><span class="sxs-lookup"><span data-stu-id="2d251-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="2d251-106">Na stránce **Parametry volna a nepřítomnosti** vyberte **Ano** pro **Umožněte zaměstnancům koupit pracovní volno**.</span><span class="sxs-lookup"><span data-stu-id="2d251-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="2d251-107">Vytvoření zásad nákupu volna</span><span class="sxs-lookup"><span data-stu-id="2d251-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="2d251-108">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="2d251-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="2d251-109">Vyberte **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="2d251-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="2d251-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="2d251-110">Select **New**.</span></span>

4. <span data-ttu-id="2d251-111">Vložte **Název** a **Popis** pro zásady v **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="2d251-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="2d251-112">Vyberte **Typ zásad**.</span><span class="sxs-lookup"><span data-stu-id="2d251-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="2d251-113">Dostupné typy zásad jsou **Množství** a **Hodiny za týden**.</span><span class="sxs-lookup"><span data-stu-id="2d251-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="2d251-114">Vyberte **Množství** pro zadání **Pevné částky** pro maximální částky, které mohou zaměstnanci koupit a prodat.</span><span class="sxs-lookup"><span data-stu-id="2d251-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="2d251-115">Pokud vyberete **Hodiny za týden**, k určení maximálního množství zásad použije pracovní doba definovaná v kalendáři přiřazené pracovní doby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="2d251-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="2d251-116">Vyberte **počáteční datum** a **koncové datum** pro zásady.</span><span class="sxs-lookup"><span data-stu-id="2d251-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="2d251-117">Žádosti o koupi nebo prodej vona budou k dispozici pouze v tomto časovém rámci.</span><span class="sxs-lookup"><span data-stu-id="2d251-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="2d251-118">V **Zásadách nákupu** vyberte **Ekvivalent plného úvazku** (FTE) k rozdělení maximální částky na základě FTE definovaného na pozici zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="2d251-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="2d251-119">Pokud je typ zásad **Množství**, vložte **Maximální pevné množství**.</span><span class="sxs-lookup"><span data-stu-id="2d251-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="2d251-120">Vyberte **Přidat**, chcete-li přidat typy pracovního volna pro zaměstnance, aby si mohli koupit volno.</span><span class="sxs-lookup"><span data-stu-id="2d251-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="2d251-121">Do zásad můžete přidat více typů volna.</span><span class="sxs-lookup"><span data-stu-id="2d251-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="2d251-122">Zadejte **Měsíce služby** pro typ volna, chcete-li povolit různé měsíce služby pro určení maximálního množství, které může zaměstnanec koupit.</span><span class="sxs-lookup"><span data-stu-id="2d251-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="2d251-123">Zadejte **maximální množství** pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="2d251-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="2d251-124">Zadejte **Sazbu**, za kterou si zaměnstnanec koupí pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="2d251-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="2d251-125">Volitelně zadejte **Kód příjmů** pro použití při nákupu volna.</span><span class="sxs-lookup"><span data-stu-id="2d251-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="2d251-126">Volitelně lze nastavit, zda použít FTE ke stanovení maximálního množství pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="2d251-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="2d251-127">Přidejte do plánu volna a nepřítomnosti zásady nákupu a prodeje volna</span><span class="sxs-lookup"><span data-stu-id="2d251-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="2d251-128">Na stránce **Pracovní volno a nepřítomnost** vyberte plán volna a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="2d251-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="2d251-129">V **Pravidlech** vyberte **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="2d251-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d251-130">Viz také</span><span class="sxs-lookup"><span data-stu-id="2d251-130">See also</span></span>

[<span data-ttu-id="2d251-131">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="2d251-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="2d251-132">Konfigurace typů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="2d251-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="2d251-133">Časově rozlišit plány pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="2d251-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="2d251-134">Koupit a prodat pracovní volno</span><span class="sxs-lookup"><span data-stu-id="2d251-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)


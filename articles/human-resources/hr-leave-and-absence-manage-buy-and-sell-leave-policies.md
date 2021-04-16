---
title: Správa zásad nákupu a prodeje pracovního volna
description: Zaměstnancům můžete povolit, aby kupovali a prodávali pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f03d6055c407b2c3e13831c8b5a6f8b0d6c47897
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794702"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="554ae-103">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="554ae-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="554ae-104">Zaměstnancům můžete povolit koupi a prodej pracovního volna vytvořením zásad nákupu a prodeje pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="554ae-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="554ae-105">Tyto zásady můžete nakonfigurovat tak, aby používaly pracovní postup pro schvalování, nastavení maximálních částek a sazeb a nastavení sazeb pro nákup a prodej.</span><span class="sxs-lookup"><span data-stu-id="554ae-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="554ae-106">Povolit zaměstnancům, aby kupovali a prodávali pracovní volno</span><span class="sxs-lookup"><span data-stu-id="554ae-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="554ae-107">Na stránce **Parametry volna a absence** vyberte **Ano** pro **Umožnit zaměstnancům koupi pracovního volna** a **Umožnit zaměstnancům prodej pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="554ae-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="554ae-108">Vytvoření zásady nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="554ae-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="554ae-109">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="554ae-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="554ae-110">Vyberte **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="554ae-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="554ae-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="554ae-111">Select **New**.</span></span>

4. <span data-ttu-id="554ae-112">Vložte **Název** a **Popis** pro zásady v **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="554ae-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="554ae-113">Vyberte **Typ zásad**.</span><span class="sxs-lookup"><span data-stu-id="554ae-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="554ae-114">Dostupné typy zásad jsou **Množství** a **Hodiny za týden**.</span><span class="sxs-lookup"><span data-stu-id="554ae-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="554ae-115">Vyberte **Množství** pro zadání **Pevné částky** pro maximální částky, které mohou zaměstnanci koupit a prodat.</span><span class="sxs-lookup"><span data-stu-id="554ae-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="554ae-116">Pokud vyberete **Hodiny za týden**, k určení maximálního množství zásad použije pracovní doba definovaná v kalendáři přiřazené pracovní doby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="554ae-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="554ae-117">Vyberte **počáteční datum** a **koncové datum** pro zásady.</span><span class="sxs-lookup"><span data-stu-id="554ae-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="554ae-118">Žádosti o koupi nebo prodej vona budou k dispozici pouze v tomto časovém rámci.</span><span class="sxs-lookup"><span data-stu-id="554ae-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="554ae-119">Vyberte **ID pracovního postupu** pro zásadu.</span><span class="sxs-lookup"><span data-stu-id="554ae-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="554ae-120">Veškeré požadavky na nákup a prodej použijí tento pracovní postup ke kontrole a schválení.</span><span class="sxs-lookup"><span data-stu-id="554ae-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="554ae-121">V **Zásadách nákupu** vyberte **Ekvivalent plného úvazku** (FTE) k rozdělení maximální částky na základě FTE definovaného na pozici zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="554ae-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="554ae-122">Pokud je typ zásad **Množství**, vložte **Maximální pevné množství**.</span><span class="sxs-lookup"><span data-stu-id="554ae-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="554ae-123">Vyberte **Přidat**, chcete-li přidat typy pracovního volna pro zaměstnance, aby si mohli koupit volno.</span><span class="sxs-lookup"><span data-stu-id="554ae-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="554ae-124">Do zásad můžete přidat více typů volna.</span><span class="sxs-lookup"><span data-stu-id="554ae-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="554ae-125">Zadejte **Měsíce služby** pro typ volna, chcete-li povolit různé měsíce služby pro určení maximálního množství, které může zaměstnanec koupit.</span><span class="sxs-lookup"><span data-stu-id="554ae-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="554ae-126">Zadejte **maximální množství** pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="554ae-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="554ae-127">Zadejte **Sazbu**, za kterou si zaměnstnanec koupí pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="554ae-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="554ae-128">Volitelně zadejte **Kód příjmů** pro použití při nákupu volna.</span><span class="sxs-lookup"><span data-stu-id="554ae-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="554ae-129">Volitelně lze nastavit, zda použít FTE ke stanovení maximálního množství pro typ volna.</span><span class="sxs-lookup"><span data-stu-id="554ae-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="554ae-130">Chcete-li vytvořit zásadu prodeje, postupujte podle kroků 8 až 14 pod částí **Zásada prodeje**.</span><span class="sxs-lookup"><span data-stu-id="554ae-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="554ae-131">Přidejte do plánu volna a nepřítomnosti zásady nákupu a prodeje volna</span><span class="sxs-lookup"><span data-stu-id="554ae-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="554ae-132">Na stránce **Pracovní volno a nepřítomnost** vyberte plán volna a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="554ae-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="554ae-133">V **Pravidlech** vyberte **Zásady nákupu a prodeje pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="554ae-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="554ae-134">Viz také</span><span class="sxs-lookup"><span data-stu-id="554ae-134">See also</span></span>

[<span data-ttu-id="554ae-135">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="554ae-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="554ae-136">Konfigurace typů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="554ae-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="554ae-137">Časově rozlišit plány pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="554ae-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="554ae-138">Koupit a prodat pracovní volno</span><span class="sxs-lookup"><span data-stu-id="554ae-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Vytvoření šablony zaškolení pomocí aplikace Dynamics 365 Talent - Onboard
description: Toto téma vysvětluje, jak pomocí aplikace Microsoft Dynamics 365 Talent - Onboard vytvořit šablonu průvodce zaškolením pro nové zaměstnance. Tento úkol je zásadním prvním krokem strategie pro nakládání s lidským kapitálem (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 63f13380f3d2c31c4cc9009142f320ad8a41e8ee
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009870"
---
# <a name="create-an-onboarding-template"></a><span data-ttu-id="15bbe-104">Vytvoření šablony zaškolení</span><span class="sxs-lookup"><span data-stu-id="15bbe-104">Create an onboarding template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15bbe-105">Microsoft Dynamics 365 Talent: Onboard poskytuje různé šablony, které vám mohou pomoci při co nejrychlejší tvorbě průvodce.</span><span class="sxs-lookup"><span data-stu-id="15bbe-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="15bbe-106">Můžete použít jednu nebo více těchto šablon, nebo můžete vytvořit vlastní šablony.</span><span class="sxs-lookup"><span data-stu-id="15bbe-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="15bbe-107">Onboard poskytuje vzorový text, který lze použít při vytváření vlastních šablon.</span><span class="sxs-lookup"><span data-stu-id="15bbe-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="15bbe-108">Tento postup je tedy jednoduchý, i když začnete úplně od začátku.</span><span class="sxs-lookup"><span data-stu-id="15bbe-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="15bbe-109">Vytvoření šablony zaškolení z existující šablony</span><span class="sxs-lookup"><span data-stu-id="15bbe-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="15bbe-110">V levé nabídce vyberte možnost **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="15bbe-111">V části **Oblíbené šablony z galerie** nebo **Moje šablony** vyberte šablonu.</span><span class="sxs-lookup"><span data-stu-id="15bbe-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="15bbe-112">Chcete-li zobrazit více šablon, vyberte **Více v galerii šablon**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="15bbe-113">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="15bbe-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="15bbe-114">Pokud je šablona z galerie, vyberte možnost **Uložit jako mou šablonu**, zadejte nový název šablony a vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="15bbe-115">Pokud je šabona z okna **Moje šablony**, vyberte **Uložit jako šablonu**, zadejte název šablony a vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="15bbe-116">[![Vytvoření šablony z existující šablony](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="15bbe-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="15bbe-117">Vytvoření nové šablony zaškolení</span><span class="sxs-lookup"><span data-stu-id="15bbe-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="15bbe-118">V levé nabídce vyberte možnost **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="15bbe-119">V části **Moje šablony** vyberte dlaždici **Přidat** (znaménko \[**+**\]plus).</span><span class="sxs-lookup"><span data-stu-id="15bbe-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="15bbe-120">[![Vytvoření nové šablony](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="15bbe-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="15bbe-121">V dialogovém okně **Vytvoření šablony průvodce** zadejte název šablony a pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="15bbe-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="15bbe-122">Další kroky</span><span class="sxs-lookup"><span data-stu-id="15bbe-122">Next steps</span></span>

- [<span data-ttu-id="15bbe-123">Úprava průvodců a šablon zaškolení</span><span class="sxs-lookup"><span data-stu-id="15bbe-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="15bbe-124">Sdílení obsahu s jinými přispěvateli</span><span class="sxs-lookup"><span data-stu-id="15bbe-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="15bbe-125">Zobrazit stav úkolů a zaškolení zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="15bbe-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="15bbe-126">Vytvořit náborové týmy v Onboard</span><span class="sxs-lookup"><span data-stu-id="15bbe-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="15bbe-127">Viz také</span><span class="sxs-lookup"><span data-stu-id="15bbe-127">See also</span></span>

- [<span data-ttu-id="15bbe-128">Vyzkoušejte nebo kupte aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="15bbe-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="15bbe-129">Novinky</span><span class="sxs-lookup"><span data-stu-id="15bbe-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="15bbe-130">Poznámky k verzi</span><span class="sxs-lookup"><span data-stu-id="15bbe-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="15bbe-131">Získání podpory</span><span class="sxs-lookup"><span data-stu-id="15bbe-131">Get support</span></span>](./talent-support.md)

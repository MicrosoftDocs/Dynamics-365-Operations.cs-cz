---
title: "Předpoklady pro standardní náklady"
description: "V tomto tématu je popsán základní postup při použití standardních nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b1b0de596c1b40a4213128d5ed51066ee414681d
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="1f87f-103">Předpoklady pro standardní náklady</span><span class="sxs-lookup"><span data-stu-id="1f87f-103">Prerequisites for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f87f-104">V tomto tématu je popsán základní postup při použití standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="1f87f-105">Následné kroky závisí na operacích dané společnosti.</span><span class="sxs-lookup"><span data-stu-id="1f87f-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="1f87f-106">Kroky se například liší pro nevýrobní prostředí, výrobní prostředí bez postupů nebo výrobní prostředí s postupy.</span><span class="sxs-lookup"><span data-stu-id="1f87f-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="1f87f-107">Chcete-li nastavit standardní náklady, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="1f87f-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="1f87f-108">**1. Vytvořte skupinu modelů položek pro standardní náklady.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="1f87f-109">Použijte stránku **Skupiny modelů položek** pro vytvoření nové skupiny pro standardní náklady a přiřaďte model zásob **standardních nákladů**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="1f87f-110">Identifikátor pro skupinu modelů položek by měl být popisný, jako například **Std Nákl**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="1f87f-111">Zaškrtnutím příslušných políček určete, že pro danou skupinu má být povoleno použití záporného finančního skladu a zaúčtovány fyzické zásoby a finanční zásoby.</span><span class="sxs-lookup"><span data-stu-id="1f87f-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="1f87f-112">Tato skupina standardních nákladů bude přiřazena položkám.</span><span class="sxs-lookup"><span data-stu-id="1f87f-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="1f87f-113">**2. Definujte účty hlavní knihy, které odpovídají odchylkám standardních nákladů.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="1f87f-114">Prostřednictvím stránky **Účtová osnova** definujte účty hlavní knihy, které odpovídají odchylkám standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="1f87f-115">Tyto účty hlavní knihy musí být definovány před přiřazením na stránce **Zaúčtování**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="1f87f-116">Účty hlavní knihy mohou odrážet skupiny položek a skupiny nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="1f87f-117">**3. Přiřaďte účty hlavní knihy k zaúčtováním položek, které odpovídají odchylkám standardních nákladů.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="1f87f-118">Pomocí stránky **Zaúčtování** proveďte přiřazení účtů hlavní knihy, které odpovídají odchylkám standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="1f87f-119">Můžete určit, zda mají být účty hlavní knihy pro odchylky specifikovány podle položky (nebo skupiny položek) a podle nákladové skupiny (nebo typu nákladové skupiny), nebo můžete zadat, že účet hlavní knihy se vztahuje ke všem položkám a všem nákladovým skupinám.</span><span class="sxs-lookup"><span data-stu-id="1f87f-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="1f87f-120">Tyto volby odpovídají nákladovým vztahům pro tabulky, skupiny a všechny položky.</span><span class="sxs-lookup"><span data-stu-id="1f87f-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="1f87f-121">Před definováním pravidel zaúčtování položky povolte prostřednictvím stránky **Kombinace transakcí** použití nákladových vztahů (pro tabulky, skupiny a všechny položky).</span><span class="sxs-lookup"><span data-stu-id="1f87f-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="1f87f-122">**4. Definujte parametry zásob, které odpovídají standardním nákladům.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="1f87f-123">Použijte kartu **Kusovníky** na stránce **Parametry zásob** s cílem definovat dva parametry řízení nákladů, které odpovídají standardním nákladům.</span><span class="sxs-lookup"><span data-stu-id="1f87f-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="1f87f-124">V poli **Rozúčtování nákladů** vyberte možnost **Žádné** nebo **Dílčí hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="1f87f-125">Vyberete-li **Dílčí hlavní kniha**, rozúčtování nákladů je *aktivní* rozúčtování nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="1f87f-126">Aktivní rozúčtování nákladů je velmi důležité pro výpočet, zachování a zobrazení rozdělení nákladových skupin do segmentů napříč víceúrovňovou strukturou produktů pro standardní nákladové položky.</span><span class="sxs-lookup"><span data-stu-id="1f87f-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="1f87f-127">Je-li rozúčtování nákladů aktivní, můžete vykázat a analyzovat zásoby, nedokončenou výrobu (NV) a náklady na prodané zboží (COGS) pro jednotlivé nákladové skupiny ve formátu s jednou úrovní, s více úrovněmi nebo v souhrnném formátu.</span><span class="sxs-lookup"><span data-stu-id="1f87f-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="1f87f-128">Když je rozúčtování nákladů aktivní a aktivujete náklady na vyráběnou položku, segmentace nákladových skupin se uloží v záznamu nákladů položky.</span><span class="sxs-lookup"><span data-stu-id="1f87f-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="1f87f-129">Vyberete-li **Žádné**, segmentace nákladových skupin nebude pro standardní nákladové položky zachována.</span><span class="sxs-lookup"><span data-stu-id="1f87f-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="1f87f-130">Jinak řečeno, standardní náklady na vyráběnou položku budou vypočteny a spravovány jako jedna částka bez rozdělení nákladových skupin do segmentů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="1f87f-131">Nákladové příspěvky vyráběných součástí budou agregovány do jediné částky.</span><span class="sxs-lookup"><span data-stu-id="1f87f-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="1f87f-132">V poli **Odchylky od standardních hodnot** vyberte **Souhrn** nebo **Na nákladovou skupinu**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="1f87f-133">Volba **Na nákladovou skupinu** vám umožňuje identifikovat odchylky nákupní ceny a odchylky výroby podle nákladové skupiny.</span><span class="sxs-lookup"><span data-stu-id="1f87f-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="1f87f-134">Můžete také identifikovat čtyři typy výrobních odchylek: velikost šarže, množství, cena a odchylky náhrady.</span><span class="sxs-lookup"><span data-stu-id="1f87f-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="1f87f-135">Volba **Souhrn** znamená, že nelze identifikovat odchylky podle nákladové skupiny a že nelze identifikovat čtyři typy výrobních odchylek.</span><span class="sxs-lookup"><span data-stu-id="1f87f-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="1f87f-136">Můžete zobrazit pouze souhrnnou výrobní odchylku.</span><span class="sxs-lookup"><span data-stu-id="1f87f-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="1f87f-137">Zásady týkající se odchylek vzhledem ke standardním hodnotám pracují nezávisle na zásadách rozúčtování nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="1f87f-138">To znamená, že můžete vybrat zásadu pro rozúčtování nákladů **Žádná** a přitom vybrat odchylky podle nákladových skupin, takže budou stále zaznamenány výrobní odchylky podle nákladových skupin.</span><span class="sxs-lookup"><span data-stu-id="1f87f-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="1f87f-139">**5. Vytvořte nákladové verze pro standardní náklady.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="1f87f-140">Prostřednictvím stránky **Nastavení nákladové verze** vytvořte jednu nebo více nákladových verzí pro standardní náklady.</span><span class="sxs-lookup"><span data-stu-id="1f87f-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="1f87f-141">Každá nákladová verze musí být označena s použitím nákladového typu pro **Standardní náklady** a umožňovat, aby obsah zahrnoval data nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f87f-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="1f87f-142">**6. Připravte existujícího odběratele v aplikaci na použití standardních nákladů.**</span><span class="sxs-lookup"><span data-stu-id="1f87f-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="1f87f-143">Odběratelé, kteří chtějí změnit existující položky na skladový model standardních nákladů, musí použít stránku **Převody standardních nákladů**.</span><span class="sxs-lookup"><span data-stu-id="1f87f-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="1f87f-144">Související témata</span><span class="sxs-lookup"><span data-stu-id="1f87f-144">Related topics</span></span>
--------

[<span data-ttu-id="1f87f-145">Přehled převodu standardních nákladů</span><span class="sxs-lookup"><span data-stu-id="1f87f-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)



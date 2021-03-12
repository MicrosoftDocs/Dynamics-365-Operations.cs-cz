---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.6. (listopad 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983668"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="3acc8-103">Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.6. (listopad 2019)</span><span class="sxs-lookup"><span data-stu-id="3acc8-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3acc8-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="3acc8-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="3acc8-105">Tato verze má číslo sestavení 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="3acc8-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="3acc8-106">Zatímco datum všeobecné dostupnosti je v listopadu, nové funkce jsou k dispozici pro dřívější vydání v říjnu.</span><span class="sxs-lookup"><span data-stu-id="3acc8-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="3acc8-107">Další informace o verzi 10.0.6 viz [Další zdroje](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="3acc8-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="3acc8-108">Přehled modelů konfigurace datovou entitu V2</span><span class="sxs-lookup"><span data-stu-id="3acc8-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="3acc8-109">Druhá verze pro datovou entitu „modely konfigurace produktu“ je uvolněna (s názvem „modely konfigurace produktu V2“).</span><span class="sxs-lookup"><span data-stu-id="3acc8-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="3acc8-110">Výchozí šablona „418 – modely konfigurace produktu“ také musí používat novou datovou entitu „modely konfigurace produktu V2“ v šablonách platformy importu/exportu.</span><span class="sxs-lookup"><span data-stu-id="3acc8-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="3acc8-111">Šablona nebude automaticky aktualizována, takže bude nutné šablonu načíst z výchozího nastavení ručně.</span><span class="sxs-lookup"><span data-stu-id="3acc8-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="3acc8-112">Entita V2 exportuje jeden řádek jako samostatný soubor přílohy namísto vloženého a vyřeší omezení velikosti entity V1.</span><span class="sxs-lookup"><span data-stu-id="3acc8-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="3acc8-113">Jakým způsobem je nutné provést tuto změnu?</span><span class="sxs-lookup"><span data-stu-id="3acc8-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="3acc8-114">Protože se entita V1 již nepoužívá, měli byste zahájit migraci z V1 na v2.</span><span class="sxs-lookup"><span data-stu-id="3acc8-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="3acc8-115">Používáte-li šablonu „418 – modely konfigurace produktu“, můžete kliknout na tlačítko „načíst výchozí šablony“ a znovu načíst šablonu s „418 – modely konfigurace produktu“.</span><span class="sxs-lookup"><span data-stu-id="3acc8-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="3acc8-116">Potřebujete-li zachovat kompatibilitu s existujícími systémy, můžete nyní nadále používat stávající šablonu a (zastaralou) entitu V1, dokud nepřesunete integrace do nové šablony.</span><span class="sxs-lookup"><span data-stu-id="3acc8-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="3acc8-117">Vylepšení správy funkcí</span><span class="sxs-lookup"><span data-stu-id="3acc8-117">Feature management enhancements</span></span>
<span data-ttu-id="3acc8-118">Správa funkcí nyní umožňuje povolit všechny nové funkce ve výchozím nastavení, vyžadovat potvrzení povolení funkce a povolit všechny funkce, které dosud nebyly povoleny.</span><span class="sxs-lookup"><span data-stu-id="3acc8-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="3acc8-119">Odpovědná strana nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="3acc8-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="3acc8-120">Nyní máte možnost definovat primární a sekundární odpovědné osoby ve formuláři klasifikace nákupní smlouvy a výsledných nákupních smlouvách.</span><span class="sxs-lookup"><span data-stu-id="3acc8-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="3acc8-121">To poskytuje uživateli přístup k aplikaci, která tyto smlouvy dohlíží.</span><span class="sxs-lookup"><span data-stu-id="3acc8-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="3acc8-122">Odkaz na požadavek na nabídku na řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="3acc8-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="3acc8-123">Můžete přidat referenční odkaz z řádků nákupní objednávky zpět na odpovídající řádky požadavku na nabídku, odkud pocházejí, a jednoduše poskytnout uživateli podpůrnou žádost o dokument nabídky.</span><span class="sxs-lookup"><span data-stu-id="3acc8-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3acc8-124">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3acc8-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3acc8-125">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="3acc8-125">Bug fixes</span></span>
<span data-ttu-id="3acc8-126">Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.6, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="3acc8-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="3acc8-127">Platform update 30</span><span class="sxs-lookup"><span data-stu-id="3acc8-127">Platform update 30</span></span>
<span data-ttu-id="3acc8-128">Aplikace Microsoft Dynamics 365 Supply Chain Management 10.0.6 zahrnuje aktualizaci Platform Update 30.</span><span class="sxs-lookup"><span data-stu-id="3acc8-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="3acc8-129">Další informace o aktualizaci Platform Update 30 naleznete v tématu [Co je nového a co se změnilo v aktualizaci Platform Update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="3acc8-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="3acc8-130">Dynamics 365: plán 2. vlny vydání v r. 2019</span><span class="sxs-lookup"><span data-stu-id="3acc8-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="3acc8-131">Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?</span><span class="sxs-lookup"><span data-stu-id="3acc8-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="3acc8-132">Přečtěte si téma [Dynamics 365: plán 2. vlny vydání v r. 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="3acc8-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="3acc8-133">Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.</span><span class="sxs-lookup"><span data-stu-id="3acc8-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="3acc8-134">Odebrané a zastaralé funkce Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3acc8-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="3acc8-135">Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.</span><span class="sxs-lookup"><span data-stu-id="3acc8-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="3acc8-136">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="3acc8-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="3acc8-137">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="3acc8-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="3acc8-138">Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.</span><span class="sxs-lookup"><span data-stu-id="3acc8-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="3acc8-139">U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="3acc8-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="3acc8-140">Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.</span><span class="sxs-lookup"><span data-stu-id="3acc8-140">Typically, these are functional updates that need to be made to the compiler.</span></span>

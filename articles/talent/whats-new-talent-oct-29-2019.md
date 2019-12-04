---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (29. října 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773870"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="11a5d-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (29. října 2019)</span><span class="sxs-lookup"><span data-stu-id="11a5d-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11a5d-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="11a5d-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="11a5d-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="11a5d-105">Changes in Attract</span></span>

<span data-ttu-id="11a5d-106">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="11a5d-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="11a5d-107">Změny v aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="11a5d-107">Changes in Onboard</span></span>

<span data-ttu-id="11a5d-108">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="11a5d-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="11a5d-109">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="11a5d-109">Changes in Core HR</span></span>

<span data-ttu-id="11a5d-110">Změny popsané v této části se vztahují na číslo sestavení 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="11a5d-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="11a5d-111">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="11a5d-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="11a5d-112">Odstranění stran bez rolí by mělo být ve výchozím nastavení zapnuté (371233)</span><span class="sxs-lookup"><span data-stu-id="11a5d-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="11a5d-113">Když zřizujete nové prostředí v aplikaci Talent, je volba **Odstranit strany, pokud neexistují role** ve výchozím nastavení zapnutá.</span><span class="sxs-lookup"><span data-stu-id="11a5d-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="11a5d-114">Když odstraníte pracovníka, nebude strana přidružená k pracovníkovi odebrána, pokud není zapnuto toto nastavení.</span><span class="sxs-lookup"><span data-stu-id="11a5d-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="11a5d-115">Tato změna omezuje duplicitní záznamy v globálním adresáři, pokud potřebujete importovat, změnit nebo znovu naimportovat pracovníky.</span><span class="sxs-lookup"><span data-stu-id="11a5d-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="11a5d-116">Mělo by být povoleno odstranění rozpracovaných a zrušených žádostí o dovolenou v Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="11a5d-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="11a5d-117">S touto změnou můžete nyní odstranit žádosti o dovolenou ve stavu **Koncept** nebo **Zrušeno** v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="11a5d-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="11a5d-118">Další hodnoty seznamu ve vlastních polích se neodrazí v Common Data Service po kliknutí na tlačítko Použít ve formuláři vlastních polí (379599)</span><span class="sxs-lookup"><span data-stu-id="11a5d-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="11a5d-119">Přidáte-li nové hodnoty seznamu do existujícího vlastního pole, které již bylo synchronizováno s aplikací Common Data Service, budou nyní k dispozici ve aplikaci Common Data Service po použití změn ve formuláři **Vlastní pole**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="11a5d-120">Použít kontrolní seznamy při zprovoznění mezi právnickými osobami, když existuje více zaměstnání (371270)</span><span class="sxs-lookup"><span data-stu-id="11a5d-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="11a5d-121">Ve vydání z tohoto týdne můžete použít kontrolní seznamy pro zaměstnance s více než jedním zaměstnáním ve formuláři **Pracovník > kontrolní seznamy**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="11a5d-122">Byla odebrána funkce náhledu zahrnutí otevřených výhod</span><span class="sxs-lookup"><span data-stu-id="11a5d-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="11a5d-123">V souladu s naším oznámením v příspěvku v blogu Strategické investice v [Core HR řídí provozní dokonalost](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) odebrala společnost Microsoft funkci registrace otevření výhod z veřejného náhledu.</span><span class="sxs-lookup"><span data-stu-id="11a5d-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="11a5d-124">Místo toho bude v budoucnu vydána nová funkce.</span><span class="sxs-lookup"><span data-stu-id="11a5d-124">New functionality will be released in the future.</span></span> <span data-ttu-id="11a5d-125">Výrobní použití funkce zahrnutí otevřených výhod není podporována.</span><span class="sxs-lookup"><span data-stu-id="11a5d-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="11a5d-126">Již brzy</span><span class="sxs-lookup"><span data-stu-id="11a5d-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="11a5d-127">Tisk kontrol výkonnosti</span><span class="sxs-lookup"><span data-stu-id="11a5d-127">Print performance reviews</span></span>

<span data-ttu-id="11a5d-128">Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.</span><span class="sxs-lookup"><span data-stu-id="11a5d-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="11a5d-129">Pracovní prostor Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="11a5d-129">Feature management workspace</span></span>

<span data-ttu-id="11a5d-130">Funkce se přidávají a aktualizují v každém vydání.</span><span class="sxs-lookup"><span data-stu-id="11a5d-130">Features are added and updated in every release.</span></span> <span data-ttu-id="11a5d-131">Funkce Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních.</span><span class="sxs-lookup"><span data-stu-id="11a5d-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="11a5d-132">Ve výchozím nastavení jsou nové funkce vypnuté.</span><span class="sxs-lookup"><span data-stu-id="11a5d-132">By default, new features are turned off.</span></span> <span data-ttu-id="11a5d-133">Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.</span><span class="sxs-lookup"><span data-stu-id="11a5d-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="11a5d-134">Další informace o změnách přicházejících ve správě funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="11a5d-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

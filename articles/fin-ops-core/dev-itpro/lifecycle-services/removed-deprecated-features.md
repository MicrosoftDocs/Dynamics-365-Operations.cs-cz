---
title: Odstraněné nebo zastaralé funkce v Lifecycle Services (LCS)
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstraněníz Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e571cc26f55e0bd7a1eef301e193921e0b3f8e31
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454688"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="7059a-103">Odstraněné nebo zastaralé funkce v Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="7059a-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7059a-104">Toto téma popisuje funkce, které byly odebrány nebo jsou zastaralé pro aplikaci Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7059a-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="7059a-105">*Odstraněná* funkce již není k dispozici ve službě.</span><span class="sxs-lookup"><span data-stu-id="7059a-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="7059a-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="7059a-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="7059a-107">Tento seznam je poskytnut, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="7059a-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="7059a-108">Oznámení z října 2019</span><span class="sxs-lookup"><span data-stu-id="7059a-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="7059a-109">Vývojové diagramy v modelování podnikových procesů</span><span class="sxs-lookup"><span data-stu-id="7059a-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="7059a-110"><strong>Důvod pro zrušení/odstranění</strong></span><span class="sxs-lookup"><span data-stu-id="7059a-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="7059a-111">V aplikaci modelování podnikových procesů (BPM) zastaráváme komponentu vývojových diagramů, protože původní návrh způsobil nízké využití.</span><span class="sxs-lookup"><span data-stu-id="7059a-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7059a-112"><strong>Nahrazeno jinou funkcí?</strong></span><span class="sxs-lookup"><span data-stu-id="7059a-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="7059a-113">Ne</span><span class="sxs-lookup"><span data-stu-id="7059a-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7059a-114"><strong>Ovlivněné oblasti</strong></span><span class="sxs-lookup"><span data-stu-id="7059a-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="7059a-115">Modelování podnikových procesů</span><span class="sxs-lookup"><span data-stu-id="7059a-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7059a-116"><strong>Stav</strong></span><span class="sxs-lookup"><span data-stu-id="7059a-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="7059a-117">Zastaralé: očekává se, že součást vývojových diagramů v BPM bude odstraněna během roku 2020.</span><span class="sxs-lookup"><span data-stu-id="7059a-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="7059a-118">Tyto funkce nebudou dostupné:</span><span class="sxs-lookup"><span data-stu-id="7059a-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="7059a-119">Všechny vývojové diagramy budou pouze pro čtení a nebudou k dispozici pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="7059a-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="7059a-120">Rovněž nebudou k dispozici vlastnosti tvaru, které jsou spojeny s činnostmi vývojového diagramu.</span><span class="sxs-lookup"><span data-stu-id="7059a-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="7059a-121">Tyto vývojové diagramy zahrnují jak výchozí vývojové diagramy, které jsou automaticky generovány, a přizpůsobené vývojové diagramy, které jsou upraveny na základě těchto výchozích vývojových diagramů.</span><span class="sxs-lookup"><span data-stu-id="7059a-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="7059a-122">Kroky procesu budou pouze pro čtení a nebudou k dispozici pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="7059a-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="7059a-123">Tato funkce analýzy přizpůsobení a mezer nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7059a-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="7059a-124">Proto nebude automaticky vytvořen nebo k dispozici pro export žádný seznam mezer.</span><span class="sxs-lookup"><span data-stu-id="7059a-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="7059a-125"><strong>Poznámka:</strong> Tato funkce byla dříve zastaralá a nahrazena integracemi Microsoft Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="7059a-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="7059a-126">Historie verzí vývojového diagramu nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7059a-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

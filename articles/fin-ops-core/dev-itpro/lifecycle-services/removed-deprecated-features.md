---
title: Odstraněné nebo zastaralé funkce v Lifecycle Services (LCS)
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstraněníz Microsoft Dynamics Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885448"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="a0e54-103">Odstraněné nebo zastaralé funkce v Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a0e54-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a0e54-104">Toto téma popisuje funkce, které byly odebrány nebo jsou zastaralé pro aplikaci Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a0e54-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="a0e54-105">*Odstraněná* funkce již není k dispozici ve službě.</span><span class="sxs-lookup"><span data-stu-id="a0e54-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="a0e54-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="a0e54-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="a0e54-107">Tento seznam je poskytnut, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="a0e54-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="a0e54-108">Oznámení z října 2019</span><span class="sxs-lookup"><span data-stu-id="a0e54-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="a0e54-109">Vývojové diagramy v modelování podnikových procesů</span><span class="sxs-lookup"><span data-stu-id="a0e54-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="a0e54-110"><strong>Důvod pro zrušení/odstranění</strong></span><span class="sxs-lookup"><span data-stu-id="a0e54-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="a0e54-111">V aplikaci modelování podnikových procesů (BPM) zastaráváme komponentu vývojových diagramů, protože původní návrh způsobil nízké využití.</span><span class="sxs-lookup"><span data-stu-id="a0e54-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0e54-112"><strong>Nahrazeno jinou funkcí?</strong></span><span class="sxs-lookup"><span data-stu-id="a0e54-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="a0e54-113">Ne</span><span class="sxs-lookup"><span data-stu-id="a0e54-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0e54-114"><strong>Ovlivněné oblasti</strong></span><span class="sxs-lookup"><span data-stu-id="a0e54-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="a0e54-115">Modelování podnikových procesů</span><span class="sxs-lookup"><span data-stu-id="a0e54-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0e54-116"><strong>Stav</strong></span><span class="sxs-lookup"><span data-stu-id="a0e54-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="a0e54-117">Zastaralé: očekává se, že součást vývojových diagramů v BPM bude odstraněna počátkem února 2020.</span><span class="sxs-lookup"><span data-stu-id="a0e54-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="a0e54-118">Dojde k odebrání těchto funkcí:</span><span class="sxs-lookup"><span data-stu-id="a0e54-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="a0e54-119">Existující vývojové diagramy nebudou k dispozici pro zobrazení nebo úpravy.</span><span class="sxs-lookup"><span data-stu-id="a0e54-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="a0e54-120">Vlastnosti obrazce, které jsou přidruženy k aktivitám vývojového diagramu, nebudou také k dispozici, protože bude odebrána celá karta <strong>vývojového diagramu</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0e54-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="a0e54-121">Tyto vývojové diagramy zahrnují jak výchozí vývojové diagramy, které jsou automaticky generovány, a přizpůsobené vývojové diagramy, které jsou upraveny na základě těchto výchozích vývojových diagramů.</span><span class="sxs-lookup"><span data-stu-id="a0e54-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="a0e54-122">Tato funkce analýzy přizpůsobení a mezer nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a0e54-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="a0e54-123">Proto nebude automaticky vytvořen nebo k dispozici pro export žádný seznam mezer.</span><span class="sxs-lookup"><span data-stu-id="a0e54-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="a0e54-124"><strong>Poznámka:</strong> Tato funkce byla dříve zastaralá a nahrazena integracemi Microsoft Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a0e54-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="a0e54-125">Historie verzí vývojového diagramu nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a0e54-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (8. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897327"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="c0283-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (8. října 2018)</span><span class="sxs-lookup"><span data-stu-id="c0283-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

<span data-ttu-id="c0283-104">**Sestavení 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="c0283-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="c0283-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="c0283-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="c0283-106">Povolení jiných dat, které mají být použity na základu úrovně pracovního volna (Správa pracovního volna)</span><span class="sxs-lookup"><span data-stu-id="c0283-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="c0283-107">Při udílení pracovního volna zaměstnancům určuje základ úrovně udělení, kolik času volna zaměstnance bude časově rozlišeno.</span><span class="sxs-lookup"><span data-stu-id="c0283-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="c0283-108">Tyto úrovně jsou v současné době založené na počátečním datu zaměstnance a služebním věku.</span><span class="sxs-lookup"><span data-stu-id="c0283-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="c0283-109">V některých případech organizace potřebují, aby tyto úrovně byly založeny na jiných datech, jako je například výročí či původní datum náboru.</span><span class="sxs-lookup"><span data-stu-id="c0283-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="c0283-110">Tato data se již používají v plánu volna pro určení toho, kdy dojde k časovému rozlišení. Byla přidána možnost těchto dat k použití při registraci zaměstnance do plánu, aby bylo možné určit množství časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="c0283-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="c0283-111">Další změny</span><span class="sxs-lookup"><span data-stu-id="c0283-111">Other changes</span></span>
<span data-ttu-id="c0283-112">V této verzi jsou obsaženy také různé opravy.</span><span class="sxs-lookup"><span data-stu-id="c0283-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c0283-113">Známý problém</span><span class="sxs-lookup"><span data-stu-id="c0283-113">Known issue</span></span>

<span data-ttu-id="c0283-114">**Problém:** Při přidání nové přílohy k pracovníkovi jsou zašedlá tlačítka **Nová** a **Upravit**. **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="c0283-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c0283-115">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="c0283-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c0283-116">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="c0283-116">(This issue will be fixed in the next platform update.)</span></span>

---
title: Konfigurace budoucích životních událostí
description: V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417587"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="b0a45-103">Konfigurace budoucích životních událostí</span><span class="sxs-lookup"><span data-stu-id="b0a45-103">Configure future life events</span></span>

<span data-ttu-id="b0a45-104">V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="b0a45-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="b0a45-105">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **budoucí životní události**.</span><span class="sxs-lookup"><span data-stu-id="b0a45-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="b0a45-106">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="b0a45-106">Select **New**.</span></span>

3. <span data-ttu-id="b0a45-107">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="b0a45-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b0a45-108">Pole</span><span class="sxs-lookup"><span data-stu-id="b0a45-108">Field</span></span> | <span data-ttu-id="b0a45-109">Popis</span><span class="sxs-lookup"><span data-stu-id="b0a45-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b0a45-110">Datum životní události</span><span class="sxs-lookup"><span data-stu-id="b0a45-110">Life event date</span></span> | <span data-ttu-id="b0a45-111">Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data.</span><span class="sxs-lookup"><span data-stu-id="b0a45-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="b0a45-112">Životní událost zaznamenána</span><span class="sxs-lookup"><span data-stu-id="b0a45-112">Life event logged</span></span> | <span data-ttu-id="b0a45-113">Datum a čas zaznamenání životní události.</span><span class="sxs-lookup"><span data-stu-id="b0a45-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="b0a45-114">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="b0a45-114">Log type</span></span> | <span data-ttu-id="b0a45-115">Zobrazí, zda je akce jedna z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="b0a45-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="b0a45-116">- **Aktualizovat** – Změna stávajícího záznamu, který sleduje životní události</span><span class="sxs-lookup"><span data-stu-id="b0a45-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="b0a45-117">- **Vložit** – vytvoření nového záznamu životní události</span><span class="sxs-lookup"><span data-stu-id="b0a45-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="b0a45-118">ID typu životních událostí</span><span class="sxs-lookup"><span data-stu-id="b0a45-118">Life event type ID</span></span> | <span data-ttu-id="b0a45-119">Jedinečný identifikátor typu životní události.</span><span class="sxs-lookup"><span data-stu-id="b0a45-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="b0a45-120">Typy životní události</span><span class="sxs-lookup"><span data-stu-id="b0a45-120">Life event type</span></span> | <span data-ttu-id="b0a45-121">Katalyzátor pro aktualizaci přihlášení zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="b0a45-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="b0a45-122">Další informace naleznete v části spouštěčů životní události.</span><span class="sxs-lookup"><span data-stu-id="b0a45-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="b0a45-123">Stav</span><span class="sxs-lookup"><span data-stu-id="b0a45-123">Status</span></span> | <span data-ttu-id="b0a45-124">Určení, zda byla životní událost zpracována nebo ne.</span><span class="sxs-lookup"><span data-stu-id="b0a45-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="b0a45-125">Řádek</span><span class="sxs-lookup"><span data-stu-id="b0a45-125">Line</span></span> | <span data-ttu-id="b0a45-126">Číslo řádku budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="b0a45-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="b0a45-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b0a45-127">Select **Save**.</span></span> 

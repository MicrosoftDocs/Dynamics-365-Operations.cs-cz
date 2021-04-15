---
title: Konfigurace budoucích životních událostí
description: V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e12a08fb36e7e2bea57dfe462edfef277875e30f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804954"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="4dcc8-103">Konfigurace budoucích životních událostí</span><span class="sxs-lookup"><span data-stu-id="4dcc8-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4dcc8-104">V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="4dcc8-105">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **budoucí životní události**.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="4dcc8-106">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-106">Select **New**.</span></span>

3. <span data-ttu-id="4dcc8-107">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="4dcc8-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4dcc8-108">Pole</span><span class="sxs-lookup"><span data-stu-id="4dcc8-108">Field</span></span> | <span data-ttu-id="4dcc8-109">Popis</span><span class="sxs-lookup"><span data-stu-id="4dcc8-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4dcc8-110">Datum životní události</span><span class="sxs-lookup"><span data-stu-id="4dcc8-110">Life event date</span></span> | <span data-ttu-id="4dcc8-111">Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="4dcc8-112">Životní událost zaznamenána</span><span class="sxs-lookup"><span data-stu-id="4dcc8-112">Life event logged</span></span> | <span data-ttu-id="4dcc8-113">Datum a čas zaznamenání životní události.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="4dcc8-114">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="4dcc8-114">Log type</span></span> | <span data-ttu-id="4dcc8-115">Zobrazí, zda je akce jedna z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="4dcc8-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="4dcc8-116">- **Aktualizovat** – Změna stávajícího záznamu, který sleduje životní události</span><span class="sxs-lookup"><span data-stu-id="4dcc8-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="4dcc8-117">- **Vložit** – vytvoření nového záznamu životní události</span><span class="sxs-lookup"><span data-stu-id="4dcc8-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="4dcc8-118">ID typu životních událostí</span><span class="sxs-lookup"><span data-stu-id="4dcc8-118">Life event type ID</span></span> | <span data-ttu-id="4dcc8-119">Jedinečný identifikátor typu životní události.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="4dcc8-120">Typy životní události</span><span class="sxs-lookup"><span data-stu-id="4dcc8-120">Life event type</span></span> | <span data-ttu-id="4dcc8-121">Katalyzátor pro aktualizaci přihlášení zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="4dcc8-122">Další informace naleznete v části spouštěčů životní události.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="4dcc8-123">Stav</span><span class="sxs-lookup"><span data-stu-id="4dcc8-123">Status</span></span> | <span data-ttu-id="4dcc8-124">Určení, zda byla životní událost zpracována nebo ne.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="4dcc8-125">Řádek</span><span class="sxs-lookup"><span data-stu-id="4dcc8-125">Line</span></span> | <span data-ttu-id="4dcc8-126">Číslo řádku budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="4dcc8-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4dcc8-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
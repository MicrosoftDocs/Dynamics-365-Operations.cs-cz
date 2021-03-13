---
title: Konfigurace budoucích životních událostí
description: V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111821"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="bd8bd-103">Konfigurace budoucích životních událostí</span><span class="sxs-lookup"><span data-stu-id="bd8bd-103">Configure future life events</span></span>

<span data-ttu-id="bd8bd-104">V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="bd8bd-105">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **budoucí životní události**.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="bd8bd-106">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-106">Select **New**.</span></span>

3. <span data-ttu-id="bd8bd-107">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="bd8bd-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bd8bd-108">Pole</span><span class="sxs-lookup"><span data-stu-id="bd8bd-108">Field</span></span> | <span data-ttu-id="bd8bd-109">Popis</span><span class="sxs-lookup"><span data-stu-id="bd8bd-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bd8bd-110">Datum životní události</span><span class="sxs-lookup"><span data-stu-id="bd8bd-110">Life event date</span></span> | <span data-ttu-id="bd8bd-111">Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="bd8bd-112">Životní událost zaznamenána</span><span class="sxs-lookup"><span data-stu-id="bd8bd-112">Life event logged</span></span> | <span data-ttu-id="bd8bd-113">Datum a čas zaznamenání životní události.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="bd8bd-114">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="bd8bd-114">Log type</span></span> | <span data-ttu-id="bd8bd-115">Zobrazí, zda je akce jedna z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="bd8bd-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="bd8bd-116">- **Aktualizovat** – Změna stávajícího záznamu, který sleduje životní události</span><span class="sxs-lookup"><span data-stu-id="bd8bd-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="bd8bd-117">- **Vložit** – vytvoření nového záznamu životní události</span><span class="sxs-lookup"><span data-stu-id="bd8bd-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="bd8bd-118">ID typu životních událostí</span><span class="sxs-lookup"><span data-stu-id="bd8bd-118">Life event type ID</span></span> | <span data-ttu-id="bd8bd-119">Jedinečný identifikátor typu životní události.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="bd8bd-120">Typy životní události</span><span class="sxs-lookup"><span data-stu-id="bd8bd-120">Life event type</span></span> | <span data-ttu-id="bd8bd-121">Katalyzátor pro aktualizaci přihlášení zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="bd8bd-122">Další informace naleznete v části spouštěčů životní události.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="bd8bd-123">Stav</span><span class="sxs-lookup"><span data-stu-id="bd8bd-123">Status</span></span> | <span data-ttu-id="bd8bd-124">Určení, zda byla životní událost zpracována nebo ne.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="bd8bd-125">Řádek</span><span class="sxs-lookup"><span data-stu-id="bd8bd-125">Line</span></span> | <span data-ttu-id="bd8bd-126">Číslo řádku budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="bd8bd-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bd8bd-127">Select **Save**.</span></span> 

---
title: Konfigurace budoucích životních událostí
description: V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008369"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="fe28c-103">Konfigurace budoucích životních událostí</span><span class="sxs-lookup"><span data-stu-id="fe28c-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="fe28c-104">V aplikaci Dynamics 365 Human Resources můžete naplánovat budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="fe28c-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="fe28c-105">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **budoucí životní události**.</span><span class="sxs-lookup"><span data-stu-id="fe28c-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="fe28c-106">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="fe28c-106">Select **New**.</span></span>

3. <span data-ttu-id="fe28c-107">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="fe28c-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="fe28c-108">Pole</span><span class="sxs-lookup"><span data-stu-id="fe28c-108">Field</span></span> | <span data-ttu-id="fe28c-109">Popis</span><span class="sxs-lookup"><span data-stu-id="fe28c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="fe28c-110">Datum životní události</span><span class="sxs-lookup"><span data-stu-id="fe28c-110">Life event date</span></span> | <span data-ttu-id="fe28c-111">Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data.</span><span class="sxs-lookup"><span data-stu-id="fe28c-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="fe28c-112">Životní událost zaznamenána</span><span class="sxs-lookup"><span data-stu-id="fe28c-112">Life event logged</span></span> | <span data-ttu-id="fe28c-113">Datum a čas zaznamenání životní události.</span><span class="sxs-lookup"><span data-stu-id="fe28c-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="fe28c-114">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="fe28c-114">Log type</span></span> | <span data-ttu-id="fe28c-115">Zobrazí, zda je akce jedna z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="fe28c-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="fe28c-116">- **Aktualizovat** – Změna stávajícího záznamu, který sleduje životní události</span><span class="sxs-lookup"><span data-stu-id="fe28c-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="fe28c-117">- **Vložit** – vytvoření nového záznamu životní události</span><span class="sxs-lookup"><span data-stu-id="fe28c-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="fe28c-118">ID typu životních událostí</span><span class="sxs-lookup"><span data-stu-id="fe28c-118">Life event type ID</span></span> | <span data-ttu-id="fe28c-119">Jedinečný identifikátor typu životní události.</span><span class="sxs-lookup"><span data-stu-id="fe28c-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="fe28c-120">Typy životní události</span><span class="sxs-lookup"><span data-stu-id="fe28c-120">Life event type</span></span> | <span data-ttu-id="fe28c-121">Katalyzátor pro aktualizaci přihlášení zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="fe28c-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="fe28c-122">Další informace naleznete v části spouštěčů životní události.</span><span class="sxs-lookup"><span data-stu-id="fe28c-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="fe28c-123">Stav</span><span class="sxs-lookup"><span data-stu-id="fe28c-123">Status</span></span> | <span data-ttu-id="fe28c-124">Určení, zda byla životní událost zpracována nebo ne.</span><span class="sxs-lookup"><span data-stu-id="fe28c-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="fe28c-125">Řádek</span><span class="sxs-lookup"><span data-stu-id="fe28c-125">Line</span></span> | <span data-ttu-id="fe28c-126">Číslo řádku budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="fe28c-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="fe28c-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fe28c-127">Select **Save**.</span></span> 

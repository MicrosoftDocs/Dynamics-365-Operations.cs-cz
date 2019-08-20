---
title: Deaktivace verze výrobního toku
description: Když aktivní verze výrobního toku již není potřeba, je možné ji deaktivovat.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c9646a01924255b8b1b40fc2a5684ba30967fe1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843834"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="24640-103">Deaktivace verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="24640-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24640-104">Když aktivní verze výrobního toku již není potřeba, je možné ji deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="24640-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="24640-105">Tuto možnost používejte pouze v případě, že všechna kanbanová pravidla a aktivity skončily a nebude znovu aktivovány.</span><span class="sxs-lookup"><span data-stu-id="24640-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="24640-106">Všimněte si, že datum konce platnosti všechna kanbanových pravidel vztahující se k této verzi výrobního toku budou aktualizována na aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="24640-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="24640-107">Chcete-li změnit aktivní verzi výrobního toku, zkuste nastavit datum vypršení platnosti aktivní verze a vytvořit novou verzi.</span><span class="sxs-lookup"><span data-stu-id="24640-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="24640-108">To vám umožní pokračovat ve výrobních operacích při přípravě nové verze a souvisejících kanbanových pravidel.</span><span class="sxs-lookup"><span data-stu-id="24640-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="24640-109">K vypršení platnosti aktivní verze výrobního toku je třeba nastavit datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="24640-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="24640-110">V tomto smyslu je deaktivace spíše výjimka než pravidlo.</span><span class="sxs-lookup"><span data-stu-id="24640-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="24640-111">Pro tuto proceduru potřebujete výrobní tok ve verzi, kterou lze deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="24640-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="24640-112">Nepokoušejte se o to ve výrobním prostředí, pokud si nejste 100% jistí, že verze je zcela zastaralá.</span><span class="sxs-lookup"><span data-stu-id="24640-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="24640-113">Deaktivace verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="24640-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="24640-114">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="24640-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="24640-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="24640-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="24640-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="24640-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="24640-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="24640-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="24640-118">Klepněte na tlačítko Deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="24640-118">Click Deactivate.</span></span>
    * <span data-ttu-id="24640-119">Pokud si nejste 100% jistí, že tato verze výrobního toku je zastaralá, nepokračujte.</span><span class="sxs-lookup"><span data-stu-id="24640-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="24640-120">Klepnutí na tlačítko OK ukončí všechna aktivní kanbanová pravidla a okamžitě zastavení všechny výrobní a doplňovací aktivity této verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="24640-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="24640-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="24640-121">Click OK.</span></span>


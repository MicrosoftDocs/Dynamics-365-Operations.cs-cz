---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (14. února 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517496"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="d9ff0-103">Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (14. února 2019)</span><span class="sxs-lookup"><span data-stu-id="d9ff0-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9ff0-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="d9ff0-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="d9ff0-105">Changes in Attract</span></span>
<span data-ttu-id="d9ff0-106">V této verzi existuje několik menších oprav chyb.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="d9ff0-107">Změny v aplikaci Onboarding</span><span class="sxs-lookup"><span data-stu-id="d9ff0-107">Changes in Onboarding</span></span>
<span data-ttu-id="d9ff0-108">V této verzi existuje několik menších oprav chyb.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="d9ff0-109">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="d9ff0-109">Changes in Core HR</span></span> 
<span data-ttu-id="d9ff0-110">**Sestavení 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="d9ff0-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="d9ff0-111">Entita fixní kompenzace zaměstnance neexportuje všechny záznamy</span><span class="sxs-lookup"><span data-stu-id="d9ff0-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="d9ff0-112">S touto změnou bude nyní entita **Fixní kompenzace zaměstnance** exportovat všechny záznamy.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="d9ff0-113">Entitu lze použít vytváření a aktualizaci stávajících záznamů fixní kompenzace pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="d9ff0-114">Koncové datum zaměstnání nedodržuje upřednostňované časové pásmo zaměstnance</span><span class="sxs-lookup"><span data-stu-id="d9ff0-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="d9ff0-115">Koncové datum zaměstnání nyní ctí uživatelem upřednostňované časové pásmo při vytváření nebo ukončení zaměstnání se společností.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="d9ff0-116">Adresy Velké Británie se zobrazují v analytice jako adresy východního Švýcarska</span><span class="sxs-lookup"><span data-stu-id="d9ff0-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="d9ff0-117">V této verzi byla provedena změna za účelem opravy nesprávného uspořádání adres v sestavě **Správy zaměstnanců** „počet osob podle umístění“.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="d9ff0-118">Kód ukončení není vyplněn na záznamu přiřazení pozice pracovníka při ukončení pozice</span><span class="sxs-lookup"><span data-stu-id="d9ff0-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="d9ff0-119">Při ukončování přiřazení pozice zaměstnanců byla provedena změna výchozího kódu důvodu ukončení.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="d9ff0-120">Byla vytvořena nová entita pro úrovně pracovní kompenzace</span><span class="sxs-lookup"><span data-stu-id="d9ff0-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="d9ff0-121">Byla vytvořena nová entita platformy správy dat (DMF).</span><span class="sxs-lookup"><span data-stu-id="d9ff0-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="d9ff0-122">Entita zajišťuje tvorbu a aktualizaci úrovní kompenzace, tržních hodnot a informací z průzkumů pro každou práci definovanou v systému.</span><span class="sxs-lookup"><span data-stu-id="d9ff0-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>

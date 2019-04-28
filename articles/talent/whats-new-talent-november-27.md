---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (27. listopadu 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "857792"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="4cbd4-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (27. listopadu 2018)</span><span class="sxs-lookup"><span data-stu-id="4cbd4-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4cbd4-104">**Sestavení 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="4cbd4-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="4cbd4-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="4cbd4-106">Změny</span><span class="sxs-lookup"><span data-stu-id="4cbd4-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="4cbd4-107">Nelze vytvořit poznámku ve správě případu</span><span class="sxs-lookup"><span data-stu-id="4cbd4-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="4cbd4-108">Byla provedena změna kvůli problému při pokusu o úpravu nebo vytvoření poznámky v protokolu případů ve správě případu.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="4cbd4-109">Překlep ve slově na kartě analýzy v pracovním prostoru kompenzace</span><span class="sxs-lookup"><span data-stu-id="4cbd4-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="4cbd4-110">Byla provedena oprava pravopisu u Ethnic Origin v grafu analýzy kompenzace v pracovním prostoru kompenzace.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="4cbd4-111">Pracovní prostor samoobsluhy pro zaměstnance se nezobrazuje, když není uživatel přiřazen k pracovníkovi</span><span class="sxs-lookup"><span data-stu-id="4cbd4-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="4cbd4-112">Byla provedena změna, když je zvolen pracovní prostor **Samoobsluha pro zaměstnance** jako počáteční stránka při spuštění pro uživatele, který není přiřazen k pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="4cbd4-113">V takovém případě se zobrazí výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="4cbd4-114">Pracovní volno a absence - chyba: Odkaz na objekt není nastaven na instanci objektu.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="4cbd4-115">Pro pracovní volno a absence byly provedeny změny za účelem opravy této chyby po schválení záznamů pracovního volna a absence v seznamu **Pracovní položky přiřazené mně**.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="4cbd4-116">Nelze vyvolat workflow obrázku</span><span class="sxs-lookup"><span data-stu-id="4cbd4-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="4cbd4-117">Po vyvolání workflow obrázku bude workflow nastaveno na zrušené a stávající požadavek lze odstranit v pracovním prostoru samoobsluhy pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="4cbd4-118">Opětovně přijatí zaměstnanci nebo dodavatelé se zobrazují po jejich skončení několikrát</span><span class="sxs-lookup"><span data-stu-id="4cbd4-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="4cbd4-119">V této aktualizaci se ukončení zaměstnanci, kteří jsou opět přijati, zobrazí v ukončeném seznamu pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="4cbd4-120">Známý problém</span><span class="sxs-lookup"><span data-stu-id="4cbd4-120">Known issue</span></span>

- <span data-ttu-id="4cbd4-121">**Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="4cbd4-122">**Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="4cbd4-123">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4cbd4-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="4cbd4-124">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="4cbd4-124">(This issue will be fixed in the next platform update.)</span></span>

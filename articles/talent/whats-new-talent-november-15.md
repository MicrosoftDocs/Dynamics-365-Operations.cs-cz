---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (15. listopadu 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b90d4230fe1e666aba4075670f6df206e8df7ce9
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "857305"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="7b649-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (15. listopadu 2018)</span><span class="sxs-lookup"><span data-stu-id="7b649-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b649-104">**Sestavení 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="7b649-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="7b649-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="7b649-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="7b649-106">Další změny/opravy</span><span class="sxs-lookup"><span data-stu-id="7b649-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="7b649-107">Nelze změnit aktuální pozici zaměstnance na budoucí otevřenou pozici</span><span class="sxs-lookup"><span data-stu-id="7b649-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="7b649-108">Byla provedena změna, která povoluje převody pozic, když je pozice dostupná pouze v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="7b649-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="7b649-109">Při vytvoření nového zaměstnance se nezobrazuje pozice</span><span class="sxs-lookup"><span data-stu-id="7b649-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="7b649-110">Byly provedeny změny za účelem všech otevřených pozic, které jsou dostupné pro přiřazení při náboru nového zaměstnance v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="7b649-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="7b649-111">To zahrnuje historické pozice nebo pozice s budoucí datem.</span><span class="sxs-lookup"><span data-stu-id="7b649-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="7b649-112">Pozice se zobrazí nyní správně na základě počátečního data zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="7b649-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="7b649-113">Datum ukončení se zobrazuje na základě nastavení uživatele</span><span class="sxs-lookup"><span data-stu-id="7b649-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="7b649-114">Byla provedena změna seznamu bývalých zaměstnanců, aby byly vysvětleny posuny časových zón u časových zón preferovaných zaměstnanci při zobrazení data ukončení.</span><span class="sxs-lookup"><span data-stu-id="7b649-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="7b649-115">Odkazy na pracovní položky přiřazené mně nezobrazují správné informace</span><span class="sxs-lookup"><span data-stu-id="7b649-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="7b649-116">Při této změně navigace k podrobnostem jednotlivých pracovních položek v seznamu zobrazí správné informace pro vybranou položku.</span><span class="sxs-lookup"><span data-stu-id="7b649-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="7b649-117">K tomuto problému dochází pouze u rozšířených možností zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="7b649-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="7b649-118">Známý problém</span><span class="sxs-lookup"><span data-stu-id="7b649-118">Known issue</span></span>

- <span data-ttu-id="7b649-119">**Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě.</span><span class="sxs-lookup"><span data-stu-id="7b649-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="7b649-120">**Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="7b649-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="7b649-121">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7b649-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="7b649-122">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="7b649-122">(This issue will be fixed in the next platform update.)</span></span>

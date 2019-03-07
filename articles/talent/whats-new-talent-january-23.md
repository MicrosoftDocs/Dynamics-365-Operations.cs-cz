---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (23. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 135be837a82af8cee22d83c015a78da3b89b7978
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303516"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="18a2b-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (23. ledna 2019)</span><span class="sxs-lookup"><span data-stu-id="18a2b-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18a2b-104">**Sestavení 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="18a2b-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="18a2b-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="18a2b-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="18a2b-106">Změny</span><span class="sxs-lookup"><span data-stu-id="18a2b-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="18a2b-107">Import fixní kompenzace zaměstnance nepracuje při vytváření nových záznamů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="18a2b-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="18a2b-108">Byla provedena změna entity fixní kompenzace zaměstnance k příjmu úrovně kompenzace při importu.</span><span class="sxs-lookup"><span data-stu-id="18a2b-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="18a2b-109">Před touto verzí byla zobrazena zpráva označující požadovalo úroveň.</span><span class="sxs-lookup"><span data-stu-id="18a2b-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="18a2b-110">Odeberte pole Minimální zůstatek z dialogového okna požadavku na volno.</span><span class="sxs-lookup"><span data-stu-id="18a2b-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="18a2b-111">Pole **Minimální zůstatek** bylo odebráno z dialogového okna **Požadavek na časový posun**.</span><span class="sxs-lookup"><span data-stu-id="18a2b-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="18a2b-112">Tato změna ovlivňuje všechny oblasti, kde lze požadovat volno.</span><span class="sxs-lookup"><span data-stu-id="18a2b-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="18a2b-113">Upgrade dat pro úrovně odměňování se neaktualizuje ve všech scénářích</span><span class="sxs-lookup"><span data-stu-id="18a2b-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="18a2b-114">Byla provedena změna k aktualizaci úrovně odměňování v plánech fixního odměňování.</span><span class="sxs-lookup"><span data-stu-id="18a2b-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="18a2b-115">Tato změna naplní úroveň odměňování ve fixních plánech pro práci přidělenou zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="18a2b-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="18a2b-116">Mzdové informace na stránce správy změn je dostupná pouze při přihlášen jako správce systému</span><span class="sxs-lookup"><span data-stu-id="18a2b-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="18a2b-117">Tato změna zaměstnancům s rolí správce výplat umožňuje přístup k informacím o výplatám na stránce **Časová osa změn > Spravovat změny** pro danou pozici.</span><span class="sxs-lookup"><span data-stu-id="18a2b-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="18a2b-118">pole zakázky výchozí pro pozice</span><span class="sxs-lookup"><span data-stu-id="18a2b-118">Job fields default to positions</span></span>
<span data-ttu-id="18a2b-119">Při změně práce pro pozici, budou pole úlohy použita jako výchozí pro pozici.</span><span class="sxs-lookup"><span data-stu-id="18a2b-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="18a2b-120">Zobrazí se výstražná zpráva s možností přijmout výchozí hodnoty nebo ponechat existující hodnoty pro tato pole.</span><span class="sxs-lookup"><span data-stu-id="18a2b-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="18a2b-121">Období zaškolení a kalendáře se nezobrazují pro zaměstnance přijaté v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="18a2b-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="18a2b-122">Při této změně byla přidána pole **Zkušební období** a **kalendář** na stránku **Správa změn** s cílem umožnit zadávání dat pro budoucí a minulé zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="18a2b-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="18a2b-123">Aktualizace platformy 23</span><span class="sxs-lookup"><span data-stu-id="18a2b-123">Platform update 23</span></span>
<span data-ttu-id="18a2b-124">Dílčí opravy chyb byly zahrnuty jako součást aktualizace platformy 23.</span><span class="sxs-lookup"><span data-stu-id="18a2b-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="18a2b-125">Další informace naleznete v tématu [Co je nového nebo změněného v Dynamics 365 for Finance and Operations aktualizace platformy 23 (leden 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="18a2b-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 

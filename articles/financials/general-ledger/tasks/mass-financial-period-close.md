---
title: Hromadné uzavření finančního období
description: Tento postup ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564474"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="46ebe-103">Hromadné uzavření finančního období</span><span class="sxs-lookup"><span data-stu-id="46ebe-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46ebe-104">Tento postup ukazuje, jak pozdržet nebo trvale uzavřít období nebo více než jednu právnickou osobu současně.</span><span class="sxs-lookup"><span data-stu-id="46ebe-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="46ebe-105">Úkol navíc ukáže, jak omezit skupinu uživatelů, kteří provádějí zaúčtování do konkrétních modulů.</span><span class="sxs-lookup"><span data-stu-id="46ebe-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="46ebe-106">Přejděte do části Hlavní kniha > Uzávěrka období > Kalendáře hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="46ebe-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="46ebe-107">Všimněte si, že zobrazený seznam právnických osob je závislý na fiskálním kalendáři vybraném na stránce.</span><span class="sxs-lookup"><span data-stu-id="46ebe-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="46ebe-108">Zobrazí se pouze právnické osoby používající vybraný fiskální kalendář.</span><span class="sxs-lookup"><span data-stu-id="46ebe-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="46ebe-109">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="46ebe-109">Click Edit.</span></span>
3. <span data-ttu-id="46ebe-110">Vyberte období, u kterého chcete změnit stav.</span><span class="sxs-lookup"><span data-stu-id="46ebe-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="46ebe-111">Vyberte právnické osoby, u kterých chcete aktualizovat stav.</span><span class="sxs-lookup"><span data-stu-id="46ebe-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="46ebe-112">Zaškrtnutím políčka v levé horní části mřížky můžete rychle vybrat všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="46ebe-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="46ebe-113">Vyberte možnost Aktualizovat přístup k modulu a definujte přístup k vybranému modulu pro zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="46ebe-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="46ebe-114">Stav modulu může být také aktualizovaný postupně úpravou záznamů v mřížce.</span><span class="sxs-lookup"><span data-stu-id="46ebe-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="46ebe-115">Tlačítko je užitečné, když chcete rychle aktualizovat více záznamů právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="46ebe-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="46ebe-116">V poli Modul aplikace vyberte nebo zadejte modul, jehož stav chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="46ebe-117">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-117">Click Select.</span></span>
7. <span data-ttu-id="46ebe-118">V poli Úroveň přístupu vyberte Vše, Žádná nebo konkrétní skupinu uživatelů.</span><span class="sxs-lookup"><span data-stu-id="46ebe-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="46ebe-119">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-119">Click Select.</span></span>
    * <span data-ttu-id="46ebe-120">Pokud je období otevřené, vše naznačuje tomu, že všichni uživatelé s přístupem k úpravám mohou zaúčtovávat do modulu.</span><span class="sxs-lookup"><span data-stu-id="46ebe-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="46ebe-121">Hodnota Žádné označuje, že uživatelé nemůžou zaúčtovávat do modulu, když je období otevřené.</span><span class="sxs-lookup"><span data-stu-id="46ebe-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="46ebe-122">Určité uživatelské skupiny určují, že pouze uživatelé ve skupině mohou zaúčtovávat do modulu, pokud je období otevřené.</span><span class="sxs-lookup"><span data-stu-id="46ebe-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="46ebe-123">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-123">Click Update.</span></span>
9. <span data-ttu-id="46ebe-124">Vyberte jiné období k aktualizaci stavu.</span><span class="sxs-lookup"><span data-stu-id="46ebe-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="46ebe-125">Vyberte právnické osoby, u kterých chcete aktualizovat stav období.</span><span class="sxs-lookup"><span data-stu-id="46ebe-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="46ebe-126">Vyberte stav aktualizace období a nastavte stav na Blokováno, Otevřeno nebo Trvale uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="46ebe-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="46ebe-127">Otevření naznačuje, že období lze zaúčtovat, pokud má uživatel přístup.</span><span class="sxs-lookup"><span data-stu-id="46ebe-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="46ebe-128">Hodnota Blokováno znamená, že období nelze zaúčtovat, ale můžete ho znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="46ebe-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="46ebe-129">Trvale uzavřené znamená, že je období uzavřeno a nikdy je nelze otevřít.</span><span class="sxs-lookup"><span data-stu-id="46ebe-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="46ebe-130">Úpravy nelze zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="46ebe-131">Nedoporučujeme nastavit období na Trvale uzavřeno, dokud nejsou dokončeny všechny úpravy a audity.</span><span class="sxs-lookup"><span data-stu-id="46ebe-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="46ebe-132">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="46ebe-132">Click Update.</span></span>


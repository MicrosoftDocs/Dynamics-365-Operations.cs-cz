---
title: Nastavení oprávnění pro objednávání produktů jménem jiného uživatele
description: Tento postup popisuje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eea1577972879cc24a2295a0c5a8d7d3de5f4520
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837967"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="be8f4-103">Nastavení oprávnění pro objednávání produktů jménem jiného uživatele</span><span class="sxs-lookup"><span data-stu-id="be8f4-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be8f4-104">Tento postup popisuje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků.</span><span class="sxs-lookup"><span data-stu-id="be8f4-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="be8f4-105">Jinak řečeno, pořizovatel" nákupního požadavku může vytvořit požadavek za jiného žadatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="be8f4-106">Postup rovněž ukazuje, jak udělit pracovníkovi oprávnění objednat zboží a služby u různých právnických osob nebo provozních jednotek.</span><span class="sxs-lookup"><span data-stu-id="be8f4-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="be8f4-107">Obvykle jsou tyto úlohy prováděny vedoucím nákupu.</span><span class="sxs-lookup"><span data-stu-id="be8f4-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="be8f4-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="be8f4-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="be8f4-109">Udělení oprávnění zadat nákupní žádanky jménem jiného pracovníka</span><span class="sxs-lookup"><span data-stu-id="be8f4-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="be8f4-110">Přejděte na Zásobování a zdroje > Nastavení > Zásady > Oprávnění nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="be8f4-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="be8f4-111">Ujistěte se, že je v poli Aktuální zobrazení vybrána možnost Podle pořizovatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="be8f4-112">V seznamu v levém podokně se zobrazí osoby, kterým mohou mít udělena oprávnění k přípravě žádanek jménem ostatních uživatelů.</span><span class="sxs-lookup"><span data-stu-id="be8f4-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="be8f4-113">Vyberte osobu, které chcete udělit oprávnění (pořizovatel).</span><span class="sxs-lookup"><span data-stu-id="be8f4-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="be8f4-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="be8f4-114">Click Add.</span></span>
4. <span data-ttu-id="be8f4-115">Vyhledejte a vyberte osobu, kterou chcete přidat jako žadatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="be8f4-116">Žadatel je osoba, jejímž jménem může pořizovatel vytvořit požadavky.</span><span class="sxs-lookup"><span data-stu-id="be8f4-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="be8f4-117">V poli Autorizace vyberte Konkrétní, pokud má být pořizovatel schopen vytvářet nákupní žádanky jménem vybraného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="be8f4-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="be8f4-118">Vyberte Vykazování, pokud pořizovatel má být také schopen vytvářet nákupní žádanky jménem všech pracovníků, kteří jsou podřízeni danému pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="be8f4-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="be8f4-119">V poli Platnost zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="be8f4-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="be8f4-120">Do pole Vypršení platnosti zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="be8f4-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="be8f4-121">Zobrazení zpracovatelů, kteří mají oprávnění k vytváření nákupních žádanek pro vybraného pracovníka</span><span class="sxs-lookup"><span data-stu-id="be8f4-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="be8f4-122">V poli Aktuální zobrazení vyberte „Podle žadatele“.</span><span class="sxs-lookup"><span data-stu-id="be8f4-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="be8f4-123">Toto zobrazení popisuje seznam pořizovatelů, kterým byla udělena oprávnění k vytváření nákupních žádanek jménem vybraného zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be8f4-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="be8f4-124">Pomocí rychlého filtru vyhledejte pracovníka, kterého jste právě vytvořili jako žadatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="be8f4-125">Vyberte žadatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-125">Select the requester.</span></span>
    * <span data-ttu-id="be8f4-126">Seznam Pořizovatel popisuje uživatele, kteří mají oprávnění k objednání položek jménem žadatele, který je vybrán v levém podokně.</span><span class="sxs-lookup"><span data-stu-id="be8f4-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="be8f4-127">Zde můžete přidat další zpracovatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-127">You can add additional preparers here.</span></span>   <span data-ttu-id="be8f4-128">Toto zobrazení umožňuje také udělit oprávnění žadatelům pro vytvoření žádanek u právnických osob a provozních jednotek, které nejsou primární právnickou osobou nebo provozní jednotkou daného uživatele.</span><span class="sxs-lookup"><span data-stu-id="be8f4-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


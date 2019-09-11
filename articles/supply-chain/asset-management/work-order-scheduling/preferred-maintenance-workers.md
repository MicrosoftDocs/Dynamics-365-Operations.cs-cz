---
title: Nastavení preferovaných pracovníků údržby
description: Toto téma vysvětluje, jak nastavit preferované pracovníky údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887404"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="4b67f-103">Preferovaní pracovníci údržby</span><span class="sxs-lookup"><span data-stu-id="4b67f-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4b67f-104">Můžete vytvořit předvolbu, která se týká pracovníků údržby přidělených k dokončení pracovních příkazů během plánování pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="4b67f-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="4b67f-105">Použití této funkce je volitelné, ale může vám pomoci vybrat pro nejvíce kvalifikovaného pracovníka údržby, aby dokončil úlohu na základě dovedností a kompetencí pracovníků.</span><span class="sxs-lookup"><span data-stu-id="4b67f-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="4b67f-106">V průběhu plánování pracovních příkazů lze tedy pomocí nastavení **Preferovaní pracovníci údržby** určit, zda má být pro pracovní příkaz naplánován určitý pracovník údržby nebo skupina pracovníků.</span><span class="sxs-lookup"><span data-stu-id="4b67f-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="4b67f-107">Naplánovány budou pouze pracovníci údržby, kteří jsou k dispozici v čase plánování.</span><span class="sxs-lookup"><span data-stu-id="4b67f-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="4b67f-108">Pokud je nastavení preferovaných pracovníků údržby během plánování shodné s pracovním příkazem, ale pracovník údržby je přidělen k jiným úlohám, bude pracovní příkaz naplánován na jiného dostupného pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="4b67f-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="4b67f-109">Před nastavením preferovaných pracovníků údržby je nutné nejprve nastavit pracovníky údržby a skupiny pracovníků, kteří by měli být k dispozici pro výběr.</span><span class="sxs-lookup"><span data-stu-id="4b67f-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="4b67f-110">Informace o tom, jak nastavit pracovníky údržby a skupin pracovníků, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="4b67f-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="4b67f-111">Nastavení preferovaných pracovníků</span><span class="sxs-lookup"><span data-stu-id="4b67f-111">Set up preferred workers</span></span>

<span data-ttu-id="4b67f-112">Upřednostňovaný pracovník údržby nebo skupina pracovníků může souviset s konkrétní</span><span class="sxs-lookup"><span data-stu-id="4b67f-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="4b67f-113">obchod</span><span class="sxs-lookup"><span data-stu-id="4b67f-113">trade</span></span>  
- <span data-ttu-id="4b67f-114">variantou typu práce údržby</span><span class="sxs-lookup"><span data-stu-id="4b67f-114">maintenance job type variant</span></span>  
- <span data-ttu-id="4b67f-115">typ práce údržby</span><span class="sxs-lookup"><span data-stu-id="4b67f-115">maintenance job type</span></span>  
- <span data-ttu-id="4b67f-116">kategorie typu práce údržby</span><span class="sxs-lookup"><span data-stu-id="4b67f-116">maintenance job type category</span></span>  
- <span data-ttu-id="4b67f-117">majetek</span><span class="sxs-lookup"><span data-stu-id="4b67f-117">asset</span></span>  
- <span data-ttu-id="4b67f-118">typ majetku</span><span class="sxs-lookup"><span data-stu-id="4b67f-118">asset type</span></span>  

<span data-ttu-id="4b67f-119">nebo kombinaci těchto výběrů.</span><span class="sxs-lookup"><span data-stu-id="4b67f-119">or a combination of those selections.</span></span> <span data-ttu-id="4b67f-120">Čím více výběrů, které provedete pro stejný záznam, tím přesnější bude nastavení.</span><span class="sxs-lookup"><span data-stu-id="4b67f-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="4b67f-121">Klikněte na **Správa majetku** > **Nastavení** > **Pracovníci** > **Preferovaní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="4b67f-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="4b67f-122">Kliknutím na možnost **Nový** vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="4b67f-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="4b67f-123">Začněte vytvořením „výchozího“ pracovníka pro údržbu nebo nastavení skupiny pracovníků, který nemá žádné výběry v polích zobrazených v předchozím seznamu odrážek.</span><span class="sxs-lookup"><span data-stu-id="4b67f-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="4b67f-124">To znamená, že provedete výběr pouze v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**.</span><span class="sxs-lookup"><span data-stu-id="4b67f-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="4b67f-125">Na níže uvedeném obrázku vidíte příklad v prvním záznamu, ve kterém je vybrána možnost „požadavky“ jako skupina preferovaných pracovníků údržby.</span><span class="sxs-lookup"><span data-stu-id="4b67f-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="4b67f-126">Toto výchozí nastavení bude použito během plánování pracovního příkazu, pokud žádná jiná specifická kombinace neodpovídá obsahu pracovního příkazu během plánování pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="4b67f-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="4b67f-127">Opakujte krok 2 a vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="4b67f-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="4b67f-128">Proveďte požadované výběry v závislosti na úrovni podrobností pro preferovaného pracovníka nebo skupinu pracovníků.</span><span class="sxs-lookup"><span data-stu-id="4b67f-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="4b67f-129">*Příklad:* na obrázku níže, v šestém záznamu, je jako preferovaný pracovník vybrán pracovník údržby Shawn Richardson.</span><span class="sxs-lookup"><span data-stu-id="4b67f-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="4b67f-130">Při plánování pracovního příkazu bude automaticky vybrána možnost, která zahrnuje majetek CH-BP1-03-02 a typ práce údržby "Hodnocení zařízení", pokud je k dispozici v naplánovaném čase.</span><span class="sxs-lookup"><span data-stu-id="4b67f-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="4b67f-131">Obecně platí, že když je při plánování pracovních příkazů vybrán preferovaný pracovník údržby, Správa majetku projde všechny záznamy **Preferovaní pracovníci údržby** a zkontroluje možné odpovídající položky. Vždy nejprve zkontroluje nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="4b67f-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="4b67f-132">Pokud není nalezena žádná shoda, bude použit "výchozí" záznam s výběrem v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**.</span><span class="sxs-lookup"><span data-stu-id="4b67f-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Obrázek č. 1](media/02-work-order-scheduling.png)

<span data-ttu-id="4b67f-134">Můžete také nastavit odpovědné pracovníky údržby, kteří mohou být vybráni při vytvoření požadavku na údržbu nebo pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="4b67f-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="4b67f-135">Ve **Všech pracovních příkazech** a **Všech požadavcích na údržbu** můžete výběr v případě potřeby upravit.</span><span class="sxs-lookup"><span data-stu-id="4b67f-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="4b67f-136">Další informace naleznete v sekci [Odpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="4b67f-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="4b67f-137">Při plánování pracovních příkazů se počítají různé výsledky s cílem určit, kteří pracovníci by měli dokončit úlohy související s pracovním příkazem (tato skóre se nastavují v nabídce **Parametry správy majetku** > **Plánování pracovních příkazů**).</span><span class="sxs-lookup"><span data-stu-id="4b67f-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="4b67f-138">Pokud při plánování pracovních příkazů získají dva nebo více preferovaných pracovníků údržby nebo odpovědných pracovníků údržby stejné hodnocení, bude jeden pracovník vybrán náhodně.</span><span class="sxs-lookup"><span data-stu-id="4b67f-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="4b67f-139">V opačném případě je vždy pracovník s nejvyšším skóre přidělen k dokončení pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="4b67f-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>


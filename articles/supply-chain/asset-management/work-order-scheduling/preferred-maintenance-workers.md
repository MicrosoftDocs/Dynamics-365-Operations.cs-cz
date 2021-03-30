---
title: Nastavení preferovaných pracovníků údržby
description: Toto téma vysvětluje, jak nastavit preferované pracovníky údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 102f48d1273ac91d5cb42eca11d2dec337c30528
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214955"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="c4f26-103">Nastavení preferovaných pracovníků údržby</span><span class="sxs-lookup"><span data-stu-id="c4f26-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c4f26-104">Během plánování pracovního příkazu můžete vytvořit předvolbu, která se týká toho, který pracovník údržby nebo skupina pracovníků budou přiděleni k dokončení pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c4f26-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="c4f26-105">Použití této funkce je volitelné, ale může vám pomoci vybrat pro nejvíce kvalifikovaného pracovníka údržby, aby dokončil úlohu na základě dovedností a kompetencí pracovníků.</span><span class="sxs-lookup"><span data-stu-id="c4f26-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="c4f26-106">Naplánovány budou pouze pracovníci údržby, kteří jsou k dispozici v čase plánování.</span><span class="sxs-lookup"><span data-stu-id="c4f26-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="c4f26-107">Pokud je nastavení preferovaných pracovníků údržby během plánování shodné s pracovním příkazem, ale pracovník údržby je přidělen k jiným úlohám, bude pracovní příkaz naplánován na jiného dostupného pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="c4f26-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="c4f26-108">Před nastavením upřednostňovaných pracovníků údržby je nejprve nutné nastavit pracovníky údržby a skupiny pracovníků.</span><span class="sxs-lookup"><span data-stu-id="c4f26-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="c4f26-109">Informace o tom, jak nastavit pracovníky údržby a skupin pracovníků, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c4f26-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="c4f26-110">Nastavení preferovaných pracovníků</span><span class="sxs-lookup"><span data-stu-id="c4f26-110">Set up preferred workers</span></span>

<span data-ttu-id="c4f26-111">Upřednostňovaný pracovník údržby nebo skupina pracovníků může souviset s jednou nebo více z následujících položek:</span><span class="sxs-lookup"><span data-stu-id="c4f26-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="c4f26-112">obchod</span><span class="sxs-lookup"><span data-stu-id="c4f26-112">trade</span></span>  
- <span data-ttu-id="c4f26-113">variantou typu práce údržby</span><span class="sxs-lookup"><span data-stu-id="c4f26-113">maintenance job type variant</span></span>  
- <span data-ttu-id="c4f26-114">typ práce údržby</span><span class="sxs-lookup"><span data-stu-id="c4f26-114">maintenance job type</span></span>  
- <span data-ttu-id="c4f26-115">kategorie typu práce údržby</span><span class="sxs-lookup"><span data-stu-id="c4f26-115">maintenance job type category</span></span>  
- <span data-ttu-id="c4f26-116">majetek</span><span class="sxs-lookup"><span data-stu-id="c4f26-116">asset</span></span>  
- <span data-ttu-id="c4f26-117">typ majetku</span><span class="sxs-lookup"><span data-stu-id="c4f26-117">asset type</span></span>  

<span data-ttu-id="c4f26-118">Čím více výběrů, které provedete pro stejný záznam, tím přesnější bude nastavení.</span><span class="sxs-lookup"><span data-stu-id="c4f26-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="c4f26-119">Klikněte na **Správa majetku** > **Nastavení** > **Pracovníci** > **Preferovaní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="c4f26-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="c4f26-120">Kliknutím na možnost **Nový** vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="c4f26-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="c4f26-121">Začněte vytvořením "výchozího" pracovníka pro údržbu nebo skupiny pracovníků.</span><span class="sxs-lookup"><span data-stu-id="c4f26-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="c4f26-122">To znamená, že provedete výběr pouze v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**.</span><span class="sxs-lookup"><span data-stu-id="c4f26-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="c4f26-123">Na níže uvedeném snímku obrazovky vidíte příklad v prvním záznamu, ve kterém je vybrána možnost „požadavky“ jako **skupina preferovaných pracovníků údržby**.</span><span class="sxs-lookup"><span data-stu-id="c4f26-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="c4f26-124">Toto výchozí nastavení bude použito během plánování pracovního příkazu, pokud žádná jiná specifická kombinace neodpovídá obsahu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c4f26-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="c4f26-125">Opakujte krok 2 a vytvořte nový záznam.</span><span class="sxs-lookup"><span data-stu-id="c4f26-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="c4f26-126">Proveďte požadované výběry v závislosti na úrovni podrobností pro preferovaného pracovníka nebo skupinu pracovníků.</span><span class="sxs-lookup"><span data-stu-id="c4f26-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="c4f26-127">*Příklad:* na snímku obrazovky níže, v šestém záznamu, je jako preferovaný pracovník vybrán pracovník údržby Shawn Richardson.</span><span class="sxs-lookup"><span data-stu-id="c4f26-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="c4f26-128">Při plánování pracovního příkazu bude automaticky vybrána možnost, která zahrnuje majetek CH-BP1-03-02 a typ práce údržby "Hodnocení zařízení", pokud je k dispozici v naplánovaném čase.</span><span class="sxs-lookup"><span data-stu-id="c4f26-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="c4f26-129">Obecně platí, že když je při plánování pracovních příkazů vybrán preferovaný pracovník údržby, Správa majetku projde všechny záznamy **Preferovaní pracovníci údržby** a zkontroluje možné odpovídající položky. Vždy nejprve zkontroluje nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="c4f26-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="c4f26-130">Pokud není nalezena žádná shoda, bude použit "výchozí" záznam s výběrem v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**.</span><span class="sxs-lookup"><span data-stu-id="c4f26-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Obrázek č. 1](media/02-work-order-scheduling.png)

<span data-ttu-id="c4f26-132">Můžete také nastavit *odpovědné* pracovníky údržby, kteří mohou být vybráni při vytvoření požadavku na údržbu nebo pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c4f26-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="c4f26-133">Ve **Všech pracovních příkazech** a **Všech požadavcích na údržbu** můžete výběr v případě potřeby upravit.</span><span class="sxs-lookup"><span data-stu-id="c4f26-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="c4f26-134">Další informace naleznete v části [Odpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="c4f26-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="c4f26-135">Při plánování pracovních příkazů se počítají různé výsledky s cílem určit, kteří pracovníci by měli dokončit úlohy související s pracovním příkazem (tato skóre se nastavují v nabídce **Parametry správy majetku** > **Plánování pracovních příkazů**).</span><span class="sxs-lookup"><span data-stu-id="c4f26-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="c4f26-136">Pokud při plánování pracovních příkazů získají dva nebo více preferovaných pracovníků údržby nebo odpovědných pracovníků údržby stejné hodnocení, bude jeden pracovník vybrán náhodně.</span><span class="sxs-lookup"><span data-stu-id="c4f26-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="c4f26-137">V opačném případě je vždy pracovník s nejvyšším skóre přidělen k dokončení pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c4f26-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
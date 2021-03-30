---
title: Vytvoření a aktualizace pracovní doby obchodu
description: V tomto tématu je popsán postup při vytváření a aktualizaci pracovní doby obchodu v programu Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 00c532dfa9ceed2cda6652496d874cb82785dc7b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230633"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="abc48-103">Vytvoření a aktualizace pracovní doby obchodu</span><span class="sxs-lookup"><span data-stu-id="abc48-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="abc48-104">Přehled</span><span class="sxs-lookup"><span data-stu-id="abc48-104">Overview</span></span>

<span data-ttu-id="abc48-105">Z jednoho místa mohou maloobchodní prodejci vytvářet, spravovat a řídit pracovní doby obchodu pro různé obchody napříč geografickými oblastmi.</span><span class="sxs-lookup"><span data-stu-id="abc48-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="abc48-106">Pracovní doby obchodu lze poté zobrazit na terminálech na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="abc48-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="abc48-107">Tímto způsobem mohou pokladní uživatelé sdílet pracovní doby obchodu se zákazníky a pomoci nakupujícím, kteří mají zájem o zásoby v jiných obchodech.</span><span class="sxs-lookup"><span data-stu-id="abc48-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="abc48-108">Pracovní doby obchodu lze rovněž vytisknout na účtenky v případě, že se odběratelé chtějí vrátit do obchodu později.</span><span class="sxs-lookup"><span data-stu-id="abc48-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="abc48-109">Více pracovních dob obchodu lze konfigurovat napříč různými kanály.</span><span class="sxs-lookup"><span data-stu-id="abc48-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="abc48-110">Tyto kanály zahrnují kamenné obchody, kontaktní střediska, mobilní zařízení a weby s elektronickým obchodováním.</span><span class="sxs-lookup"><span data-stu-id="abc48-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="abc48-111">Pokud má odběratel objednávku výdeje pro jiný obchod, může pokladník vybrat data, kdy bude výdej v daném obchodě k dispozici.</span><span class="sxs-lookup"><span data-stu-id="abc48-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="abc48-112">Vyhledávání obchodu poskytne odkaz na data a pracovní doby obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="abc48-113">Pokladník může vybrat datum a místo a také můžete vytisknout příjemku odběru, která zahrnuje pracovní dobu obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="abc48-114">Tato funkce je k dispozici v Microsoft Dynamics 365 Retail verze 8.1.2 a novější.</span><span class="sxs-lookup"><span data-stu-id="abc48-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="abc48-115">Konfigurace pracovní doby obchodu</span><span class="sxs-lookup"><span data-stu-id="abc48-115">Configure store hours</span></span>

<span data-ttu-id="abc48-116">Chcete-li nakonfigurovat pracovní dobu obchodu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="abc48-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="abc48-117">Přejděte na **Retail a Commerce** \> **Nastavení kanálu** \> **Pracovní doba obchodu**.</span><span class="sxs-lookup"><span data-stu-id="abc48-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="abc48-118">Vyberte **Nová** pro vytvoření nové šablony pracovní doby obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="abc48-119">Chcete-li použít existující šablonu, vyberte ji v levém podokně.</span><span class="sxs-lookup"><span data-stu-id="abc48-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="abc48-120">V dialogovém okně **Přidat rozsah** definujte rozsah dat, pracovní dobu obchodu a všechny požadované svátky.</span><span class="sxs-lookup"><span data-stu-id="abc48-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="abc48-121">Pokud se pracovní doba obchodu nezmění, vyberte **Nikdy nekončí** v poli **Koncové datum**.</span><span class="sxs-lookup"><span data-stu-id="abc48-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="abc48-122">Pokud je pracovní doba obchodu pro určitý měsíc, týden nebo den, nastavte příslušná data v polích **Počáteční datum** a **Koncové datum**.</span><span class="sxs-lookup"><span data-stu-id="abc48-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="abc48-123">Je možné vytvořit více šablon, které se překrývají s počátečním a koncovým datem.</span><span class="sxs-lookup"><span data-stu-id="abc48-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="abc48-124">Lze tedy například definovat pracovní dobu obchodu pro obchody v různých časových pásmech.</span><span class="sxs-lookup"><span data-stu-id="abc48-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="abc48-125">![Dialogové okno Přidat rozsah](../dev-itpro/media/Storehours1.png "Dialogové okno Přidat rozsah")</span><span class="sxs-lookup"><span data-stu-id="abc48-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="abc48-126">Přiřaďte k šabloně pracovní doby obchodu obchody, kde bude použita.</span><span class="sxs-lookup"><span data-stu-id="abc48-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="abc48-127">V dialogovém okně **Vybrat uzly organizace** vyberte obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.</span><span class="sxs-lookup"><span data-stu-id="abc48-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="abc48-128">Ke každému obchodu lze přidružit pouze jednu šablonu pracovní doby obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="abc48-129">Pomocí tlačítek se šipkami vyberte obchody, regiony nebo organizace.</span><span class="sxs-lookup"><span data-stu-id="abc48-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="abc48-130">Kalendář bude k dispozici pro obchody nebo skupiny obchodů a bude viditelný na POS pro referenci.</span><span class="sxs-lookup"><span data-stu-id="abc48-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="abc48-131">![Dialogové okno Vybrat organizační uzly](../dev-itpro/media/Storehours2.png "Dialogové okno Vybrat organizační uzly")</span><span class="sxs-lookup"><span data-stu-id="abc48-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="abc48-132">Na stránce **Plán distribuce** spusťte úlohy **1070** a **1090**, které umožní POS zpřístupnit pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="abc48-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="abc48-133">Přidat pracovní dobu obchodu do vytištěných účtenek</span><span class="sxs-lookup"><span data-stu-id="abc48-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="abc48-134">Pomocí následujících kroků přidejte do tištěných příjemek POS pracovní dobu obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="abc48-135">Otevřete návrhář formátu příjemky.</span><span class="sxs-lookup"><span data-stu-id="abc48-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="abc48-136">V levém dolním rohu vyberte možnost **Zápatí**.</span><span class="sxs-lookup"><span data-stu-id="abc48-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="abc48-137">Přetáhněte prvek **Pracovní doba obchodu** z levého podokna do zápatí v dolní části šablony účtenky.</span><span class="sxs-lookup"><span data-stu-id="abc48-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="abc48-138">Můžete upravit výchozí popisek v prvku **Pracovní doba obchodu** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="abc48-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="abc48-139">Uložte příjemku a zavřete návrhář účtenky.</span><span class="sxs-lookup"><span data-stu-id="abc48-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="abc48-140">Na stránce **Plán distribuce** spusťte úlohy **1070** a **1090**.</span><span class="sxs-lookup"><span data-stu-id="abc48-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="abc48-141">Přihlaste se k systému POS.</span><span class="sxs-lookup"><span data-stu-id="abc48-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="abc48-142">Dokončete prodej a vyberte Tisk účtenky.</span><span class="sxs-lookup"><span data-stu-id="abc48-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="abc48-143">Příjemky POS nyní zahrnují pracovní dobu obchodu.</span><span class="sxs-lookup"><span data-stu-id="abc48-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="abc48-144">Pokud byly do šablony zahrnuty nějaké svátky, zobrazí se na účtence.</span><span class="sxs-lookup"><span data-stu-id="abc48-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="abc48-145">![Příklad účtenky](../dev-itpro/media/Storehours3.png "Příklad účtenky")</span><span class="sxs-lookup"><span data-stu-id="abc48-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
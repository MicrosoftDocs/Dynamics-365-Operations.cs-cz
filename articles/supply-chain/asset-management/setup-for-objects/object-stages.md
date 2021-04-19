---
title: Stavy životního cyklu majetku
description: Toto téma vysvětluje stavy životního cyklu majetku a modely životního cyklu v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 985fedc13e28caee90c9db27b145e415d256208d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808273"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="47745-103">Stavy životního cyklu majetku</span><span class="sxs-lookup"><span data-stu-id="47745-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="47745-104">Toto téma vysvětluje stavy životního cyklu majetku a modely životního cyklu v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="47745-105">Stavy životního cyklu majetku se používají k definování, zda je majetek aktivní nebo neaktivní.</span><span class="sxs-lookup"><span data-stu-id="47745-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="47745-106">Můžete například nastavit stavy životního cyklu majetku jako **Vytvořené**, **Aktivní** a **Ukončené**.</span><span class="sxs-lookup"><span data-stu-id="47745-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="47745-107">Stavy životního cyklu požadavku jsou propojeny se stavy životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="47745-108">Proto, pokud je požadavek změněn na nový stav životního cyklu požadavku, je majetek připojený k požadavku změněn na nový stav životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="47745-109">Pokud je například stav životního cyklu požadavku změněn na **Příchozí**, stav životního cyklu připojeného majetku se změní na stav životního cyklu, který je vybrán v poli **Stav aktivního cyklu příchozí** na pevné záložce **Stav životního cyklu majetku** na stránce **Modely životního cyklu majetku**.</span><span class="sxs-lookup"><span data-stu-id="47745-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="47745-110">Stavy životního cyklu majetku lze nastavit v modelech životního cyklu majetku, kde můžete definovat požadované stavy životního cyklu pro různé typy majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="47745-111">Nejprve nastavíte stavy životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-111">You first set up lifecycle states.</span></span> <span data-ttu-id="47745-112">Poté vytvořte model životního cyklu a vyberte pro něj stavy životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="47745-113">Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="47745-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="47745-114">Zvolte **Nový** pro vytvoření stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="47745-115">Do pole **Stav životního cyklu** zadejte ID stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="47745-116">Do pole **Název** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="47745-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="47745-117">Pole **Modely časového cyklu** zobrazuje počet modelů životního cyklu majetku, které používají stav životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="47745-118">Nastavte možnost **Aktivní** na **Ano**, pokud by tento stav životního cyklu měl být aktivním stavem životního cyklu (jinými slovy, pokud lze vytvořit pracovní příkazy pro majetek, který je v tomto stavu životního cyklu).</span><span class="sxs-lookup"><span data-stu-id="47745-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="47745-119">Nastavte možnost **Odstranit řádky otevřeného kalendáře** na **Ano**, pokud si přejete odstranit řádky otevřeného kalendáře, které mají stav životního cyklu **Vytvořeno**, pokud jsou v tomto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="47745-120">Toto nastavení je užitečné, pokud chcete vyčistit všechny otevřené plány údržby, které již nejsou pro daný majetek relevantní (například pokud majetek již není aktivní).</span><span class="sxs-lookup"><span data-stu-id="47745-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="47745-121">Stavy životního cyklu majetku, modely životního cyklu majetku a typy majetku jsou propojeny.</span><span class="sxs-lookup"><span data-stu-id="47745-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="47745-122">Používají se stejným způsobem jako stavy životního cyklu pracovních příkazů, modely životního cyklu pracovních příkazů a typy pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="47745-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="47745-123">Po vytvoření požadovaných stavů životního cyklu majetku můžete nastavit stavy životního cyklu v modelech životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="47745-124">Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Modely životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="47745-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="47745-125">Zvolte **Nový** pro vytvoření modelu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="47745-126">Do pole **Model životního cyklu** zadejte ID modelu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="47745-127">Do pole **Název** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="47745-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="47745-128">Pole **Stavy časového cyklu** zobrazuje počet stavů životního cyklu majetku, které jsou vybrány v modelu životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="47745-129">Pole **Typy majetku** zobrazuje počet typů životního cyklu majetku, které používají model životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="47745-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="47745-130">Na pevné záložce **Stavy časového cyklu** vyberte stavy životního cyklu majetku, které si přejete zahrnout v modelu životního cyklu majetku:</span><span class="sxs-lookup"><span data-stu-id="47745-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="47745-131">Chcete-li pro model použít stav životního cyklu, vyberte jej v části **Zbývající stavy životního cyklu** a potom vyberte tlačítko šipky vpravo ![Šipka vpravo](media/15-setup-for-objects.png) a přesuňte jej do části **Vybrané stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="47745-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="47745-132">Chcete-li pro model použít všechny dostupné stavy životního cyklu, vyberte tlačítko **Všechny dostupné stavy životního cyklu** ![Všechny dostupné stavy životního cyklu](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="47745-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="47745-133">Všechny stavy životního cyklu jsou převedeny do části **Vybrané stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="47745-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="47745-134">Chcete-li z modelu odebrat stav životního cyklu, vyberte jej v části **Vybrané stavy životního cyklu** a potom vyberte tlačítko šipky vlevo ![Šipka vlevo](media/16-setup-for-objects.png) a přesuňte jej do části **Zbývající stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="47745-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="47745-135">Vyberte **Aktualizace stavu životního cyklu**, chcete-li definovat stavy životního cyklu majetku, které mohou následovat po vybraném stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="47745-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="47745-136">Pevná záložka **Stav majetku** se používá, pokud manipulujete s majetkem, který obdržíte k opravě.</span><span class="sxs-lookup"><span data-stu-id="47745-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="47745-137">V sekci **Příchozí/odchozí** můžete vybrat stavy životního cyklu majetku a vyznačit tak pracovní postup majetku, který obdržíte k opravě.</span><span class="sxs-lookup"><span data-stu-id="47745-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="47745-138">Pokud nabízíte zapůjčený majetek zákazníkům nebo oddělením, můžete v sekci **Výpůjčka** vybrat stavy životního cyklu pro zapůjčený majetek.</span><span class="sxs-lookup"><span data-stu-id="47745-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
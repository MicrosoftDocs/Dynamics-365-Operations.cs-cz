---
title: Stavy životního cyklu požadavku na údržbu
description: Toto téma popisuje, jak nastavit stavy životního cyklu požadavků na údržbu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790474"
---
# <a name="maintenance-request-states"></a><span data-ttu-id="3541e-103">Stavy požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="3541e-103">Maintenance request states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3541e-104">Stavy životního cyklu požadavků údržby definují fáze, kterými může požadavek projít.</span><span class="sxs-lookup"><span data-stu-id="3541e-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="3541e-105">Příklady zahrnují **Vytvořené**, **Aktivní**a **Ukončené**.</span><span class="sxs-lookup"><span data-stu-id="3541e-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="3541e-106">Když je požadavek na údržbu převeden na pracovní příkaz, stav životního cyklu požadavku údržby by měl být aktualizován na **Ukončený** nebo **Uzavřený**, aby bylo možné označit, že požadavek na údržbu již není aktivní.</span><span class="sxs-lookup"><span data-stu-id="3541e-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="3541e-107">Na stránce seznamu **Všechny požadavky na údržbu** můžete vidět všechny požadavky na údržbu bez ohledu na jejich stav životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="3541e-108">Nastavit stavy životního cyklu požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="3541e-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="3541e-109">Vyberte **Správa majetku**\>**Nastavení**\> **Požadavky na údržbu** \>**Stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="3541e-110">Zvolte **Nový** pro vytvoření stavu životního cyklu požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="3541e-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="3541e-111">Do pole **Stav životního cyklu** zadejte ID stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="3541e-112">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="3541e-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="3541e-113">Na kartě **Podrobnosti** pole **Modely životního cyklu** zobrazuje počet modelů životního cyklu požadavku na údržbu, které používají tento stav životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="3541e-114">Na záložce **Obecné** nastavte možnost **Aktivní** na **Ano**, pokud by požadavek údržby měl být aktivní v době, kdy je v tomto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="3541e-115">Nastavte možnost **Nastavit skutečné ukončení** na **Ano**, pokud má být skutečné koncové datum a čas automaticky zadáno do požadavku údržby, který je v tomto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="3541e-116">Možnost **Vytvořit pracovní příkaz** nastavte na **Ano**, pokud lze pracovní příkaz vytvořit z požadavku na údržbu, který je v tomto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="3541e-117">Možnost **Odstranit** nastavte na **Ano**, pokud lze požadavek na údržbu odstranit v době, kdy je v tomto stavu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="3541e-118">Na kartě **Aktualizace** jsou možnosti **Příchozí** a **Odchozí** v sekci **Majetek** relevantní, pokud použijete opravu skladu. Nastavte vhodnou volbu na **ANO**, pokud stav životního cyklu majetku vybraného v požadavku na údržbu by měl být automaticky aktualizován na **Příchozí** nebo **Odchozí**, pokud je stav životního cyklu tohoto požadavku na údržbu nastaven na **Příchozí** nebo **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="3541e-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="3541e-119">Následující ilustrace znázorňuje příklad stránky **Stavy životního cyklu požadavků na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Obrázek č. 1](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="3541e-121">Stavy životního cyklu požadavků na údržbu, skupiny stavů životního cyklu a typy jsou propojeny a používány stejným způsobem jako stavy životního cyklu pracovních příkazů, skupiny stavů životního cyklu a typy.</span><span class="sxs-lookup"><span data-stu-id="3541e-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="3541e-122">Nastavit modely životního cyklu požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="3541e-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="3541e-123">Po vytvoření stavů životního cyklu, které jsou požadovány pro vaše požadavky na údržbu, je lze rozdělit do skupin stavů životního cyklu nebo do modelů životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="3541e-124">Modely životního cyklu požadavků na údržbu slouží k vytvoření toku, který lze použít pro různé typy požadavků na údržbu.</span><span class="sxs-lookup"><span data-stu-id="3541e-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="3541e-125">Je třeba vytvořit minimálně jeden standardní model životního cyklu požadavků na údržbu.</span><span class="sxs-lookup"><span data-stu-id="3541e-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="3541e-126">Vyberte **Správa majetku**\>**Nastavení**\> **Požadavky na údržbu** \>**Modely životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="3541e-127">Zvolte **Nový** pro vytvoření modelu životního cyklu požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="3541e-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="3541e-128">Do pole **Model životního cyklu** zadejte ID modelu životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="3541e-129">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="3541e-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="3541e-130">Na kartě **Podrobnosti** ukazuje položka **Stavy životního cyklu** počet stavů životního cyklu, které jsou vybrány v tomto modelu životního cyklu majetku.</span><span class="sxs-lookup"><span data-stu-id="3541e-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="3541e-131">Pole **Typy požadavků na údržbu** zobrazuje počet typů požadavků na údržbu, které používají tento model životního cyklu.</span><span class="sxs-lookup"><span data-stu-id="3541e-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="3541e-132">Na kartě **Stavy životního cyklu** vyberte stavy životního cyklu, které si přejete zahrnout v modelu životního cyklu:</span><span class="sxs-lookup"><span data-stu-id="3541e-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="3541e-133">Chcete-li v modelu životního cyklu použít stav životního cyklu, vyberte jej v části **Zbývající stavy životního cyklu** a potom vyberte tlačítko šipky vpravo ![Šipka vpravo](media/03-setup-for-requests.png) a přesuňte jej do části **Vybrané stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3541e-134">Chcete-li do modelu životního cyklu zahrnout všechny dostupné stavy životního cyklu, vyberte tlačítko **Vybrat všechny dostupné stavy** ![Vybrat všechny dostupné stavy](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="3541e-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="3541e-135">Všechny stavy životního cyklu jsou přesunuty do části **Vybrané stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3541e-136">Chcete-li z modelu životního cyklu odebrat stav životního cyklu, vyberte jej v části **Vybrané stavy životního cyklu** a potom vyberte tlačítko šipky vlevo ![Šipka vlevo](media/05-setup-for-requests.png) a přesuňte jej do části **Zbývající stavy životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="3541e-137">Na kartě **Obecné** jsou pole v části **Aktualizace** relevantní, pokud používáte opravu skladu.</span><span class="sxs-lookup"><span data-stu-id="3541e-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="3541e-138">V poli **Stav životního cyklu u přijatého majetku** vyberte stav životního cyklu majetku, kterým se má automaticky aktualizovat majetek vybraný v požadavku na údržbu, pokud je přijat k opravě.</span><span class="sxs-lookup"><span data-stu-id="3541e-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="3541e-139">V poli **Stav životního cyklu u doručeného majetku** vyberte stav životního cyklu majetku, kterým se má automaticky aktualizovat majetek vybraný v požadavku na údržbu, jakmile je vrácen po opravě.</span><span class="sxs-lookup"><span data-stu-id="3541e-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="3541e-140">Následující ilustrace znázorňuje příklad stránky **Modely životního cyklu požadavků na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="3541e-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Obrázek č. 2](media/06-setup-for-requests.png)

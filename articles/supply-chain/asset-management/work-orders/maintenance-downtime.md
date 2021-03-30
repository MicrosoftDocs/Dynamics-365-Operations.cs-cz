---
title: Prostoj údržby pro pracovní příkazy
description: Tohle téma popisuje jak vytvořit registrace prostojů údržby u majetku vybraného v pracovním příkazu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba24ae9e82debf9a67761e4e2ca0817e1645db28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209724"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="9fc2a-103">Prostoj údržby pro pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="9fc2a-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="9fc2a-104">Registrace prostojů údržby můžete vytvořit u majetku vybraného v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="9fc2a-105">Tato schopnost je užitečná v případě, že chcete zaznamenávat prostoje údržby na jednom nebo více počítačích v produkční oblasti.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="9fc2a-106">Nejprve vytvořte kódy důvodů prostojů údržby, které chcete použít, například **Rozdělení** a **Plálnované zastavení**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="9fc2a-107">Tento krok se provádí na stránce **Kódy důvodů prostojů údržby**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="9fc2a-108">Dále můžete vytvořit registrace prostojů údržby na stránce **Prostoje údržby** a přidat příslušné kódy důvodů prostoje údržby.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="9fc2a-109">Vytváření kódů důvodů prostojů údržby</span><span class="sxs-lookup"><span data-stu-id="9fc2a-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="9fc2a-110">Vyberte položky **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Kódy důvodů prostojů údržby**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="9fc2a-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-111">Select **New**.</span></span>

3. <span data-ttu-id="9fc2a-112">Do pole **Kód důvodu prostojů údržby** zadejte ID pro kód důvodu prostojů údržby.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="9fc2a-113">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="9fc2a-114">Zaškrtněte políčko **Zahrnutí KPI**, pokud by měl být kód důvodu zahrnut do výpočtů klíčových ukazatelů výkonu (KPI) pro majetek.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="9fc2a-115">Obecně platí, že by plánované zastavení výroby nemělo být zahrnuto do výpočtů ukazatelů KPI, protože neovlivňují očekávaný výkon.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="9fc2a-116">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-116">Select **Save**.</span></span>

<span data-ttu-id="9fc2a-117">Následující ilustrace znázorňuje příklad stránky **Kódy důvodu prostoje údržby**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Obrázek č. 1](media/15-work-orders.png)

<span data-ttu-id="9fc2a-119">Po vytvoření kódů důvodů prostojů údržby, které chcete použít, můžete vytvořit registrace prostojů údržby pro pracovní příkazy a majetek.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="9fc2a-120">Vytvoření registrací prostojů údržby</span><span class="sxs-lookup"><span data-stu-id="9fc2a-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="9fc2a-121">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9fc2a-122">Vyberte pracovní příkaz a pak na kartě **Pracovní příkaz** ve skupině **Majetek** vyberte **Prostoj údržby**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="9fc2a-123">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-123">Select **New**.</span></span>

4. <span data-ttu-id="9fc2a-124">Do polí **Od** a **Do** zadejte interval data a času pro registraci prostoje údržby.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="9fc2a-125">Když ponecháte pole **Do** prázdné, do pole **Doba trvání** bude automaticky vložena doba trvání v hodinách.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="9fc2a-126">V poli **Kód důvodu prostoje údržby** vyberte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="9fc2a-127">Opakováním kroků 3 až 5 přidejte další registrace.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="9fc2a-128">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-128">Select **Save**.</span></span>

<span data-ttu-id="9fc2a-129">Následující ilustrace znázorňuje příklad stránky registrace prostoje údržby.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Obrázek č. 2](media/16-work-orders.png)

<span data-ttu-id="9fc2a-131">Kalendář použitý k výpočtu registrace prostoje údržby závisí na výběru v nastavení majetku a parametrů.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="9fc2a-132">Pokud je prostředek vybrán pro majetek v poli **Prostředek** pevné záložky **Investiční majetek** na stránce **Veškerý majetek**, použije se nastavený kalendář pro přidruženou skupinu prostředků, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Obrázek č. 3](media/17-work-orders.png)

<span data-ttu-id="9fc2a-134">Není-li pro majetek vybrán žádný prostředek, použije se standardní kalendář vybraný v části **Parametry správy majetku**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Obrázek č. 4](media/18-work-orders.png)

<span data-ttu-id="9fc2a-136">Pokud chcete zobrazit přehled všech registrací prostojů údržby, klikněte na **Správa majetku** > **Dotazy** > **Prostoj údržby**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="9fc2a-137">Všechny kalendáře používané v modulu **Správa majetku** se nastavují v umístění **Správa organizace** > **Nastavení** > **Kalendáře** > **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
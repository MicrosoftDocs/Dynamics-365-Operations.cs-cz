---
title: Prostoj údržby
description: Tohle téma popisuje prostoje údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918237"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="0e80f-103">Prostoj údržby</span><span class="sxs-lookup"><span data-stu-id="0e80f-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0e80f-104">Registrace prostojů údržby můžete vytvořit u majetku vybraného v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="0e80f-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="0e80f-105">To je užitečné v případě, že chcete zaznamenávat prostoje údržby na jednom nebo více počítačích v produkční oblasti.</span><span class="sxs-lookup"><span data-stu-id="0e80f-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="0e80f-106">Nejprve vytvořte kódy důvodů prostojů údržby, které chcete použít, například porucha nebo plánované zastavení.</span><span class="sxs-lookup"><span data-stu-id="0e80f-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="0e80f-107">To se provádí v části **Kódy důvodů prostojů údržby**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="0e80f-108">Dále můžete vytvořit registrace prostojů údržby v části **Prostoje údržby** a přidat odpovídající kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="0e80f-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="0e80f-109">Vytváření kódů důvodů prostojů údržby</span><span class="sxs-lookup"><span data-stu-id="0e80f-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="0e80f-110">Klikněte na položky **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Kódy důvodů prostojů údržby**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="0e80f-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-111">Click **New**.</span></span>

3. <span data-ttu-id="0e80f-112">Do pole **Kód důvodu prostoje údržby** zadejte ID.</span><span class="sxs-lookup"><span data-stu-id="0e80f-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="0e80f-113">Do pole **Název** zadejte název kódu důvodu.</span><span class="sxs-lookup"><span data-stu-id="0e80f-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="0e80f-114">Chcete-li, aby byl kód důvodu zahrnut do výpočtů klíčového indikátoru výkonu, zaškrtněte políčko **Zahrnout do ukazatele KPI**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="0e80f-115">Obvykle by plánované zastavení výroby nemělo být zahrnuto do výpočtů ukazatelů KPI, protože neovlivňují očekávaný výkon.</span><span class="sxs-lookup"><span data-stu-id="0e80f-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="0e80f-116">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-116">Click **Save**.</span></span>

![Obrázek č. 1](media/15-work-orders.png)


<span data-ttu-id="0e80f-118">Po vytvoření kódů důvodů prostojů údržby, které chcete použít, můžete vytvořit registrace prostojů údržby pro pracovní příkazy a majetek.</span><span class="sxs-lookup"><span data-stu-id="0e80f-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="0e80f-119">Vytvoření registrací prostojů údržby</span><span class="sxs-lookup"><span data-stu-id="0e80f-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="0e80f-120">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0e80f-121">Vyberte pracovní příkaz a klikněte na položku **Prostoj údržby**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="0e80f-122">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-122">Click **New**.</span></span>

4. <span data-ttu-id="0e80f-123">Do polí **Od** a **Do** zadejte interval data a času pro registraci prostoje údržby.</span><span class="sxs-lookup"><span data-stu-id="0e80f-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="0e80f-124">Když ponecháte pole **Do** prázdné, do pole **Doba trvání** bude automaticky vložena doba trvání v hodinách.</span><span class="sxs-lookup"><span data-stu-id="0e80f-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="0e80f-125">V poli **Kód důvodu prostoje údržby** vyberte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="0e80f-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="0e80f-126">Chcete-li přidat další registrace, zopakujte kroky 3–6.</span><span class="sxs-lookup"><span data-stu-id="0e80f-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="0e80f-127">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-127">Click **Save**.</span></span>


![Obrázek č. 2](media/16-work-orders.png)


<span data-ttu-id="0e80f-129">Kalendář použitý k výpočtu registrace prostoje údržby závisí na výběru v nastavení majetku a parametrů.</span><span class="sxs-lookup"><span data-stu-id="0e80f-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="0e80f-130">Pokud je prostředek vybrán pro majetek v umístění **Všechen majetek** >  záložka s náhledem **Dlouhodobý majetek** > pole **Prostředek**, použije se nastavený kalendář pro přidruženou skupinu prostředků, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="0e80f-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Obrázek č. 3](media/17-work-orders.png)


<span data-ttu-id="0e80f-132">Není-li pro majetek vybrán žádný prostředek, použije se standardní kalendář vybraný v části **Parametry správy majetku**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="0e80f-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Obrázek č. 4](media/18-work-orders.png)


<span data-ttu-id="0e80f-134">Kliknutím na položky **Správa podnikového majetku** > **Dotazy** > **Prostoj údržby** zobrazíte přehled všech registrací prostojů údržby.</span><span class="sxs-lookup"><span data-stu-id="0e80f-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="0e80f-135">Všechny kalendáře používané v modulu **Správa majetku** se nastavují v umístění **Správa organizace** > **Nastavení** > **Kalendáře** > **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="0e80f-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>


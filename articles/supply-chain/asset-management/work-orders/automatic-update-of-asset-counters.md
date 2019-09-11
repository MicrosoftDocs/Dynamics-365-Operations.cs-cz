---
title: Automatická aktualizace čítačů majetku
description: Toto téma popisuje automatickou aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875553"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="6c643-103">Automatická aktualizace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="6c643-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6c643-104">V předchozí části je popsána ruční registrace čítačů majetku.</span><span class="sxs-lookup"><span data-stu-id="6c643-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="6c643-105">Nastavení čítačů majetku je popsáno v části [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="6c643-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="6c643-106">Hodnoty čítačů lze také automaticky aktualizovat z registrací výroby na základě výrobních hodin nebo výrobního množství.</span><span class="sxs-lookup"><span data-stu-id="6c643-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="6c643-107">To se provádí v možnosti **Aktualizace čítačů majetku**.</span><span class="sxs-lookup"><span data-stu-id="6c643-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="6c643-108">Jeden nebo více majetků lze aktualizovat vložením jednoho parametru, **Od data**.</span><span class="sxs-lookup"><span data-stu-id="6c643-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="6c643-109">Tento parametr určuje počáteční datum registrací výroby (hodiny nebo vyrobené množství), což znamená počáteční datum, od kterého se mají aktualizovat hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="6c643-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="6c643-110">Všechny majetky, které souvisejí se zdrojem *a* mají čítače majetku, které jsou nastaveny pro aktualizaci na základě vyrobeného množství nebo výrobních hodin , budou zahrnuty do automatické aktualizace a budou vytvořeny nové hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="6c643-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="6c643-111">V počtu jsou zahrnuty čítače založené na množství výroby, množství zboží a zaregistrovaném chybném množství.</span><span class="sxs-lookup"><span data-stu-id="6c643-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="6c643-112">Pokud se jednotka použitá pro registraci vyrobeného množství liší od jednotky použité v čítači, bude množství převedeno tak, aby odpovídalo jednotce čítače.</span><span class="sxs-lookup"><span data-stu-id="6c643-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="6c643-113">Jak bylo uvedeno výše, automatické čítače lze aktualizovat z registrací výroby.</span><span class="sxs-lookup"><span data-stu-id="6c643-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="6c643-114">Majetek, pro který chcete automaticky aktualizovat čítače, musí tedy souviset se zdrojem (stroj).</span><span class="sxs-lookup"><span data-stu-id="6c643-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="6c643-115">Následující popisy poskytují přehled nastavení a zpracování výrobních zakázek (v modulu **Řízení výroby**), který slouží jako základ pro automatickou aktualizaci čítačů majetku v modulu **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="6c643-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="6c643-116">Po zaregistrování vyrobeného množství nebo výrobních hodin u zdroje můžete aktualizovat související čítače majetku.</span><span class="sxs-lookup"><span data-stu-id="6c643-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="6c643-117">Klikněte na **Správa majetku** > **Periodická** > **Majetek** > **Aktualizovat čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="6c643-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="6c643-118">V poli **Od data** vyberte počáteční datum automatické aktualizace.</span><span class="sxs-lookup"><span data-stu-id="6c643-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="6c643-119">Datum v tomto poli je datem nedokončené výroby z **Transakce postupu** (**Řízení výroby** > **Dotazy a sestavy** > **Výroba** > **Transakce postupu** > **Fyzické datum**).</span><span class="sxs-lookup"><span data-stu-id="6c643-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="6c643-120">Chcete-li zvolit konkrétní majetek, typy majetku nebo zdroje pro automatickou aktualizaci, klikněte na **Filtr** na záložce s náhledem **Záznamy k zahrnutí** a proveďte příslušný výběr.</span><span class="sxs-lookup"><span data-stu-id="6c643-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="6c643-121">Pokud je to nutné, na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="6c643-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Obrázek č. 1](media/12-work-orders.png)

5. <span data-ttu-id="6c643-123">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c643-123">Click **OK**.</span></span> <span data-ttu-id="6c643-124">Po dokončení automatické aktualizace čítače majetku můžete zobrazit registrace čítačů související s majetkem v možnostech **Čítače majetku** (**Správa majetku** > **Společné** > **Majetek** > **Všechen majetek** > zvolte majatek > tlačítko **Čítače**).</span><span class="sxs-lookup"><span data-stu-id="6c643-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="6c643-125">V **součtech čítače majetku** lze získat přehled o poslední registraci provedené na všech typech čítačů na veškerém majetku.</span><span class="sxs-lookup"><span data-stu-id="6c643-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="6c643-126">Klikněte na **Správa majetku** > **Dotazy** > **Majetek** > **Agregovaná hodnota majetku**.</span><span class="sxs-lookup"><span data-stu-id="6c643-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="6c643-127">Zobrazení je velmi podobné **čítačům majetku**, ale nelze přidávat ani upravovat registrace v možnosti **Agregovaná hodnota majetku**.</span><span class="sxs-lookup"><span data-stu-id="6c643-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="6c643-128">Zobrazení je určeno pouze pro přehled.</span><span class="sxs-lookup"><span data-stu-id="6c643-128">It is for overview only.</span></span>

![Obrázek č. 2](media/13-work-orders.png)


- <span data-ttu-id="6c643-130">Je stále možné vytvořit ruční registrace hodnot čítačů pro typy čítačů, které jsou automaticky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="6c643-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="6c643-131">Další informace naleznete v části Ruční aktualizace čítačů majetku.</span><span class="sxs-lookup"><span data-stu-id="6c643-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="6c643-132">Můžete nastavit čítače související s jiným čítačem, což znamená, že při aktualizaci čítače budou související čítače automaticky aktualizovány ve stejnou dobu.</span><span class="sxs-lookup"><span data-stu-id="6c643-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="6c643-133">Informace o nastavení souvisejícch čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="6c643-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>

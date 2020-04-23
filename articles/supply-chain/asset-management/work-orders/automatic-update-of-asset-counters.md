---
title: Automatická aktualizace čítačů majetku
description: Toto téma popisuje automatickou aktualizaci čítačů majetku ve správě majetku.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209161"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="17e49-103">Automatická aktualizace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="17e49-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17e49-104">Informace o ruční registraci čítačů majetku naleznete v tématu [Ruční aktualizace čítačů majetku](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="17e49-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="17e49-105">Další informace o nastavení čítačů majetku naleznete v tématu [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="17e49-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="17e49-106">Hodnoty čítačů lze také automaticky aktualizovat z registrací výroby na základě výrobních hodin nebo výrobního množství (tj. vyrovené množství).</span><span class="sxs-lookup"><span data-stu-id="17e49-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="17e49-107">Tato aktualizace je prováděna na stránce **Aktualizovat čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="17e49-108">Jeden nebo více majetků lze aktualizovat nastavením jednoho parametru, **Od data**.</span><span class="sxs-lookup"><span data-stu-id="17e49-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="17e49-109">Tento parametr určuje počáteční datum registrací výroby (výrobní hodiny nebo výrobní množství).</span><span class="sxs-lookup"><span data-stu-id="17e49-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="17e49-110">Jinými slovy, určuje datum, od kterého se mají aktualizovat hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="17e49-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="17e49-111">Všechny majetky, které souvisejí se zdrojem *a* mají čítače majetku, které jsou nastaveny pro aktualizaci na základě vyrobeného množství nebo výrobního množství, budou zahrnuty do automatické aktualizace a budou vytvořeny nové hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="17e49-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="17e49-112">Budou vytvořeny nové hodnoty čítačů.</span><span class="sxs-lookup"><span data-stu-id="17e49-112">New counter values will be created.</span></span>

<span data-ttu-id="17e49-113">U čítačů, které jsou založeny na množství výroby, zahrnuje množství zboží i zaregistrované chybné množství.</span><span class="sxs-lookup"><span data-stu-id="17e49-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="17e49-114">Pokud se jednotka použitá pro registraci výrobního množství odlišuje od jednotky použité pro čítač, bude množství převedeno tak, aby odpovídalo jednotce čítače.</span><span class="sxs-lookup"><span data-stu-id="17e49-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="17e49-115">Jak bylo uvedeno výše, automatické čítače lze aktualizovat z registrací výroby.</span><span class="sxs-lookup"><span data-stu-id="17e49-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="17e49-116">Majetek, pro který chcete automaticky aktualizovat čítače, musí tedy souviset se zdrojem (stroj).</span><span class="sxs-lookup"><span data-stu-id="17e49-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="17e49-117">Po zaregistrování vyrobeného množství nebo výrobních hodin u zdroje můžete aktualizovat související čítače majetku.</span><span class="sxs-lookup"><span data-stu-id="17e49-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="17e49-118">Vyberte **Správa majetku** > **Periodická** > **Majetek** > **Aktualizovat čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="17e49-119">V poli **Od data** vyberte počáteční datum automatické aktualizace.</span><span class="sxs-lookup"><span data-stu-id="17e49-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="17e49-120">Datum v tomto poli je datem nedokončené výroby z **Transakce postupu** (**Řízení výroby** > **Dotazy a sestavy** > **Výroba** > **Transakce postupu** > **Fyzické datum**).</span><span class="sxs-lookup"><span data-stu-id="17e49-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="17e49-121">Na pevné záložce **Záznamy, které mají být zahrnuty** můžete vybrat konkrétní majetek, typy majetku nebo zdroje pro automatickou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="17e49-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="17e49-122">Výběrem možnosti **Filtr** proveďte příslušné výběry.</span><span class="sxs-lookup"><span data-stu-id="17e49-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="17e49-123">Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="17e49-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="17e49-124">Následující ilustrace znázorňuje příklad dialogu **Aktualizovat čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Obrázek č. 1](media/12-work-orders.png)

5. <span data-ttu-id="17e49-126">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="17e49-126">Select **OK**.</span></span> 

<span data-ttu-id="17e49-127">Po dokončení aktualizace automatického čítače majetku můžete zobrazit registrace čítačů, které souvisejí s majetkem na stránce **Čítače majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="17e49-128">Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**, vyberte majetek a pak v podokně akcí na kartě **Majetek** ve skupině **Preventivní** vyberte **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="17e49-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="17e49-129">Na stránce **Souhrnná hodnota majetku** lze získat přehled o poslední registraci provedené na všech typech čítačů na veškerém majetku.</span><span class="sxs-lookup"><span data-stu-id="17e49-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="17e49-130">Vyberte **Správa majetku** > **Dotazy** > **Majetek** > **Agregovaná hodnota majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="17e49-131">Tato stránka se podobá stránce **Čítače majetku**, ale nelze přidávat ani upravovat registrace.</span><span class="sxs-lookup"><span data-stu-id="17e49-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="17e49-132">Zobrazení je určeno pouze pro přehled.</span><span class="sxs-lookup"><span data-stu-id="17e49-132">It's for overview only.</span></span>

<span data-ttu-id="17e49-133">Následující ilustrace znázorňuje příklad stránky **Agregovaná hodnota majetku**.</span><span class="sxs-lookup"><span data-stu-id="17e49-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Obrázek č. 2](media/13-work-orders.png)

<span data-ttu-id="17e49-135">Mějte na paměti následující body:</span><span class="sxs-lookup"><span data-stu-id="17e49-135">Note the following points:</span></span>

- <span data-ttu-id="17e49-136">Je stále možné vytvořit ruční registrace hodnot čítačů pro typy čítačů, které jsou automaticky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="17e49-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="17e49-137">Další informace naleznete v části [Ruční aktualizace čítačů majetku](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="17e49-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="17e49-138">Můžete nastavit čítače, které souvisejí s jiným čítačem.</span><span class="sxs-lookup"><span data-stu-id="17e49-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="17e49-139">V takovém případě jsou při aktualizaci čítače automaticky aktualizovány související čítače.</span><span class="sxs-lookup"><span data-stu-id="17e49-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="17e49-140">Další informace o nastavení souvisejících čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="17e49-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>


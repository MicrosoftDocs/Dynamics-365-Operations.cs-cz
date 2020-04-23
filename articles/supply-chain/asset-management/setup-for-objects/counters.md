---
title: Měrný systém majetku
description: Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku.
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
ms.openlocfilehash: d128a7d20891353927441bb343831876d72aecbe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208885"
---
# <a name="counters"></a><span data-ttu-id="79a1e-103">Čítače</span><span class="sxs-lookup"><span data-stu-id="79a1e-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79a1e-104">Toto téma vysvětluje, jak vytvořit typy čítačů v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="79a1e-105">Typy čítačů majetku se používají k provádění registrací čítačů u majetku, například pokud jde o počet hodin výroby nebo množství vyrobeného majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="79a1e-106">Typy majetku souvisí s typy čítačů.</span><span class="sxs-lookup"><span data-stu-id="79a1e-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="79a1e-107">To znamená, že čítačů majetku lze použít u majetku použít pouze v případě, že je u typu majetku použitého pro daný majetek nastaven čítač majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="79a1e-108">Před provedením registrací čítače u majetku nejprve vytvořte typy čítače majetku, které chcete použít, v části **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="79a1e-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="79a1e-109">Dále můžete vytvořit registrace čítače u majetku v okně **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="79a1e-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="79a1e-110">Čítače je možné používat v plánech údržby.</span><span class="sxs-lookup"><span data-stu-id="79a1e-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="79a1e-111">Řádek Plán údržby může být typu Čítač, například v souvislosti s počtem hodin výroby nebo vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="79a1e-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="79a1e-112">Registraci čítače majetku lze aktualizovat ručně nebo automaticky na základě hodin výroby nebo vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="79a1e-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="79a1e-113">Čítač lze nastavit pro použití jedné ze tří metod aktualizace (vybraných v poli **Aktualizovat** v **čítačích**):</span><span class="sxs-lookup"><span data-stu-id="79a1e-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="79a1e-114">Ručně - hodnoty čítače je nutné registrovat ručně.</span><span class="sxs-lookup"><span data-stu-id="79a1e-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="79a1e-115">Výrobní hodiny - čítač je automaticky aktualizován na základě počtu výrobních hodin.</span><span class="sxs-lookup"><span data-stu-id="79a1e-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="79a1e-116">Množství výroby - čítač je automaticky aktualizován na základě počtu vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="79a1e-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="79a1e-117">Pokud se použije vyrobené množství, *všechny* registrované položky jsou zahrnuty do registrace čítače, dobrého množství i chybového množství.</span><span class="sxs-lookup"><span data-stu-id="79a1e-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="79a1e-118">V případě potřeby je vždy možné provést ruční registraci čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="79a1e-119">Vytvoření typů čítačů pro registrace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="79a1e-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="79a1e-120">Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="79a1e-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="79a1e-121">Zvolte **Nový** pro vytvoření nového typu čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="79a1e-122">Zadejte ID do pole **Čítač** a název čítače do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="79a1e-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="79a1e-123">Na pevné záložce **Obecné** vyberte čítač v poli **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="79a1e-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="79a1e-124">V poli **Aktualizovat** vyberte metodu aktualizace, která bude použita pro čítač.</span><span class="sxs-lookup"><span data-stu-id="79a1e-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="79a1e-125">Vyberte Ano u přepínacího tlačítka **Zdědit hodnoty čítače**, pokud má podřízený majetek ve struktuře majetku automaticky zdědit registrace čítače provedené v nadřízeném majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="79a1e-126">V poli **Agregovaný součet** vyberte metodu sumarizace, která má být použita pro čítač s použitím tohoto typu čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="79a1e-127">"Součet" je standardní výběr použitý pro nepřetržité přidávání registrovaných hodnot k celkové hodnotě.</span><span class="sxs-lookup"><span data-stu-id="79a1e-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="79a1e-128">"Průměr" lze použít, pokud je čítač nastaven na sledování prahové hodnoty, například ohledně teploty, vibrací nebo opotřebení majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="79a1e-129">Do pole **Odchylka nad** zadejte horní úroveň v procentech pro ověření, zda jsou položky ručního čítače v očekávaném rozsahu.</span><span class="sxs-lookup"><span data-stu-id="79a1e-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="79a1e-130">Ověření je založeno na lineárním nárůstu ve stávajících registracích čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="79a1e-131">Do pole **Odchylka pod** zadejte dolní úroveň v procentech pro ověření, zda jsou položky ručního čítače v očekávaném rozsahu.</span><span class="sxs-lookup"><span data-stu-id="79a1e-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="79a1e-132">Ověření je založeno na lineárním snížení ve stávajících registracích čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="79a1e-133">V poli **Typ** vyberte typ zprávy (informace, upozornění, chyba), která se zobrazí, pokud se při provádění ručních registrací čítače vyskytnou odchylky mimo definovaný rozsah.</span><span class="sxs-lookup"><span data-stu-id="79a1e-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="79a1e-134">Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly být schopny používat čítač.</span><span class="sxs-lookup"><span data-stu-id="79a1e-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="79a1e-135">Na pevné záložce **Související čítače majetku** přidejte čítač, který chcete automaticky aktualizovat při aktualizaci tohoto čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="79a1e-136">Související čítač je automaticky aktualizován pouze v případě, že má odpovídající čítač typ majetku, ke kterému se vztahuje, v nastavení měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="79a1e-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="79a1e-137">Například: nastavíte čítač na "výrobní hodiny" a přidáte typ majetku " Motor nákladního automobilu".</span><span class="sxs-lookup"><span data-stu-id="79a1e-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="79a1e-138">Při aktualizaci tohoto čítače je aktualizován také související čítač "benzín" se stejnými hodnotami čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="79a1e-139">Nastavení v poli **čítače** zahrnuje nastavení v poli "hodiny".</span><span class="sxs-lookup"><span data-stu-id="79a1e-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="79a1e-140">U čítače "Benzín" by měl být na pevnou záložku **Typy majetku** přidán typ majetku Motor nákladního automobilu pro zajištění vztahu čítače.</span><span class="sxs-lookup"><span data-stu-id="79a1e-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="79a1e-141">Na následujících snímcích obrazovky je uveden příklad nastavení v čítačích Hodiny a Benzín.</span><span class="sxs-lookup"><span data-stu-id="79a1e-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="79a1e-142">Když jsou typy majetku přidány k typu čítače v poli **Čítače**, je tento čítač automaticky přidán k typům majetku na pevné záložce v okně **čítače** v poli [Typy majetku](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="79a1e-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Obrázek č. 1](media/071-setup-for-objects.png)


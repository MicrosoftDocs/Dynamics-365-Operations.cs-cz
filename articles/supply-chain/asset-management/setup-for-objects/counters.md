---
title: Měrný systém majetku
description: Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783133"
---
# <a name="asset-measures"></a><span data-ttu-id="5a7ee-103">Mšrné systémy majetku</span><span class="sxs-lookup"><span data-stu-id="5a7ee-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5a7ee-104">Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="5a7ee-105">Typy měrných systémů majetku se používají k provádění registrací měrného systému u majetku, například pokud jde o počet hodin výroby nebo množství vyrobeného majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="5a7ee-106">Typy majetku souvisí s typy měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="5a7ee-107">To znamená, že měrný systém majetku lze použít u majetku použít pouze v případě, že je u typu majetku použitého pro daný majetek nastaven měrný systém majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="5a7ee-108">Před provedením registrací měrného systému u majetku nejprve vytvořte typy měrného systému majetku, které chcete použít, v části **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="5a7ee-109">Dále můžete vytvořit registrace měrného systému u majetku v okně **Měrný systém majetku**.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="5a7ee-110">Měrný systém majetku je možné používat v plánech údržby.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="5a7ee-111">Řádek Plán údržby může být typu Čítač, například v souvislosti s počtem hodin výroby nebo vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="5a7ee-112">Registraci měrného systému majetku lze aktualizovat ručně nebo automaticky na základě hodin výroby nebo vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="5a7ee-113">Měrný systém majetku lze nastavit pro použití jedné ze tří metod aktualizace (vybraných v poli **Aktualizovat** v **čítačích**):</span><span class="sxs-lookup"><span data-stu-id="5a7ee-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="5a7ee-114">Ručně - hodnoty měrného systému majetku je nutné registrovat ručně.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="5a7ee-115">Výrobní hodiny - čítač je automaticky aktualizován na základě počtu výrobních hodin.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="5a7ee-116">Množství výroby - čítač je automaticky aktualizován na základě počtu vyrobeného množství.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="5a7ee-117">Pokud se použije vyrobené množství, *všechny* registrované položky jsou zahrnuty do registrace měrného systému, dobrého množství i chybového množství.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="5a7ee-118">V případě potřeby je vždy možné provést ruční registraci měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="5a7ee-119">Vytvoření typů čítačů pro registrace čítačů majetku</span><span class="sxs-lookup"><span data-stu-id="5a7ee-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="5a7ee-120">Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="5a7ee-121">Zvolte **Nový** pro vytvoření nového typu měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="5a7ee-122">Zadejte ID do pole **Čítač** a název čítače do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="5a7ee-123">Na pevné záložce **Obecné** vyberte měrnou jednotku v poli **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="5a7ee-124">V poli **Aktualizovat** vyberte metodu aktualizace, která bude použita pro měrný systém majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="5a7ee-125">Vyberte Ano u přepínacího tlačítka **Zdědit hodnoty čítače**, pokud má podřízený majetek ve struktuře majetku automaticky zdědit registrace měření majetku provedené v nadřízeném majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="5a7ee-126">V poli **Agregovaný součet** vyberte metodu sumarizace, která má být použita pro měrný systém majetku s použitím tohoto typu měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="5a7ee-127">"Součet" je standardní výběr použitý pro nepřetržité přidávání registrovaných hodnot k celkové hodnotě.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="5a7ee-128">"Průměr" lze použít, pokud je měrný systém majetku nastaven na sledování prahové hodnoty, například ohledně teploty, vibrací nebo opotřebení majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="5a7ee-129">Do pole **Odchylka nad** zadejte horní úroveň v procentech pro ověření, zda jsou položky ručního měrného systému majetku v očekávaném rozsahu.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="5a7ee-130">Ověření je založeno na lineárním nárůstu ve stávajících registracích měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="5a7ee-131">Do pole **Odchylka pod** zadejte dolní úroveň v procentech pro ověření, zda jsou položky ručního měrného systému majetku v očekávaném rozsahu.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="5a7ee-132">Ověření je založeno na lineárním snížení ve stávajících registracích měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="5a7ee-133">V poli **Typ** vyberte typ zprávy (informace, upozornění, chyba), která se zobrazí, pokud se při provádění ručních registrací měrného systému majetku vyskytnou odchylky mimo definovaný rozsah.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="5a7ee-134">Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly být schopny používat měrný systém majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="5a7ee-135">Na pevné záložce **Související měrné jednotky majetku** přidejte měrné systémy majetku, který chcete automaticky aktualizovat při aktualizaci tohoto měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="5a7ee-136">Související měrný systém majetku je automaticky aktualizován pouze v případě, že má odpovídající měrný systém majetku typ majetku, ke kterému se vztahuje, v nastavení měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="5a7ee-137">Například: nastavíte měrný systém majetku na "výrobní hodiny" a přidáte typ majetku " Motor nákladního automobilu".</span><span class="sxs-lookup"><span data-stu-id="5a7ee-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="5a7ee-138">Při aktualizaci tohoto měrného systému majetku je aktualizován také související čítač "benzín" se stejnými hodnotami měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="5a7ee-139">Nastavení v poli **čítače** zahrnuje nastavení v poli "hodiny".</span><span class="sxs-lookup"><span data-stu-id="5a7ee-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="5a7ee-140">U měrného systému majetku "Benzín" by měl být na pevnou záložku **Typy majetku** přidán typ majetku Motor nákladního automobilu pro zajištění vztahu měrného systému majetku.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="5a7ee-141">Na následujících snímcích obrazovky je uveden příklad nastavení v měrném systému Hodiny a Benzín.</span><span class="sxs-lookup"><span data-stu-id="5a7ee-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="5a7ee-142">Když jsou typy majetku přidány k typu měrného systému majetku v poli **Čítače**, je tento měrný systém majetku automaticky přidán k typům majetku na pevné záložce v okně **čítače** v poli [Typy majetku](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5a7ee-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Obrázek č. 1](media/071-setup-for-objects.png)



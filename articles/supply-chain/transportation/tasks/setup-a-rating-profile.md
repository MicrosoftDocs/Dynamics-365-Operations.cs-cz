---
title: Profily sazeb
description: Toto téma popisuje, jak nastavit data pro profily sazeb.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f754a8b86b0d369af03812a831d77a8a6fa8154
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233504"
---
# <a name="rating-profiles"></a><span data-ttu-id="a2d81-103">Profily sazeb</span><span class="sxs-lookup"><span data-stu-id="a2d81-103">Rating profiles</span></span>

<span data-ttu-id="a2d81-104">Profil sazby se podobá logistické smlouvě (ale nikoli právní smlouvě).</span><span class="sxs-lookup"><span data-stu-id="a2d81-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="a2d81-105">Používá se k určení přepravních tarifů pro náklady.</span><span class="sxs-lookup"><span data-stu-id="a2d81-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="a2d81-106">Každý profil sazeb je pro dopravce jedinečný.</span><span class="sxs-lookup"><span data-stu-id="a2d81-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="a2d81-107">V profilu přidružíte dopravce k hlavní sazbě.</span><span class="sxs-lookup"><span data-stu-id="a2d81-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="a2d81-108">Hlavní sazba definuje přiřazení základní sazby a základní sazbu.</span><span class="sxs-lookup"><span data-stu-id="a2d81-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="a2d81-109">Základní sazba určuje sazbu dopravce.</span><span class="sxs-lookup"><span data-stu-id="a2d81-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="a2d81-110">Profil sazeb můžete nastavit pomocí obecné stránky, která zobrazuje přehled o všech existujících profilech.</span><span class="sxs-lookup"><span data-stu-id="a2d81-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="a2d81-111">Nebo můžete také nastavit profil sazeb přímo od dopravce.</span><span class="sxs-lookup"><span data-stu-id="a2d81-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="a2d81-112">V obou případech jsou informace, které jste pro profil hodnocení nastavili, stejné.</span><span class="sxs-lookup"><span data-stu-id="a2d81-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="a2d81-113">Vytvořte nebo upravte profil sazeb na stránce Profily sazeb</span><span class="sxs-lookup"><span data-stu-id="a2d81-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="a2d81-114">Na stránce **Profily sazeb** můžete zkontrolovat všechny dostupné profily sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="a2d81-115">Můžete také upravit stávající profily a vytvořit nové profily.</span><span class="sxs-lookup"><span data-stu-id="a2d81-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="a2d81-116">Přejděte do nabídky **Správa přepravy \> Nastavení \> Sazby \> Profily sazeb**.</span><span class="sxs-lookup"><span data-stu-id="a2d81-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="a2d81-117">V podokně akcí vyberte **Nový** pro přidání nového profilu sazeb do mřížky nebo zvolte **Upravit** pro úpravu existujícího profilu.</span><span class="sxs-lookup"><span data-stu-id="a2d81-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="a2d81-118">V řádku pro nový nebo stávající profil sazeb nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="a2d81-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="a2d81-119">**Profil sazeb** – Zadejte jedinečný identifikátor (ID) profilu sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="a2d81-120">**Název** – Zadejte popisný název profilu sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="a2d81-121">**Přepravce** - Vyberte přepravce.</span><span class="sxs-lookup"><span data-stu-id="a2d81-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="a2d81-122">Profil sazeb, který nastavujete, se také zobrazí na stránce **Přepravci** pro zvoleného přepravce.</span><span class="sxs-lookup"><span data-stu-id="a2d81-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="a2d81-123">**Pracoviště** a **Sklad** - Vyberte pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="a2d81-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="a2d81-124">**Výpočet přepravních sazeb** - Vyberte výpočet přepravních sazeb pro profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="a2d81-125">**Hlavní sazba** - Vyberte hlavní sazbu pro profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="a2d81-126">Můžete použít základní sazbu k definování základního typu sazby a hlavní sazby.</span><span class="sxs-lookup"><span data-stu-id="a2d81-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="a2d81-127">Další informace naleznete v tématu [Nastavení hlavních sazeb](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="a2d81-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="a2d81-128">**Modul mezioperačního času** - Vyberte modul mezioperačního času pro profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="a2d81-129">**Index paliva dopravce** - Vyberte index paliva dopravce pro profil hodnocení.</span><span class="sxs-lookup"><span data-stu-id="a2d81-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="a2d81-130">**Počáteční datum a čas platnosti** a **Koncové datum a čas platnosti** - Definujte období, kdy by měl být aktivní profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="a2d81-131">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a2d81-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="a2d81-132">Vytvořte profil sazeb přímo na stránce Přepravci</span><span class="sxs-lookup"><span data-stu-id="a2d81-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="a2d81-133">Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.</span><span class="sxs-lookup"><span data-stu-id="a2d81-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="a2d81-134">V seznamu vyberte přepravce.</span><span class="sxs-lookup"><span data-stu-id="a2d81-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="a2d81-135">Na záložce s náhledem **Profily sazeb** vyberte **Nový** a vytvořte profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="a2d81-136">Nastavte pole pro nový profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2d81-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="a2d81-137">Tato pole odpovídají polím na stránce **Profily sazeb**, jak je popsáno v předchozí části tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="a2d81-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d81-138">Profily, které jsou vytvořeny na stránce **Přepravci**, se také zobrazují na stránce **Profily sazeb**.</span><span class="sxs-lookup"><span data-stu-id="a2d81-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
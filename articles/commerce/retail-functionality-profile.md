---
title: Vytvoření funkčního profilu maloobchodu
description: Toto téma popisuje, jak vytvořit nový maloobchodní funkční profil v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002836"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="15f3e-103">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="15f3e-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="15f3e-104">Toto téma popisuje, jak vytvořit nový maloobchodní funkční profil v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15f3e-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15f3e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="15f3e-105">Overview</span></span>

<span data-ttu-id="15f3e-106">Maloobchodní funkční profil poskytuje různá nastavení používaná pro online kanály.</span><span class="sxs-lookup"><span data-stu-id="15f3e-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="15f3e-107">Každý maloobchodní kanál musí určovat maloobchodní funkční profil.</span><span class="sxs-lookup"><span data-stu-id="15f3e-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="15f3e-108">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="15f3e-108">Create a retail functionality profile</span></span>

<span data-ttu-id="15f3e-109">Při vytváření nového maloobchodního funkčního profilu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="15f3e-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="15f3e-110">V navigačním podokně přejděte na **Moduly \> Nastavení kanálu \> Profily POS \> Profily funkcí**.</span><span class="sxs-lookup"><span data-stu-id="15f3e-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="15f3e-111">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="15f3e-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="15f3e-112">V poli **Profil** zadejte ID profilu ("FN006" v níže uvedeném příkladu obrázku).</span><span class="sxs-lookup"><span data-stu-id="15f3e-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="15f3e-113">Do pole **popis** zadejte hodnotu ("profil Adventure Works" v následujícím příkladu obrázku).</span><span class="sxs-lookup"><span data-stu-id="15f3e-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="15f3e-114">V části **obecné** vyberte zemi pro národní prostředí **ISO**.</span><span class="sxs-lookup"><span data-stu-id="15f3e-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="15f3e-115">V části **Obecné** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="15f3e-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="15f3e-116">V části **Obecné** vyberte **ID profilu účtenky** pro příjem e-mailů.</span><span class="sxs-lookup"><span data-stu-id="15f3e-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="15f3e-117">V části **Funkce** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="15f3e-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="15f3e-118">V části **částka** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="15f3e-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="15f3e-119">V části **Informační kódy** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="15f3e-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="15f3e-120">V části **Číslování příjmu** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="15f3e-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="15f3e-121">Následující obrázek znázorňuje příklad funkčního profilu maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="15f3e-121">The following image shows an example retail functionality profile.</span></span>
  
![Příklad maloobchodního funkčního profilu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="15f3e-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="15f3e-123">Additional resources</span></span>

[<span data-ttu-id="15f3e-124">Informační kódy a skupiny informačních kódů</span><span class="sxs-lookup"><span data-stu-id="15f3e-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="15f3e-125">Vytvoření nového adresáře</span><span class="sxs-lookup"><span data-stu-id="15f3e-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="15f3e-126">Přehled rozložení obrazovky</span><span class="sxs-lookup"><span data-stu-id="15f3e-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="15f3e-127">Konfigurace a instalace Retail hardware station</span><span class="sxs-lookup"><span data-stu-id="15f3e-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 

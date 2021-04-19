---
title: Vytvoření funkčního profilu maloobchodu
description: Toto téma popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791990"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="eedc6-103">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="eedc6-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eedc6-104">Toto téma popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eedc6-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="eedc6-105">Funkční profil Commerce poskytuje různá nastavení používaná pro online kanály.</span><span class="sxs-lookup"><span data-stu-id="eedc6-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="eedc6-106">Každý kanál musí určovat funkční profil.</span><span class="sxs-lookup"><span data-stu-id="eedc6-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="eedc6-107">Vytvořit funkční profil</span><span class="sxs-lookup"><span data-stu-id="eedc6-107">Create a functionality profile</span></span>

<span data-ttu-id="eedc6-108">Při vytváření nového funkčního profilu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="eedc6-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="eedc6-109">V navigačním podokně přejděte na **Moduly \> Nastavení kanálu \> Profily POS \> Profily funkcí**.</span><span class="sxs-lookup"><span data-stu-id="eedc6-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="eedc6-110">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="eedc6-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="eedc6-111">V poli **Profil** zadejte ID profilu ("FN006" v níže uvedeném příkladu obrázku).</span><span class="sxs-lookup"><span data-stu-id="eedc6-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="eedc6-112">Do pole **popis** zadejte hodnotu ("profil Adventure Works" v následujícím příkladu obrázku).</span><span class="sxs-lookup"><span data-stu-id="eedc6-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="eedc6-113">V části **obecné** vyberte zemi pro národní prostředí **ISO**.</span><span class="sxs-lookup"><span data-stu-id="eedc6-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="eedc6-114">V části **Obecné** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="eedc6-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="eedc6-115">V části **Obecné** vyberte **ID profilu účtenky** pro příjem e-mailů.</span><span class="sxs-lookup"><span data-stu-id="eedc6-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="eedc6-116">V části **Funkce** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="eedc6-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="eedc6-117">V části **částka** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="eedc6-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="eedc6-118">V části **Informační kódy** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="eedc6-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="eedc6-119">V části **Číslování příjmu** upravte podle potřeby další nastavení.</span><span class="sxs-lookup"><span data-stu-id="eedc6-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="eedc6-120">Následující obrázek znázorňuje příklad funkčního profilu.</span><span class="sxs-lookup"><span data-stu-id="eedc6-120">The following image shows an example functionality profile.</span></span>
  
![Příklad funkčního profilu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="eedc6-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="eedc6-122">Additional resources</span></span>

[<span data-ttu-id="eedc6-123">Informační kódy a skupiny informačních kódů</span><span class="sxs-lookup"><span data-stu-id="eedc6-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="eedc6-124">Vytvoření nového adresáře</span><span class="sxs-lookup"><span data-stu-id="eedc6-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="eedc6-125">Přehled rozložení obrazovky</span><span class="sxs-lookup"><span data-stu-id="eedc6-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="eedc6-126">Konfigurace a instalace Retail hardware station</span><span class="sxs-lookup"><span data-stu-id="eedc6-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

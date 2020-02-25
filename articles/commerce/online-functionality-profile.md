---
title: Vytvoření online funkčního profilu
description: Toto téma popisuje, jak vytvořit nový online funkční profil v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003365"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="33a92-103">Vytvoření online funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="33a92-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="33a92-104">Toto téma obsahuje přehled nastavení online funkčních profilů pro Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33a92-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="33a92-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="33a92-105">Overview</span></span>

<span data-ttu-id="33a92-106">Profil online funkcí poskytuje různá nastavení používaná pro online kanály.</span><span class="sxs-lookup"><span data-stu-id="33a92-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="33a92-107">Každý online kanál musí určovat profil online funkcí.</span><span class="sxs-lookup"><span data-stu-id="33a92-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="33a92-108">Vytvoření online funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="33a92-108">Create an online functionality profile</span></span>

<span data-ttu-id="33a92-109">Následující postup vysvětluje, jak vytvořit online profil funkcí z aplikace Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="33a92-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="33a92-110">V navigačním podokně přejděte na **Moduly \> Nastavení kanálu \> Nastavení online obchodu \> Profily funkcí**.</span><span class="sxs-lookup"><span data-stu-id="33a92-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="33a92-111">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="33a92-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="33a92-112">V poli **Profil** zadejte ID profilu.</span><span class="sxs-lookup"><span data-stu-id="33a92-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="33a92-113">Do pole **popis** zadejte hodnotu ("profil Adventure Works" v následujícím příkladu obrázku).</span><span class="sxs-lookup"><span data-stu-id="33a92-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="33a92-114">V části **Funkce** upravte podle potřeby nastavení **KOšíK**, **ZáKAZNíCI MALOOBCHODU** nebo **POKLADNA**.</span><span class="sxs-lookup"><span data-stu-id="33a92-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="33a92-115">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="33a92-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="33a92-116">Následující obrázek znázorňuje příklad online funkčního profilu.</span><span class="sxs-lookup"><span data-stu-id="33a92-116">The following image shows an example online functionality profile.</span></span>
  
![Příklad online funkčního profilu](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="33a92-118">Funkce</span><span class="sxs-lookup"><span data-stu-id="33a92-118">Functions</span></span>

- <span data-ttu-id="33a92-119">**Agregované produkty** Pokud je tato funkce povolena, umožňuje košíku aktualizovat množství při vícenásobném přidání stejné položky.</span><span class="sxs-lookup"><span data-stu-id="33a92-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="33a92-120">**Povolit rezervaci bez plateb**: Pokud je tato funkce povolena, zpracuje scénář, kdy položky přidané do vozíku mají cenu 0.00 USD.</span><span class="sxs-lookup"><span data-stu-id="33a92-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="33a92-121">**Vytvořit odběratele v asynchronním režimu**: Toto nastavení je zastaralé pro kanály elektronického obchodu třetí strany a není použitelné pro web Dynamics 365 e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="33a92-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33a92-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="33a92-122">Additional resources</span></span>

[<span data-ttu-id="33a92-123">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="33a92-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="33a92-124">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="33a92-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="33a92-125">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="33a92-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="33a92-126">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="33a92-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="33a92-127">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="33a92-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)

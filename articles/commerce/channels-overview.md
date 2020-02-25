---
title: Přehled kanálů
description: Toto téma poskytuje přehled kanálů v Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002351"
---
# <a name="channels-overview"></a><span data-ttu-id="5e1a0-103">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="5e1a0-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5e1a0-104">Toto téma poskytuje přehled kanálů v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="5e1a0-105">Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení každého kanálu.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="5e1a0-106">Typy kanálů</span><span class="sxs-lookup"><span data-stu-id="5e1a0-106">Types of Channels</span></span>

<span data-ttu-id="5e1a0-107">Dynamics 365 Commerce podporuje tři různé typy kanálů: maloobchodní, kontaktní a online kanály.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="5e1a0-108">Maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="5e1a0-108">Retail channels</span></span>

<span data-ttu-id="5e1a0-109">Maloobchodní kanály představují standardní kamenné obchody.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="5e1a0-110">Každý obchod může mít vlastní pokladní místo (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="5e1a0-111">Kanály kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5e1a0-111">Call center channels</span></span>

<span data-ttu-id="5e1a0-112">Kanály kontaktního střediska reprezentují objednávku střediska volání a řízení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="5e1a0-113">Online kanály</span><span class="sxs-lookup"><span data-stu-id="5e1a0-113">Online channels</span></span>

<span data-ttu-id="5e1a0-114">Online kanály představují online poutače e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="5e1a0-115">Po vytvoření online kanálu je nutné vytvořit web pomocí nástroje Microsoft Dynamics 365 Commerce Site Builder nebo jiného řešení e-Commerce třetí strany.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="5e1a0-116">Základy nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-116">Channel setup basics</span></span>

<span data-ttu-id="5e1a0-117">Nastavení kanálu se provádí v nástroji Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="5e1a0-118">Každý kanál může mít vlastní metody platby, cenové skupiny, hierarchie produktů, sortimenty a sadu produktů.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="5e1a0-119">Po vytvoření kanálu přiřadíte produkty, které má obsahovat a prodávat.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="5e1a0-120">Každý typ kanálu má jedinečnou sadu funkcí, které je nutné nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="5e1a0-121">Maloobchodní kanál například vyžaduje přiřazení zaměstnanců, registrů a odběratelů.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="5e1a0-122">Jakmile je vytvořen nový kanál, musí být přiřazen k organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="5e1a0-123">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-123">Channel setup prerequisites</span></span>

<span data-ttu-id="5e1a0-124">Před nastavením kanálu je nutné dokončit některé požadované úkoly na základě typu kanálu.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="5e1a0-125">Další informace naleznete v tématu [Předpoklady pro nastavení kanálů](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5e1a0-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="5e1a0-126">Nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-126">Set up a channel</span></span>

<span data-ttu-id="5e1a0-127">Po dokončení požadovaných úloh proveďte další pokyny k instalaci aplikace pomocí následujících odkazů.</span><span class="sxs-lookup"><span data-stu-id="5e1a0-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="5e1a0-128">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="5e1a0-129">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5e1a0-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="5e1a0-130">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="5e1a0-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5e1a0-131">Additional resources</span></span>

[<span data-ttu-id="5e1a0-132">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5e1a0-133">Nastavení maloobchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="5e1a0-134">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="5e1a0-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="5e1a0-135">Nastavení kanálu kontaktního střediska</span><span class="sxs-lookup"><span data-stu-id="5e1a0-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="5e1a0-136">Nastavení organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="5e1a0-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

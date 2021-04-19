---
title: Vytvářejte hierarchie modelování org pro organizace B2B
description: Toto téma popisuje, jak vytvořit hierarchie organizačního modelování pro organizace business-to-business (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799822"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="4c29a-103">Vytvářejte hierarchie modelování org pro organizace B2B</span><span class="sxs-lookup"><span data-stu-id="4c29a-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c29a-104">Toto téma popisuje, jak vytvořit hierarchie organizačního modelování pro organizace business-to-business (B2B) v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c29a-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4c29a-105">V centrále Commerce jsou organizace obchodních partnerů reprezentovány entitami zákazníků a entitami hierarchie zákazníků.</span><span class="sxs-lookup"><span data-stu-id="4c29a-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="4c29a-106">Organizace obchodního partnera a její uživatelé jsou reprezentováni jako zákazníci a hierarchie zákazníků se používají k přidružení těchto zákazníků k sobě navzájem.</span><span class="sxs-lookup"><span data-stu-id="4c29a-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="4c29a-107">Po schválení požadavku obchodního partnera na připojení k webu elektronického obchodování B2B se provedou následující akce:</span><span class="sxs-lookup"><span data-stu-id="4c29a-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="4c29a-108">V systému jsou vytvořeny dva nové záznamy o zákaznících: záznam zákazníka **Typ organizace** pro organizaci obchodního partnera a **Typ osoba** pro žadatele (tzn. obchodního partnera, který podal žádost).</span><span class="sxs-lookup"><span data-stu-id="4c29a-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="4c29a-109">Nový záznam hierarchie zákazníků je vytvořen v **Zákazník \> Hierarchie zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="4c29a-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="4c29a-110">Tento záznam má následující vlastnosti záhlaví:</span><span class="sxs-lookup"><span data-stu-id="4c29a-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="4c29a-111">**ID hierarchie zákazníků** - Jedinečné ID pro hierarchii zákazníků.</span><span class="sxs-lookup"><span data-stu-id="4c29a-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="4c29a-112">Toto ID používá číselnou sekvenci, která je definována ve sdílených parametrech Commerce v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c29a-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="4c29a-113">**Název** - Název organizace obchodního partnera, jak je uveden v žádosti o přihlášení.</span><span class="sxs-lookup"><span data-stu-id="4c29a-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="4c29a-114">**Účel** - Tato vlastnost je nastavena na předdefinovanou hodnotu **B2B organizace**.</span><span class="sxs-lookup"><span data-stu-id="4c29a-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="4c29a-115">**Organizace** - zákaznické ID obchodního partnera.</span><span class="sxs-lookup"><span data-stu-id="4c29a-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="4c29a-116">Zde jsou podrobnosti záznamu hierarchie zákazníků:</span><span class="sxs-lookup"><span data-stu-id="4c29a-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="4c29a-117">Záznam zákazníka - žadatele - je spojen s hierarchií zákazníků.</span><span class="sxs-lookup"><span data-stu-id="4c29a-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="4c29a-118">Role správce je přidružena k žadateli.</span><span class="sxs-lookup"><span data-stu-id="4c29a-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="4c29a-119">Když správce přidá více uživatelů do organizace obchodního partnera na webu B2B, vytvoří se v centrále Commerce nový záznam zákazníka pro každého uživatele.</span><span class="sxs-lookup"><span data-stu-id="4c29a-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="4c29a-120">Tento záznam zákazníka je také přidán do příslušného záznamu hierarchie zákazníků obchodního partnera a má roli „uživatele“.</span><span class="sxs-lookup"><span data-stu-id="4c29a-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="4c29a-121">Ve většině případů by se měly odpovídající hodnoty vlastností všech záznamů zákazníků v hierarchii shodovat.</span><span class="sxs-lookup"><span data-stu-id="4c29a-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="4c29a-122">Například proto, že všichni uživatelé obchodních partnerů by měli získat podobné ceny produktů, jejich cenová skupina a související konfigurace by se měly shodovat.</span><span class="sxs-lookup"><span data-stu-id="4c29a-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="4c29a-123">Systém však tuto konzistenci nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="4c29a-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="4c29a-124">Příslušní uživatelé centrály Commerce jsou proto zodpovědní za zajištění shody hodnot vlastností a konfigurací pro všechny zákazníky v dané hierarchii.</span><span class="sxs-lookup"><span data-stu-id="4c29a-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="4c29a-125">Uživatelé centrály Commerce se mohou podívat na hodnoty vlastností pro všechny záznamy zákazníků v hierarchii v souběžném zobrazení.</span><span class="sxs-lookup"><span data-stu-id="4c29a-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="4c29a-126">Vyberte příslušné vlastnosti záznamu zákazníka výběrem názvů karet v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="4c29a-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="4c29a-127">Uživatelé mohou přímo prohlížet a upravovat hodnoty vlastností z tohoto zobrazení.</span><span class="sxs-lookup"><span data-stu-id="4c29a-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="4c29a-128">Alternativně, pokud chcete použít všechny hodnoty ze záznamu zákazníka správce na všechny záznamy zákazníků uživatele, vyberte **Přepsat** v podrobnostech hierarchie zákazníků.</span><span class="sxs-lookup"><span data-stu-id="4c29a-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c29a-129">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4c29a-129">Additional resources</span></span>

[<span data-ttu-id="4c29a-130">Nastavení webu elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="4c29a-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="4c29a-131">Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="4c29a-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="4c29a-132">Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="4c29a-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="4c29a-133">Nastavte limity množství produktů pro weby B2B elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="4c29a-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
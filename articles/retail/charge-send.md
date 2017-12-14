---
title: "Dodání objednávky z jiného obchodu"
description: "Toto téma popisuje funkci odeslání nákladů."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: cs-cz
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="87b97-103">Dodání objednávky z jiného obchodu</span><span class="sxs-lookup"><span data-stu-id="87b97-103">Ship an order from a different store</span></span>

<span data-ttu-id="87b97-104">Díky funkci odeslání nákladů v aplikaci Dynamics 365 for Retail mohou být objednávky odběratele provedeny v jednom obchodě a expedovány z jiného obchodu.</span><span class="sxs-lookup"><span data-stu-id="87b97-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="87b97-105">Objednávky odběratele v klientovi pokladního místa (POS) podporují více možností plnění.</span><span class="sxs-lookup"><span data-stu-id="87b97-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="87b97-106">Některé příklady možností plnění zahrnují:</span><span class="sxs-lookup"><span data-stu-id="87b97-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="87b97-107">Vyzvednutí ze stejného obchodu v jiné datum.</span><span class="sxs-lookup"><span data-stu-id="87b97-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="87b97-108">Vyzvednutí z jiného obchodu ve stejné nebo jiné datum.</span><span class="sxs-lookup"><span data-stu-id="87b97-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="87b97-109">Odeslání z výchozího expedičního skladu, který je přiřazen k obchodu, a doručení v určené datum.</span><span class="sxs-lookup"><span data-stu-id="87b97-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="87b97-110">Funkce odeslání nákladů používá následující operace POS: Expedovat všechny produkty a Expedovat vybrané produkty.</span><span class="sxs-lookup"><span data-stu-id="87b97-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="87b97-111">To umožňuje pracovníkovi obchodu zvolit místo expedice, odkud lze plnit objednávku nebo řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="87b97-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="87b97-112">Místo expedice ve výchozím nastavení je expediční sklad, který je přidružen k obchodu.</span><span class="sxs-lookup"><span data-stu-id="87b97-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="87b97-113">Pracovník obchodu však může změnit toto místo a zvolit jakýkoliv obchod definovaný ve skupině lokátorů obchodů, která je přiřazená k obchodu.</span><span class="sxs-lookup"><span data-stu-id="87b97-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="87b97-114">Možnost vybrat adresy pro dodání zůstává nezměněna.</span><span class="sxs-lookup"><span data-stu-id="87b97-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="87b97-115">Způsoby dodání, které lze použít k plnění řádku objednávky, jsou založeny na konfiguraci platných způsobů dodání pro produkty a adresy.</span><span class="sxs-lookup"><span data-stu-id="87b97-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="87b97-116">Protože pravidla pro platné způsoby dodání se udržují pouze v modulu Retail headquarters (HQ), klient POS zavolá v reálném čase pro načtení platných způsobů dodání pro řádek expedice.</span><span class="sxs-lookup"><span data-stu-id="87b97-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


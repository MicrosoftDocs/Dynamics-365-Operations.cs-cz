---
title: Prodej a návrat produktů, které nejsou součástí sortimentu obchodu
description: V aplikaci Dynamics 365 Commerce můžete prodávat a vracet produkty mimo sortiment.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4f0801828086a7c5cc316895b5426a184a345ce1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982387"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="09fa4-103">Prodej a návrat produktů, které nejsou součástí sortimentu obchodu</span><span class="sxs-lookup"><span data-stu-id="09fa4-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09fa4-104">Běžným scénářem pro prodejce je prodej produktů zákazníkům nebo příjem vrácených produktů od zákazníků i v případě, že ve svém obchodě nemají konkrétní produkty (jinými slovy, produkty nejsou do obchodu dodány).</span><span class="sxs-lookup"><span data-stu-id="09fa4-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="09fa4-105">Zde jsou některé typické scénáře:</span><span class="sxs-lookup"><span data-stu-id="09fa4-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="09fa4-106">Maloobchodní prodejce nemá všechny produkty v konkrétním obchodě.</span><span class="sxs-lookup"><span data-stu-id="09fa4-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="09fa4-107">Zbývající produkty jsou uloženy ve skladu.</span><span class="sxs-lookup"><span data-stu-id="09fa4-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="09fa4-108">Zaměstnanec obchodu může zákazníkům pomáhat pomocí vyhledávání a procházení produktů ve skladě, přidávání do košíku a dokončení platby výběrem způsobu dodání, jako je například dodání na adresu ze skladu nebo umožnění zákazníkovi vyzvednout produkt z aktuálního obchodu nebo z jiného obchodu.</span><span class="sxs-lookup"><span data-stu-id="09fa4-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="09fa4-109">Prodejce nemá konkrétní produkty ve svém obchodě nebo je nemá na skladě v obchodě, který zákazník navštívil, ale produkty jsou k dispozici v jiných obchodech.</span><span class="sxs-lookup"><span data-stu-id="09fa4-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="09fa4-110">Zaměstnanec obchodu může pomoci zákazníkovi vyhledáním a procházením produktů v jiném obchodě, jejich přidáním do nákupního košíku a dokončením rezervace výběrem způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="09fa4-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="09fa4-111">Prodejce má více obchodů v konkrétním městě nebo na konkrétním poštovním směrovacím čísle a nechce nutit zákazníky, aby vraceli produkty do stejného obchodu, kde nakupovali.</span><span class="sxs-lookup"><span data-stu-id="09fa4-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="09fa4-112">Místo toho mohou zákazníci vracet produkty v libovolném obchodě.</span><span class="sxs-lookup"><span data-stu-id="09fa4-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="09fa4-113">Běžné scénáře jsou k dispozici pro prodejce používající aplikaci Commerce.</span><span class="sxs-lookup"><span data-stu-id="09fa4-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="09fa4-114">V aplikaci Commerce můžete:</span><span class="sxs-lookup"><span data-stu-id="09fa4-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="09fa4-115">Vyhledávat nebo procházet produkty v dalších obchodech.</span><span class="sxs-lookup"><span data-stu-id="09fa4-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="09fa4-116">Vyhledávat nebo procházet všechny vydané produkty.</span><span class="sxs-lookup"><span data-stu-id="09fa4-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="09fa4-117">Vytvářet objednávky a transakce nebo objednávky cash-and-carry.</span><span class="sxs-lookup"><span data-stu-id="09fa4-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="09fa4-118">Vybírat možnosti dodání pro objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="09fa4-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="09fa4-119">Vyskladňovat produkty v aktuálním obchodě nebo jiném obchodě.</span><span class="sxs-lookup"><span data-stu-id="09fa4-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="09fa4-120">Zrušit objednávku v aktuálním obchodě nebo jiném obchodě.</span><span class="sxs-lookup"><span data-stu-id="09fa4-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="09fa4-121">Vrátit objednávku s či bez příjmu v aktuálním obchodě nebo jiném obchodě.</span><span class="sxs-lookup"><span data-stu-id="09fa4-121">Return an order with or without the receipt at the current store or another store.</span></span>

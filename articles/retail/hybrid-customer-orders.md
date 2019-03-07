---
title: Hybridní objednávky odběratele
description: Hybridní objednávka odběratele je jedna objednávka, která obsahuje produkty, které si může zákazník odnést z obchodu, jakož i výrobky, které budou dodány nebo vyzvednuty později.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a00e69a589ffe744f88edb6a8b3709c4029fc1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "364320"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="62998-103">Hybridní objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="62998-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62998-104">Hybridní objednávka odběratele je jedna objednávka, která obsahuje produkty, které si může zákazník odnést z obchodu, jakož i výrobky, které budou dodány nebo vyzvednuty později.</span><span class="sxs-lookup"><span data-stu-id="62998-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="62998-105">V aplikaci Microsoft Dynamics 365 for Retail můžete u objednávky odběratele vybrat realizaci všech produktů nebo vybraných produktů.</span><span class="sxs-lookup"><span data-stu-id="62998-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="62998-106">Řádky produktu označené jako řádky k provedení, jsou automaticky fakturovány po vytvoření objednávky. Podobně to platí pro objednávku, která má být vyzvednuta po vytvoření objednávky.</span><span class="sxs-lookup"><span data-stu-id="62998-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="62998-107">Částka splatná u hybridních objednávek je určena přidáním procenta zálohy k řádkám produktu pro vyskladnění a dodávku s plnou částkou prováděcích linek.</span><span class="sxs-lookup"><span data-stu-id="62998-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="62998-108">U hybridních objednávek systém přepíná mezi režimem objednávky zákazníka a režimem Cash and Carry takto:</span><span class="sxs-lookup"><span data-stu-id="62998-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="62998-109">Pokud mají všechny produkty v košíku hodnotu **Provádět dodávku**, objednávka bude zpracovávána jako transakce Cash and Carry.</span><span class="sxs-lookup"><span data-stu-id="62998-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="62998-110">Pokud některé nebo všechny řádky v košíku jsou nastaveny na hodnotu **Vybrat** nebo **Expedice dodávky**, objednávka bude zpracovávána jako transakce objednávky zákazníka.</span><span class="sxs-lookup"><span data-stu-id="62998-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="62998-111">Pokud je vybrán řádek nákupního košíku a je vybraná možnost **Zvolené vyskladnění**, **Vybraná expedice**, nebo **Vyvézt vybrané**, je s touto metodu doručení nastaven pouze konkrétní řádek košíku.</span><span class="sxs-lookup"><span data-stu-id="62998-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="62998-112">V takovém případě bude tok operace pokračovat obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="62998-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="62998-113">Pokud jsou ale možnost **Zvolené vyskladnění**, **Vybraná expedice**, nebo **Vyvézt vybrané** vybrány bez výběru řádku košíku, otevře se nová stránka se seznamem všech řádků košíku.</span><span class="sxs-lookup"><span data-stu-id="62998-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="62998-114">Na této obrazovce můžete vybrat více řádků najednou k nastavení způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="62998-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="62998-115">Při použití této metody pro výběr řádků bude přepsána jakákoli předchozí metoda doručení, která byla přiřazena k řádku.</span><span class="sxs-lookup"><span data-stu-id="62998-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62998-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="62998-116">Additional resources</span></span>

[<span data-ttu-id="62998-117">Přehled objednávek zákazníka</span><span class="sxs-lookup"><span data-stu-id="62998-117">Customer orders overview</span></span>](customer-orders-overview.md)

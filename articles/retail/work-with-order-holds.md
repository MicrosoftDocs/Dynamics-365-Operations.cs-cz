---
title: "Blokování objednávky"
description: "Toto téma popisuje blokování objednávek v aplikaci Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="order-holds"></a><span data-ttu-id="1346f-103">Blokování objednávky</span><span class="sxs-lookup"><span data-stu-id="1346f-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1346f-104">Toto téma popisuje blokování objednávek v aplikaci Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1346f-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1346f-105">Objednávky mohou být blokovány z různých důvodů.</span><span class="sxs-lookup"><span data-stu-id="1346f-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="1346f-106">Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele.</span><span class="sxs-lookup"><span data-stu-id="1346f-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="1346f-107">Během prodejního procesu se stává, že prodejní objednávky musí být blokovány.</span><span class="sxs-lookup"><span data-stu-id="1346f-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="1346f-108">Například prodejní objednávka může být blokována kvůli potížím s platbou odběratele kvůli podezření z podvodu nebo kvůli nutné kontrole správcem.</span><span class="sxs-lookup"><span data-stu-id="1346f-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="1346f-109">Při blokování prodejní objednávky můžete určit důvody pro blokování prodejní objednávky přiřazením kódu prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="1346f-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="1346f-110">Kódy blokování prodejních objednávek se konfigurují v nabídce **Prodej a marketing** &gt; **Konfigurace** &gt; **Prodejní objednávky** &gt; **Kódy blokování objednávek**.</span><span class="sxs-lookup"><span data-stu-id="1346f-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="1346f-111">Prodejní objednávku můžete blokovat ručně v době vytvoření objednávky nebo později.</span><span class="sxs-lookup"><span data-stu-id="1346f-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="1346f-112">Navíc objednávku můžete blokovat automaticky na základě pravidel o podvodu.</span><span class="sxs-lookup"><span data-stu-id="1346f-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="1346f-113">Zatímco je prodejní objednávka blokována, může ji aktualizovat dalšími informacemi.</span><span class="sxs-lookup"><span data-stu-id="1346f-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="1346f-114">Případně můžete zkontrolovat prodejní objednávku, a pokračovat v práci na ní.</span><span class="sxs-lookup"><span data-stu-id="1346f-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="1346f-115">Prodejní objednávku můžete zkontrolovat, zkontrolovat ji po přijetí, a dokonce i přebít kontrolu jiným uživatelem pomocí pracovní plochy pro blokování objednávky (**Maloobchodní prodej** &gt; **Odběratelé** &gt; **Blokování objednávek**).</span><span class="sxs-lookup"><span data-stu-id="1346f-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="1346f-116">Když je objednávka hotová k dokončení, je nutné odebrat blokování před dokončením zpracování objednávek.</span><span class="sxs-lookup"><span data-stu-id="1346f-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>





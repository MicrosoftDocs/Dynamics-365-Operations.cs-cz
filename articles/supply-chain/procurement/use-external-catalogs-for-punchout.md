---
title: "Použití externích katalogů pro funkci PunchOut eProcurement"
description: "Toto téma vysvětluje, jak lze použít externí katalogy k vytvoření a odeslání požadavků."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 577204b49355a470769237eb46ad74e7f319a55e
ms.openlocfilehash: a81382e19a0d9446a419402d8fa8a00ca66c3378
ms.contentlocale: cs-cz
ms.lasthandoff: 01/15/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="d9d28-103">Použití externích katalogů pro funkci PunchOut eProcurement</span><span class="sxs-lookup"><span data-stu-id="d9d28-103">Use external catalogs for PunchOut eProcurement</span></span>
<span data-ttu-id="d9d28-104">Díky externím katalogům elektronického nákupu PunchOut nemusíte spravovat informace o produktech svých dodavatelů ve svých hlavních datech.</span><span class="sxs-lookup"><span data-stu-id="d9d28-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="d9d28-105">Místo toho je nákupní košík na webu dodavatele převeden na řádky požadavku, které mají správné informace o produktu.</span><span class="sxs-lookup"><span data-stu-id="d9d28-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="d9d28-106">Měli byste se vyhnout udržování popisů a cen produktů svých dodavatelů v hlavních datech svých produktů.</span><span class="sxs-lookup"><span data-stu-id="d9d28-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="d9d28-107">Místo toho použijte externí katalogy pro funkci PunchOut eProcurement</span><span class="sxs-lookup"><span data-stu-id="d9d28-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="d9d28-108">Když potom zaměstnanci vytvářejí žádanky, mohou „proniknout“ na web externího katalogu dodavatele (jinými slovy - odejdou z vašeho systému a přejdou na web dodavatele).</span><span class="sxs-lookup"><span data-stu-id="d9d28-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="d9d28-109">Produkty, které jsou přidány do nákupního košíku na webu dodavatele, lze poté převést na řádky požadavků.</span><span class="sxs-lookup"><span data-stu-id="d9d28-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="d9d28-110">Proto získáte správné informace o produktu správné: ID produktu, název, cena a podobně.</span><span class="sxs-lookup"><span data-stu-id="d9d28-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="d9d28-111">Aby bylo možné použít externí katalogy, zaměstnanec musí vytvořit požadavek na stránce **Moje nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="d9d28-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="d9d28-112">Zaměstnanec, který vytvoří žádanku, se označuje jako pořizovatel žádanky.</span><span class="sxs-lookup"><span data-stu-id="d9d28-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="d9d28-113">Jako pořizovatel můžete provést následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="d9d28-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="d9d28-114">Můžete použít akci na řádku **Externí katalogy** k otevření stránky, která zahrnuje všechny externí katalogy, které jsou k dispozici pro zadaného žadatele, kupující právnickou osobu a přijímající provozní jednotku.</span><span class="sxs-lookup"><span data-stu-id="d9d28-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="d9d28-115">V závislosti na svých oprávněních změňte žadatele, kupující právnickou osobu a přijímající provozní jednotku.</span><span class="sxs-lookup"><span data-stu-id="d9d28-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="d9d28-116">Změna těchto hodnot může změnit seznam externích katalogů, které jsou k dispozici žadateli.</span><span class="sxs-lookup"><span data-stu-id="d9d28-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="d9d28-117">Externí katalogy, které jsou k dispozici, závisí na aktuálních aktivních zásadách nákupu pro kupující právnickou osobu nebo přijímající provozní jednotku.</span><span class="sxs-lookup"><span data-stu-id="d9d28-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="d9d28-118">Tyto zásady mohou povolit nebo zakázat přístup k určité kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="d9d28-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="d9d28-119">Z tohoto důvodu může být ovlivněn seznam externích katalogů, které jsou mapovány na tyto kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="d9d28-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="d9d28-120">Další informace o způsobech nastavení zásad naleznete v tématu [Zásady nákupu](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d9d28-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="d9d28-121">Pokud chcete vyhledat externí katalogy pro konkrétní kategorie zásobování, zadejte text v poli pro vyhledávání katalogu.</span><span class="sxs-lookup"><span data-stu-id="d9d28-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="d9d28-122">Pokud chcete přidat produkty z externího katalogu dodavatele na web dodavatele, klikněte na externí katalog.</span><span class="sxs-lookup"><span data-stu-id="d9d28-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="d9d28-123">Poté přidejte produkty do nákupního košíku a přejděte k pokladně. Řádky nákupního košíku se přesunou do aplikace Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d9d28-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="d9d28-124">Pokud existuje několik možností pro kategorie nákupu, vyberte kategorii nákupu před přidáním řádků do žádanky.</span><span class="sxs-lookup"><span data-stu-id="d9d28-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="d9d28-125">Po přidání řádků do žádanky můžete přidat další řádky bez použití externích katalogů.</span><span class="sxs-lookup"><span data-stu-id="d9d28-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="d9d28-126">Případně můžete dále pokračovat v používání externích katalogů k přidávání řádků.</span><span class="sxs-lookup"><span data-stu-id="d9d28-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="d9d28-127">Jakmile je žádanka připravena, použijte akci **Workflow** > **Odeslat** pro předložení ke schválení.</span><span class="sxs-lookup"><span data-stu-id="d9d28-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>


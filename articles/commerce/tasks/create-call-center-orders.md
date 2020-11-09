---
title: " Vytváření objednávek v kontaktním středisku"
description: Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107345"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="3472e-103"> Vytváření objednávek v kontaktním středisku</span><span class="sxs-lookup"><span data-stu-id="3472e-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3472e-104">Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele.</span><span class="sxs-lookup"><span data-stu-id="3472e-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="3472e-105">Tato procedura používá ukázková data USRT společnosti a je určena pro úředníka prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3472e-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="3472e-106">Předpoklady: Uživatelé provádějící proceduru jsou nastaveni jako uživatelé kontaktního střediska a pololetní katalog společnosti Fabrikam je publikovaném s alespoň jedním zdrojovým kódem.</span><span class="sxs-lookup"><span data-stu-id="3472e-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="3472e-107">Přejděte na **Retail a Commerce \> Odběratelé \> Služby odběratele**.</span><span class="sxs-lookup"><span data-stu-id="3472e-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="3472e-108">V poli **SearchText** zadejte kritéria vyhledávání pro vyhledávání odběratele.</span><span class="sxs-lookup"><span data-stu-id="3472e-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="3472e-109">Pro tuto vzorovou proceduru zadejte text „karen“ a vyberte **Tab**.</span><span class="sxs-lookup"><span data-stu-id="3472e-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="3472e-110">Vyberte Vyhledat.</span><span class="sxs-lookup"><span data-stu-id="3472e-110">Select Search.</span></span>
    * <span data-ttu-id="3472e-111">Jelikož v ukázkových datech existuje pouze jeden odběratel se jménem Karen, bude výsledek vybrán automaticky.</span><span class="sxs-lookup"><span data-stu-id="3472e-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="3472e-112">Vyberte **Nová prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="3472e-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="3472e-113">Rozbalte nebo sbalte oddíl záhlaví **prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="3472e-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="3472e-114">Vyberte typ zdrojového kódu pro katalog.</span><span class="sxs-lookup"><span data-stu-id="3472e-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="3472e-115">Pokud neexistují žádné aktivní zdrojové kódy, můžete tento krok vynechat.</span><span class="sxs-lookup"><span data-stu-id="3472e-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="3472e-116">Vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="3472e-116">Select **Add line**.</span></span>
8. <span data-ttu-id="3472e-117">Do **Čísla položky** zadejte hledaný výraz položky.</span><span class="sxs-lookup"><span data-stu-id="3472e-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="3472e-118">U této vzorové procedury zadejte číslo dílčí položky „8111“ a stiskněte tabulátor. Objeví se místní okno hledání položky.</span><span class="sxs-lookup"><span data-stu-id="3472e-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="3472e-119">Vyberte produkt, který chcete přidat do prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3472e-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="3472e-120">Zadejte prodejní množství.</span><span class="sxs-lookup"><span data-stu-id="3472e-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="3472e-121">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="3472e-121">Select **Create**.</span></span>
12. <span data-ttu-id="3472e-122">Výběrem **Dokončit** zachytíte platbu odběratele.</span><span class="sxs-lookup"><span data-stu-id="3472e-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="3472e-123">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="3472e-123">Select **Add**.</span></span>
    * <span data-ttu-id="3472e-124">Odkaz Přidat se nachází na kartě Platby. Pokud je sbalena karta Platby, rozbalte ji.</span><span class="sxs-lookup"><span data-stu-id="3472e-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="3472e-125">Vyberte způsob platby.</span><span class="sxs-lookup"><span data-stu-id="3472e-125">Select the payment method.</span></span>
    * <span data-ttu-id="3472e-126">V této proceduře vyberte hotovostní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="3472e-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="3472e-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3472e-127">Close the page.</span></span>
16. <span data-ttu-id="3472e-128">Zadejte částku.</span><span class="sxs-lookup"><span data-stu-id="3472e-128">Enter the amount.</span></span>
    * <span data-ttu-id="3472e-129">V této proceduře zadejte částku odpovídající výši zůstatku objednávky, který lze zobrazit na stránce Souhrn prodejní objednávky vlevo od pole Částka.</span><span class="sxs-lookup"><span data-stu-id="3472e-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="3472e-130">Díky této akci budete moci ukončit objednávku jako plně zaplacenou.</span><span class="sxs-lookup"><span data-stu-id="3472e-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="3472e-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3472e-131">Select **OK**.</span></span>
18. <span data-ttu-id="3472e-132">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="3472e-132">Select **Submit**.</span></span>


---
title: "Přehled doporučení přizpůsobeného produktu"
description: "Toto téma obsahuje informace o doporučení produktu v aplikaci Dynamics 365 for Retail, která lze zobrazit na zařízení pokladního místa (POS)."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: fde7face188bbfd3bfdf66fbff81969f75704302
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="f89b0-103">Přehled doporučení přizpůsobeného produktu</span><span class="sxs-lookup"><span data-stu-id="f89b0-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="f89b0-104">Tato funkce je v současné době k dispozici pouze v karanténě a topologiích výrobního nasazení (s vysokou dostupností).</span><span class="sxs-lookup"><span data-stu-id="f89b0-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="f89b0-105">V aplikaci Dynamics 365 for Retail je možné zobrazit doporučení ohledně produktů v zařízení pokladního místa (POS).</span><span class="sxs-lookup"><span data-stu-id="f89b0-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="f89b0-106">Doporučení jsou položky, které mohou zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech.</span><span class="sxs-lookup"><span data-stu-id="f89b0-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="f89b0-107">Pro maloobchody s velkým katalogy doporučení pomáhají s objevováním produktu.</span><span class="sxs-lookup"><span data-stu-id="f89b0-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="f89b0-108">Vystavením produktů zaměřených na zájmy a nákupní zvyklosti zákazníka mohou doporučení produktu pomáhat maloobchodníkům navýšit prodeje a použít křížové prodeje a zlepšit udržení si zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f89b0-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="f89b0-109">V aplikaci Dynamics 365 for Retail jsou doporučení produktu podpořena kognitivní službou a službou Microsoft Azure machine learning.</span><span class="sxs-lookup"><span data-stu-id="f89b0-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="f89b0-110">Scénáře</span><span class="sxs-lookup"><span data-stu-id="f89b0-110">Scenarios</span></span>
---------

<span data-ttu-id="f89b0-111">Doporučení produktu jsou povolena pro následující scénáře POS.</span><span class="sxs-lookup"><span data-stu-id="f89b0-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="f89b0-112">Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f89b0-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="f89b0-113">Na stránce **Podrobnosti o produktu**:</span><span class="sxs-lookup"><span data-stu-id="f89b0-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="f89b0-114">Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, modul doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně.</span><span class="sxs-lookup"><span data-stu-id="f89b0-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="f89b0-115">Pokud pracovník obchodu přidá zákazníka k transakci a poté navštíví stránku **Podrobnosti o produktu**, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f89b0-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="f89b0-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="f89b0-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="f89b0-117">Na stránce **Transakce**:</span><span class="sxs-lookup"><span data-stu-id="f89b0-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="f89b0-118">Modul doporučení navrhuje položky na základě celého seznamu položek v košíku.</span><span class="sxs-lookup"><span data-stu-id="f89b0-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="f89b0-119">Pokud pracovník obchodu přidá zákazníka k transakci a, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka a seznamu položek v košíku.</span><span class="sxs-lookup"><span data-stu-id="f89b0-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="f89b0-120">Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f89b0-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="f89b0-121">Ovládací prvek **Doporučení** musí být na stránce **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="f89b0-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="f89b0-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="f89b0-123">Na stránce **Podrobnosti o zákazníkovi**:</span><span class="sxs-lookup"><span data-stu-id="f89b0-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="f89b0-124">Modul doporučení navrhuje položky na základě ID uživatele a položek na seznamu přání uživatele.</span><span class="sxs-lookup"><span data-stu-id="f89b0-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="f89b0-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="f89b0-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="f89b0-126">Konfigurace aplikace Dynamics 365 for Retail na povolení doporučení POS</span><span class="sxs-lookup"><span data-stu-id="f89b0-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="f89b0-127">Při nastavování doporučení produktu potřebujete provést tyto akce.</span><span class="sxs-lookup"><span data-stu-id="f89b0-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="f89b0-128">Ujistěte se, zda jste vybrali správnou **právnickou osobu**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="f89b0-129">Přejděte na **Úložiště entit**, vyberte **Maloobchodní prodej** a poté klikněte na tlačítko **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="f89b0-130">Použijí se ukázková data (nebo vaše data) z vaší provozní databáze a přesunou se do úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="f89b0-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="f89b0-131">Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky**, zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**, a potom umístěte ovládací prvek **doporučení**, kam je třeba.</span><span class="sxs-lookup"><span data-stu-id="f89b0-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="f89b0-132">Přejděte na **Parametry maloobchodu**, vyberte **Strojové učení** a vyberte **Ano** v části **Povolit doporučení POS**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="f89b0-133">Doporučení na POS zobrazíte spuštěním globální konfigurační úlohy **1110**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="f89b0-134">Aby se změny návrháře rozvržení obrazovky POS projevily, spusťte úlohu konfigurace kanálu **1070**.</span><span class="sxs-lookup"><span data-stu-id="f89b0-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="f89b0-135">[]()Jak to funguje?</span><span class="sxs-lookup"><span data-stu-id="f89b0-135">[]()How does it work?</span></span>
<span data-ttu-id="f89b0-136">Když aktualizujete **Úložiště entit**, proběhnou následující akce.</span><span class="sxs-lookup"><span data-stu-id="f89b0-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="f89b0-137">Data ve formátu vyžadovaném kognitivními službami je extrahováno z pracovní databáze Dynamics 365 for Retail a odesláno do úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="f89b0-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="f89b0-138">Data používá Azure Data Factory (ADF) k vyčištění pomocí skriptů Hive v rámci aktivit ADF.</span><span class="sxs-lookup"><span data-stu-id="f89b0-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="f89b0-139">Vyčištěná data jsou uložena do úložiště objektů blob.</span><span class="sxs-lookup"><span data-stu-id="f89b0-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="f89b0-140">Data z úložiště objektů blob použije rozhraní API kognitivních služeb k vyzkoušení modelu doporučení.</span><span class="sxs-lookup"><span data-stu-id="f89b0-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="f89b0-141">Při zapnutí možnosti **Povolit doporučení** a spuštění úloh konfigurace jsou uplatněny následující akce.</span><span class="sxs-lookup"><span data-stu-id="f89b0-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="f89b0-142">Pověření a ID modelu jsou vybrána z rozhraní API a uložena do provozní databáze Dynamics 365 for Retail v souboru web.config pro AOS a také na maloobchodním serveru.</span><span class="sxs-lookup"><span data-stu-id="f89b0-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="f89b0-143">ID a pověření modelu jsou zpřístupněny CRT, aby bylo možné provést volání doporučení produktu z Cloud POS a MPOS.</span><span class="sxs-lookup"><span data-stu-id="f89b0-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="f89b0-144">Viz také</span><span class="sxs-lookup"><span data-stu-id="f89b0-144">See also</span></span>
--------

[<span data-ttu-id="f89b0-145">Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS</span><span class="sxs-lookup"><span data-stu-id="f89b0-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)





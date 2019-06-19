---
title: Doporučení přizpůsobeného produktu
description: Toto téma obsahuje informace o doporučení produktu v aplikaci Dynamics 365 for Retail, která lze zobrazit na zařízení pokladního místa (POS).
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: c73bc10332329e81986a259969f8fe34b57f4ee6
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606989"
---
# <a name="personalized-product-recommendations"></a><span data-ttu-id="51d5e-103">Přizpůsobená doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="51d5e-103">Personalized product recommendations</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="51d5e-104">Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod.</span><span class="sxs-lookup"><span data-stu-id="51d5e-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="51d5e-105">Další informace naleznete v části [Odstraněné nebo zastaralé funkce](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="51d5e-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

<span data-ttu-id="51d5e-106">V aplikaci Dynamics 365 for Retail je možné zobrazit doporučení ohledně produktů v zařízení pokladního místa (POS).</span><span class="sxs-lookup"><span data-stu-id="51d5e-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="51d5e-107">Doporučení jsou položky, které mohou zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech.</span><span class="sxs-lookup"><span data-stu-id="51d5e-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="51d5e-108">Pro maloobchody s velkým katalogy doporučení pomáhají s objevováním produktu.</span><span class="sxs-lookup"><span data-stu-id="51d5e-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="51d5e-109">Vystavením produktů zaměřených na zájmy a nákupní zvyklosti zákazníka mohou doporučení produktu pomáhat maloobchodníkům navýšit prodeje a použít křížové prodeje a zlepšit udržení si zákazníka.</span><span class="sxs-lookup"><span data-stu-id="51d5e-109">By showcasing products targeted to a customer's interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="51d5e-110">V aplikaci Dynamics 365 for Retail využívají doporučení produktu kognitivní služby a strojové učení Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51d5e-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

## <a name="scenarios"></a><span data-ttu-id="51d5e-111">Scénáře</span><span class="sxs-lookup"><span data-stu-id="51d5e-111">Scenarios</span></span>

<span data-ttu-id="51d5e-112">Doporučení produktu jsou povolena pro následující scénáře POS.</span><span class="sxs-lookup"><span data-stu-id="51d5e-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="51d5e-113">Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="51d5e-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="51d5e-114">Na stránce **Podrobnosti o produktu**:</span><span class="sxs-lookup"><span data-stu-id="51d5e-114">On the **Product details** page:</span></span>

    - <span data-ttu-id="51d5e-115">Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, modul doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně.</span><span class="sxs-lookup"><span data-stu-id="51d5e-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
    - <span data-ttu-id="51d5e-116">Pokud pracovník obchodu přidá zákazníka k transakci a poté navštíví stránku **Podrobnosti o produktu**, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka.</span><span class="sxs-lookup"><span data-stu-id="51d5e-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

    <span data-ttu-id="51d5e-117">[![Doporučení na stránce Podrobnosti produktu](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="51d5e-117">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="51d5e-118">Na stránce **Transakce**:</span><span class="sxs-lookup"><span data-stu-id="51d5e-118">On the **Transaction** page:</span></span>

    - <span data-ttu-id="51d5e-119">Modul doporučení navrhuje položky na základě celého seznamu položek v košíku.</span><span class="sxs-lookup"><span data-stu-id="51d5e-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
    - <span data-ttu-id="51d5e-120">Pokud pracovník obchodu přidá zákazníka k transakci a, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka a seznamu položek v košíku.</span><span class="sxs-lookup"><span data-stu-id="51d5e-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer's transaction history and the list of items in the basket.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51d5e-121">Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="51d5e-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="51d5e-122">Ovládací prvek **Doporučení** musí být na stránce **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span>

    <span data-ttu-id="51d5e-123">[![Doporučení na stránce Transakce](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="51d5e-123">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3. <span data-ttu-id="51d5e-124">Na stránce **Podrobnosti o odběrateli** modul doporučení navrhuje položky na základě ID uživatele a položek na seznamu přání uživatele.</span><span class="sxs-lookup"><span data-stu-id="51d5e-124">On the **Customer details** page, the recommendation engine suggests items based on the user ID and items in the customer's wish list.</span></span>

    <span data-ttu-id="51d5e-125">[![Doporučení na stránce Podrobnosti o odběrateli](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="51d5e-125">[![Recommendations on the Customer details page](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="51d5e-126">Konfigurace aplikace Dynamics 365 for Retail pro povolení doporučení POS</span><span class="sxs-lookup"><span data-stu-id="51d5e-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>

<span data-ttu-id="51d5e-127">Při nastavování doporučení produktu potřebujete provést tyto akce.</span><span class="sxs-lookup"><span data-stu-id="51d5e-127">To set up product recommendations, you need to do the following.</span></span>

1. <span data-ttu-id="51d5e-128">Ujistěte se, zda jste vybrali správnou **právnickou osobu**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2. <span data-ttu-id="51d5e-129">Přejděte na **Úložiště entit**, vyberte **Maloobchodní prodej** a poté klikněte na tlačítko **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="51d5e-130">Použijí se ukázková data (nebo vaše data) z vaší provozní databáze a přesunou se do úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="51d5e-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3. <span data-ttu-id="51d5e-131">Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky**, zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**, a potom umístěte ovládací prvek **doporučení**, kam je třeba.</span><span class="sxs-lookup"><span data-stu-id="51d5e-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="51d5e-132">Přejděte na **Parametry maloobchodu**, vyberte **Strojové učení** a vyberte **Ano** v části **Povolit doporučení POS**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="51d5e-133">Doporučení na POS zobrazíte spuštěním globální konfigurační úlohy **1110**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="51d5e-134">Aby se změny návrháře rozvržení obrazovky POS projevily, spusťte úlohu konfigurace kanálu **1070**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="51d5e-135">Jak to funguje?</span><span class="sxs-lookup"><span data-stu-id="51d5e-135">How does it work?</span></span>

<span data-ttu-id="51d5e-136">Když aktualizujete **Úložiště entit**, proběhnou následující akce.</span><span class="sxs-lookup"><span data-stu-id="51d5e-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

- <span data-ttu-id="51d5e-137">Data ve formátu vyžadovaném kognitivními službami je extrahováno z pracovní databáze Dynamics 365 for Retail a odesláno do úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="51d5e-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="51d5e-138">Data používá Azure Data Factory (ADF) k vyčištění pomocí skriptů Hive v rámci aktivit ADF.</span><span class="sxs-lookup"><span data-stu-id="51d5e-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="51d5e-139">Vyčištěná data jsou uložena do úložiště objektů blob.</span><span class="sxs-lookup"><span data-stu-id="51d5e-139">Cleansed data is stored in blob storage.</span></span>
- <span data-ttu-id="51d5e-140">Data z úložiště objektů blob použije rozhraní API kognitivních služeb k vyzkoušení modelu doporučení.</span><span class="sxs-lookup"><span data-stu-id="51d5e-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="51d5e-141">Při zapnutí možnosti **Povolit doporučení** a spuštění úloh konfigurace jsou uplatněny následující akce.</span><span class="sxs-lookup"><span data-stu-id="51d5e-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

- <span data-ttu-id="51d5e-142">Pověření a ID modelu jsou vybrána z rozhraní API a uložena do provozní databáze Dynamics 365 for Retail v souboru web.config pro AOS a také na maloobchodním serveru.</span><span class="sxs-lookup"><span data-stu-id="51d5e-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
- <span data-ttu-id="51d5e-143">ID a pověření modelu jsou zpřístupněny CRT, aby bylo možné provést volání doporučení produktu z Cloud POS a MPOS.</span><span class="sxs-lookup"><span data-stu-id="51d5e-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="51d5e-144">Řešení problémů, když máte doporučení produktu již povolena</span><span class="sxs-lookup"><span data-stu-id="51d5e-144">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="51d5e-145">Přejděte na **Parametry maloobchodu** \> **Strojové učení** \> **Zakázat doporučení produktu** a spusťte **globální konfigurační úlohu \[1110\]**.</span><span class="sxs-lookup"><span data-stu-id="51d5e-145">Navigate to **Retail Parameters** \> **Machine learning** \> **Disable product recommendations** and run **Global configuration job \[1110\]**.</span></span> <span data-ttu-id="51d5e-146">Pokud nemůžete nalézt kartu **Strojové účení**, obraťte se na podporu Dynamics.</span><span class="sxs-lookup"><span data-stu-id="51d5e-146">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span>
- <span data-ttu-id="51d5e-147">Pokud jste přidali **Řízení doporučení** na svou obrazovku transakcí pomocí nástroje **Návrhář rozložení obrazovky**, odstraňte ho také.</span><span class="sxs-lookup"><span data-stu-id="51d5e-147">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51d5e-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="51d5e-148">Additional resources</span></span>

[<span data-ttu-id="51d5e-149">Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS</span><span class="sxs-lookup"><span data-stu-id="51d5e-149">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)

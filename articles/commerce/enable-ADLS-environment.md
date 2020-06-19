---
title: Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce
description: V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 83b829306c2da2d10924e547fd3cac6ae6781db3
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404179"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="04bc3-103">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="04bc3-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04bc3-104">V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="04bc3-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="04bc3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="04bc3-105">Overview</span></span>

<span data-ttu-id="04bc3-106">V řešení Dynamics 365 Commerce jsou všechny informace o produktech a transakcích sledovány v úložišti entit prostředí.</span><span class="sxs-lookup"><span data-stu-id="04bc3-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="04bc3-107">Chcete-li zpřístupnit tato data jiným službám Dynamics 365, jako například analýze dat, business intelligence a personalizovaná doporučení, je nutné připojit prostředí k řešení Azure Data Lake Storage Gen 2 vlastněnému zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="04bc3-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="04bc3-108">Protože Azure Data Lake Storage je nakonfigurováno v prostředí, jsou všechna potřebná data zrcadlena z úložiště entit a přitom jsou stále chráněna a pod kontrolou odběratele.</span><span class="sxs-lookup"><span data-stu-id="04bc3-108">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="04bc3-109">Pokud jsou v prostředí také povolena doporučení produktu nebo přizpůsobená doporučení, bude mít zásobník doporučení produktu přístup k vyhrazené složce v Azure Data Lake Storage, aby bylo možné načíst data odběratele a vypočítávat doporučení na jejich základě.</span><span class="sxs-lookup"><span data-stu-id="04bc3-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04bc3-110">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="04bc3-110">Prerequisites</span></span>

<span data-ttu-id="04bc3-111">Zákazníci musí mít Azure Data Lake Storage nakonfigurované v předplatném Azure, které vlastní.</span><span class="sxs-lookup"><span data-stu-id="04bc3-111">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="04bc3-112">Toto téma nezahrnuje nákup předplatného Azure nebo nastavení účtu úložiště s podporou Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="04bc3-112">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="04bc3-113">Další informace o Azure Data Lake Storage naleznete v [oficiální dokumentaci Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="04bc3-113">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="04bc3-114">Kroky konfigurace</span><span class="sxs-lookup"><span data-stu-id="04bc3-114">Configuration steps</span></span>

<span data-ttu-id="04bc3-115">V této části jsou popsány konfigurační kroky, které jsou nezbytné pro povolení Azure Data Lake Storage v prostředí ve vztahu k doporučením produktu.</span><span class="sxs-lookup"><span data-stu-id="04bc3-115">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="04bc3-116">Podrobnější přehled kroků potřebných k povolení Azure Data Lake Storage naleznete v tématu [Nastavení úložiště entit jako Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="04bc3-116">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="04bc3-117">Povolení Azure Data Lake Storage v prostředí</span><span class="sxs-lookup"><span data-stu-id="04bc3-117">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="04bc3-118">Přihlaste se k portálu administrativního systému prostředí.</span><span class="sxs-lookup"><span data-stu-id="04bc3-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="04bc3-119">Vyhledejte **Systémové parametry** a přejděte na kartu **Datová připojení**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="04bc3-120">Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="04bc3-121">Nastavte možnost **Postupná aktualizace Data Lake** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="04bc3-122">Dále zadejte následující požadované informace:</span><span class="sxs-lookup"><span data-stu-id="04bc3-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="04bc3-123">**ID aplikace** // **Tajný klíč aplikace** // **Název DNS** - Je třeba se připojit ke KeyVault, kde je uložen tajný klíč Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="04bc3-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="04bc3-124">**Název tajného klíče** - Název tajného klíče uloženého v KeyVault a použitého k ověření s Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="04bc3-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="04bc3-125">Uložte své změny v levém horním rohu stránky.</span><span class="sxs-lookup"><span data-stu-id="04bc3-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="04bc3-126">Následující obrázek znázorňuje příklad konfigurace Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="04bc3-126">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Příklad konfigurace Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="04bc3-128">Test připojení Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="04bc3-128">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="04bc3-129">Otestujte připojení ke KeyVault pomocí odkazu **Testovat Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="04bc3-130">Otestujte připojení k Azure Data Lake Storage pomocí odkazu **Testovat úložiště Azure**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-130">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="04bc3-131">Pokud se testy nezdaří, zkontrolujte správnost výše popsaných informací o KeyVault a potom to zkuste znovu.</span><span class="sxs-lookup"><span data-stu-id="04bc3-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="04bc3-132">Jakmile jsou testy připojení úspěšné, je nutné povolit automatickou aktualizaci úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="04bc3-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="04bc3-133">Chcete-li povolit automatickou aktualizaci pro úložiště entit, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="04bc3-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="04bc3-134">Vyhledávejte v **úložišti entit**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="04bc3-135">V seznamu vlevo přejděte na položku **RetailSales** a vyberte možnost **upravit**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="04bc3-136">Zkontrolujte, zda **Automatická aktualizace povolena** je nastaveno na **Ano**, zvolte **Obnovit** a pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04bc3-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="04bc3-137">Následující obrázek znázorňuje příklad úložiště entit s povolenou automatickou aktualizací.</span><span class="sxs-lookup"><span data-stu-id="04bc3-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Příklad úložiště entit s povolenou automatickou aktualizací](./media/exampleADLSConfig2.png)

<span data-ttu-id="04bc3-139">Azure Data Lake Storage je nyní nakonfigurováno pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="04bc3-139">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="04bc3-140">Pokud jste to již nedokončili, postupujte podle kroků pro [povolení doporučení produktu a individuální nastavení](enable-product-recommendations.md) pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="04bc3-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04bc3-141">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="04bc3-141">Additional resources</span></span>

[<span data-ttu-id="04bc3-142">Zpřístupnit úložiště entit jako Data Lake</span><span class="sxs-lookup"><span data-stu-id="04bc3-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="04bc3-143">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="04bc3-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="04bc3-144">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="04bc3-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="04bc3-145">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="04bc3-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="04bc3-146">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="04bc3-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="04bc3-147">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="04bc3-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="04bc3-148">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="04bc3-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="04bc3-149">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="04bc3-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="04bc3-150">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="04bc3-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="04bc3-151">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="04bc3-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="04bc3-152">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="04bc3-152">Product recommendations FAQ</span></span>](faq-recommendations.md)

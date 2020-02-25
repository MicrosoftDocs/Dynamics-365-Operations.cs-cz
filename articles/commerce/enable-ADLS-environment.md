---
title: Povolení ADLS v prostředí Dynamics 365 Commerce
description: V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage (ADLS) pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025230"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="10ddf-103">Povolení ADLS v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="10ddf-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10ddf-104">V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage (ADLS) pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="10ddf-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="10ddf-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="10ddf-105">Overview</span></span>

<span data-ttu-id="10ddf-106">V řešení Dynamics 365 Commerce jsou všechny informace o produktech a transakcích sledovány v úložišti entit prostředí.</span><span class="sxs-lookup"><span data-stu-id="10ddf-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="10ddf-107">Chcete-li zpřístupnit tato data jiným službám Dynamics 365, jako například analýze dat, business intelligence a personalizovaná doporučení, je nutné připojit prostředí k řešení Azure Data Lake Storage Gen 2 (ADLS) vlastněnému zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="10ddf-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="10ddf-108">Protože ADLS je nakonfigurováno v prostředí, jsou všechna potřebná data zrcadlena z úložiště entit a přitom jsou stále chráněna a pod kontrolou odběratele.</span><span class="sxs-lookup"><span data-stu-id="10ddf-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="10ddf-109">Pokud jsou v prostředí také povolena doporučení produktu nebo přizpůsobená doporučení, bude mít zásobník doporučení produktu přístup k vyhrazené složce v ADLS, aby bylo možné načíst data odběratele a vypočítávat doporučení na jejich základě.</span><span class="sxs-lookup"><span data-stu-id="10ddf-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10ddf-110">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="10ddf-110">Prerequisites</span></span>

<span data-ttu-id="10ddf-111">Zákazníci musí mít ADLS nakonfigurované v předplatném Azure, které vlastní.</span><span class="sxs-lookup"><span data-stu-id="10ddf-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="10ddf-112">Toto téma nezahrnuje nákup předplatného Azure nebo nastavení účtu úložiště s podporou ADLS.</span><span class="sxs-lookup"><span data-stu-id="10ddf-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="10ddf-113">Další informace o ADLS naleznete v [oficiální dokumentaci ADLS](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="10ddf-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="10ddf-114">Kroky konfigurace</span><span class="sxs-lookup"><span data-stu-id="10ddf-114">Configuration steps</span></span>

<span data-ttu-id="10ddf-115">V této části jsou popsány konfigurační kroky, které jsou nezbytné pro povolení ADLS v prostředí.</span><span class="sxs-lookup"><span data-stu-id="10ddf-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="10ddf-116">Povolení ADLS v prostředí</span><span class="sxs-lookup"><span data-stu-id="10ddf-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="10ddf-117">Přihlaste se k portálu administrativního systému prostředí.</span><span class="sxs-lookup"><span data-stu-id="10ddf-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="10ddf-118">Vyhledejte **Systémové parametry** a přejděte na kartu **Datová připojení**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="10ddf-119">Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="10ddf-120">Nastavte možnost **Postupná aktualizace Data Lake** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="10ddf-121">Dále zadejte následující požadované informace:</span><span class="sxs-lookup"><span data-stu-id="10ddf-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="10ddf-122">**ID aplikace** // **Tajný klíč aplikace** // **Název DNS** - Je třeba se připojit ke KeyVault, kde je uložen tajný klíč ADLS.</span><span class="sxs-lookup"><span data-stu-id="10ddf-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="10ddf-123">**Název tajného klíče** - Název tajného klíče uloženého v KeyVault a použitého k ověření s ADLS.</span><span class="sxs-lookup"><span data-stu-id="10ddf-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="10ddf-124">Uložte své změny v levém horním rohu stránky.</span><span class="sxs-lookup"><span data-stu-id="10ddf-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="10ddf-125">Následující obrázek znázorňuje příklad konfigurace ADLS.</span><span class="sxs-lookup"><span data-stu-id="10ddf-125">The following image shows an example ADLS configuration.</span></span>

![Příklad konfigurace ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="10ddf-127">Test ADLS připojení</span><span class="sxs-lookup"><span data-stu-id="10ddf-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="10ddf-128">Otestujte připojení ke KeyVault pomocí odkazu **Testovat Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="10ddf-129">Otestujte připojení k ADLS pomocí odkazu **Testovat úložiště Azure**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="10ddf-130">Pokud se testy nezdaří, zkontrolujte správnost výše popsaných informací o KeyVault a potom to zkuste znovu.</span><span class="sxs-lookup"><span data-stu-id="10ddf-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="10ddf-131">Jakmile jsou testy připojení úspěšné, je nutné povolit automatickou aktualizaci úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="10ddf-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="10ddf-132">Chcete-li povolit automatickou aktualizaci pro úložiště entit, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="10ddf-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="10ddf-133">Vyhledávejte v **úložišti entit**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="10ddf-134">V seznamu vlevo přejděte na položku **RetailSales** a vyberte možnost **upravit**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="10ddf-135">Zkontrolujte, zda **Automatická aktualizace povolena** je nastaveno na **Ano**, zvolte **Obnovit** a pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="10ddf-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="10ddf-136">Následující obrázek znázorňuje příklad úložiště entit s povolenou automatickou aktualizací.</span><span class="sxs-lookup"><span data-stu-id="10ddf-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Příklad úložiště entit s povolenou automatickou aktualizací](./media/exampleADLSConfig2.png)

<span data-ttu-id="10ddf-138">ADLS je nyní nakonfigurováno pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="10ddf-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="10ddf-139">Pokud jste to již nedokončili, postupujte podle kroků pro [povolení doporučení produktu a individuální nastavení](enable-product-recommendations.md) pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="10ddf-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10ddf-140">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="10ddf-140">Additional resources</span></span>

[<span data-ttu-id="10ddf-141">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="10ddf-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="10ddf-142">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="10ddf-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="10ddf-143">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="10ddf-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="10ddf-144">Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="10ddf-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)



---
title: Nastavení prostředí pro vyhledávání hlavních dat
description: Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924147"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="30fda-103">Nastavení prostředí pro vyhledávání hlavních dat</span><span class="sxs-lookup"><span data-stu-id="30fda-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30fda-104">Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="30fda-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="30fda-105">Nastavte integraci power platform ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="30fda-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="30fda-106">Další informace naleznete v tématu [Integrace Microsoft Power Platform – Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30fda-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="30fda-107">Nastavte Dynamics 365 Finance a Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30fda-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="30fda-108">Další informace viz [Získání řešení](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) a [Ověřování a autorizace](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="30fda-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="30fda-109">Nastavte následující entity.</span><span class="sxs-lookup"><span data-stu-id="30fda-109">Set up the following entities.</span></span> <span data-ttu-id="30fda-110">Další informace viz [Povolení datových entit](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="30fda-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="30fda-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="30fda-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-112">CurrencyEntity</span></span>
      - <span data-ttu-id="30fda-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="30fda-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="30fda-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="30fda-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="30fda-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="30fda-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="30fda-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="30fda-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="30fda-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="30fda-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="30fda-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="30fda-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="30fda-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="30fda-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="30fda-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="30fda-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="30fda-125">Nastavte Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="30fda-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="30fda-126">Vytvořte požadavek na službu pro Microsoft, abyste povolili spuštění následujících funkcí:</span><span class="sxs-lookup"><span data-stu-id="30fda-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="30fda-127">Funkce ERCds</span><span class="sxs-lookup"><span data-stu-id="30fda-127">ERCdsFeature</span></span>
      - <span data-ttu-id="30fda-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="30fda-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="30fda-129">V pracovním prostoru **Správa funkcí** a zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="30fda-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="30fda-130">(Preview) Podpora datových zdrojů Dataverse elektronického vykazování</span><span class="sxs-lookup"><span data-stu-id="30fda-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="30fda-131">(Preview) Podpora datových zdrojů Dataverse daňové služby</span><span class="sxs-lookup"><span data-stu-id="30fda-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="30fda-132">Globalizační funkce (Preview)</span><span class="sxs-lookup"><span data-stu-id="30fda-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="30fda-133">Přihlaste se k RCS pomocí účtu správce klienta.</span><span class="sxs-lookup"><span data-stu-id="30fda-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="30fda-134">Přejděte na **Elektronické vykazování** > **Připojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="30fda-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="30fda-135">Vyberte **Nový** k přidání záznamu a zadejte následující informace do pole.</span><span class="sxs-lookup"><span data-stu-id="30fda-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="30fda-136">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="30fda-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="30fda-137">V poli **Typ** vyberte **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="30fda-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="30fda-138">Do pole **Aplikace** zadejte adresu URL Dataverse.</span><span class="sxs-lookup"><span data-stu-id="30fda-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="30fda-139">Do pole **Klient** zadejte klienta.</span><span class="sxs-lookup"><span data-stu-id="30fda-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="30fda-140">Do pole **Vlastní URL** zadejte svou adresu URL Dataverse a za ni napište „/api/data/v9.1“.</span><span class="sxs-lookup"><span data-stu-id="30fda-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="30fda-141">Vyberte **Zkontrolovat připojení** a dokončete proces připojení.</span><span class="sxs-lookup"><span data-stu-id="30fda-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="30fda-142">[![Tlačítko Zkontrolovat připojení](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="30fda-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="30fda-143">Přejděte na **Elektronické výkaznictví** > **Daňové konfigurace** a importujte daňové konfigurace z [Daňové konfigurace](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="30fda-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="30fda-144">[![Stránka Daňové konfigurace, strom datového modelu daní](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="30fda-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="30fda-145">Přejděte na **Mapování modelu zdanitelného dokumentu** nebo **Mapování modelu Dataverse**, pokud používáte konfiguraci Microsoftu a v poli **Připojená aplikace** vyberte záznam, který jste vytvořili v kroku 7.</span><span class="sxs-lookup"><span data-stu-id="30fda-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="30fda-146">Nastavte možnost **Výchozí pro mapování modelu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="30fda-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="30fda-147">[![Stránka mapování modelu](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="30fda-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

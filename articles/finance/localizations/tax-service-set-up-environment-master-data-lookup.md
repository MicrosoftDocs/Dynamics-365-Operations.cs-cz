---
title: Nastavení prostředí pro vyhledávání hlavních dat
description: Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.
author: kai-cloud
ms.date: 03/31/2021
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
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869049"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="33c80-103">Nastavení prostředí pro vyhledávání hlavních dat</span><span class="sxs-lookup"><span data-stu-id="33c80-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="33c80-104">Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="33c80-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="33c80-105">Nastavte integraci power platform ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="33c80-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="33c80-106">Další informace naleznete v tématu [Integrace Microsoft Power Platform – Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33c80-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="33c80-107">Nastavte Dynamics 365 Finance a Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="33c80-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="33c80-108">Další informace viz [Získání řešení](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) a [Ověřování a autorizace](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="33c80-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="33c80-109">Importujte *Nezbytné řešení virtuální entity pro daňovou službu* z [Virtuální entity daňové služby](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="33c80-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="33c80-110">Nastavte Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="33c80-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="33c80-111">Vytvořte požadavek na službu pro Microsoft, abyste povolili spuštění následujících funkcí:</span><span class="sxs-lookup"><span data-stu-id="33c80-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="33c80-112">Funkce ERCds</span><span class="sxs-lookup"><span data-stu-id="33c80-112">ERCdsFeature</span></span>
      - <span data-ttu-id="33c80-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="33c80-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="33c80-114">Ve Finance přejděte do pracovního prostoru **Správa funkcí** a zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="33c80-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="33c80-115">(Preview) Podpora datových zdrojů Dataverse elektronického vykazování</span><span class="sxs-lookup"><span data-stu-id="33c80-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="33c80-116">(Preview) Podpora datových zdrojů Dataverse daňové služby</span><span class="sxs-lookup"><span data-stu-id="33c80-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="33c80-117">Globalizační funkce (Preview)</span><span class="sxs-lookup"><span data-stu-id="33c80-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="33c80-118">Přihlaste se k RCS pomocí účtu správce klienta.</span><span class="sxs-lookup"><span data-stu-id="33c80-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="33c80-119">Přejděte na **Elektronické vykazování** > **Připojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="33c80-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="33c80-120">Vyberte **Nový** k přidání záznamu a zadejte následující informace do pole.</span><span class="sxs-lookup"><span data-stu-id="33c80-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="33c80-121">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="33c80-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="33c80-122">V poli **Typ** vyberte **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="33c80-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="33c80-123">Do pole **Aplikace** zadejte adresu URL Dataverse.</span><span class="sxs-lookup"><span data-stu-id="33c80-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="33c80-124">Do pole **Klient** zadejte klienta.</span><span class="sxs-lookup"><span data-stu-id="33c80-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="33c80-125">Do pole **Vlastní URL** zadejte svou adresu URL Dataverse a za ni napište „/api/data/v9.1“.</span><span class="sxs-lookup"><span data-stu-id="33c80-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="33c80-126">Vyberte **Zkontrolovat připojení** a dokončete proces připojení.</span><span class="sxs-lookup"><span data-stu-id="33c80-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="33c80-127">[![Tlačítko Zkontrolovat připojení](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="33c80-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="33c80-128">Přejděte na **Elektronické výkaznictví** > **Daňové konfigurace** a importujte daňové konfigurace z [Daňové konfigurace](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="33c80-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="33c80-129">[![Stránka Daňové konfigurace, strom datového modelu daní](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="33c80-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="33c80-130">Přejděte na **Mapování modelu zdanitelného dokumentu** nebo **Mapování modelu Dataverse**, pokud používáte konfiguraci Microsoftu a v poli **Připojená aplikace** vyberte záznam, který jste vytvořili v kroku 7.</span><span class="sxs-lookup"><span data-stu-id="33c80-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="33c80-131">Nastavte možnost **Výchozí pro mapování modelu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="33c80-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="33c80-132">[![Stránka mapování modelu](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="33c80-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="0802a-103">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="0802a-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0802a-104">Řešení zpeněžení potenciálního zákazníka používá [Integraci dat](/common-data-service/entity-reference/dynamics-365-integration) k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales prostřednictvím služby Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="0802a-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="0802a-105">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="0802a-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="0802a-106">V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a zpracovávat plnění objednávky v rámci správy skladů v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0802a-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="0802a-107">Toto řešení umožňuje integraci v rámci následujících oblastí:</span><span class="sxs-lookup"><span data-stu-id="0802a-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="0802a-108">Správa účtů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0802a-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="0802a-109">Správa kontaktů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0802a-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="0802a-110">Správa produktů v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="0802a-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="0802a-111">Vytvoření prodejních nabídek v aplikaci Sales a jejich synchronizace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0802a-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="0802a-112">Vytvoření prodejních objednávek v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="0802a-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="0802a-113">Vytvoření prodejních faktur v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="0802a-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="0802a-114">Systémové požadavky pro aplikaci Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="0802a-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="0802a-115">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující:</span><span class="sxs-lookup"><span data-stu-id="0802a-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="0802a-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) s aktualizací Platform update 8 (aplikací 7.2.11792.56024 s platformou 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="0802a-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="0802a-117">Dvě opravy hotfix Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017).</span><span class="sxs-lookup"><span data-stu-id="0802a-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="0802a-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do Sales.</span><span class="sxs-lookup"><span data-stu-id="0802a-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="0802a-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do Sales.</span><span class="sxs-lookup"><span data-stu-id="0802a-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="0802a-120">**Poznámka**: Musíte pouze nainstalovat KB4036524, protože instalace obsahuje změny z KB4036461.</span><span class="sxs-lookup"><span data-stu-id="0802a-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="0802a-121">Systémové požadavky pro Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="0802a-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="0802a-122">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující:</span><span class="sxs-lookup"><span data-stu-id="0802a-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="0802a-123">Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="0802a-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="0802a-124">Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="0802a-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0802a-125">Instalace řešení zpeněžení potenciálního zákazníka pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="0802a-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="0802a-126">Stáhněte [Zip soubor s balíčkem řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) z webu CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="0802a-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="0802a-127">Ujistěte se, že ZIP soubor není blokován, aby se vám při instalaci balíčku řešení nezobrazila chybová zpráva „Nebyl nalezen žádný balíček pro import“.</span><span class="sxs-lookup"><span data-stu-id="0802a-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="0802a-128">Abyste odblokovali soubor, proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="0802a-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="0802a-129">Klikněte pravým tlačítkem soubor ZIP.</span><span class="sxs-lookup"><span data-stu-id="0802a-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="0802a-130">Vyberte **Vlastnosti** a poté vyberte **Odblokovat**.</span><span class="sxs-lookup"><span data-stu-id="0802a-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="0802a-131">Rozbalte a spusťte soubor PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="0802a-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="0802a-132">Nainstalujte řešení zpeněžení potenciálního zákazníka do své instance aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="0802a-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="0802a-133">Vyberte typ nasazení **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="0802a-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="0802a-134">Vyberte **Zobrazit podrobné**.</span><span class="sxs-lookup"><span data-stu-id="0802a-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="0802a-135">Pro rychlou instalaci zvolte **Oblast**.</span><span class="sxs-lookup"><span data-stu-id="0802a-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="0802a-136">Vyberete-li **Nevím**, systém vyhledá všechny oblasti a instalace bude trvat déle.</span><span class="sxs-lookup"><span data-stu-id="0802a-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="0802a-137">Zadejte **Uživatelské jméno** a **Heslo** uživatele s rolí správce, který má k instalaci uživatelská práva.</span><span class="sxs-lookup"><span data-stu-id="0802a-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>


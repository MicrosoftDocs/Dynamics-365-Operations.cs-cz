---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: cs-cz
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="a0e25-103">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="a0e25-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a0e25-104">Řešení zpeněžení potenciálního zákazníka nabízí přímou synchronizaci mezi aplikacemi Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="a0e25-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="a0e25-105">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="a0e25-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="a0e25-106">V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a můžete zpracovávat plnění objednávky pomocí správy skladů v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0e25-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="a0e25-107">V aktuální verzi poskytuje řešení zpeněžení potenciálního zákazníka následující typy přímé synchronizace:</span><span class="sxs-lookup"><span data-stu-id="a0e25-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="a0e25-108">Správa účtů v aplikaci Sales a jejich synchronizace přímo z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="a0e25-109">Správa produktů v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="a0e25-110">Správa kontaktů v aplikaci Sales a jejich přímá synchronizace na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="a0e25-111">Synchronizace prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="a0e25-112">Synchronizace prodejních objednávek přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="a0e25-113">Synchronizace prodejních objednávek přímo mezi aplikací Finance and Operations a aplikací Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="a0e25-114">Synchronizace prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="a0e25-115">V dřívějších verzích poskytuje řešení zpeněžení potenciálního zákazníka následující typy nepřímé synchronizace:</span><span class="sxs-lookup"><span data-stu-id="a0e25-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="a0e25-116">Správa účtů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="a0e25-117">Správa kontaktů v aplikaci Sales a jejich synchronizace do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="a0e25-118">Správa produktů v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="a0e25-119">Vytvoření prodejních nabídek v aplikaci Sales a jejich synchronizace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0e25-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="a0e25-120">Vytvoření prodejních objednávek v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="a0e25-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="a0e25-121">Vytvoření prodejních faktur v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="a0e25-122">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0e25-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="a0e25-123">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="a0e25-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="a0e25-124">Rozvržení v aplikaci Dynamics 365 for Finance and Operations, Enterprise edition (červenec 2017)</span><span class="sxs-lookup"><span data-stu-id="a0e25-124">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="a0e25-125">Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) s aktualizací Platform update 8 (sestavení aplikace 7.2.11792.56024 se sestavením platformou 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="a0e25-125">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="a0e25-126">Následující opravy hotfix jsou vyžadovány:</span><span class="sxs-lookup"><span data-stu-id="a0e25-126">The following hotfixes are required:</span></span>

    - <span data-ttu-id="a0e25-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a0e25-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="a0e25-128">Poskytuje několik různých vylepšení.</span><span class="sxs-lookup"><span data-stu-id="a0e25-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="a0e25-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="a0e25-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="a0e25-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="a0e25-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0e25-131">Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných oprav hotfix.</span><span class="sxs-lookup"><span data-stu-id="a0e25-131">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="a0e25-132">Dynamics 365 for Finance and Operations, verze 1611 (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="a0e25-132">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span> 

- <span data-ttu-id="a0e25-133">Dynamics 365 for Finance and Operations, verze 1611, s aktualizací platformy 8 nebo vyšší (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="a0e25-133">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="a0e25-134">Následující opravy hotfix jsou vyžadovány:</span><span class="sxs-lookup"><span data-stu-id="a0e25-134">The following hotfixes are required:</span></span>

    - <span data-ttu-id="a0e25-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Povoluje synchronizaci prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="a0e25-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Povoluje synchronizaci řádku a záhlaví prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="a0e25-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Podpora integrace zpeněžení potenciálního zákazníka prostřednictvím datových entit je požadována.</span><span class="sxs-lookup"><span data-stu-id="a0e25-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a0e25-138">Po instalaci oprav hotfix je nutné spustit následující dávkovou úlohu z formuláře **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="a0e25-138">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="a0e25-139">Tento formulář je skrytý, protože ho potřebujete pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="a0e25-139">This form is hidden because you only need it once.</span></span> <span data-ttu-id="a0e25-140">Pro přístup k formuláři se přihlaste do prostředí a přidejte následující adresu URL do adresy prohlížeče: &mi=action:SalesPopulateProspectToCash, například https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="a0e25-140">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="a0e25-141">Když se formulář otevře, klikněte na OK.</span><span class="sxs-lookup"><span data-stu-id="a0e25-141">When the form opens, click OK.</span></span> <span data-ttu-id="a0e25-142">Vypublikuje se nové pole **LineCreationSequnceNumber** v tabulkách **SalesLine**, **SalesQuotationLine** a **CustInvoiceTrans** s jedinečnými hodnotami a obnoví se seznam produktů.</span><span class="sxs-lookup"><span data-stu-id="a0e25-142">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="a0e25-143">To je nutné pro fungování integrace zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a0e25-143">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="a0e25-144">Systémové požadavky pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-144">System requirements for Sales</span></span>

<span data-ttu-id="a0e25-145">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="a0e25-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="a0e25-146">Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online</span><span class="sxs-lookup"><span data-stu-id="a0e25-146">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="a0e25-147">Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="a0e25-147">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="a0e25-148">Šablony s verzí 1.0.0.0 a 1.0.0.1 jsou podporovány na řešení zpeněžení potenciálního zákazníka pro aplikaci Dynamics 365 for Sales, verze 1.14.1.0</span><span class="sxs-lookup"><span data-stu-id="a0e25-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="a0e25-149">Šablony s verzí 2.0.0.0 a 2.1.0.0 jsou podporovány na řešení zpeněžení potenciálního zákazníka pro aplikaci Dynamics 365 for Sales, verze 1.15.0.0</span><span class="sxs-lookup"><span data-stu-id="a0e25-149">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a0e25-150">Instalace řešení zpeněžení potenciálního zákazníka pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="a0e25-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="a0e25-151">Stáhněte [Zip soubor s balíčkem řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) z webu CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="a0e25-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="a0e25-152">Ověřte, že soubor zip není blokován.</span><span class="sxs-lookup"><span data-stu-id="a0e25-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="a0e25-153">V opačném případě se při pokusu o instalací balíčku řešení může zobrazit následující chybová zpráva: Nebyly nalezeny žádné balíčky pro import.</span><span class="sxs-lookup"><span data-stu-id="a0e25-153">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="a0e25-154">Chcete-li odblokovat zip soubor, klikněte pravým tlačítkem a vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="a0e25-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="a0e25-155">Vyberte **Odblokovat**.</span><span class="sxs-lookup"><span data-stu-id="a0e25-155">Select **Unblock**.</span></span>
3. <span data-ttu-id="a0e25-156">Rozbalte a spusťte soubor **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="a0e25-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="a0e25-157">Nainstalujte řešení zpeněžení potenciálního zákazníka na své instanci aplikace Sales:</span><span class="sxs-lookup"><span data-stu-id="a0e25-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="a0e25-158">Vyberte **Office 365** jako typ nasazení.</span><span class="sxs-lookup"><span data-stu-id="a0e25-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="a0e25-159">Vyberte **Zobrazit podrobné**.</span><span class="sxs-lookup"><span data-stu-id="a0e25-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="a0e25-160">Pro rychlou instalaci zvolte oblast.</span><span class="sxs-lookup"><span data-stu-id="a0e25-160">For a quick installation, select a region.</span></span> <span data-ttu-id="a0e25-161">Vyberete-li **Nevím**, systém vyhledá všechny oblasti a instalace bude trvat déle.</span><span class="sxs-lookup"><span data-stu-id="a0e25-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="a0e25-162">Zadejte uživatelské jméno a heslo uživatele s rolí správce, který má k instalaci práva.</span><span class="sxs-lookup"><span data-stu-id="a0e25-162">Enter the user name and password of an admin user who has installation rights.</span></span>


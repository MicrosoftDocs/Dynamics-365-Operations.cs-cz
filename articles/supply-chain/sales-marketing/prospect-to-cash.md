---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: cs-cz
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="d24a4-103">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="d24a4-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d24a4-104">Řešení zpeněžení potenciálního zákazníka nabízí přímou synchronizaci mezi aplikacemi Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="d24a4-104">The Prospect to cash solution provides direct synchronization across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and Microsoft Dynamics 365 for Sales.</span></span> <span data-ttu-id="d24a4-105">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="d24a4-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="d24a4-106">V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a můžete zpracovávat plnění objednávky pomocí správy skladů v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d24a4-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="d24a4-107">V aktuální verzi poskytuje řešení zpeněžení potenciálního zákazníka následující typy přímé synchronizace:</span><span class="sxs-lookup"><span data-stu-id="d24a4-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="d24a4-108">Správa účtů v aplikaci Sales a jejich synchronizace přímo z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="d24a4-109">Správa produktů v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="d24a4-110">Správa kontaktů v aplikaci Sales a jejich přímá synchronizace na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="d24a4-111">Synchronizace prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="d24a4-112">Synchronizace prodejních objednávek přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="d24a4-113">Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="d24a4-114">Synchronizace prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="d24a4-115">V dřívějších verzích poskytuje řešení zpeněžení potenciálního zákazníka následující typy nepřímé synchronizace:</span><span class="sxs-lookup"><span data-stu-id="d24a4-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="d24a4-116">Správa účtů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="d24a4-117">Správa kontaktů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="d24a4-118">Správa produktů v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="d24a4-119">Vytvoření prodejních nabídek v aplikaci Sales a jejich synchronizace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d24a4-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="d24a4-120">Vytvoření prodejních objednávek v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="d24a4-121">Vytvoření prodejních faktur v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="d24a4-122">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d24a4-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="d24a4-123">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="d24a4-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="july-2017"></a><span data-ttu-id="d24a4-124">Červenec 2017</span><span class="sxs-lookup"><span data-stu-id="d24a4-124">July 2017</span></span> 

- <span data-ttu-id="d24a4-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) s aktualizací Platform update 8 (sestavení aplikace 7.2.11792.56024 se sestavením platformou 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="d24a4-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="d24a4-126">Následující opravy hotfix pro aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d24a4-126">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="d24a4-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d24a4-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="d24a4-128">Poskytuje několik různých vylepšení.</span><span class="sxs-lookup"><span data-stu-id="d24a4-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="d24a4-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="d24a4-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="d24a4-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="d24a4-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d24a4-131">Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných článků znalostní báze.</span><span class="sxs-lookup"><span data-stu-id="d24a4-131">You only have to install KB4045570, because the installation includes the changes from the other Microsoft Knowledge Base (KB) articles.</span></span>

### <a name="november-2016-version-1611"></a><span data-ttu-id="d24a4-132">Listopad 2016 (verze 1611)</span><span class="sxs-lookup"><span data-stu-id="d24a4-132">November 2016 (Version 1611)</span></span>

- <span data-ttu-id="d24a4-133">Co je nového nebo co se změnilo v aktualizaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, s aktualizací platformy 2016 (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="d24a4-133">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (November 2016) with platform update 8 or higher</span></span>

- <span data-ttu-id="d24a4-134">Následující opravy hotfix pro aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d24a4-134">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="d24a4-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Povoluje synchronizaci prodejní objednávky s integrátorem dat z aplikace Microsoft Dynamics 365 for Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span> 
    - <span data-ttu-id="d24a4-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Povoluje synchronizaci hlavičky a řádku prodejní objednávky s integrátorem dat z aplikace Microsoft Dynamics 365 for Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span>
    - <span data-ttu-id="d24a4-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Podpora integrace zpeněžení potenciálního zákazníka prostřednictvím datových entit je požadována</span><span class="sxs-lookup"><span data-stu-id="d24a4-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d24a4-138">Po instalaci oprav hotfix je nutné spustit následující dávkovou úlohu z formuláře SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="d24a4-138">After installing the hotfixes you have to trigger the following batch job from the form SalesPopulateProspectToCash.</span></span> <span data-ttu-id="d24a4-139">Tento formulář je skrytý, protože ho potřebujete pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="d24a4-139">This form is hidden as you only need it once.</span></span> <span data-ttu-id="d24a4-140">Abyste k němu získali přístup, přidejte při přihlášení do prostředí do svého prohlížeče toto: &mi=action:SalesPopulateProspectToCash Například</span><span class="sxs-lookup"><span data-stu-id="d24a4-140">To access it add the following to your browser address, when logged in to the environment: &mi=action:SalesPopulateProspectToCash E.g.</span></span> <span data-ttu-id="d24a4-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Ve formuláři, který se otevře, klikněte na OK.</span><span class="sxs-lookup"><span data-stu-id="d24a4-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash In the form that opens click OK.</span></span>
    <span data-ttu-id="d24a4-142">Vypublikuje se nové pole v tabulkách LineCreationSequnceNumber, SalesLine, SalesQuotationLine a CustInvoiceTrans s jedinečnými hodnotami a obnoví se seznam produktů.</span><span class="sxs-lookup"><span data-stu-id="d24a4-142">This will populate a new “LineCreationSequnceNumber” field in “SalesLine”, “SalesQuotationLine” and “CustInvoiceTrans” tables with unique values and refresh the product list.</span></span> <span data-ttu-id="d24a4-143">To je nutné pro integraci P2C, aby bylo možné pracovat ve verzi 7.1.</span><span class="sxs-lookup"><span data-stu-id="d24a4-143">This is needed for the P2C integration to work on 7.1</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="d24a4-144">Systémové požadavky pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-144">System requirements for Sales</span></span>

<span data-ttu-id="d24a4-145">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="d24a4-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="d24a4-146">Microsoft Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online</span><span class="sxs-lookup"><span data-stu-id="d24a4-146">Microsoft Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="d24a4-147">Řešení zpeněžení potenciálního zákazníka pro Microsoft Dynamics 365 for Sales, verze 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="d24a4-147">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="d24a4-148">Šablony s verzí 1.0.0.0 a 1.0.0.1 jsou podporovány na řešení zpeněžení potenciálního zákazníka pro aplikaci Microsoft Dynamics 365 for Sales, verze 1.14.1.0</span><span class="sxs-lookup"><span data-stu-id="d24a4-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="d24a4-149">Šablony s verzí 2.0.0.0 a 2.1.0.0 jsou podporovány na řešení zpeněžení potenciálního zákazníka pro aplikaci Microsoft Dynamics 365 for Sales, verze 1.15.0.0</span><span class="sxs-lookup"><span data-stu-id="d24a4-149">Templates with version 2.0.0.0 and 2.1.0.0 are upported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d24a4-150">Instalace řešení zpeněžení potenciálního zákazníka pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="d24a4-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="d24a4-151">Stáhněte [Zip soubor s balíčkem řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) z webu CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="d24a4-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="d24a4-152">Ověřte, že soubor zip není blokován.</span><span class="sxs-lookup"><span data-stu-id="d24a4-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="d24a4-153">V opačném případě se při pokusu o instalací balíčku řešení zobrazí následující chybová zpráva: Nebyly nalezeny žádné balíčky pro import.</span><span class="sxs-lookup"><span data-stu-id="d24a4-153">Otherwise, when you try to install the solution package, you receive the following error message: "No import packages were found."</span></span> <span data-ttu-id="d24a4-154">Chcete-li odblokovat zip soubor, klikněte pravým tlačítkem a vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="d24a4-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="d24a4-155">Vyberte **Odblokovat**.</span><span class="sxs-lookup"><span data-stu-id="d24a4-155">Then select **Unblock**.</span></span>
3. <span data-ttu-id="d24a4-156">Rozbalte a spusťte soubor **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="d24a4-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="d24a4-157">Nainstalujte řešení zpeněžení potenciálního zákazníka na své instanci aplikace Sales:</span><span class="sxs-lookup"><span data-stu-id="d24a4-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="d24a4-158">Vyberte **Office 365** jako typ nasazení.</span><span class="sxs-lookup"><span data-stu-id="d24a4-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="d24a4-159">Vyberte **Zobrazit podrobné**.</span><span class="sxs-lookup"><span data-stu-id="d24a4-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="d24a4-160">Pro rychlou instalaci zvolte oblast.</span><span class="sxs-lookup"><span data-stu-id="d24a4-160">For a quick installation, select a region.</span></span> <span data-ttu-id="d24a4-161">Vyberete-li **Nevím**, systém vyhledá všechny oblasti a instalace bude trvat déle.</span><span class="sxs-lookup"><span data-stu-id="d24a4-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="d24a4-162">Zadejte uživatelské jméno a heslo uživatele s rolí správce, který má k instalaci práva.</span><span class="sxs-lookup"><span data-stu-id="d24a4-162">Enter the user name and password of an admin user who has installation rights.</span></span>


---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ce9c24a0a89dd4e6a0f3f2c7789b4f553d88d412
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="1b79d-103">zpeněžení potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="1b79d-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b79d-104">Řešení zpeněžení potenciálního zákazníka nabízí přímou synchronizaci mezi aplikacemi Dynamics 365 for Finance and Operations a Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="1b79d-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="1b79d-105">Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales.</span><span class="sxs-lookup"><span data-stu-id="1b79d-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="1b79d-106">V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a můžete zpracovávat plnění objednávky pomocí správy skladů v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b79d-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="1b79d-107">Další informace o zpeněžení potenciálního zákazníka naleznete v krátkém videu na YouTube [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="1b79d-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="1b79d-108">V aktuální verzi poskytuje řešení zpeněžení potenciálního zákazníka následující typy přímé synchronizace:</span><span class="sxs-lookup"><span data-stu-id="1b79d-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="1b79d-109">Správa účtů v aplikaci Sales a jejich synchronizace přímo z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b79d-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="1b79d-110">Správa produktů v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="1b79d-111">Správa kontaktů v aplikaci Sales a jejich přímá synchronizace na kontakty nebo odběratele v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b79d-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="1b79d-112">Synchronizace prodejních nabídek z aplikace Sales do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b79d-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="1b79d-113">Synchronizace prodejních objednávek přímo mezi aplikací Finance and Operations a aplikací Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="1b79d-114">Synchronizace prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="1b79d-115">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1b79d-115">System requirements for Finance and Operations</span></span>
<span data-ttu-id="1b79d-116">Integrace zpeněžení potenciálního zákazníka je podporována v následujících verzích:</span><span class="sxs-lookup"><span data-stu-id="1b79d-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="1b79d-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (prosinec 2017)</span><span class="sxs-lookup"><span data-stu-id="1b79d-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="1b79d-118">Dynamics 365 for Finance and Operations, Enterprise edition (prosinec 2017) - sestavení aplikace 7.3.11971.56116 s aktualizací Platform Update 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="1b79d-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="1b79d-119">Rozvržení v aplikaci Dynamics 365 for Finance and Operations, Enterprise edition (červenec 2017)</span><span class="sxs-lookup"><span data-stu-id="1b79d-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="1b79d-120">Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) - s aktualizací Platform update 8 (sestavení aplikace 7.2.11792.56024 se sestavením platformou 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="1b79d-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="1b79d-121">Následující opravy hotfix jsou vyžadovány:</span><span class="sxs-lookup"><span data-stu-id="1b79d-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="1b79d-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Sales do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b79d-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="1b79d-123">Poskytuje několik různých vylepšení.</span><span class="sxs-lookup"><span data-stu-id="1b79d-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="1b79d-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="1b79d-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="1b79d-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.</span><span class="sxs-lookup"><span data-stu-id="1b79d-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b79d-126">Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných oprav hotfix.</span><span class="sxs-lookup"><span data-stu-id="1b79d-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="1b79d-127">Dynamics 365 for Finance and Operations, verze 1611 (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="1b79d-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="1b79d-128">Dynamics 365 for Finance and Operations, verze 1611, s aktualizací platformy 8 nebo vyšší (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="1b79d-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="1b79d-129">Následující opravy hotfix jsou vyžadovány:</span><span class="sxs-lookup"><span data-stu-id="1b79d-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="1b79d-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Povoluje synchronizaci prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="1b79d-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Povoluje synchronizaci řádku a záhlaví prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="1b79d-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Podpora integrace zpeněžení potenciálního zákazníka prostřednictvím datových entit je požadována.</span><span class="sxs-lookup"><span data-stu-id="1b79d-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1b79d-133">Po instalaci oprav hotfix je nutné spustit následující dávkovou úlohu z formuláře **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="1b79d-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="1b79d-134">Tento formulář je skrytý, protože ho potřebujete pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="1b79d-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="1b79d-135">Abyste získali přístup k formuláři, přihlaste se do prostředí a přidejte do URL adresy ve svém prohlížeči toto: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="1b79d-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="1b79d-136">Když se formulář otevře, klikněte na OK.</span><span class="sxs-lookup"><span data-stu-id="1b79d-136">When the form opens, click OK.</span></span> <span data-ttu-id="1b79d-137">Vypublikuje se nové pole **LineCreationSequnceNumber** v tabulkách **SalesLine**, **SalesQuotationLine** a **CustInvoiceTrans** s jedinečnými hodnotami a obnoví se seznam produktů.</span><span class="sxs-lookup"><span data-stu-id="1b79d-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="1b79d-138">To je nutné pro fungování integrace zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1b79d-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="1b79d-139">Systémové požadavky pro aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="1b79d-139">System requirements for Sales</span></span>

<span data-ttu-id="1b79d-140">Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="1b79d-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="1b79d-141">Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online nebo vyšší verze.</span><span class="sxs-lookup"><span data-stu-id="1b79d-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="1b79d-142">Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.15.0.0 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="1b79d-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="1b79d-143">Řešení je k dispozici ke stažení na webech AppSource.</span><span class="sxs-lookup"><span data-stu-id="1b79d-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="1b79d-144">[Stáhnout Dynamics 365, zpeněžení potenciálního zákazníka](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="1b79d-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


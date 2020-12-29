---
title: Import katalogů dodavatele
description: Toto téma popisuje proces importu dat katalogu dodavatele.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7ed2c50b28fdbd1baf4caa0a8a7f2f05d6a53fd6
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424234"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="8ea7c-103">Import katalogů dodavatele</span><span class="sxs-lookup"><span data-stu-id="8ea7c-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="8ea7c-104">Import katalogů dodavatele</span><span class="sxs-lookup"><span data-stu-id="8ea7c-104">Vendor catalogs import</span></span>

<span data-ttu-id="8ea7c-105">V aplikaci Dynamics 365 Supply Chain Management mohou nakupující profesionálové vytvářet a udržovat katalogy, které zaměstnanci společnosti mohou použít při objednání položek a služeb pro interní použití.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="8ea7c-106">Chcete-li vytvořit zásobovací katalog, můžete přidat položky a služby, které chcete zpřístupnit zaměstnancům, buď importem dat katalogu produktů nebo ručním přidáním dat katalogu produktů do základního produktu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="8ea7c-107">Můžete načíst data katalogu odeslaná dodavatelem z klienta aplikace Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="8ea7c-108">Data produktu, které vám dodavatel odešle ve formě souboru požadavku na údržbu katalogu (CMR), musí být ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="8ea7c-109">Soubor CMR by měl obsahovat podrobné informace o produktech, které dodavatel poskytuje vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="8ea7c-110">Import dat katalogů dodavatele</span><span class="sxs-lookup"><span data-stu-id="8ea7c-110">Import vendor catalog data</span></span>

<span data-ttu-id="8ea7c-111">Chcete-li importovat data katalogu dodavatele, je nutné provést následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="8ea7c-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="8ea7c-112">Nastavte projekt v pracovním prostoru Správa dat, kde jste definovali pravidla mapování dat.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="8ea7c-113">Vyberte **Správa dat** a poté vyberte **Nastavit role pro datové projekty**.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="8ea7c-114">Nastavte hierarchii kategorií zásobování a přiřaďte své dodavatele do kategorií zásobování.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="8ea7c-115">Při použití kódů komodit přidejte kódy komodit do kategorií zásobování.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="8ea7c-116">Informace o nastavení hierarchie kategorií zásobování naleznete v tématu [Nastavení hierarchie kategorií zásobování](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="8ea7c-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="8ea7c-117">Konfigurujte dodavatele pro import katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="8ea7c-118">Vyberte dodavatele a poté vyberte **Zásobování** > **nastavit** > **Konfigurovat dodavatele pro importu katalogu**.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="8ea7c-119">Nakonfigurujte workflow pro import katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="8ea7c-120">Vytvořte šablonu souboru CMR a nasdílejte ji se svým dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="8ea7c-121">Vyberte **Zásobování a zdroje** \> **Společné** \> **Katalogy** \> **Katalogy dodavatele** a vytvořte katalog dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="8ea7c-122">Soubory požadavku na údržbu katalogu (CMR), které jste přijali od dodavatele, jsou seskupeny v tomto katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="8ea7c-123">Odešlete soubor CMR.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="8ea7c-124">Zrevidujte, schvalte nebo zamítněte produkty v katalogu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="8ea7c-125">Produkty jsou automaticky přiřazeny do kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="8ea7c-126">Schválené produkty jsou přidány do základního produktu a jsou uvolněny pro vybrané právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="8ea7c-127">Pouze schválené produkty lze přidat do zásobovacího katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="8ea7c-128">Generování šablony souboru pro import katalogu</span><span class="sxs-lookup"><span data-stu-id="8ea7c-128">Generate a catalog import file template</span></span>

<span data-ttu-id="8ea7c-129">Soubor šablony pro import katalogu je soubor průmyslového standardu XSD, který použijete k vytvoření souboru CMR pro produkty dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="8ea7c-130">Můžete použít soubor CMR pro vytvoření nového katalogu, nahrazení existujícího katalogu nebo úpravě existujícího katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="8ea7c-131">Vyberte **Zásobování a zdroje** \> **Katalogy** \> **Katalogy dodavatele** a dvakrát klikněte na katalog, se kterým chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="8ea7c-132">Stáhněte aktuální šablonu importu katalogu (soubor XSD).</span><span class="sxs-lookup"><span data-stu-id="8ea7c-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="8ea7c-133">Na stránce **Aktualizovat katalog** v **podokně akcí** na kartě **Katalogy** ve skupině **Související informace** klikněte na **Generovat šablonu katalogu** a vyberte **Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="8ea7c-134">S možností **Kategorie zásobování** můžete generovat šablonu katalogu, která obsahuje kategorie zásobování, ve které je dodavatel oprávněn poskytovat produkty.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="8ea7c-135">V dialogovém okně **Uložit jako** vyberte umístění, do kterého chcete šablonu souboru s katalogem uložit a soubor uložte.</span><span class="sxs-lookup"><span data-stu-id="8ea7c-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="8ea7c-136">Další informace a příklady naleznete v tomto příspěvku blogu: [Katalogy dodavatele v aplikaci Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="8ea7c-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>

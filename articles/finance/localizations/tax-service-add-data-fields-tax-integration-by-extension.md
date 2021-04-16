---
title: Přidání datových polí do daňové integrace pomocí rozšíření
description: Toto téma vysvětluje, jak používat rozšíření X++ k přidání datových polí do daňové integrace.
author: qire
ms.date: 03/26/2021
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
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830333"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="ee0c6-103">Přidání datových polí do daňové integrace pomocí rozšíření</span><span class="sxs-lookup"><span data-stu-id="ee0c6-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ee0c6-104">Toto téma vysvětluje, jak používat rozšíření X++ k přidání datových polí do daňové integrace.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="ee0c6-105">Tato pole lze rozšířit na daňový datový model daňové služby a použít k určení daňových kódů.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="ee0c6-106">Další informace najdete v tématu [Přidání datových polí do daňových konfigurací](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="ee0c6-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="ee0c6-107">Datový model</span><span class="sxs-lookup"><span data-stu-id="ee0c6-107">Data model</span></span>

<span data-ttu-id="ee0c6-108">Data v datovém modelu jsou přenášena objekty a implementována třídami.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="ee0c6-109">Zde je seznam hlavních objektů:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="ee0c6-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="ee0c6-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="ee0c6-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="ee0c6-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="ee0c6-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="ee0c6-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="ee0c6-113">Následující obrázek ukazuje, jak tyto objekty souvisejí.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="ee0c6-114">[![Vztah objektu datového modelu](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="ee0c6-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="ee0c6-115">Objekt **Document** může obsahovat mnoho objektů **Line**.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="ee0c6-116">Každý objekt obsahuje metadata pro daňovou službu.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="ee0c6-117">`TaxIntegrationDocumentObject` má metadata `originAddress`, která obsahují informace o zdrojové adrese, a metadata `includingTax`, která označují, zda částka zahrnuje daň z obratu.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="ee0c6-118">`TaxIntegrationLineObject` má metadata `itemId`, `quantity` a `categoryId`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="ee0c6-119">`TaxIntegrationLineObject` také implementuje objekty **Charge**.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="ee0c6-120">Tok integrace</span><span class="sxs-lookup"><span data-stu-id="ee0c6-120">Integration flow</span></span>

<span data-ttu-id="ee0c6-121">Údaje v toku jsou manipulovány aktivitami.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="ee0c6-122">Klíčové aktivity</span><span class="sxs-lookup"><span data-stu-id="ee0c6-122">Key activities</span></span>

* <span data-ttu-id="ee0c6-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ee0c6-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="ee0c6-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ee0c6-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="ee0c6-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ee0c6-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="ee0c6-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ee0c6-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="ee0c6-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ee0c6-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="ee0c6-128">Aktivity probíhají v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="ee0c6-129">Nastavení načítání</span><span class="sxs-lookup"><span data-stu-id="ee0c6-129">Setting Retrieval</span></span>
2. <span data-ttu-id="ee0c6-130">Načítání dat</span><span class="sxs-lookup"><span data-stu-id="ee0c6-130">Data Retrieval</span></span>
3. <span data-ttu-id="ee0c6-131">Výpočetní služba</span><span class="sxs-lookup"><span data-stu-id="ee0c6-131">Calculation Service</span></span>
4. <span data-ttu-id="ee0c6-132">Směnný kurz měny</span><span class="sxs-lookup"><span data-stu-id="ee0c6-132">Currency Exchange</span></span>
5. <span data-ttu-id="ee0c6-133">Perzistence dat</span><span class="sxs-lookup"><span data-stu-id="ee0c6-133">Data Persistence</span></span>

<span data-ttu-id="ee0c6-134">Rozšiřte například fázi **Načítání dat** před **Výpočetní službu**.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="ee0c6-135">Aktivity načítání dat</span><span class="sxs-lookup"><span data-stu-id="ee0c6-135">Data Retrieval activities</span></span>

<span data-ttu-id="ee0c6-136">Aktivity **Načítání dat** načítají data z databáze.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="ee0c6-137">K načítání dat z různých transakčních tabulek jsou k dispozici adaptéry pro různé transakce:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="ee0c6-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="ee0c6-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ee0c6-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="ee0c6-145">V těchto aktivitách **Načítání dat** se data zkopírují z databáze do objektů `TaxIntegrationDocumentObject` a `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="ee0c6-146">Protože všechny tyto aktivity rozšiřují stejnou abstraktní třídu šablony, mají společné metody.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="ee0c6-147">Aktivity výpočetní služby</span><span class="sxs-lookup"><span data-stu-id="ee0c6-147">Calculation Service activities</span></span>

<span data-ttu-id="ee0c6-148">Aktivita **Výpočetní služba** je odkazem mezi daňovou službou a daňovou integrací.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="ee0c6-149">Tato aktivita je zodpovědná za následující funkce:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="ee0c6-150">Sestavení požadavku.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-150">Construct the request.</span></span>
2. <span data-ttu-id="ee0c6-151">Zaslání požadavku daňové službě.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="ee0c6-152">Získání odpovědi od daňové služby.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="ee0c6-153">Syntaktickou analýzu odpovědi.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-153">Parse the response.</span></span>

<span data-ttu-id="ee0c6-154">Datové pole, které přidáte k požadavku, bude zasláno společně s dalšími metadaty.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="ee0c6-155">Implementace rozšíření</span><span class="sxs-lookup"><span data-stu-id="ee0c6-155">Extension implementation</span></span>

<span data-ttu-id="ee0c6-156">Tato část poskytuje podrobné kroky, které vysvětlují, jak implementovat rozšíření.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="ee0c6-157">Jako příklady využívá finanční dimenze **Nákladové středisko** a **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="ee0c6-158">Krok 1.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-158">Step 1.</span></span> <span data-ttu-id="ee0c6-159">Přidejte datovou proměnnou do třídy objektu</span><span class="sxs-lookup"><span data-stu-id="ee0c6-159">Add the data variable in the object class</span></span>

<span data-ttu-id="ee0c6-160">Třída objektu obsahuje datovou proměnnou a metody getter/setter pro načítání/zápis dat.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="ee0c6-161">Přidejte datové pole buď do objektu `TaxIntegrationDocumentObject`, nebo do objektu `TaxIntegrationLineObject`, v závislosti na úrovni pole.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="ee0c6-162">Následující příklad používá úroveň řádku a název souboru je `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="ee0c6-163">Pokud je datové pole, které přidáváte, na úrovni dokumentu, změňte název souboru na `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="ee0c6-164">**Nákladové středisko** a **Projekt** jsou přidány jako soukromé proměnné.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="ee0c6-165">Vytvořte metody getter a setter pro tato datová pole, které zajistí manipulaci s daty.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="ee0c6-166">Krok 2.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-166">Step 2.</span></span> <span data-ttu-id="ee0c6-167">Načtěte data z databáze</span><span class="sxs-lookup"><span data-stu-id="ee0c6-167">Retrieve data from the database</span></span>

<span data-ttu-id="ee0c6-168">Určete transakci a rozšiřte příslušné třídy adaptérů tak, aby se data načetla.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="ee0c6-169">Například pokud používáte transakci **Nákupní objednávka**, musíte rozšířit třídy `TaxIntegrationPurchTableDataRetrieval` a `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="ee0c6-170">Třída `TaxIntegrationPurchParmTableDataRetrieval` dědí ze třídy `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="ee0c6-171">Nemělo by se to měnit, pokud se liší logika tabulek `purchTable` a `purchParmTable`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="ee0c6-172">Pokud má být datové pole přidáno pro všechny transakce, rozšiřte všechny třídy `DataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="ee0c6-173">Protože všechny aktivity **Načítání dat** rozšiřují stejnou třídu šablony, jsou struktury tříd, proměnné a metody podobné.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="ee0c6-174">Následující příklad ukazuje základní strukturu, když se používá tabulka `PurchTable`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="ee0c6-175">Když je volána metoda `CopyToDocument`, vyrovnávací paměť `this.purchTable` již existuje.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="ee0c6-176">Účelem této metody je zkopírovat všechna požadovaná data z objektu `this.purchTable` do objektu `document` pomocí metody setter, která byla vytvořena ve třídě `DocumentObject`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="ee0c6-177">Obdobně již existuje vyrovnávací paměť `this.purchLine` v metodě `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="ee0c6-178">Účelem této metody je zkopírovat všechna požadovaná data z objektu `this.purchLine` do objektu `_line` pomocí metody setter, která byla vytvořena ve třídě `LineObject`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="ee0c6-179">Nejpřímějším přístupem je rozšíření metod `CopyToDocument` a `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="ee0c6-180">Doporučujeme však vyzkoušet nejprve metody `copyToDocumentFromHeaderTable` a `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="ee0c6-181">Pokud nefungují tak, jak požadujete, implementujte vlastní metodu a volejte ji v metodách `CopyToDocument` a `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="ee0c6-182">Existují tři běžné situace, kdy můžete použít tento přístup:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="ee0c6-183">Povinné pole je ve třídě `PurchTable` nebo `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="ee0c6-184">V této situaci můžete rozšířit metody `copyToDocumentFromHeaderTable` a `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="ee0c6-185">Zde je ukázkový kód.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="ee0c6-186">Požadovaná data nejsou ve výchozí tabulce transakce.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="ee0c6-187">Existují však některé relace spojení s výchozí tabulkou a toto pole je u většiny řádků povinné.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="ee0c6-188">V této situaci nahraďte metody `getDocumentQueryObject` nebo `getLineObject` a dotazujte se v tabulce podle relace spojení.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="ee0c6-189">V následujícím příkladu je pole **Doručit ihned** integrováno s prodejní objednávkou na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="ee0c6-190">V tomto příkladu je deklarována vyrovnávací paměť `mcrSalesLineDropShipment` a dotaz je definován v metodě `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="ee0c6-191">Dotaz používá relaci `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="ee0c6-192">Když v této situaci rozšiřujete třídu, můžete nahradit `getLineQueryObject` vlastním vytvořeným objektem dotazu.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="ee0c6-193">Upozorňujeme však na tyto aspekty:</span><span class="sxs-lookup"><span data-stu-id="ee0c6-193">However, note the following points:</span></span>

    * <span data-ttu-id="ee0c6-194">Protože návratová hodnota metody `getLineQueryObject` je objekt `SysDaQueryObject`, musíte tento objekt sestavit pomocí přístupu SysDa.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="ee0c6-195">Existující tabulku nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-195">Can't remove existed table.</span></span>

- <span data-ttu-id="ee0c6-196">Požadovaná data souvisí s transakční tabulkou komplikovanou relací spojení, nebo relace není jedna ku jedné (1:1), ale jedna k mnoha (1:N).</span><span class="sxs-lookup"><span data-stu-id="ee0c6-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="ee0c6-197">V tomto případě se věci trochu komplikují.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="ee0c6-198">Tato situace platí pro příklad finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="ee0c6-199">V tomto případě můžete implementovat vlastní metodu k načtení dat.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="ee0c6-200">Zde je ukázkový kód v souboru `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="ee0c6-201">Krok 3.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-201">Step 3.</span></span> <span data-ttu-id="ee0c6-202">Přidejte k požadavku data</span><span class="sxs-lookup"><span data-stu-id="ee0c6-202">Add data to the request</span></span>

<span data-ttu-id="ee0c6-203">Rozšiřte metodu `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` nebo `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`, aby přidávala data k požadavku.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="ee0c6-204">Zde je ukázkový kód v souboru `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="ee0c6-205">V tomto kódu je `_destination` objektem obálky, který se používá ke generování zasílaného požadavku, a `_source` je objekt třídy `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="ee0c6-206">Definujte klíč, který se používá ve formuláři žádosti, jako `private const str`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="ee0c6-207">Nastavte pole v metodě `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` pomocí metody `SetField`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="ee0c6-208">Datový typ druhého parametru by měl být `string`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="ee0c6-209">Pokud datový typ není `string` převeďte ho na `string`.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="ee0c6-210">Dodatek</span><span class="sxs-lookup"><span data-stu-id="ee0c6-210">Appendix</span></span>

<span data-ttu-id="ee0c6-211">Tato příloha ukazuje kompletní ukázkový kód pro integraci finančních dimenzí (**Nákladové středisko** a **Projekt**) na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="ee0c6-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="ee0c6-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ee0c6-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="ee0c6-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ee0c6-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="ee0c6-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ee0c6-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

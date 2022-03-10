---
title: Přidání datových polí do daňové integrace pomocí rozšíření
description: Toto téma vysvětluje, jak používat rozšíření X++ k přidání datových polí do daňové integrace.
author: qire
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: acbe8070424febf24883362448ea56857d9d72d9
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323516"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Přidání datových polí do daňové integrace pomocí rozšíření

[!include [banner](../includes/banner.md)]


Toto téma vysvětluje, jak používat rozšíření X++ k přidání datových polí do daňové integrace. Tato pole lze rozšířit na daňový datový model daňové služby a použít k určení daňových kódů. Další informace najdete v tématu [Přidání datových polí do daňových konfigurací](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Datový model

Data v datovém modelu jsou přenášena objekty a implementována třídami.

Zde je seznam hlavních objektů:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Následující obrázek ukazuje, jak tyto objekty souvisejí.

[![Vztah objektu datového modelu.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Objekt **Document** může obsahovat mnoho objektů **Line**. Každý objekt obsahuje metadata pro daňovou službu.

- `TaxIntegrationDocumentObject` má metadata `originAddress`, která obsahují informace o zdrojové adrese, a metadata `includingTax`, která označují, zda částka zahrnuje daň z obratu.
- `TaxIntegrationLineObject` má metadata `itemId`, `quantity` a `categoryId`.

> [!NOTE]
> `TaxIntegrationLineObject` také implementuje objekty **Charge**.

## <a name="integration-flow"></a>Tok integrace

Údaje v toku jsou manipulovány aktivitami.

### <a name="key-activities"></a>Klíčové aktivity

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Aktivity probíhají v následujícím pořadí:

1. Nastavení načítání
2. Načítání dat
3. Výpočetní služba
4. Směnný kurz měny
5. Perzistence dat

Rozšiřte například fázi **Načítání dat** před **Výpočetní službu**.

#### <a name="data-retrieval-activities"></a>Aktivity načítání dat

Aktivity **Načítání dat** načítají data z databáze. K načítání dat z různých transakčních tabulek jsou k dispozici adaptéry pro různé transakce:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

V těchto aktivitách **Načítání dat** se data zkopírují z databáze do objektů `TaxIntegrationDocumentObject` a `TaxIntegrationLineObject`. Protože všechny tyto aktivity rozšiřují stejnou abstraktní třídu šablony, mají společné metody.

#### <a name="calculation-service-activities"></a>Aktivity výpočetní služby

Aktivita **Výpočetní služba** je odkazem mezi daňovou službou a daňovou integrací. Tato aktivita je zodpovědná za následující funkce:

1. Sestavení požadavku.
2. Zaslání požadavku daňové službě.
3. Získání odpovědi od daňové služby.
4. Syntaktickou analýzu odpovědi.

Datové pole, které přidáte k požadavku, bude zasláno společně s dalšími metadaty. 

## <a name="extension-implementation"></a>Implementace rozšíření

Tato část poskytuje podrobné kroky, které vysvětlují, jak implementovat rozšíření. Jako příklady využívá finanční dimenze **Nákladové středisko** a **Projekt**.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Krok 1. Přidejte datovou proměnnou do třídy objektu

Třída objektu obsahuje datovou proměnnou a metody getter/setter pro načítání/zápis dat. Přidejte datové pole buď do objektu `TaxIntegrationDocumentObject`, nebo do objektu `TaxIntegrationLineObject`, v závislosti na úrovni pole. Následující příklad používá úroveň řádku a název souboru je `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Pokud je datové pole, které přidáváte, na úrovni dokumentu, změňte název souboru na `TaxIntegrationDocumentObject_Extension.xpp`.

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

**Nákladové středisko** a **Projekt** jsou přidány jako soukromé proměnné. Vytvořte metody getter a setter pro tato datová pole, které zajistí manipulaci s daty.

### <a name="step-2-retrieve-data-from-the-database"></a>Krok 2. Načtěte data z databáze

Určete transakci a rozšiřte příslušné třídy adaptérů tak, aby se data načetla. Například pokud používáte transakci **Nákupní objednávka**, musíte rozšířit třídy `TaxIntegrationPurchTableDataRetrieval` a `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> Třída `TaxIntegrationPurchParmTableDataRetrieval` dědí ze třídy `TaxIntegrationPurchTableDataRetrieval`. Nemělo by se to měnit, pokud se liší logika tabulek `purchTable` a `purchParmTable`.

Pokud má být datové pole přidáno pro všechny transakce, rozšiřte všechny třídy `DataRetrieval`.

Protože všechny aktivity **Načítání dat** rozšiřují stejnou třídu šablony, jsou struktury tříd, proměnné a metody podobné.

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

Následující příklad ukazuje základní strukturu, když se používá tabulka `PurchTable`.

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

Když je volána metoda `CopyToDocument`, vyrovnávací paměť `this.purchTable` již existuje. Účelem této metody je zkopírovat všechna požadovaná data z objektu `this.purchTable` do objektu `document` pomocí metody setter, která byla vytvořena ve třídě `DocumentObject`.

Obdobně již existuje vyrovnávací paměť `this.purchLine` v metodě `CopyToLine`. Účelem této metody je zkopírovat všechna požadovaná data z objektu `this.purchLine` do objektu `_line` pomocí metody setter, která byla vytvořena ve třídě `LineObject`.

Nejpřímějším přístupem je rozšíření metod `CopyToDocument` a `CopyToLine`. Doporučujeme však vyzkoušet nejprve metody `copyToDocumentFromHeaderTable` a `copyToLineFromLineTable`. Pokud nefungují tak, jak požadujete, implementujte vlastní metodu a volejte ji v metodách `CopyToDocument` a `CopyToLine`. Existují tři běžné situace, kdy můžete použít tento přístup:

- Povinné pole je ve třídě `PurchTable` nebo `PurchLine`. V této situaci můžete rozšířit metody `copyToDocumentFromHeaderTable` a `copyToLineFromLineTable`. Zde je ukázkový kód.

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

- Požadovaná data nejsou ve výchozí tabulce transakce. Existují však některé relace spojení s výchozí tabulkou a toto pole je u většiny řádků povinné. V této situaci nahraďte metody `getDocumentQueryObject` nebo `getLineObject` a dotazujte se v tabulce podle relace spojení. V následujícím příkladu je pole **Doručit ihned** integrováno s prodejní objednávkou na úrovni řádku.

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

    V tomto příkladu je deklarována vyrovnávací paměť `mcrSalesLineDropShipment` a dotaz je definován v metodě `getLineQueryObject`. Dotaz používá relaci `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Když v této situaci rozšiřujete třídu, můžete nahradit `getLineQueryObject` vlastním vytvořeným objektem dotazu. Upozorňujeme však na tyto aspekty:

    * Protože návratová hodnota metody `getLineQueryObject` je objekt `SysDaQueryObject`, musíte tento objekt sestavit pomocí přístupu SysDa.
    * Existující tabulku nelze odstranit.

- Požadovaná data souvisí s transakční tabulkou komplikovanou relací spojení, nebo relace není jedna ku jedné (1:1), ale jedna k mnoha (1:N). V tomto případě se věci trochu komplikují. Tato situace platí pro příklad finančních dimenzí. 

    V tomto případě můžete implementovat vlastní metodu k načtení dat. Zde je ukázkový kód v souboru `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.

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

### <a name="step-3-add-data-to-the-request"></a>Krok 3. Přidejte k požadavku data

Rozšiřte metodu `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` nebo `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`, aby přidávala data k požadavku. Zde je ukázkový kód v souboru `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.

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

V tomto kódu je `_destination` objektem obálky, který se používá ke generování zasílaného požadavku, a `_source` je objekt třídy `TaxIntegrationLineObject`.

> [!NOTE]
> Definujte klíč, který se používá ve formuláři žádosti, jako **private const str**. Řetězec by měl být přesně stejný jako název míry přidané v tématu [Přidání datových polí v daňových konfiguracích](tax-service-add-data-fields-tax-configurations.md).
> Nastavte pole v metodě **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** pomocí metody **SetField**. Datový typ druhého parametru by měl být **string**. Pokud datový typ není **string**, převeďte ho na něj.
> Pokud je rozšířen **výčtový typ** X++, všimněte si rozdílu mezi jeho hodnotou, popiskem a názvem.
> 
>   - Hodnota výčtu je typu integer.
>   - Popisek výčtu se může v různých preferovaných jazycích lišit. Nepoužívejte **enum2Str** k převodu výčtového typu na řetězec.
>   - Název výčtu je doporučen, protože je pevný. **enum2Symbol** lze použít k převodu výčtu na jeho název. Přidaná hodnota výčtu v konfiguraci daně by měla být přesně stejná jako název výčtu.

## <a name="model-dependency"></a>Závislost na modelu

Chcete-li úspěšně sestavit projekt, přidejte do závislostí modelu následující referenční modely:

- ApplicationPlatform
- ApplicationSuite
- Daňový modul
- Dimenze, pokud je použita finanční dimenze
- Další potřebné modely uvedené v kódu

## <a name="validation"></a>Ověření

Po dokončení předchozích kroků můžete potvrdit své změny.

1. V části Finance přejděte na **Závazky** a přidejte k adrese URL část **&debug=vs%2CconfirmExit&**. Například https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&. Závěrečný znak **&** je zásadní.
2. Otevřete stránku **Nákupní objednávka** a výběrem položky **Nová** vytvořte nákupní objednávku.
3. Nastavte hodnotu pro přizpůsobené pole a poté vyberte **Prodejní daň**. Soubor pro odstraňování problémů s předponou **TaxServiceTroubleshootingLog** se stáhne automaticky. Tento soubor obsahuje informace o transakci odeslané do služby pro výpočet daně. 
4. Zkontrolujte, zda je přidané přizpůsobené pole přítomno v sekci **Vstupní JSON služby pro výpočet daně** a zda je jeho hodnota správná. Pokud hodnota není správná, znovu zkontrolujte kroky v tomto dokumentu.

Příklad souboru:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Dodatek

Tato příloha ukazuje kompletní ukázkový kód pro integraci finančních dimenzí **Nákladové středisko** a **Projekt** na úrovni řádku.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

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

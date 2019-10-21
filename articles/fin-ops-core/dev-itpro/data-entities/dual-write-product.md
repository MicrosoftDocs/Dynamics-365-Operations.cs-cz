---
title: Používání sjednoceného produktu
description: Toto téma popisuje integraci dat produktů mezi aplikacemi Finance and Operations a Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249321"
---
# <a name="unified-product-experience"></a>Používání sjednoceného produktu

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Pokud se obchodní ekosystém skládá z aplikace Dynamics 365, jako je například finance, Supply Chain Management a Sales, je pro zákazníky přirozené, aby tyto aplikace používali ke zdrojování údajů o produktů. Důvodem je skutečnost, že tyto aplikace poskytují robustní produktovou infrastrukturu doplněnou sofistikovanými koncepty ocenění a přesnými daty o zásobách. Zákazníci, kteří používají externí systém správy životního cyklu produktu (PLM) pro výrobu dat produktu, mohou sdílet produkty z aplikací Finance and Operations do jiných aplikací Dynamics 365. Nabízený produkt přináší do modelu dat integrovaného produktu do Common Data Service, takže všichni uživatelé aplikace včetně uživatelů Power Platform mohou využívat obsáhlá data o produktech přicházející z aplikací Finance and Operations.

Zde je datový model produktu z aplikace Sales.

![Datový model pro prodej produktů](media/dual-write-product-4.jpg)

Zde je datový model produktů z aplikací Finance and Operations.

![Datový model pro produkty ve Finance and Operations](media/dual-write-products-5.jpg)

Tyto dva modely datových modelů produktů byly integrovány do Common Data Service, jak je uvedeno níže.

![Datový model pro produkty v aplikacích Dynamics 365](media/dual-write-products-6.jpg)

Mapování entit dvojího zápisu pro produkty bylo navrženo tak, aby data proudila pouze jednosměrně, a to v téměř reálném čase z aplikací Finance and Operations do Common Data Service. Byla však vytvořena otevřená infrastruktura produktů, aby byla v případě potřeby obousměrná. Zákazníci si jej mohou přizpůsobit na vlastní riziko, protože společnost Microsoft tento přístup nedoporučuje.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map entit pro synchronizaci produktů a souvisejících informací.

Finance and Operations | Jiné aplikace Dynamics 365
-----------------------|--------------------------------
Uvolněné produkty V2 | msdyn\_sharedproductdetails
Uvolněné jedinečné produkty CDS | Produkt
Identifikované čárové kódy čísla produktu | msdyn\_productbarcodes
Výchozí nastavení objednávky | msdyn\_productdefaultordersettings
Výchozí nastavení pořadí konkrétních produktů | msdyn_productspecificdefaultordersettings
Skupiny dimenzí produktu | msdyn\_productdimensiongroups
Skupiny dimenze úložiště | msdyn\_productstoragedimensiongroups
Skupiny sledovací dimenze | msdyn\_producttrackingdimensiongroups
Barvy | msdyn\_productcolors
Velikosti | msdyn\_productsizes
Styly | msdyn\_productsytles
Konfigurace | msdyn\_productconfigurations
Barvy základního produktu | msdyn_sharedproductcolors
Velikosti základního produktu | msdyn_sharedproductsizes
Styly základního produktu | msdyn_sharedproductstyles
Konfigurace základního produktu | msdyn_sharedproductconfigurations
Všechny výrobky | msdyn_globalproducts
Jednotka | uoms
Převody jednotek | msdyn_ unitofmeasureconversions
Převod měrné jednotky konkrétního produktu | msdyn_productspecificunitofmeasureconversion
Weby | msdyn\_operationalsites
Sklady | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Integrace produktů

V tomto modelu je produkt reprezentován kombinací dvou entit v Common Data Service: **Produkt** a **msdyn\_sharedproductdetails.** Zatímco první entita obsahuje definici produktu (jedinečný identifikátor produktu, název produktu a popis), druhá entita obsahuje pole uložená na úrovni produktu. Kombinace těchto dvou entit se používá k definování výrobku podle konceptu skladové jednotky (SKU). Každý uvolněný produkt bude mít své informace v uvedených entitách (podrobnosti o produktu a sdíleném produktu). Chcete-li sledovat všechny produkty (uvolněné a neuvolněné), použije se entita **Globální produkty**. 

Vzhledem k tomu, že produkt je reprezentován jako skladová jednotka, koncepty jedinečných produktů, základních produktů a variant produktů lze zaznamenat v Common Data Service následujícím způsobem:

- **Produkty s podtypem** jsou produkty definované samy sebou. Pro ně není nutné definovat žádné dimenze. Příkladem je určitá kniha. Pro tyto produkty je vytvořen jeden záznam v entitě **Produkt** a jeden záznam je vytvořen v entitě **msdyn\_sharedproductdetails**. Není vytvořen žádný záznam produktové řady.
- **Základní produkty** se používají jako obecné výrobky, které obsahují definici a pravidla určující chování obchodních procesů. Na základě těchto definic mohou být vygenerovány jedinečné produkty, které jsou známy jako varianty produktu. Například tričko je základní produkt a může mít barvu a velikost jako dimenze. Varianty lze uvolnit s různými kombinacemi těchto dimenzí, jako je například malé modré triko nebo středně velké zelené triko. V rámci integrace je v tabulce produktů vytvořen jeden záznam na variantu. Tento záznam obsahuje specifické informace o variantách, jako jsou například různé dimenze. Obecné informace o produktu jsou uloženy v entitě **msdyn\_sharedproductdetails**. (Tyto obecné informace se uchovávají v základním produktu.) Kromě toho je pro každý základní produkt vytvořen záznam produktové řady. Informace základního produktu se synchronizují s Common Data Service, jakmile je vytvořen uvolněný hlavní produkt (před uvolněním variant).
- **Jedinečné produkty** odkazují na všechny produkty podtypu produktu a všechny varianty produktu. 

![Datový model pro produkty](media/dual-write-product.png)

V případě povolené funkce dvojího zápisu budou aplikace z Finance and Operations syncronizovány v dalších aplikacích Dynamics 365 ve stavu **Koncept**. Budou přidány do prvního ceníku se stejnou měnou. Jinými slovy se přidají k prvnímu ceníku v aplikaci Dynamics 365, která odpovídá měně právnické osoby, kde je produkt uvolněn v aplikaci Finance and Operations. 

Chcete-li synchronizovat produkt se stavem **Aktivní**, aby jej bylo možné přímo použít v nabídkách prodejních objednávek, je třeba vybrat následující nastavení: v části **Systém > Správa > Správa systému > Nastavení systému > Prodej** vybrat **Vytvořit produkty v aktivním stavu =Ano**. 

### <a name="cds-released-distinct-products-to-product"></a>Jedinečné produkty uvolněné z CDS do Produktu

Entita **Produkt** obsahuje pole, která definují produkt. Zahrnuje jednotlivé produkty (produkty s dílčím typem produktu) a varianty produktu. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | název
PRODUCTDESCRIPTION | >> | popis
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | cena
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>Jedinečné produkty uvolněné z V2 do msdyn\_sharedproductdetails

Entita **msdyn\_Sharedproductdetails** obsahuje pole z aplikací Finance and Operations, které definují produkt a obsahují finanční a řídící informace o produktu. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>Všechny produkty do produktů msdyn_global

Entita všechny produkty obsahuje všechny produkty, které jsou k dispozici v aplikacích Finance and Operations, a to jak uvolněné produkty, tak i neuvolněné produkty. Tyto produkty jsou k dispozici v Common Data Service pomocí následujících mapování:

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Dimenze produktu 

Dimenze produktu jsou vlastnosti, které identifikují variantu produktu. K definování variant produktu jsou mapovány do Common Data Service také čtyři dimenze produktu (barva, velikost, styl a konfigurace). Následující ilustrace znázorňuje datový model pro dimenzi produktu Barva. Stejný model se použije pro Velikosti, Styly a Konfigurace. 

![Datový model pro produkty](media/dual-write-product-2.PNG)

### <a name="colors"></a>Barvy

Možné barvy v jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Velikosti

Možné velikosti v jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Styly

Možné styly v jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Konfigurace

Možné konfigurace v jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

Pokud má produkt jiné dimenze produktu (například velikost a barvu základního produktu jako dimenze produktu), je každý jedinečný produkt (tj. každá varianta produktu) definován jako kombinace těchto dimenzí produktů. Například číslo produktu B0001 je velmi malé černé triko a číslo produktu B0002 je malé černé triko. V tomto případě jsou definovány existující kombinace dimenzí produktů. Například tričko z předchozího příkladu může být velmi malé a černé, malé a černé, střední a černé nebo velké a černé, ale nemůže být navíc velmi velké a černé. Jinými slovy se specifikují dimenze produktu, které může základní produkt, a varianty mohou být uvolněny na základě těchto hodnot.

Chcete-li sledovat dimenze produktu, které může mít základní produkt, budou vytvořeny a mapovány následující entity v Common Data Service pro každou dimenzi produktu. Další informace viz [Přehled informací o produktech](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Barva sdíleného produktu

Entita **Sdílená barva produktu** produktu označuje barvy, které může mít určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Common Data Service je zachování konzistence dat. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Sdílená velikost produktu

Entita **Sdílená velikost produktu** produktu označuje velikosti, které má určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Common Data Service je zachování konzistence dat. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Sdíleý styl produktu

Entita **Sdílený styl produktu** produktu označuje styly, které má určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Common Data Service je zachování konzistence dat. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Sdílená konfigurace produktu

Entita **Sdílená konfigurace produktu** produktu označuje konfigurace, které má určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Common Data Service je zachování konzistence dat. Následující tabulka zobrazuje mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Identifikované čárové kódy čísla produktu

Čárové kódy produktů se používají k jednoznačné identifikaci produktů. Tyto čárové kódy produktů jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Výchozí nastavení objednávky a výchozí nastavení objednávky specifické pro produkt

Výchozí nastavení objednávky definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek. Tyto informace budou k dispozici v SDC pomocí výchozího nastavení objednávky a výchozí entity nastavení objednávky specifické pro produkt. Další informace o funkci naleznete na [stránce Výchozí nastavení objednávky](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

### <a name="default-order-settings"></a>Výchozí nastavení objednávky

Výchozí nastavení objednávk je k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Výchozí nastavení pořadí konkrétních produktů

Výchozí nastavení objednávk specifických produktů je k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Převody měrných jednotek

Měrné jednotky a odpovídající převody budou k dispozici v Common Data Service dle datovém modelu zobrazeném v diagramu.

![Datový model pro produkty](media/dual-write-product-3.PNG)

Pojem měrné jednotky je integrován mezi aplikacemi Finance and Operations a jinými aplikacemi Dynamics 365. Pro každou třídu jednotek v Finance and Operations se v aplikaci Dynamics 365 vytvoří skupina jednotek, která obsahuje jednotky náležející ke třídě jednotek. Výchozí základní jednotka je také vytvořena pro každou skupinu jednotek. 

### <a name="unit-of-measure"></a>Měrná jednotka

Následující mapování slouží k vytváření měrných jednotek v aplikacích Finance and Operations, které jsou k dispozici v Common Data Service.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | název
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Převody měrných jednotek

Následující mapování slouží k vytváření převodů měrných jednotek v aplikacích Finance and Operations, které jsou k dispozici v Common Data Service.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>Převody měrných jednotek konkrétního produktu

Následující mapování slouží k vytváření převodů měrných jednotek konkrétních produktů v aplikacích Finance and Operations, které jsou k dispozici v Common Data Service.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Zásady produktu: dimenze, sledování a skupiny úložišť

Zásady produktu jsou sady zásad, které se používají pro definování produktů a jejich charakteristik v zásobách. Jako zásady produktu lze nalézt skupinu dimenzí produktu, skupinu dimenzí sledování produktu a skupinu dimenzí úložiště. 

### <a name="product-dimension-group"></a>Skupina dimenzí produktů

Skupina dimenzí produktu definuje, které dimenze produktu definují produkt. K dispozici jsou čtyři skupiny dimenzí produktu: velikost, barva, styl a konfigurace. Skupiny dimenzí produktů jsou k dispozici v Common Data Service pomocí následujících mapování. 

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Skupiny sledovací dimenze produktů

Skupina sledovací dimenze produktů představuje metodu použitou ke sledování produktu v zásobách. Jsou k dispozici v Common Data Service pomocí následujících mapování. 

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Skupina dimenze úložiště produktů

Skupina dimenze úložiště produktů představuje metodu, která se používá k definování umístění produktu ve skladu. Jsou k dispozici v Common Data Service pomocí následujících mapování. 

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation


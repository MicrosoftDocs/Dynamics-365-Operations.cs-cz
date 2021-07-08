---
title: Importujte příchozí ASN prostřednictvím datové entity V2
description: Toto téma vysvětluje, jak spravovat import příchozích oznámení o odeslání (ASN) prostřednictvím datové entity Příchozí ASN V2.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249069"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="58db5-103">Importujte příchozí ASN prostřednictvím datové entity V2</span><span class="sxs-lookup"><span data-stu-id="58db5-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58db5-104">Pokročilá oznámení o přepravě (ASN) vás informují o dodávkách dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="58db5-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="58db5-105">Pomáhají odesílateli popsat obsah zásilky a další informace o ní, například položky a obal.</span><span class="sxs-lookup"><span data-stu-id="58db5-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="58db5-106">ASN mohou pracovníkům skladu pomoci zjistit, co kdy dorazí.</span><span class="sxs-lookup"><span data-stu-id="58db5-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="58db5-107">Proto se mohou připravit.</span><span class="sxs-lookup"><span data-stu-id="58db5-107">Therefore, they can prepare.</span></span> <span data-ttu-id="58db5-108">Pracovníci skladu mohou navíc pomocí ASN přiřadit podrobnosti zásilky k související nákupní objednávce, která byla dříve vytvořena.</span><span class="sxs-lookup"><span data-stu-id="58db5-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="58db5-109">Toto téma představuje sbírku scénářů, které prostřednictvím příkladů ukazují, jak pracovat se soubory ASN.</span><span class="sxs-lookup"><span data-stu-id="58db5-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58db5-110">Import *Příchozí ASN* se vztahuje pouze na položky, které jsou povoleny pro pokročilou správu skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="58db5-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="58db5-111">Než obdržíte ASN, musí být v systému zaregistrována nákupní objednávka u dodavatele, který dané ASN odesílá.</span><span class="sxs-lookup"><span data-stu-id="58db5-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="58db5-112">Příchozí entita ASN V2</span><span class="sxs-lookup"><span data-stu-id="58db5-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="58db5-113">Importujete příchozí ASN pomocí složené datové entity *Příchozí ASN V2*.</span><span class="sxs-lookup"><span data-stu-id="58db5-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="58db5-114">*Příchozí ASN V2* využívá výhod následujících entit:</span><span class="sxs-lookup"><span data-stu-id="58db5-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="58db5-115">Záhlaví příchozího vytížení</span><span class="sxs-lookup"><span data-stu-id="58db5-115">Inbound load header</span></span>
- <span data-ttu-id="58db5-116">Záhlaví příchozí dodávky</span><span class="sxs-lookup"><span data-stu-id="58db5-116">Inbound shipment header</span></span>
- <span data-ttu-id="58db5-117">Struktury balení pro příchozí vytížení</span><span class="sxs-lookup"><span data-stu-id="58db5-117">Inbound load packing structures</span></span>
- <span data-ttu-id="58db5-118">Případy struktury balení pro příchozí vytížení</span><span class="sxs-lookup"><span data-stu-id="58db5-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="58db5-119">Řádky případu struktury balení pro příchozí vytížení</span><span class="sxs-lookup"><span data-stu-id="58db5-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="58db5-120">Řádky struktury balení pro příchozí vytížení</span><span class="sxs-lookup"><span data-stu-id="58db5-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="58db5-121">Složená datová entita *Příchozí ASN V2* je určena pro scénáře asynchronní integrace, kde se používají importy založené na souborech XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="58db5-122">Formát XML pro import ASN</span><span class="sxs-lookup"><span data-stu-id="58db5-122">XML format for importing ASNs</span></span>

<span data-ttu-id="58db5-123">Microsoft Dynamics 365 Supply Chain Management podporuje následující formát XML pro import ASN.</span><span class="sxs-lookup"><span data-stu-id="58db5-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="58db5-124">Každý uzel v souboru XML představuje atribut od jednotlivé entity.</span><span class="sxs-lookup"><span data-stu-id="58db5-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="58db5-125">Příklad</span><span class="sxs-lookup"><span data-stu-id="58db5-125">Examples</span></span>

<span data-ttu-id="58db5-126">Následující podsekce poskytují příklady souborů importu ASN XML pro dodávky dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="58db5-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="58db5-127">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="58db5-127">Example 1</span></span>

<span data-ttu-id="58db5-128">Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro jednu nákupní objednávku, pokud nejsou zahrnuty žádné podrobnosti případu.</span><span class="sxs-lookup"><span data-stu-id="58db5-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="58db5-129">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="58db5-129">Example 2</span></span>

<span data-ttu-id="58db5-130">Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro jednu nákupní objednávku, pokud jsou zahrnuty podrobnosti případu.</span><span class="sxs-lookup"><span data-stu-id="58db5-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="58db5-131">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="58db5-131">Example 3</span></span>

<span data-ttu-id="58db5-132">Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro více nákupních objednávek, pokud jsou zahrnuty podrobnosti případu.</span><span class="sxs-lookup"><span data-stu-id="58db5-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="58db5-133">Zkontrolujte výsledky importu souboru ASN</span><span class="sxs-lookup"><span data-stu-id="58db5-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="58db5-134">Podle těchto pokynů zkontrolujte výsledky importu souboru ASN.</span><span class="sxs-lookup"><span data-stu-id="58db5-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="58db5-135">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="58db5-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="58db5-136">Najděte a otevřete náklad, který byl vytvořen jako součást importu ASN.</span><span class="sxs-lookup"><span data-stu-id="58db5-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="58db5-137">Na pevné záložce **Náklad** byste měli vidět hodnoty, které jsou založeny na souboru XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="58db5-138">Na pevné záložce **Řádky nákladu** byste měli vidět čísla objednávek a podrobnosti o položkách, které jsou založeny na souboru XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="58db5-139">V podokně akcí na kartě **Odeslat a přijmout** ve skupině **Přijmout** vyberte položku **Struktura balení**, chcete-li zkontrolovat strukturu balení nákladu.</span><span class="sxs-lookup"><span data-stu-id="58db5-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="58db5-140">Na pevné záložce **Palety** byste měli vidět registrační značky, které jsou založeny na souboru XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="58db5-141">Na pevné záložce **Případy** byste měli vidět případy, které jsou založeny na souboru XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="58db5-142">Na pevné záložce **Položky** byste měli vidět položky a množství, které jsou založeny na souboru XML.</span><span class="sxs-lookup"><span data-stu-id="58db5-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

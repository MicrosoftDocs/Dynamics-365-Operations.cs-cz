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
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Importujte příchozí ASN prostřednictvím datové entity V2

[!include [banner](../../includes/banner.md)]

Pokročilá oznámení o přepravě (ASN) vás informují o dodávkách dodavatelů. Pomáhají odesílateli popsat obsah zásilky a další informace o ní, například položky a obal.

ASN mohou pracovníkům skladu pomoci zjistit, co kdy dorazí. Proto se mohou připravit. Pracovníci skladu mohou navíc pomocí ASN přiřadit podrobnosti zásilky k související nákupní objednávce, která byla dříve vytvořena.

Toto téma představuje sbírku scénářů, které prostřednictvím příkladů ukazují, jak pracovat se soubory ASN.

> [!IMPORTANT]
> Import *Příchozí ASN* se vztahuje pouze na položky, které jsou povoleny pro pokročilou správu skladu (WMS). Než obdržíte ASN, musí být v systému zaregistrována nákupní objednávka u dodavatele, který dané ASN odesílá.

## <a name="inbound-asn-v2-entity"></a>Příchozí entita ASN V2

Importujete příchozí ASN pomocí složené datové entity *Příchozí ASN V2*. *Příchozí ASN V2* využívá výhod následujících entit:

- Záhlaví příchozího vytížení
- Záhlaví příchozí dodávky
- Struktury balení pro příchozí vytížení
- Případy struktury balení pro příchozí vytížení
- Řádky případu struktury balení pro příchozí vytížení
- Řádky struktury balení pro příchozí vytížení

Složená datová entita *Příchozí ASN V2* je určena pro scénáře asynchronní integrace, kde se používají importy založené na souborech XML.

## <a name="xml-format-for-importing-asns"></a>Formát XML pro import ASN

Microsoft Dynamics 365 Supply Chain Management podporuje následující formát XML pro import ASN. Každý uzel v souboru XML představuje atribut od jednotlivé entity.

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

## <a name="examples"></a>Příklad

Následující podsekce poskytují příklady souborů importu ASN XML pro dodávky dodavatelů.

### <a name="example-1"></a>Příklad 1

Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro jednu nákupní objednávku, pokud nejsou zahrnuty žádné podrobnosti případu.

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

### <a name="example-2"></a>Příklad 2

Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro jednu nákupní objednávku, pokud jsou zahrnuty podrobnosti případu.

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

### <a name="example-3"></a>Příklad 3

Následující příklad ukazuje soubor XML pro import zásilek dodavatele pro více nákupních objednávek, pokud jsou zahrnuty podrobnosti případu.

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Zkontrolujte výsledky importu souboru ASN

Podle těchto pokynů zkontrolujte výsledky importu souboru ASN.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Najděte a otevřete náklad, který byl vytvořen jako součást importu ASN.
1. Na pevné záložce **Náklad** byste měli vidět hodnoty, které jsou založeny na souboru XML.
1. Na pevné záložce **Řádky nákladu** byste měli vidět čísla objednávek a podrobnosti o položkách, které jsou založeny na souboru XML.
1. V podokně akcí na kartě **Odeslat a přijmout** ve skupině **Přijmout** vyberte položku **Struktura balení**, chcete-li zkontrolovat strukturu balení nákladu.
1. Na pevné záložce **Palety** byste měli vidět registrační značky, které jsou založeny na souboru XML.
1. Na pevné záložce **Případy** byste měli vidět případy, které jsou založeny na souboru XML.
1. Na pevné záložce **Položky** byste měli vidět položky a množství, které jsou založeny na souboru XML.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

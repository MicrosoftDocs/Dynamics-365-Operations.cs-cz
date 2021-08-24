---
title: Přiznání k DPH (Česká republika)
description: Toto téma poskytuje informace o přiznání k dani z přidané hodnoty (DPH) pro Českou republiku.
author: anasyash
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Czech Republic
ms.author: anasyash
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a13c19e28cafe245fc45eb8b6dd7a26c630728d2243e4b7e6db4db9d86c730d2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747066"
---
# <a name="vat-declaration-czech-republic"></a>Přiznání k DPH (Česká republika)

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o přiznání k dani z přidané hodnoty (DPH) pro Českou republiku. Obsahuje pokyny pro nastavení a generování přiznání k DPH a kontrolního hlášení DPH.

## <a name="vat-declaration-overview"></a><a name="overview"></a>Přehled přiznání k DPH

### <a name="vat-declaration"></a>Přiznání k DPH

Tato část popisuje sekce a řádky přiznání k DPH, jeho výpočtů a vztahů mezi přiznáním k DPH a kontrolním hlášením DPH.

Chcete-li automaticky generovat přiznání k DPH a kontrolní hlášení DPH, musíte nejprve vytvořit dostatek kódů DPH, abyste mohli vést samostatné účtování DPH pro každé pole v přiznání k DPH. Navíc v parametrech specifických pro aplikaci týkajících se formátu přiznání k DPH a formátu kontrolního hlášení DPH musíte přidružit kódy DPH k výsledku vyhledávání v polích pro přiznání k DPH. Další informace, jak nastavit parametry specifické pro aplikaci, najdete v části [Nastavení parametrů pro pole přiznání](#set-up-parameters-for-declaration-fields) dále v tomto tématu.

V tabulce v části 1 sloupec „Výsledek vyhledávání“ zobrazuje výsledek vyhledávání, který je předkonfigurován pro konkrétní řádek přiznání k DPH ve formátu přiznání k DPH a formátu kontrolního hlášení DPH. Tyto informace použijte ke správnému přidružení kódů DPH k výsledku vyhledávání a poté k řádku přiznání k DPH.

> [!NOTE]
> Pokud nakonfigurujete kódy DPH tak, aby zaúčtovaly přenesení daňové povinnosti k DPH pomocí importního DPH, měli byste své kódy DPH přidružit k výsledku vyhledávání, který v názvu obsahuje „UseTax“. Například u nákupů uvnitř Společenství nakonfigurujte výsledek vyhledávání **EUPurchaseGoodsUseTaxStandard** pro kódy DPH **Importní DPH**, nebo nakonfigurujte výsledek vyhledávání **EUPurchaseGoodsVATPayableStandard** pro kódy DPH, které mají přenesení daňové povinnosti. Další informace, jak konfigurovat přenesení daňové povinnosti k DPH, viz [Přenesení daňové povinnosti](emea-reverse-charge.md).

Formát přiznání k DPH v České republice obsahuje následující oddíly:

- [Oddíl 1: Zdanitelná plnění](#taxabletransactions)
- [Oddíl 2: Další plnění a plnění pocházející z území mimo Českou republiku s nárokem na odpočet](#othersupplies)
- [Oddíl 3: Další údaje](#additionaldata)
- [Oddíl 4: Odpočet DPH](#vatreduction)
- [Oddíl 5: Omezení nároku na odpočet](#righttodeduct)
- [Oddíl 6: Výpočet daně](#taxcalculation)

### <a name="section-1-taxable-transactions"></a><a name="taxabletransactions"></a>Oddíl 1: Zdanitelná plnění

| Řádek | Oddíl kontrolního prohlášení | popis                                                            | Sazba           | Základ daně (prvek XML) | Odváděná daň (prvek XML) | Výsledek vyhledávání |
|-----|---------------------------|------------------------------------------------------------------------|----------------|------------------------|---------------------------|---------------|
| 1   | A4/A5                     | Domácí prodej zboží a služeb                                   | Standardní       | obrat23                | dan23                     | DomesticSalesVATPayableStandard – VATAdjustmentCustomerBadDebtsStandard |
| 2   | A4/A5                     | Domácí prodej zboží a služeb                                   | Snížená        | obrat5                 | dan5                      | <ul><li>DomesticSalesVATPayableReduced – VATAdjustmentCustomerBadDebtsReduced</li><li>DomesticSalesVATPayableReduced2 – VATAdjustmentCustomerBadDebtsReduced2</li></ul> |
| 3   | A2                        | Nákup zboží uvnitř Společenství                                      | Standardní       | p\_zb23                | dan\_pzb23                | <ul><li>EUPurchaseGoodsVATPayableStandard</li><li>EUPurchaseGoodsUseTaxStandard</li></ul> |
| 4   | A2                        | Nákup zboží uvnitř Společenství                                      | Snížená        | p\_zb5                 | dan\_pzb5                 | <ul><li>EUPurchaseGoodsVATPayableReduced</li><li>EUPurchaseGoodsVATPayableReduced2</li><li>EUPurchaseGoodsUseTaxReduced</li><li>EUPurchaseGoodsUseTaxReduced2</li></ul> |
| 5   | A2                        | Nákup služeb uvnitř Společenství                                   | Standardní       | p\_sl23\_e             | dan\_psl23\_e             | <ul><li>EUPurchaseServicesVATPayableStandard</li><li>EUPurchaseServicesUseTaxStandard</li></ul> |
| 6   | A2                        | Nákup služeb uvnitř Společenství                                   | Snížená        | p\_sl5\_e              | dan\_psl5\_e              | <ul><li>EUPurchaseServicesVATPayableReduced</li><li>EUPurchaseServicesVATPayableReduced2</li><li>EUPurchaseServicesUseTaxReduced</li><li>EUPurchaseServicesUseTaxReduced2</li></ul> |
| 7   | Nelze použít            | Dovoz zboží                                                        | Standardní       | dov\_zb23              | dan\_dzb23                | <ul><li>ImportGoodsVATPayableStandard</li><li>ImportGoodsUseTaxStandard</li></ul> |
| 8   | Nelze použít            | Dovoz zboží                                                        | Snížená        | dov\_zb5               | dan\_dzb5                 | <ul><li>ImportGoodsVATPayableReduced</li><li>ImportGoodsUseTaxReduced</li></ul> |
| 9   | A2                        | Nákup nových dopravních prostředků uvnitř Společenství                     | Nelze použít | p\_dop\_nrg            | dan\_pdop\_nrg            | <ul><li>EUPurchaseNewTransportVATPayable</li><li>EUPurchaseNewTransportUseTax</li></ul> |
| 10  | B1                        | Nákup zboží a služeb v rámci tuzemského přenesení daňové povinnosti (\§92) | Standardní       | rez\_pren23            | dan\_rpren23              | <ul><li>DomesticPurchaseReverseChargeVATPayableStandard</li><li>DomesticPurchaseReverseChargeUseTaxStandard</li></ul> |
| 11  | B1                        | Nákup zboží a služeb v rámci tuzemského přenesení daňové povinnosti (\§92) | Snížená        | rez\_pren5             | dan\_rpren5               | <ul><li>DomesticPurchaseReverseChargeVATPayableReduced</li><li>DomesticPurchaseReverseChargeVATPayableReduced2</li><li>DomesticPurchaseReverseChargeUseTaxReduced</li><li>DomesticPurchaseReverseChargeUseTaxReduced2</li></ul> |
| 12  | A2                        | Ostatní nákupy s povinností platby DPH                          | Standardní       | p\_sl23\_z             | dan\_psl23\_z             | <ul><li>OtherPurchasesVATPayableStandard</li><li>OtherPurchasesUseTaxStandard</li></ul> |
| 13  | A2                        | Ostatní nákupy s povinností platby DPH                          | Snížená        | p\_sl5\_z              | dan\_psl5\_z              | <ul><li>OtherPurchasesVATPayableReduced</li><li>OtherPurchasesVATPayableReduced2</li><li>OtherPurchasesUseTaxReduced</li><li>OtherPurchasesUseTaxReduced2</li></ul> |

## <a name="section-2-other-supplies-and-supplies-that-originate-outside-of-the-czech-republic-with-the-right-to-deduct"></a><a name="othersupplies"></a>Oddíl 2: Další plnění a plnění pocházející z území mimo Českou republiku s nárokem na odpočet

| Řádek | Oddíl kontrolního prohlášení | popis                                                         | Základ daně (prvek XML) | Pole sestavy (výsledek vyhledávání) |
|-----|---------------------------|---------------------------------------------------------------------|------------------------|------------------------------|
| 20  | Nelze použít            | Prodej zboží uvnitř Společenství                                      | dod\_zb                | EUSalesGoods |
| 21  | Nelze použít            | Prodej služeb uvnitř Společenství                                   | pln\_sluzby            | EUSalesServices |
| 22  | Nelze použít            | Vývoz zboží                                                     | pln\_vyvoz             | ExportGoods |
| 23  | Nelze použít            | Prodej nových dopravních prostředků osobě nepovinné k dani uvnitř Společenství      | dod\_dop\_nrg          | EUSalesNewTransport |
| 24  | Nelze použít            | Zásilka zboží uvnitř Společenství                                | pln\_zaslani           | EUConsignmentGoods |
| 25  | A1                        | Prodej zboží a služeb v rámci tuzemského přenesení daňové povinnosti (\§92) | pln\_rez\_pren         | DomesticSalesReverseCharge |
| 26  | A3 a ostatní              | Ostatní daňově odečitatelné transakce                                   | pln\_ost               | <ul><li>OtherSalesWithRightToDeduct</li><li>OtherSalesWithRightToDeductGoldInvestment</li></ul> |

## <a name="section-3-additional-data"></a><a name="additionaldata"></a>Oddíl 3: Další údaje

| Řádek | Oddíl kontrolního prohlášení | popis                                                | Základ daně (prvek XML) | Částka daně (prvek XML) | Pole sestavy (výsledek vyhledávání) |
|-----|---------------------------|------------------------------------------------------------|------------------------|--------------------------|------------------------------|
| 30  | Nelze použít            | Zjednodušené trojúhelníkové pořízení zboží uvnitř Společenství | tri\_pozb              | Nelze použít           | SimplifiedTriangularEUPurchaseGoods |
| 31  | Nelze použít            | Zjednodušený trojúhelníkový prodej zboží uvnitř Společenství        | tri\_dozb              | Nelze použít           | SimplifiedTriangularEUSalesGoods |
| 32  | Nelze použít            | Dovoz zboží osvobozeného od daně                                     | dov\_osv               | Nelze použít           | ImportGoodsVATExempt |
| 33  | A4                        | Úprava částky DPH u nedobytných pohledávek – věřitel             | Nelze použít         | opr\_verit               | <p>Informační hodnota zahrnutá v řádcích 1 a 2:</p><ul><li>VATAdjustmentCustomerBadDebtsStandard</li><li>VATAdjustmentCustomerBadDebtsReduced</li><li>VATAdjustmentCustomerBadDebtsReduced2</li></ul> |
| 34  | B2                        | Úprava částky DPH u nedobytných pohledávek – dlužník               | Nelze použít         | opr\_dluz                | <p>Informační hodnota zahrnutá v řádcích 40 a 41:</p><ul><li>VATAdjustmentVendorBadDebtsStandard</li><li>VATAdjustmentVendorBadDebtsReduced</li><li>VATAdjustmentVendorBadDebtsReduced2</li></ul> |

## <a name="section-4-vat-deduction"></a><a name="vatreduction"></a>Oddíl 4: Odpočet DPH

| Řádek | Oddíl kontrolního prohlášení | popis                                                         | Sazba     | Základ daně (prvek XML) | Plný odpočet daně (prvek XML) | Úprava odpočtu daně (prvek XML) | Pole sestavy (výsledek vyhledávání) |
|-----|---------------------------|---------------------------------------------------------------------|----------|------------------------|----------------------------------|------------------------------------------|------------------------------|
| 40  | B2/B3                     | Ze zdanitelných nákupů                                              | Standardní | pln23                  | odp\_taz23\_nar                  | odp\_tuz23                                | <p>**Plný odpočet:**</p><ul><li>PurchaseVATDeductionStandard</li><li>AcquiredAssetsStandard – VATAdjustmentVendorBadDebtsStandard</li></ul><p>**Úprava odpočtu:**</p><ul><li>PurchaseVATDeductionAdjustStandard</li><li>AcquiredAssetsAdjustStandard – VATAdjustmentVendorBadDebtsAdjustStandard</li></ul> |
| 41  | B2/B3                     | Ze zdanitelných nákupů                                              | Snížená  | pln5                   | odp\_tuz5\_nar                   | odp\_tuz5                                 | <p>**Plný odpočet:**</p><ul><li>PurchaseVATDeductionReduced</li><li>PurchaseVATDeductionReduced2</li><li>AcquiredAssetsReduced – VATAdjustmentVendorBadDebtsReduced – VATAdjustmentVendorBadDebtsReduced2</li></ul><p>**Úprava odpočtu:**</p><ul><li>PurchaseVATDeductionAdjustReduced</li><li>PurchaseVATDeductionAdjustReduced2 – VATAdjustmentVendorBadDebtsAdjustReduced – VATAdjustmentVendorBadDebtsAdjustReduced2</li><li>AcquiredAssetsAdjustReduced</li></ul> |
| 42  | Nelze použít            | Z dovozu zboží, když je finančním úřadem celní úřad | Nelze použít      | dov\_cu                 | odp\_cu\_nar                       | odp\_cu                                   | <p>**Plný odpočet:**</p><ul><li>ImportVATDeductionTaxAdminCustomsOffice</li></ul><p>**Úprava odpočtu:**</p><ul><li>ImportVATDeductionAdjustTaxAdminCustomsOffice</li></ul> |
| 43  | Nelze použít            | Ze zdanitelných transakcí vykázaných v řádcích 3 až 13                 | Standardní | nar\_zdp23              | od\_zdp23                         | odkr\_zdp23                               | <p>**Plný odpočet:**</p><ul><li>VATDeductionFromPurchasesWithBATPayableStandard</li><li>EUPurchaseGoodsUseTaxStandard (řádek 3)</li><li>EUPurchaseServicesUseTaxStandard (řádek 5)</li><li>ImportGoodsUseTaxStandard (řádek 7)</li><li>EUPurchaseNewTransportUseTax (řádek 9)</li><li>DomesticPurchaseReverseChargeUseTaxStandard (řádek 10)</li><li>OtherPurchasesUseTaxStandard (řádek 12)</li></ul><p>**Úprava odpočtu:**</p><ul><li>VATDeductionAdjustFromPurchasesWithVATPayableStandard</li></ul> |
| 44  | Nelze použít            | Ze zdanitelných transakcí vykázaných v řádcích 3 až 13                | Snížená  | nar\_zdp5               | od\_zdp5                          | odkr\_zdp5                                | <p>**Plný odpočet:**</p><ul><li>VATDeductionFromPurchasesWithVATPayableReduced</li><li>EUPurchaseGoodsUseTaxReduced (řádek 4)</li><li>EUPurchaseGoodsUseTaxReduced2 (řádek 4)</li><li>EUPurchaseServicesUseTaxReduced (řádek 6)</li><li>EUPrchaseServicesUseTaxReduced2 (řádek 6)</li><li>ImportGoodsUseTaxReduced (řádek 8)</li><li>DomesticPurchaseReverseChargeUseTaxReduced (řádek 11)</li><li>DomesticPurchaseReverseChargeUseTaxReduced (řádek 11)</li><li>OtherPurchasesUseTaxReduced (řádek 13)</li><li>OtherPurchasesUseTaxReduced2 (řádek 13)</li></ul><p>**Úprava odpočtu:**</p><ul><li>VATDeductionAdjustFromPurchasesWithVATPayableReduced</li></ul> |
| 45  | Nelze použít            | Oprava odpočtů daně                                        | Nelze použít      | Nelze použít                    | odp\_rez\_nar                      | odp\_rezim                                | <p>**Plný odpočet:**</p><ul><li>VATDeductionCorrection</li></ul><p>**Úprava odpočtu:**</p><ul><li>VATDeductionAdjustCorrection</li></ul> |
| 46  | Nelze použít            | Celkový odpočet<br>(40 + 41 + 42 + 43 + 44 + 45)                 | Nelze použít      | Nelze použít                    | odp\_sum\_nar                      | odp\_sum\_kr                               | |
| 47  | Nelze použít            | Hodnota nabytého majetku definovaná v \§4 odst. d) ae)        | x        | nar\_maj                | od\_maj                           | odkr\_maj                                 | <p>Informační hodnota zahrnutá v řádcích 40 a 41.</p><p>**Plný odpočet:**</p><ul><li>AcquiredAssetsStandard</li><li>AcquiredAssetsReduced</li></ul><p>**Úprava odpočtu:**</p><ul><li>AcquiredAssetsAdjustStandard</li><li>AcquiredAssetsAdjustReduced</li></ul> |

### <a name="section-5-reduction-of-the-right-to-deduct"></a><a name="righttodeduct"></a>Oddíl 5: Omezení nároku na odpočet

| Řádek | popis                                                                                    | Základ daně (prvek XML) | Komentář |
|-----|------------------------------------------------------------------------------------------------|------------------------|---------|
| 50  | Prodej osvobozený od daně                                                                                   | plnosv\_kf             | Výsledek vyhledávání parametrů specifických pro aplikaci: **SalesVATExempt**. |
| 51  | Hodnota prodeje nezahrnutá do výpočtu koeficientu řádku 53 – s nárokem na odpočet    | pln\_nkf               | <p>Informační hodnota: Pouze pro prosincové přiznání. Tato hodnota platí pro všechny transakce od ledna do prosince.</p><p>Uživatel ručně zadá částku parametru **Hodnota zdanitelného prodeje nezahrnutá do výpočtu koeficientu** v dialogovém okně sestavy.</p> |
| 51  | Hodnota prodeje nezahrnutá do výpočtu koeficientu řádku 53 – bez nároku na odpočet | plnosv\_nkf            | <p>Informační hodnota: Pouze pro prosincové přiznání. Tato hodnota platí pro všechny transakce od ledna do prosince.</p><p>Uživatel ručně zadá částku parametru **Hodnota zdanitelného prodeje nezahrnutá do výpočtu koeficientu** v dialogovém okně sestavy.</p> |
| 52  | Část sníženého odpočtu daně (s úpravou odpočtu): poměrný koeficient            | koef\_p20\_nov         | <p>Poměrný koeficient.</p><p>Vstupní parametr uživatele: **Poměrný koeficient**.</p> |
| 52  | Část sníženého odpočtu daně (s úpravou odpočtu): částka odpočtu                | dp\_uprav\_kf          | Automaticky vypočteno jako částka odpočtu = 46.odp\_sum\_kr × 52.koef\_p20\_nov. |
| 53  | Vypořádání odpočtu daně – nový poměrný koeficient                                         | koef\_p20\_vypor       | <p>Pouze pro prosincové přiznání.</p><p>Nový poměrný koeficient.</p><p>Uživatel ručně zadá částku parametru **Nový poměrný koeficient**.</p><p>Tuto částku můžete ručně vypočítat na základě všech částek uvedených v přiznání, které pochází z časového rozmezí leden až prosinec, následujícím způsobem:</p><ol><li>Výpočet pro **Hodnota zdanitelného prodeje** jako řádky (1 + 2 + 20 + 21 + 22 + 23 + 24 + 25 + 26 + 31).TaxBase.</li><li>Výpočet pro **Hodnota prodeje osvobozeného od daně** jako řádek 50.TaxBase.</li><li>Výpočet pro **Nový poměrný koeficient** jako **Hodnota zdanitelného prodeje** – **Hodnota zdanitelného prodeje nezahrnutá do výpočtu koeficientu** – **Hodnota prodeje osvobozeného od daně nezahrnutá do výpočtu koeficientu**.</li></ol> |
| 53  | Vypořádání odpočtu daně – Změna odpočtu                                              | vypor\_odp             | <p>Pouze pro prosincové přiznání.</p><p>Úprava odpočtu daně.</p><p>Tento řádek odráží opravu ročních odpočtů DPH na základě skutečného poměrného koeficientu oproti odhadovanému poměrnému koeficientu, který byl použit v průběhu roku.</p><p>Uživatel ručně zadá částku parametru **Hodnota ročního vypořádání odpočtu daně** v dialogovém okně sestavy.</p><p>Tuto částku můžete ručně vypočítat na základě všech částek uvedených v přiznání, které pochází z časového rozmezí leden až prosinec, následujícím způsobem:</p><p>Řádek 46.Úprava odpočtu daně × (**Nový poměrný koeficient** – **Poměrný koeficient**)</p>|

### <a name="section-6-tax-calculation"></a><a name="taxcalculation"></a>Oddíl 6: Výpočet daně

| Řádek | popis                          | Hodnota       | Komentář |
|-----|--------------------------------------|-------------|---------|
| 60  | Oprava srážky daně             | uprav\_odp  | <p>Pouze pro prosincové přiznání.</p><p>Výsledek vyhledávání parametru specifického pro aplikaci: **DPHDeductionAdjustmentFA**.</p><p>U veškerého dlouhodobého majetku, u kterého daňový poplatník uplatnil odpočet DPH, musí poplatník sledovat, jak je dlouhodobý majetek využíván. Pokud se během sledovaného období změní nárok na odpočet DPH, musí poplatník upravit příslušný odpočet DPH ve výkazu DPH v prosinci za rok, kdy došlo ke změně nároku na odpočet DPH.</p><p>Nastavte speciální kód DPH pro úpravu odpočtu daně, ke které dojde z důvodu změny v používání dlouhodobého majetku, a ručně zaúčtujte daňovou transakci na 100 procent částky daně, když musíte na tomto řádku upravit odpočet DPH.</p> |
| 61  | Vrácení daně                           | dan\_vrac   | <p>Výsledek vyhledávání parametru specifického pro aplikaci: **TaxRefund**.</p><p>Za určitých podmínek musí daňový poplatník částečně vrátit DPH, kterou zaplatil zákazník. Například osoba ze třetí země nebo regionu zaplatila českou DPH za zboží, které zakoupila v České republice a poté přepravila do třetí země nebo regionu.</p><p>V takovém případě daňový poplatník přizná příslušnou transakci na řádku 1 nebo 2 ve výkazu DPH a poté může po splnění všech podmínek stanovených českým zákonem o DPH požadovat vrácení daně na řádku 61.</p><p>Nastavte speciální kód DPH pro vrácení daně takovým osobám a ručně zaúčtujte daňovou transakci na 100 procent částky daně, když musíte na tomto řádku zobrazit vrácení daně.</p> |
| 62  | Celková odváděná daň                    | dan\_zocelk | Automaticky počítáno jako řádky 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 + 11 + 12 + 13−61. |
| 63  | Celkový odpočet daně                  | odp\_zocelk | Automaticky počítáno jako řádek 46.Plný odpočet daně + řádek 52.Odpočet + řádek 53.Změna odpočtu + řádek 60. |
| 64  | Daň k zaplacení                       | dano\_da    | Automaticky počítáno jako řádek 62 – řádek 63, pokud 62 je \> 63. |
| 65  | Nadměrný odpočet                     | dano\_no    | Automaticky počítáno jako řádek 63 – řádek 62, pokud 63 je \> 62. |
| 66  | Úprava pro dodatečné daňové přiznání | dano        | Automaticky počítáno jako řádek 62 – řádek 63. |

## <a name="vat-control-statement"></a>Kontrolní hlášení DPH

Následující sekce poskytují přehled oddílů kontrolního hlášení DPH.

### <a name="section-a1-sale-of-goods-and-services-under-domestic-reverse-charges"></a><a name="sectiona1"></a>Oddíl A1: Prodej zboží a služeb v rámci tuzemského přenesení daňové povinnosti

Oddíl A1 zobrazuje dokumenty, které generují částku v řádku 25 přiznání k DPH. O každém dokumentu poskytuje následující informace.

| Pole                                          | Prvek XML   |
|------------------------------------------------|---------------|
| Číslo daňového dokladu                            | c\_evid\_dd   |
| DIČ zákazníka (pouze číselná část) | ic\_odb       |
| Datum (což je datum registrace k DPH)       | duzp          |
| Kód předmětu                                   | kod\_pred\_pl |
| Základ daně                                       | zakl\_dane1   |

Chcete-li automaticky určit kód subjektu pro dokument, nastavte dostatek skupin položek přenesení daňové povinnosti a přidružte je k položkám (produktům), skupinám položek nebo kategoriím nákupu. Další informace naleznete v části [Nastavení skupin položek přenesení daňové povinnosti](#set-up-reverse-charge-item-groups) později v tomto tématu. Další informace, jak konfigurovat přenesení daňové povinnosti, viz [Přenesení daňové povinnosti k DPH](emea-reverse-charge.md). Pokud účtujete příchozí přenesení daňové povinnosti v denících faktur dodavatele, které nejsou přidruženy k produktům, musíte mít dostatek skupin DPH položek k rozlišení kódů subjektu přenesené daňové povinnosti.

K výsledku vyhledávání **\$SubjectCodeLookup** v parametrech specifických pro aplikaci formátu **Kontrolní hlášení DPH (CZ)** musíte také přidružit dvojice skupin položek přenesení daňové povinnosti a daňových kódů. Další informace, jak nastavit parametry specifické pro aplikaci, najdete v části [Nastavení parametrů pro kódy subjektu](#set-up-parameters-for-subject-codes) dále v tomto tématu.

Následující kódy subjektu jsou k dispozici ve formátu **Kontrolní hlášení DPH v XML (CZ)**.

| Kód                     | popis                                                                   |
|--------------------------|-------------------------------------------------------------------------------|
| GoldDelivery             | 1. Dodávka zlata (\§92b)                                                      |
| TangibleAssetDelivery    | 3. Dodávka hmotného majetku (\§92d)                                        |
| ConstructionInstallation | 4. Výstavba nebo montáž (\§92e)                                       |
| GoodsAnnex5              | 5. Zboží uvedené v příloze 5 zákona o DPH (\§92c)                             |
| AllowancesGasEmission    | 11. Převod povolenek a emisí skleníkových plynů                       |
| CerealsIndustrialCrops   | 12. Obiloviny a průmyslové plodiny                                              |
| Metals                   | 13. Kovy, včetně drahých kovů                                         |
| MobilePhones             | 14. Mobilní telefony                                                             |
| IntegratedCircuits      | 15. Integrované obvody a desky tištěných spojů                            |
| PortableDevices          | 16. Přenosná zařízení pro automatické zpracování dat (např. tablety nebo notebook) |
| VideoGameConsole         | 17. Videoherní konzole                                                       |

### <a name="section-b1-purchase-of-goods-and-services-under-the-domestic-reverse-charge-92"></a>Oddíl B1: Nákup zboží a služeb v rámci tuzemského přenesení daňové povinnosti (§92)

Oddíl B1 poskytuje informace, které jsou obsaženy v dokumentech a slouží ke generování částek v řádcích 10 a 11 přiznání k DPH.

Tento oddíl poskytuje o každém dokumentu následující informace.

| Pole                                               | Prvek XML   |
|-----------------------------------------------------|---------------|
| Číslo daňového dokladu                                 | c\_evid\_dd   |
| DIČ dodavatele (pouze číselná část)        | dic\_dod      |
| Datum (což je datum příchozí faktury dodavatele) | duzp          |
| Kód předmětu                                        | kod\_pred\_pl |
| Základ daně se standardní sazbou                           | zakl\_dane1   |
| Částka daně se standardní sazbou                         | dan1          |
| Základ daně s první sníženou sazbou                      | zakl\_dane2   |
| Částka daně s první sníženou sazbou                    | dan2          |
| Základ daně s druhou sníženou sazbou                     | zakl\_dane3   |
| Částka daně s druhou sníženou sazbou                   | dan3          |

Chcete-li automaticky určit kód subjektu pro dokument, musíte použít stejná nastavení, která byla popsána v oddílu A1.

### <a name="section-a2-purchases-with-reverse-charge-excluding-domestic-reverse-charge-with-an-obligation-to-pay-vat"></a>Oddíl A2: Nákupy s přenesením daňové povinnosti, s výjimkou tuzemského přenesení daňové povinnosti, s povinností platit DPH

Oddíl A2 zobrazuje dokumenty, které generují částky v řádcích 3, 4, 5, 6 a 9 (nákup zboží uvnitř Společenství, nákup služeb uvnitř Společenství a nákup nových dopravních prostředků uvnitř Společenství) a řádcích 12 a 13 (ostatní nákupy s povinností platby DPH) v přiznání k DPH.

Tento oddíl poskytuje o každém dokumentu následující informace.

| Pole                                                                  | Prvek XML |
|------------------------------------------------------------------------|-------------|
| Číslo daňového dokladu                                                    | c\_evid\_dd |
| DIČ dodavatele z jiného členského státu (pouze číselná část) | vatid\_dod  |
| Země, která dodavateli přidělila DIČ                    | k\_stat     |
| Datum (což je datum registrace k DPH)                               | Dppd        |
| Základ daně se standardní sazbou                                              | zakl\_dane1 |
| Částka daně se standardní sazbou                                            | dan1        |
| Základ daně s první sníženou sazbou                                         | zakl\_dane2 |
| Částka daně s první sníženou sazbou                                       | dan2        |
| Základ daně s druhou sníženou sazbou                                        | zakl\_dane3 |
| Částka daně s druhou sníženou sazbou                                      | dan3        |

### <a name="section-a3-transactions-with-the-special-scheme-of-gold-sales"></a>Oddíl A3: Transakce se zvláštním režimem prodeje zlata

Oddíl A3 obsahuje dokumenty, které generují částku v řádku 25 přiznání k DPH a ostatní prodeje s nárokem na odpočet DPH na vstupu.

Chcete-li automaticky určit transakce, nastavte pro ně speciální kód DPH a přidružte jej k výsledku vyhledávání **OtherSalesWithRightToDeductGoldInvestment** pro **\$ReportFieldLookup** v parametrech specifických pro aplikaci ve formátu přiznání k DPH a formátu kontrolního hlášení DPH.

Tento oddíl poskytuje o každém dokumentu následující informace.

| Pole                                                         | Prvek XML      |
|---------------------------------------------------------------|------------------|
| Číslo daňového dokladu                                           | c\_evid\_dd      |
| DIČ zákazníka (pouze číselná část), pokud existuje   | vatid\_odb       |
| Země, která zákazníkovi přidělila DIČ         | k\_stat          |
| Datum (rejstřík DPH)                                           | dup              |
| Hodnota prodeje                                        | osv\_plneni      |
| Místo bydliště zákazníka, pokud nemá DIČ  | m\_pobytu\_sidlo |
| Jméno a příjmení zákazníka, pokud nemá DIČ | jm\_prijm\_obch  |
| Datum narození zákazníka, pokud nemá DIČ       | d\_narozeni      |

## <a name="section-a4-taxable-sales-with-amounts-above-10000-including-vat-and-all-vat-adjustments-made-for-customer-bad-debts"></a><a name="sectionA4"></a>Oddíl A4: Zdanitelný prodej s částkami nad 10 000 včetně DPH a se všemi úpravami DPH provedenými u nedobytných pohledávek zákazníků

Oddíly A4 a A5 obsahuje dokumenty, které generují částky v řádcích 1 a 2 přiznání k DPH.

Informace o úpravách částky DPH u nedobytných pohledávek zákazníků jsou také uvedeny v řádku 33 přiznání k DPH.

Chcete-li automaticky určit úpravu částky DPH u nedobytných pohledávek, vytvořte speciální kód daně a použijte jej k zaúčtování odpisu nedobytných pohledávek zákazníka. Další informace viz [Odepsání nedobytných pohledávek zákazníků pomocí funkce Odepsat](#write-off-customer-bad-debts-by-using-the-write-off-function) dále v tomto tématu. Také přidružte tento kód DPH k výsledkům vyhledávání **VATAdjustmentCustomerBadDebtsStandard**, **VATAdjustmentCustomerBadDebtsReduced** a **VATAdjustmentCustomerBadDebtsReduced2** pro **\$ReportFieldLookup** v parametrech specifických pro aplikaci ve formátu přiznání k DPH a formátu kontrolního hlášení DPH.

Tento oddíl poskytuje o každém dokumentu následující informace.

| Pole                                                                                                                                              | Prvek XML  |
|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| Číslo daňového dokladu                                                                                                                                | c\_evid\_dd    |
| DIČ zákazníka                                                                                                                         | dic\_odb      |
| Datum (rejstřík DPH)                                                                                                                                | Dppd         |
| <p>Kód režimu plnění:</p><ul><li>**0** – Normální plnění</li><li>**1** – Zvláštní režim pro cestovní služby</li><li>**2** – Zvláštní režim pro použité zboží</li></ul> | kod\_rezim\_pl |
| Základ daně se standardní sazbou                                                                                                                          | zakl\_dane1   |
| Částka daně se standardní sazbou                                                                                                                        | dan1         |
| Základ daně s první sníženou sazbou                                                                                                                     | zakl\_dane2   |
| Částka daně s první sníženou sazbou                                                                                                                   | dan2         |
| Základ daně s druhou sníženou sazbou                                                                                                                    | zakl\_dane3   |
| Částka daně s druhou sníženou sazbou                                                                                                                  | dan3         |
| <p>Příznak úpravy DPH u nedobytných pohledávek:</p><ul><li>**N** – Dokument není úpravou DPH u nedobytných pohledávek.</li><li>**P** – Dokument je úpravou DPH u nedobytných pohledávek.</li></ul> | zdph\_44      |

Chcete-li automaticky určit kód režimu plnění, přidružte kódy DPH k výsledku vyhledávání **\$FulfillmentModeCodeLookup** v parametrech specifických pro aplikaci formátu kontrolního hlášení DPH. Další informace, jak nastavit parametry specifické pro aplikaci, najdete v části [Nastavení parametrů pro kódy režimu plnění](#set-up-parameters-for-fulfillment-mode-codes) dále v tomto tématu.

Následující kódy režimu plnění jsou k dispozici ve formátu XML kontrolního hlášení DPH.

| Kód                            | popis                                          |
|---------------------------------|------------------------------------------------------|
| NormalFilling                   | 0. Normální plnění                                    |
| SpecialSchemeForTravelService   | 1. \§ 89 ZDPH (zvláštní režim pro cestovní služby)    |
| SpecialRegimeForSecondHandGoods | 2. \§ 90 ZDPH (zvláštní režim pro použité zboží) |

### <a name="section-b2-taxable-purchases-with-an-amount-above-10000-including-vat-and-all-vat-adjustments-made-for-vendor-bad-debts"></a>Oddíl B2: Zdanitelné nákupy s částkami nad 10 000 včetně DPH a se všemi úpravami DPH provedenými u nedobytných pohledávek dodavatelů

Oddíly B2 a B2 obsahují dokumenty, které generují částky v řádcích 40 a 41 přiznání k DPH.

Informace o úpravách částky DPH u nedobytných pohledávek dodavatelů jsou také uvedeny v řádku 34 přiznání k DPH.

Chcete-li automaticky určit úpravu částky DPH u nedobytných pohledávek, vytvořte speciální kód daně a použijte jej k zaúčtování odpisu nedobytných pohledávek dodavatele. Další informace najdete v části [Ruční odpisy nedobytných pohledávek dodavatele](#manually-write-off-vendor-bad-debts) dále v tomto tématu. Přidružte tento kód DPH k výsledkům vyhledávání **VATAdjustmentVendorBadDebtsStandard**, **VATAdjustmentVendorBadDebtsReduced**, and **VATAdjustmentVendorBadDebtsReduced2** pro **\$ReportFieldLookup** v parametrech specifických pro aplikaci ve formátu přiznání k DPH a formátu kontrolního hlášení DPH.

Oddíl B2 poskytuje o každém dokumentu následující informace.

| Pole                                                                                                                                               | Prvek XML |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Číslo daňového dokladu                                                                                                                                 | c\_evid\_dd |
| DIČ dodavatele                                                                                                                            | dic\_dod    |
| Datum (datum příchozí faktury dodavatele)                                                                                                          | Dppd        |
| Základ daně se standardní sazbou                                                                                                                           | zakl\_dane1 |
| Částka daně se standardní sazbou                                                                                                                         | dan1        |
| Základ daně s první sníženou sazbou                                                                                                                      | zakl\_dane2 |
| Částka daně s první sníženou sazbou                                                                                                                    | dan2        |
| Základ daně s druhou sníženou sazbou                                                                                                                     | zakl\_dane3 |
| Částka daně s druhou sníženou sazbou                                                                                                                   | dan3        |
| <p>Příznak úpravy DPH u nedobytných pohledávek:</p><ul><li>**N** – Dokument není úpravou DPH u nedobytných pohledávek.</li><li>**P** – Dokument je úpravou DPH u nedobytných pohledávek.</li></ul> | zdph\_44     |
| <p>Příznak nároku na poměrný odpočet: Ano/Ne</p><p>**Poznámka:** Ve výchozím nastavení je tohle pole nastaveno na **Ne**.</p> | pomer       |

### <a name="section-a5-taxable-sales-with-an-amount-below-10-000-including-vat-and-when-there-is-no-obligation-to-issue-a-tax-document"></a>Oddíl A5: Zdanitelný prodej s částkou pod 10 000 včetně DPH a bez povinnosti vystavit daňový doklad

Oddíly A4 a A5 obsahuje dokumenty, které generují částky v řádcích 1 a 2 přiznání k DPH.

Oddíl A5 obsahuje jeden řádek, který obsahuje následující informace pro všechny dokumenty obsažené v této části.

| Pole                             | Prvek XML |
|-----------------------------------|-------------|
| Základ daně se standardní sazbou         | zakl\_dane1 |
| Částka daně se standardní sazbou       | dan1        |
| Základ daně s první sníženou sazbou    | zakl\_dane2 |
| Částka daně s první sníženou sazbou  | dan2        |
| Základ daně s druhou sníženou sazbou   | zakl\_dane3 |
| Částka daně s druhou sníženou sazbou | dan3        |

### <a name="section-b3-taxable-purchases-with-an-amount-below-10000-including-vat"></a>Oddíl B3: Zdanitelné nákupy s částkou pod 10 000 včetně DPH

Oddíly B2 a B2 obsahují dokumenty, které generují částky v řádcích 40 a 41 přiznání k DPH.

Oddíl B3 obsahuje jeden řádek, který obsahuje následující informace pro všechny dokumenty obsažené v této části.

| Pole                             | Prvek XML |
|-----------------------------------|-------------|
| Základ daně se standardní sazbou         | zakl\_dane1 |
| Částka daně se standardní sazbou       | dan1        |
| Základ daně s první sníženou sazbou    | zakl\_dane2 |
| Částka daně s první sníženou sazbou  | dan2        |
| Základ daně s druhou sníženou sazbou   | zakl\_dane3 |
| Částka daně s druhou sníženou sazbou | dan3        |

## <a name="set-up-the-vat-declaration"></a>Vytvoření přiznání k DPH

Chcete-li začít pracovat s přiznáním k DPH, měli byste si stáhnout formáty elektronického výkaznictví. V [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) v knihovně Sdílený majetek si stáhněte nejnovější verze následujících konfigurací elektronického výkaznictví (ER) pro formát přiznání k DPH:

- **Model daňového přiznání**
- **Mapování modelu daňového přiznání**
- **Přiznání k DPH v XML (CZ)** – Tato konfigurace je ve formátu XML DPHDP3.
- **Přiznání k DPH pro Excel (CZ)** – Tuto konfiguraci lze použít k náhledu částek přiznání k DPH v Microsoft Excel. Šablona aplikace Excel je k dispozici pouze v angličtině. Pokud musí být zpráva vytištěna v jiném jazyce, musíte provést malé přizpůsobení překladu šablony aplikace Excel do jiného jazyka a toto přizpůsobení musíte připojit k odvozené konfiguraci.
- **Kontrolní hlášení DPH (CZ)** – Tato konfigurace je ve formátu XML DPHKH1.

Další informace viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="set-up-application-specific-parameters-for-formats"></a>Nastavení parametrů specifických pro přihlášení pro dané formáty

### <a name="set-up-parameters-for-declaration-fields"></a>Nastavení parametrů pro pole přiznání

Chcete-li automaticky generovat přiznání k DPH, musíte přidružit kódy DPH v polích aplikace a sestavy v konfiguraci ER.

1. Přejděte na **Pracovní prostory \> Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Přiznání k DPH v XML (CZ)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na záložce s náhledem **Vyhledávání** vyberte vyhledávání **\$ReportFieldLookup**.
4. Na záložce s náhledem **Podmínky** přidružte kódy DPH a pole sestavy.

    | Sloupcový          | popis |
    |-----------------|-------------|
    | Výsledek vyhledávání   | Vyberte pole sestavy pro nastavení. Další informace o polích sestavy a jejich přiřazení k řádkům přiznání k DPH najdete v části [Přehled přiznání k DPH](#overview) dříve v tomto tématu. |
    | Kód daně (kód) | <p>Vyberte kód DPH, který chcete přidružit k poli sestavy. Zaúčtované daňové transakce, které používají vybraný kód DPH, budou shromážděny v příslušném poli sestavy.</p><p>Doporučujeme oddělit kódy DPH tak, aby jeden kód DPH generoval částky pouze v jednom poli sestavy.</p> |
    | Jméno            | <p>Pokud jste nevytvořili dostatek kódů DPH, takže jeden kód DPH vygeneruje částky pouze v jednom poli sestavy, můžete vytvořit klasifikátor transakcí. K dispozici jsou následující klasifikátory transakcí:</p><ul><li>**Nákup**</li><li>**PurchaseExempt** (nákup osvobozený od daně)</li><li>**PurchaseReverseCharge** (daň splatná z přenesené daňové povinnosti při nákupu)</li><li>**Prodej.**</li><li>**SalesExempt** (prodej osvobozený od daně)</li><li>**SalesReverseCharge** (daň odvedená z přenesené daňové povinnosti při nákupu nebo prodeji)</li><li>**Importní DPH**</li></ul>Pro každý klasifikátor transakcí je k dispozici také klasifikátor dobropisu. Například jeden z těchto klasifikátorů je **PurchaseCreditNote** (nákupní dobropis). |

5. Chcete-li zabránit tomu, aby formát vyvolal chybovou zprávu o výjimce z důvodu zmeškaného nastavení při spuštění sestavy, vytvořte následující řádek jako poslední řádek v parametrech.

    | Výsledek vyhledávání | Kód daně (kód) | Jméno          |
    |---------------|-----------------|---------------|
    | Ostatní         | \*Neprázdné\*   | \*Neprázdné\* |

    > [!IMPORTANT]
    > Tento řádek musí být posledním řádkem v parametrech.
    >
    > Pokud vytvoříte tento řádek, ujistěte se, že jste nastavili parametry pro všechny kódy DPH v systému. V tom případě, pokud v nastavení chybí nějaké kódy DPH, nebudou pro přiznání k DPH shromažďovány daňové transakce, které tyto kódy používají. Pokud tento řádek nevytvoříte a některé daňové transakce používají kódy DPH, které nejsou nakonfigurovány v parametrech specifických pro aplikaci, zobrazí se při spuštění sestavy chybová zpráva.

6. V poli **Stát** vyberte **Dokončeno** a zkontrolujte parametry.

    [![Záložka s náhledem Podmínky na stránce s parametry specifickými pro aplikaci.](media/Pic1_ReportFieldLookup.png)](media/Pic1_ReportFieldLookup.png)

7. V podokně Akce volbou **Export** exportujte parametry do souboru XML.
8. Vyberte konfiguraci **Přiznání k DPH pro Excel (CZ**) a poté v podokně Akce volbou **Import** importujte parametry, pro které jste nakonfigurovali **Přiznání k DPH v XML (CZ)**. 
9. V poli **Stav** vyberte možnost **Dokončeno**.
10. Vyberte konfiguraci **Kontrolní hlášení DPH v XML (CZ)** a poté vyberte stejné hodnoty, které jste vybrali v kroku 4.
11. V poli **Stav** vyberte možnost **Dokončeno**.

### <a name="set-up-parameters-for-subject-codes"></a>Nastavení parametrů pro kódy subjektů 

Chcete-li automaticky klasifikovat transakci podle kódu subjektu přenesení daňové povinnosti v oddílech A1 a B1 kontrolního hlášení DPH, přidružte v aplikaci páry skupin položek přenesení daňové povinnosti a skupin DPH položek a poté kódy zadejte do konfigurace ER.

1. Přejděte na **Pracovní prostory \> Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Kontrolní hlášení DPH v XML (CZ)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na záložce s náhledem **Vyhledávání** vyberte **\$SubjectCodeLookup**.
4. Na záložce s náhledem **Podmínky** přidružte skupiny položek přenesení daňové povinnosti a kódy subjektů.

    | Sloupcový                              | popis |
    |-------------------------------------|-------------|
    | Výsledek vyhledávání                       | Vyberte kód subjektu. Úplný seznam kódů subjektů naleznete v části [Oddíl A1: Prodej zboží a služeb v rámci tuzemského přenesení daňové povinnosti](#sectiona1) dříve v tomto tématu. |
    | Kód přenesení daňové povinnosti (kód)          | Vyberte skupinu položek přenesení daňové povinnosti, kterou chcete přidružit k vybranému kódu subjektu. U některých transakcí, pokud zaúčtujete příchozí transakce přenesení daňové povinnosti, které neobsahují odkaz na produkt, musíte přidružit skupinu DPH položky s kódem subjektu. V takovém případě vyberte v tomto poli hodnotu **\*Prázdné\***. Aby se zabránilo generování chyby při výjimce, když transakce neobsahují přenesení daňové povinnosti, parametry specifické pro aplikaci musí vždy obsahovat jeden řádek, kde pole **Výsledek vyhledávání** je nastaveno na **Ostatní** a **Kód přenesení daňové povinnosti (kód)** je nastaveno na **\*Prázdné\***. Tento řádek musí být posledním řádkem v nastavení. |
    | Skupina DPH položky (TaxItemGroup) | Vyberte skupinu DPH položky, kterou chcete přidružit k vybranému kódu subjektu. Pokud nemáte k dispozici příslušnou skupinu položky přenesení daňové povinnosti, která se použije při zaúčtování příchozích transakcí přenesení daňové povinnosti, které neobsahují odkaz na produkt (například transakce z deníku faktury dodavatele), musíte vybrat konkrétní skupinu DPH položky. Jinak můžete pro všechny řádky v tomto sloupci vybrat **\*Není prázdné\***. |

5. Chcete-li zabránit tomu, aby formát selhal a vyvolal chybovou zprávu o výjimce z důvodu zmeškaného nastavení, vytvořte následující řádek jako poslední řádek.

    | Výsledek vyhledávání | Kód přenesení daňové povinnosti (kód) | Skupina DPH položky (TaxItemGroup) | Komentář |
    |---------------|----------------------------|-------------------------------------|---------|
    | Ostatní         | \*Bianko\*                  | \*Neprázdné\*                       | Tento řádek musí být vytvořen, aby se zabránilo generování chybové zprávy u transakcí, které nemají kód přenesení daňové povinnosti. |

[![Vyhledání kódu subjektu.](media/Pic2_SubjectCodeLookup.png)](media/Pic2_SubjectCodeLookup.png)

### <a name="set-up-parameters-for-fulfillment-mode-codes"></a>Nastavení parametrů pro kódy režimu plnění

Chcete-li automaticky klasifikovat transakci podle kódu režimu plnění v oddílu A4 kontrolního hlášení DPH, přidružte kódy DPH v aplikaci a kódy režimu subjektu plnění v konfiguraci ER.

1. Přejděte na **Pracovní prostory \> Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Kontrolní hlášení DPH v XML (CZ)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na záložce s náhledem **Vyhledávání** vyberte **\$FulfillmentModeCodeLookup**.
4. Na záložce s náhledem **Podmínky** přidružte kódy DPH a kódy režimu subjektu plnění.

    | Sloupcový          | popis |
    |-----------------|-------------|
    | Výsledek vyhledávání   | Vyberte kód plnění. Úplný seznam kódů naleznete v části [Oddíl A4: Zdanitelný prodej s částkami nad 10 000 včetně DPH a se všemi úpravami DPH provedenými u nedobytných pohledávek zákazníků](#sectionA4) dříve v tomto tématu. |
    | Kód daně (kód) | Vyberte kód DPH. |

5. Pokud máte transakce, které používají pouze normální plnění, můžete v nastavení vytvořit následující řádek. Jinak vytvořte stejný řádek, který jste vytvořili jako poslední řádek v předchozím nastavení, chcete-li zabránit tomu, aby formát selhal a vyvolal chybovou zprávu o výjimce z důvodu zmeškaného nastavení.

    | Výsledek vyhledávání | Kód daně (kód) |
    |---------------|-----------------|
    | NormalFilling | \*Neprázdné\*   |

### <a name="set-up-parameters-for-no-obligation-to-issue-a-tax-document"></a>Nastavení parametrů pro zbavení povinnosti vystavit daňový doklad

Prodejní transakci lze automaticky klasifikovat, že splňuje podmínku, že neexistovala povinnost vystavit daňový doklad, takže transakce by měla být uvedena v oddílu A5 bez ohledu na prahovou hodnotu. Chcete-li automaticky klasifikovat prodejní transakci tímto způsobem, přidružte páry skupin DPH a kódy DPH z aplikace s podmínkami **Ano** nebo **Ne** v konfiguraci ER.

1. Přejděte na **Pracovní prostory \> Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte konfiguraci **Kontrolní hlášení DPH v XML (CZ)** a poté vyberte **Konfigurace \> Nastavení parametrů specifických pro aplikaci**.
3. Na záložce s náhledem **Vyhledávání** vyberte **\$NoTaxDocument**.
4. Na záložce s náhledem **Podmínky** přidružte skupiny DPH a kódy DPH.

    | Sloupcový          | popis |
    |-----------------|-------------|
    | Výsledek vyhledávání   | Vyberte **Ano**, pokud neexistuje povinnost vystavit daňový doklad. K této situaci obvykle dochází, když zákazník není registrován pro účely DPH. |
    | Skupina prodejní daně | Vyberte skupinu DPH, kterou chcete přidružit k zákazníkovi, pokud neexistuje povinnost vystavit daňový doklad. Pokud můžete určit podmínku pouze pomocí kódu DPH, vyberte **\*Není prázdné\***. |
    | Kód daně (kód) | Vyberte kód DPH, který chcete přidružit k transakci, pokud neexistuje povinnost vystavit daňový doklad. Pokud můžete určit podmínky pouze pomocí skupiny DPH, vyberte **\*Není prázdné\***. |

5. Chcete-li zabránit tomu, aby formát selhal a vyvolal chybovou zprávu o výjimce z důvodu zmeškaného nastavení, vytvořte následující řádek jako poslední řádek v nastavení.

    | Výsledek vyhledávání | Skupina DPH (TaxGroup) | Kód daně (kód) |
    |---------------|----------------------------|-----------------|
    | Žádný            | \*Neprázdné\*              | \*Neprázdné\*   |

6. Zkontrolujte parametry.

    [![Vyhledání podmínky, že neexistuje povinnost vystavit daňový doklad.](media/Pic3_NoTaxDocumentLookup.png)](media/Pic3_NoTaxDocumentLookup.png)

7. Aktualizujte pole **Stav** pro všechny parametry na **Dokončeno**.

## <a name="download-and-import-the-data-management-package-that-has-example-settings-for-electronic-messages"></a>Stažení a import balíčku správy dat, který obsahuje ukázkové nastavení elektronických zpráv

Balíček dat, který obsahuje ukázková nastavení, obsahuje nastavení elektronických zpráv, která se používají ke generování přiznání k DPH a kontrolního hlášení DPH, stejně jako k zobrazení náhledu přiznání k DPH v aplikaci Excel. Tato nastavení můžete rozšířit nebo vytvořit vlastní. Další informace, jak pracovat s elektronickými zprávami a jak vytvořit vlastní nastavení, najdete v části [Elektronické zasílání zpráv](../general-ledger/electronic-messaging.md).

1. V LCS v knihovně Sdílený majetek vyberte **Datový balíček** jako typ majteku a poté stáhněte balíček **Balíček přiznání k DPH CZ EZ**. Stažený soubor má název **Balíček přiznání k DPH CZ EZ.zip**.
2. V pracovním prostoru **Správa dat** vyberte **Importovat**.
3. V části **Podrobnosti úlohy** nastavte následující hodnoty:

    - Do pole **Název** zadejte název úlohy.
    - V poli **Formát zdroje dat** vyberte **Balíček**.

4. V poli **Odeslaný datový soubor** vyberte **Odeslat** a potom vyberte soubor **Balíček přiznání k DPH CZ EZ.zip**, který jste stáhli.
5. Po nahrání datových entit vyberte **Importovat**.
6. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy** a ověřte zpracování importovaných elektronických zpráv.

    | Zpracovává se            | Kód zpracování | popis                                 |
    |-----------------------|-----------------|---------------------------------------------|
    | Přiznání k DPH       | DPHDP3          | Přiznání k DPH v České republice       |
    | Kontrolní hlášení DPH | DPHKH1          | Kontrolní hlášení DPH v České republice |

## <a name="configure-electronic-messages"></a>Konfigurace elektronických zpráv

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Dodatečná pole** a vyberte řádek, který má dodatečné pole.
2. Na záložce s náhledem **Hodnota** přidejte následující hodnoty pro pole.

    | Dodatečné pole     | Hodnota |
    |----------------------|--------|
    | DataBoxID            | Zadejte ID služby Data Box společnosti. |
    | MainEconomicActivity | Zadejte kód hlavní ekonomické aktivity společnosti. |
    | TaxAuthorityToFile   | Zadejte kód finančního úřadu, kterému bude zaslán soubor s přiznáním. |
    | ProRataCoef          | Zadejte poměrný koeficient, který byl použit v průběhu roku. Pokud musíte v přiznání použít poměrný koeficient, zadejte desetinnou hodnotu mezi 0 a 1 a jako oddělovač použijte čárku. |

3. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Zpracování elektronické zprávy** a vyberte řádek, který má zpracování. 
4. Na záložce s náhledem **Další pole zprávy** nastavte výchozí hodnoty pro parametry přiznání.

    | Zpracovává se                                               | Dodatečné pole         | Komentář | Prvek XML |
    |----------------------------------------------------------|--------------------------|---------|-------------|
    | DPHKH1 (kontrolní hlášení DPH)                           | \<DataBoxID\>            | Vyberte ID služby Data Box, které jste zadali dříve. | id\_dats |
    | DPHDP3 (přiznání k DPH)                                 | \<MainEconomicActivity\> | Vyberte hlavní kód ekonomické aktivity, který jste zadali dříve. | c\_okec |
    | DPHDP3 (přiznání k DPH), DPHKH1 (kontrolní hlášení DPH) | \<TaxAuthorityToFile\>   | Vyberte kód finančního úřadu, který jste zadali dříve. | c\_pracufo |
    | DPHDP3 (přiznání k DPH), DPHKH1 (kontrolní hlášení DPH) | \<ReportPeriodicity\>    | Vyberte četnost podání přiznání ve vykazovaném roce: **Měsíčně** nebo **Čtvrtletně** . | <ul><li>**Ctvrt** – U čtvrtletního přehledu bude prvek vyplněn číslem čtvrtletí.</li><li>**Mesic** – U měsíčního přehledu bude prvek vyplněn číslem měsíce.</li></ul> |
    | DPHDP3 (přiznání k DPH)                                 | \<TaxpayerType\>         | Vyberte typ plátce daně: **Plátce daně**, **Skupina** nebo **Ostatní** . | typ\_platce |
    | DPHDP3 (přiznání k DPH), DPHKH1 (kontrolní hlášení DPH) | \<TaxpayerLegalForm\>    | Vyberte formu plátce daně: **Osoba** nebo **Organizace**. | typ\_ds |
    | DPHDP3 (přiznání k DPH)                                 | \<ProRataCoef\>          | Vyberte poměrný koeficient, který jste zadali dříve. | koef\_p20\_nov |
    | DPHDP3 (přiznání k DPH), DPHKH1 (kontrolní hlášení DPH) | \<NullDeclaration\>      | Vyberte **Ne**, což je výchozí hodnota. Toto pole označuje, zda podáte přiznání s hodnotou null. Během zpracování přiznání byste měli mít možnost změnit výchozí hodnotu. | <p>**Přiznání k DPH:**</p><ul><li>Trans = "N", pokud ano</li><li>Trans = "A", pokud ne</li></ul><p>**Kontrolní hlášení DPH:**</p><ul><li>vyzva\_odp = "B", pokud ano</li></ul> |

5. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Akce naplnění záznamů**, vyberte řádek a poté vyberte **Upravit dotaz**.
6. Pomocí filtru vyberte období vyrovnání, která chcete zahrnout do sestavy. 
7. Pokud musíte vykazovat daňové transakce z jiných období vyrovnání v jiném přiznání, vytvořte novou akci **Naplnit záznamy** a vyberte příslušná období vypořádání.

## <a name="configure-system-parameters-and-master-records"></a>Konfigurace parametrů systému a hlavních záznamů

Před vygenerováním přiznání k DPH byste měli zadat následující nastavení.

| Strana                           | popis |
|--------------------------------|-------------|
| Právnické osoby (**Správa organizace \> Organizace \> Právnické osoby**) | Typ daňové registrace musí být přiřazen ke kategorii daňové registrace **ID DPH**. Další informace naleznete v tématu [Nastavení DIČ](tasks/eur-00015-vat-id.md). |
| Právnické osoby                 | <p>Na záložce s náhledem **Adresy** definujte primární adresu právnické osoby.</p><p>Na záložce s náhledem **Kontaktní informace** v polích **Telefon** a **E-mail** vyberte **Primární**.</p> |
| Finanční úřady (**Daň \> Nepřímé daně \> DPH \> Finanční úřady**) | Vytvořte finanční úřad, kam chcete předložit daňové přiznání. Zadejte kód finančního úřadu do pole **Identifikace úřadu**. |
| Všichni zákazníci (**Pohledávky \> Zákazníci \> Všichni zákazníci**), Všichni prodejci (**Závazky \> Dodavatelé \> Všichni dodavatelé**) | Nastavení čísel DIČ pro zákazníky a dodavatele. Další informace naleznete v tématu [Registrace DIČ dodavatele](tasks/eur-00015-registration-vendor-vat-id.md). |
| Parametry hlavní knihy (**Hlavní kniha \> Nastavení \> Nastavení hlavní knihy \> Parametry hlavní knihy**) | <p>Na kartě **DPH** na záložce s náhledem **Možnosti daně** v poli **Mapování formátu přiznání k DPH** vyberte **Přiznání k DPH pro Excel (CZ)**.</p><p>Tento formát bude vytištěn při spuštění sestavy **Vykázat DPH pro období vyrovnání**. Formát se vytiskne také při výběru **Tisk** na stránce **Platby DPH**.</p> |
| Parametry hlavní knihy       | Na kartě **DPH** v oddíle **Speciální sestava** nastavte volbu **Datum rejstříku DPH** na **Ano**. |
| Parametry hlavní knihy       | <p>Na kartě **DPH** na záložce s náhledem **Výkaz DPH** definujte pro společnost následující parametry:</p><ul><li>**Stav plátce daně**</li><li>**Typ plátce daně**</li><li>**Hlavní ekonomická aktivita**</li><li>**Faktor** – zadejte poměrný koeficient, který byl použit v průběhu roku.</li></ul><p>Stejné informace o společnosti můžete nakonfigurovat v dalších polích pro elektronické zprávy.</p><p>Když spustíte přiznání, budete moci vybrat zdroj informací o společnosti v poli **Příslušnost k dani**. Pro místní pole, která jsou k dispozici pro právnickou osobu v České republice, vyberte **Česká republika**. Pro dodatečná pole pro elektronické zprávy vyberte **Výchozí**.</p> |

## <a name="set-up-reverse-charge-item-groups"></a>Nastavení skupin položek přenesení daňové povinnosti

Další informace, jak konfigurovat a použít funkci přenesení daňové povinnosti, viz [Přenesení daňové povinnosti k DPH](emea-reverse-charge.md).

1. Přejděte na **Daň \> Nastavení \> DPH \> Skupiny položek přenesení daňové povinnosti**.
2. Na záložce s náhledem **Nastavení** v poli **Prodej/nákup** vyberte **Nákup**.
3. Vytvořte řádek a vyberte kód položky, skupinu položek nebo kód kategorie nákupu, abyste přidružili nákup k nové skupině položek přenesení daňové povinnosti. 
4. V poli **Kód položky** vyberte **Tabulka**, **Skupina** nebo **Kategorie**.
5. Pokud jste vybrali **Tabulka** nebo **Skupina** v poli **Kód položky**, v poli **Vztah položky** vyberte kód položky nebo skupinu položky.
6. Pokud jste vybrali **Kategorie** v poli **Kód položky**, v poli **Kategorie** vyberte kategorii nákupu.
7. Na záložce s náhledem **Nastavení** v poli **Prodej/nákup** vyberte **Prodej** a přidružte položku, skupinu položek nebo kategorii nákupu, jak je popsáno v krocích 4 až 6.

## <a name="generate-a-vat-declaration"></a>Generování přiznání k DPH

### <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generování přiznání k DPH z elektronických zpráv

Následující kroky lze použít pro ukázku zpracování elektronických zpráv, která je k dispozici v LCS.

Chcete-li generovat soubor XML pro přiznání k DPH, postupujte takto.

1. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
2. V levém podokně vyberte formát zprávy, který chcete vygenerovat. Vyberte například **DPHDP3**.
3. Na záložce s náhledem **Zprávy** vyberte **Novýá** a poté v dialogovém okně **Spuštění zpracování** vyberte **OK**.
4. Vyberte řádek zprávy, který je vytvořen, zadejte popis a poté zadejte počáteční a konečné datum přiznání.
5. Na záložce s náhledem **Zprávy** vyberte **Shromažďovat data** a potom vyberte **OK**.
6. Na kartě s náhledem **Položky zprávy** zkontrolujte platby DPH, které jsou přeneseny ke zpracování. Ve výchozím nastavení jsou zahrnuty všechny platby DPH ve vybraném období, které nebyly zahrnuty v žádné jiné zprávě stejného zpracování.
7. Volitelně: Vyberte **Původní dokument**, chcete-li zkontrolovat platby DPH, nebo zvolte **Odstranit**, chcete-li vyloučit ze zpracování platby DPH. Pokud tento krok přeskočíte, stále můžete vygenerovat přiznání k DPH pomocí pole **Verze přiznání k DPH** v dialogovém okně přiznání.
8. Na kartě s náhledem **Další pole zprávy** ověřte hodnotu u možnosti \<**NullDeclaration\>**. Nastavte ji na **Ano**, pokud vykazujete prázdné přiznání.
9. Na záložce s náhledem **Zprávy** vyberte **Aktualizovat status**. V dialogovém okně **Aktualizovat status** vyberte akci **Připraveno k vygenerování** a poté vyberte **OK**. Ověřte, že se stav zprávy změnil na **Připraveno k vygenerování**.
10. Vyberte **Generovat sestavu**. Chcete-li zobrazit náhled částek přiznání k DPH, v dialogovém okně **Spustit zpracování** vyberte **Náhled DPHDP3 v aplikaci Excel** a potom vyberte **OK**. 
11. V dialogovém okně **Parametry elektronického výkaznictví** zadejte parametry přiznání k DPH a poté vyberte **OK**. Informace o dostupných parametrech najdete v tabulce v kroku 14. 
12. Pokud vygenerujete soubor Excel společně s náhledem přiznání k DPH, vyberte **Přílohy** v pravém horním rohu stránky a poté vyberte **Otevřít**, čímž soubor otevřete. Zkontrolujte částky, které jsou v dokumentu Excel.
13. Na záložce s náhledem **Zprávy** vyberte **Generovat sestavu**. V dialogovém okně **Spuštění zpracování** volbou **Generovat DPHDP3** vygenerujte soubor XML a poté vyberte **OK**.
14. V dialogovém okně **Parametry elektronického výkaznictví** zadejte následující údaje.

    | Pole                                                                                                                               | popis |
    |-------------------------------------------------------------------------------------------------------------------------------------|-------------|
    | Období vyrovnání daní                                                                                                               | Pokud jste vybrali **Shromažďovat data** v kroku 5, ponechejte toto pole prázdné. V opačném případě vyberte příslušné období vyrovnání. |
    | Verze daňového přiznání                                                                                                             | <p>Pokud jste vybrali **Shromažďovat data** v kroku 5, ponechejte toto pole prázdné. V tomto případě bude sestava vygenerována pro transakce DPH, které jsou zahrnuty ve shromážděných platbách DPH. Jinak vyberte jednu z následujících hodnot:</p><ul><li>**Původní** – Generuje sestavu transakcí DPH původní platby DPH nebo před vygenerováním platby DPH (pole **Verze platby DPH** je nastaveno na **Původní**).</li><li>**Opravy** – Generuje sestavu transakcí DPH všech následných plateb DPH za dané období (pole **Verze platby DPH** je nastaveno na **Poslední opravy**).</li><li>**Celkový seznam** – Generuje sestavu všech transakcí DPH za dané období, včetně původní a všech oprav.</li></ul> |
    | Příslušnost k dani                                                                                                                    | Vyberte **Výchozí**, chcete-li použít informace o společnosti, které jsou zahrnuty v dalších polích pro elektronické výkaznictví. Vyberte **Česká republika**, chcete-li použít informace o společnosti v místních českých polích na stránce **Parametry hlavní knihy**. |
    | Kontaktní osoba                                                                                                                      | Vyberte zaměstnance, který vytvořil sestavu. Jméno, příjmení a telefonní číslo zaměstnance se exportují do souboru XML. |
    | Podepisující osoba                                                                                                                           | Vyberte zaměstnance, který podepsal sestavu. Jméno, příjmení a pozice zaměstnance ve společnosti se exportují do souboru XML. |
    | Datum důvodu opravy                                                                                                              | Zadejte datum, kdy došlo k důvodu pro podání doplňkového přiznání. Toto pole se vztahuje na doplňková a doplňková/opravná přiznání. |
    | Nový poměrný koeficient                                                                                                            | Pro prosincové přiznání zadejte nový poměrný koeficient, který jste vypočítali na základě ročních údajů.<p>Tato hodnota bude exportována do řádku 53 přiznání.</p> |
    | Periodicita sestavy následující rok                                                                                                        | U prosincového prohlášení uveďte periodicitu prohlášení pro následující rok, pokud se liší od aktuální periodicity. |
    | Hodnota zdanitelného prodeje nezahrnutá do výpočtu koeficientu, Hodnota zdanitelného prodeje nezahrnutá do výpočtu koeficientu | <p>V prosincovém přznání uveďte částky prodeje osvobozeného od daně a zdanitelného prodeje, které nejsou zahrnuty do výpočtu nového koeficientu, pokud vaše společnost tyto prodeje měla v průběhu roku.</p><p>Tato částka bude exportována do řádku 51 přiznání.</p> |
    | Hodnota ročního vypořádání odpočtu daně                                                                                         | <p>Pro prosincové přiznání uveďte částku úpravy ročního odpočtu daně, která je způsobena použitím nového poměrného koeficientu.</p><p>Tato částka bude exportována do řádku 53 přiznání.</p> |

15. Vyberte **OK**. Po vygenerování přiznání ve formátu XML se stav zprávy změní na **Vygenerováno**.

    [![Elektronická zpráva, která má stav Vygenerováno.](media/PicEM.jpg)](media/PicEM.jpg)

    Pokud během generování sestavy dojde k chybě, stav zprávy se změní na **Technická chyba**.

16. Vyberte **Přílohy** a potom volbou **Otevřít** soubor otevřete. Prohlédněte si soubor. Pokud je v pořádku, aktualizujte stav na **Schváleno**. Vyberte **Aktualizovat stav** a poté v dialogovém okně **Aktualizovat stav** vyberte **Schválit** a potom vyberte **OK**.

    Pokud musíte odstranit zprávu, můžete vybrat **Povolit odstranění** a poté vyberte **OK**.

    Pokud je stav zprávy **Technická chyba**, můžete stav zprávy aktualizovat na jeden z počátečních stavů: **Vytvořeno** nebo **Připraveno k vygenerování**.

17. Na záložce s náhledem **Protokol akcí** zkontrolujte všechny akce uživatele pro aktuální zprávu.
18. Po dokončení generování přiznání k DPH ručně odešlete vygenerovaný soubor finančnímu úřadu.

### <a name="generate-a-vat-control-statement-from-electronic-messages"></a>Generování kontrolního hlášení DPH z elektronických zpráv

Chcete-li generovat soubor XML pro kontrolní hlášení DPH, postupujte takto.

1. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
2. V levém podokně vyberte formát zprávy, který chcete vygenerovat. Vyberte například **DPHKH1**.
3. Podle kroků 3 až 9 předchozího postupu vytvořte zprávu a aktualizujte její stav na **Připraveno k vygenerování**.
4. Na záložce s náhledem **Zprávy** vyberte **Generovat sestavu**. V dialogovém okně **Spuštění zpracování** volbou **Generovat DPHKH1** vygenerujte soubor XML a poté vyberte **OK**.
5. V dialogovém okně **Parametry elektronického výkaznictví** zadejte následující údaje.

    | Pole                                                                                                               | popis |
    |---------------------------------------------------------------------------------------------------------------------|-------------|
    | Období daňového vyrovnání, verze daňového přiznání, kontaktní osoba, signatář, datum důvodu opravy, typ přiznání | Nastavte tato pole, jak je popsáno v tabulce v kroku 14 předchozího postupu. |
    | Odkaz na číslo                                                                                                    | Zadejte referenční číslo, je-li k dispozici. |
    | Práh                                                                                                           | Zadejte prahovou částku pro rozdělení dokumentů mezi oddíly A4/A5 a B2/B3. Například pro rok 2020 zadejte **10000**. |

### <a name="generate-a-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Generování přiznání k DPH v aplikaci Excel z periodické úlohy Vykázat DPH pro období vyrovnání.

1. Přejděte na **Daň \> Periodické úlohy \> Prohlášení \> DPH \> Vykázat DPH pro období vyrovnání**.
2. Zadejte následující informace.

    | Pole                     | popis |
    |---------------------------|-------------|
    | Období vyrovnání         | Vyberte období vyrovnání. |
    | Verze platby DPH | <p>Vyberte jednu z následujících hodnot:</p><ul><li>**Původní** – Generuje sestavu transakcí DPH původní platby DPH nebo před vygenerováním platby DPH (pole **Verze platby DPH** je nastaveno na **Původní**).</li><li>**Opravy** – Generuje sestavu transakcí DPH všech následných plateb DPH za dané období (pole **Verze platby DPH** je nastaveno na **Poslední opravy**).</li><li>**Celkový seznam** – Generuje sestavu všech transakcí DPH za dané období, včetně původní a všech oprav.</li></ul> |
    | Od data                 | Vyberte první datum z období vykazování. |

3. Vyberte **OK** a zkontrolujte vygenerovaný soubor Excel.

### <a name="generate-vat-declaration-in-excel-from-sales-tax-payments"></a>Generování přiznání k DPH v aplikaci Excel z plateb DPH

1. Přejděte na **Daň \> Periodické úlohy \> Přiznání \> DPH \> Vyrovnat a zaúčtovat DPH**.
2. Zadejte následující informace.

    | Pole                     | popis |
    |---------------------------|-------------|
    | Období vyrovnání         | Vyberte období vyrovnání. |
    | Verze platby DPH | <p>Vyberte jednu z následujících hodnot:</p><ul><li>**Původní** – Vygeneruje původní platbu DPH pro období vyrovnání.</li><li>**Poslední opravy** – Vygeneruje opravu platby DPH po vytvoření původní platby DPH pro období vyrovnání.</li></ul> |
    | Od data                 | Vyberte první datum z období vykazování. |

3. Vyberte **OK**. 
4. Přejděte na **Daň \> Dotazy a sestavy \> Dotazy na DPH \> Platby DPH** a zkontrolujte vygenerovaný řádek platby DPH.

## <a name="run-a-vat-declaration-for-several-legal-entities"></a>Spuštění přiznání k DPH pro několik právnických osob

Chcete-li použít formáty k vykázání přiznání k DPH pro skupinu několika právnických osob, měli byste nejprve nastavit parametry formátů ER specifické pro aplikaci pro každou z právnických osob.

### <a name="set-up-electronic-messages-to-collect-data-from-several-legal-entities"></a>Vytvoření elektronických zpráv ke shromažďování údajů od několika právnických osob

1. Přejděte na **Pracovní prostory \> Správa funkcí**, v seznamu vyhledejte **Dotazy mezi více společnostmi pro akce naplnění záznamů** a poté volbou **Povolit** zapněte tuto funkci.
2. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Akce naplnění záznamů**.

    Na stránce **Akce naplnění záznamů** v mřížce **Nastavení zdrojů dat** je dostupné pole **Společnost**. U existujících záznamů toto pole zobrazuje identifikátor aktuální právnické osoby.

3. V mřížce **Nastavení zdrojů dat** přidejte řádek pro každou další právnickou osobu, která musí být zahrnuta do vykazování, a zadejte následující informace.

    | Pole                  | popis |
    |------------------------|-------------|
    | Jméno                   | Zadejte textovou hodnotu, která vám pomůže pochopit, odkud tento záznam pochází. Například zadejte **Platba DPH dceřiné společnosti 1**. |
    | Typ položky zprávy      | Vyberte **Vratka DPH**. Tato hodnota je jedinou hodnotou, která je k dispozici pro všechny záznamy. |
    | Typ účtu           | Vyberte **Vše**. |
    | Název hlavní tabulky      | Zadejte **TaxReportVoucher** pro všechny záznamy. |
    | Pole čísla dokumentu  | Zadejte **Voucher** pro všechny záznamy. |
    | Pole data dokumentu    | Zadejte **TransDate** pro všechny záznamy. |
    | Pole účtu dokumentu | Zadejte **TaxPeriod** pro všechny záznamy. |
    | Společnost                | Vyberte ID právnické osoby. |
    | Dotaz uživatele             | Zaškrtávací políčko je automaticky zaškrtnuto, když definujete kritéria volbou **Upravit dotaz**. |

4. U každého nového řádku vyberte **Upravit dotaz** a zadejte související zúčtovací období pro právnickou osobu, která je uvedena v poli **Společnost** na řádku.

Po dokončení tohoto nastavení bude funkce **Shromažďovat data** na stránce **Elektronické zprávy** shromažďovat platby DPH od všech právnických osob, které zde definujete.

### <a name="generate-a-vat-declaration-for-several-legal-entities"></a>Generování přiznání k DPH pro několik právnických osob

Než budete následovat tento postup, musí být splněny následující předpoklady:

- Pole **Datum registrace k DPH** na kartě **DPH** na stránce **Parametry hlavní knihy** musí mít stejnou hodnotu pro všechny právnické osoby, pro které shromažďujete údaje.
- Platba DPH musí být za sledované období zaúčtována u všech právnických osob.

Chcete-li vygenerovat přiznání k DPH pro více právnických osob, postupujte takto.

1. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
2. V levém podokně vyberte formát zprávy, který chcete vygenerovat. Vyberte například **DPHDP3**.
3. Na záložce s náhledem **Zprávy** vyberte **Novýá** a poté v dialogovém okně **Spuštění zpracování** vyberte **OK**.
4. Vyberte řádek zprávy, který byl vytvořen, zadejte popis a poté zadejte počáteční a konečné datum přiznání.
5. Na záložce s náhledem **Zprávy** vyberte **Shromažďovat data** a potom vyberte **OK**.
6. Na kartě s náhledem **Položky zprávy** zkontrolujte platby DPH, které jsou přeneseny ke zpracování. Na každém řádku pole **Společnost** označuje právnickou osobu, pro kterou je zpracována platba DPH.
7. Chcete-li zkontrolovat platby DPH, vyberte **Původní dokument**.
8. Chcete-li ze zpracování vyloučit některé platby DPH, vyberte **Odstranit**.
9. Zpracujte přiznání. Po vygenerování souboru zkontrolujte sestavu a ověřte, zda obsahuje všechny daňové transakce, které jsou zahrnuty ve vybraných platbách DPH.

## <a name="attach-a-file-or-a-note-to-the-vat-declaration"></a>Připojení souboru nebo poznámky k přiznání k DPH

K souboru XML můžete pro přiznání k DPH připojit soubor nebo textovou poznámku. Přiložené soubory budou exportovány jako přílohy binárních souborů Base64 do prvku XML **Prilohy**. Přiložené textové poznámky budou exportovány do sekce **VetaR** souboru XML. 

1. Přejděte na **Správa organizace \> Správa dokumentů \> Tabulky aktivního dokumentu** a poté v poli **Název tabulky** vyberte **Platba DPH**.
2. Přejděte na **Daň \> Dotazy a sestavy \> Dotazy na DPH \> Platby DPH**, vyberte řádek, který obsahuje platbu DPH, a poté vyberte tlačítko **Přílohy** v pravém horním rohu.
3. Na stránce **Přílohy k platbám DPH** proveďte jeden z těchto kroků:

    - Chcete-li připojit soubor, vyberte **Nové \> Soubor** a přidejte souborovou přílohu.
    - Chcete-li přidat textovou poznámku, vyberte **Nové \> Poznámka** a poté zadejte informace do polí **Popis** a **Poznámky**.

## <a name="post-a-vat-adjustment-for-bad-debts"></a>Zaúčtování úpravy DPH u nedobytných pohledávek

### <a name="write-off-customer-bad-debts-by-using-the-write-off-function"></a>Odepsání nedobytných pohledávek zákazníků pomocí funkce Odepsat

1. Na stránce **Všichni zákazníci** vytvořte zákazníka.
2. Na stránce **Všechny volné faktury** vytvořte a zaúčtujte volnou fakturu.
3. Na stránce **Kódy DPH** vytvořte kód DPH s názvem **WRITEOFF21**. Tento kód DPH se použije k odpisu nedobytných pohledávek ve výši 21 procent sazby DPH.
4. Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Nastavení deníku \> Názvy deníků** a vytvořte deník hlavní knihy s názvem **Odpis**. V poli **Typ deníku** vyberte **Denně**.
5. Přejděte na **Pohledávky \> Nastavení \> Parametry pohledávek** a poté na kartě **Kolekce** na záložce s náhledem **Odepis** v poli **Odpisový deník** vyberte deník **Odpis**. Nastavte možnost **Samostatná DPH** na **Ano**.
6. Přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci**, vyberte záznam zákazníka, který jste vytvořili v kroku 1, a poté vyberte **Kolekce \> Odpis** . V dialogovém okně **Odpis** nastavte pole **Datum odpisu**, **Kód důvodu** a **Popis** a poté vyberte **OK**.
7. Přejděte na **Hlavní kniha \> Položky deníku \> Hlavní deníky**, vyberte deník **Odpis**, který byl automaticky vygenerován, a poté vyberte **Řádky**. Zkontrolujte tři řádky, které byly vytvořeny:

    - první řádek má typ účtu **Zákazník** a celkovou částku faktury včetně DPH
    - druhý řádek má typ účtu **Hlavní kniha** a částku faktury bez DPH
    - třetí řádek má typ účtu **Hlavní kniha** a částku DPH

8. Vyberte řádek, který obsahuje částku DPH. Pak na kartě **Obecné** v poli **Kód DPH** vyberte kód DPH **WRITEOFF21**, který jste vytvořili v kroku 3.
9. Zaúčtujte deník a poté zkontrolujte zaúčtovanou transakci DPH:

    - Pole **Směr DPH** musí být nastaveno na **DPH na výstupu**.
    - Pole **Základ DPH** se musí rovnat částce faktury bez DPH.
    - Pole **Skutečná částka DPH** se musí rovnat částce DPH.

10. V pracovním prostoru **Elektronické výkaznictví** vyberte konfiguraci, která má formát přiznání k DPH, vyberte **Konfigurace \> Parametry specifické pro aplikaci \> Nastavit** a potom vytvořte následující řádky.

    | Výsledek vyhledávání                         | Kód daně (kód) | Jméno              |
    |---------------------------------------|-----------------|-------------------|
    | VATAdjustmentCustomerBadDebtsStandard | WRITEOFF19      | Prodej.             |
    | VATAdjustmentCustomerBadDebtsStandard | WRITEOFF19      | Prodejní dobropis |

### <a name="manually-write-off-vendor-bad-debts"></a>Ruční odpis nedobytných pohledávek dodavatele

Následující postup je příklad, jak odepsat nedobytné pohledávky dodavatele.

1. Přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé** a vytvořte záznam dodavatele.
2. Vytvořte a zaúčtujte fakturu dodavatele.
3. Na stránce **Kódy DPH** zkontrolujte nastavení kódu DPH **WRITEOFF21**. Případně vytvořte nového dodavatele, než odepíšete nedobytné pohledávky dodavatele.
4. Vytvořte skupinu DPH s názvem **WRITEOFF**. Pak na záložce s náhledem **Nastavení** přidejte řádek, který používá kód DPH **WRITEOFF21**.
5. Na stránce **Skupiny DPH položek** vyberte příslušnou skupinu DPH položek. Pak na záložce s náhledem **Nastavení** přidejte řádek, který používá kód DPH **WRITEOFF21**.
6. Na stránce **Denní hlavní deník** vytvořte řádek pro ruční odpis faktury dodavatele a zadejte následující informace.

    | Pole               | popis |
    |---------------------|-------------|
    | Datum                | Zadejte datum. |
    | Typ účtu        | Vyberte **Dodavatel**. |
    | Účet             | Vyberte účet dodavatele, který jste právě vytvořili. |
    | Debet               | Zadejte částku odpisu. |

7. Na kartě **Obecné** vyberte skupinu DPH **WRITEOFF** a skupinu DPH položek, kterou jste vybrali v kroku 5.
8. Vyrovnejte otevřenou fakturu dodavatele a zaúčtujte deník. Poté zkontrolujte následující informace v zaúčtované transakci DPH:

    - Pole **Směr DPH** musí být nastaveno na **DPH na vstupu**.
    - Hodnota pole **Základ DPH** se musí rovnat částce faktury bez DPH.
    - Hodnota pole **Skutečná částka DPH** se musí rovnat částce DPH.

9. V pracovním prostoru **Elektronické výkaznictví** vyberte konfiguraci, která má formát přiznání k DPH, vyberte **Konfigurace \> Parametry specifické pro aplikaci \> Nastavit** a potom vytvořte následující řádky.

    | Výsledek vyhledávání                       | Kód daně (kód) | Jméno                 |
    |-------------------------------------|-----------------|----------------------|
    | VATAdjustmentVendorBadDebtsStandard | WRITEOFF19      | Nákup             |
    | VATAdjustmentVendorBadDebtsStandard | WRITEOFF19      | Nákupní dobropis |

## <a name="post-a-tax-amount-correction"></a>Zaúčtování opravy částky daně

Následující postup představuje příklad, jak zaúčtovat opravu odpočtu DPH (řádek 45).

1. Na stránce **Kódy DPH** vytvořte kód DPH s názvem **CORR**. Tento kód se použije konkrétně pro opravy odpočtu DPH, které se projeví v řádku 45 přiznání k DPH.
2. Přejděte na **Hlavní kniha \> Položky deníku \> Hlavní knihy** a vyberte denní deník. Poté vyberte **Řádky** a vytvořte následující řádek deníku.

    | Pole               | popis |
    |---------------------|-------------|
    | Datum                | Zadejte datum. |
    | Typ účtu        | Vyberte **Hlavní kniha**. |
    | Účet             | Vyberte účet hlavní knihy používaný pro zaúčtování odpočtu DPH. |
    | popis         | Zadejte popis transakce. |
    | Debet               | Zadejte zvýšenou částku odpočtu DPH. |
    | Typ protiúčtu | Vyberte **Hlavní kniha**. |
    | Protiúčet      | Vyberte účet hlavní knihy používaný pro posunutí zaúčtování odpočtu DPH. |
 
3. Na kartě **Obecné** v poli **Kód DPH** vyberte kód DPH **CORR**, který jste právě vytvořili.
4. Zaúčtujte deník a poté zkontrolujte následující informace v zaúčtované transakci DPH:

    - Pole **Směr DPH** musí být nastaveno na **DPH na vstupu**.
    - Pole **Základ DPH** musí být nastaveno na **0** (nula).
    - Hodnota pole **Skutečná částka DPH** se musí rovnat částce Má dáti.

5. V pracovním prostoru **Elektronické výkaznictví** vyberte konfiguraci, která má formát přiznání k DPH, vyberte **Konfigurace \> Parametry specifické pro aplikaci \> Nastavit** a potom vytvořte následující řádky.

    | Výsledek vyhledávání          | Kód daně (kód) | Jméno                 |
    |------------------------|-----------------|----------------------|
    | VATDeductionCorrection | CORR            | Nákup             |
    | VATDeductionCorrection | CORR            | Nákupní dobropis |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

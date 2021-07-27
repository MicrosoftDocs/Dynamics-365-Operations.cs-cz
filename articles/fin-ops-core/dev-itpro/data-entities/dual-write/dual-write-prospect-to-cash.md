---
title: Zpeněžení potenciálního zákazníka ve dvojím připisování
description: Toto téma obsahuje informace o Zpeněžení potenciálního zákazníka ve dvojím zapisování.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 7554189c779404559187ecd99f4bca4636054446
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361374"
---
# <a name="prospect-to-cash-in-dual-write"></a>Zpeněžení potenciálního zákazníka ve dvojím připisování

[!include [banner](../../includes/banner.md)]



Důležitým cílem většiny společností je převod potenciálních zákazníků na odběratele a následný obchodní vztah s těmito odběrateli. V aplikacích Microsoft Dynamics 365 se proces zpeněžení potenciálního zákazníka uskutečňuje prostřednictvím nabídek nebo workflowů zpracování objednávek a finanční záznamy jsou odsouhlaseny a uznány. Integrace zpeněžení potenciálního zákazníka s dvojím zapisováním vytvoří workflow, který přebírá nabídku a objednávku, která pochází z produktu Dynamics 365 Sales nebo Dynamics 365 Supply Chain Management a zpřístupňuje nabídku a objednávku v obou aplikacích.

V rozhraní aplikace můžete přistupovat ke stavům zpracování a informacím o fakturách v reálném čase. Z tohoto důvodu je možné snadněji spravovat funkce, jako je například výdeje produktu, zpracování zásob a splnění v modulu Supply Chain Management, aniž by bylo nutné znovu vytvářet nabídky a objednávky.

![Datový tok s dvojím zápisem ve zpeněžení potenciálního zákazníka.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Informace o integraci zákazníků a kontaktů najdete v části [Integrovaný kmenový soubor zákazníka](customer-mapping.md). Informace o integraci produktu najdete v části [Jednotná zkušenost s produktem](product-mapping.md).

> [!NOTE]
> V Dynamics 365 Sales se potenciální zákazník i zákazník odvolávají na záznam v tabulce **Účet**, kde je sloupec **Typ vztahu** buď **potenciální zákazník** nebo **Zákazník**. Pokud vaše obchodní logika obsahuje kvalifikační proces **Účet**, kde je vytvořen záznam **Účet** a je nejprve kvalifikován jako potenciální zákazník a poté jako zákazník, tento záznam se synchronizuje s aplikací Finance and Operations pouze v případě, že se jedná o zákazníka (`RelationshipType=Customer`). Pokud chcete řádek **Účet** synchronizovat jako potenciálního zákazníka, pak potřebujete vlastní mapu pro integraci dat potenciálního zákazníka.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

Než bude možné synchronizovat prodejní nabídky, je nutné aktualizovat následující nastavení.

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

V Sales přejděte na **Nastavení \> Správa \> Nastavení systému \> Prodej** a ujistěte se, že se používají následující nastavení:

- Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
- Sloupec **Metoda výpočtu slevy** je nastaven na **Položka řádku**.

### <a name="sites-and-warehouses"></a>Pracoviště a sklady

V Supply Chain Management jsou sloupce **Pracoviště** a **sklad** vyžadovány pro řádky nabídky a řádky objednávky. Pokud nastavíte pracoviště a sklad ve výchozím nastavení objednávky, tyto sloupce budou automaticky nastaveny při přidání produktu do řádku nabídky nebo řádku objednávky. 

### <a name="number-sequences-for-quotations-and-orders"></a>Číselné řady pro nabídky a objednávky

Číselné řady pro Supply Chain Management a Sales nejsou propojeny, když jsou nabídky a objednávky vytvořeny a synchronizovány v modulu Sales a Supply Chain Management. Je-li prodejní objednávka vytvořená v Sales a synchronizována se Supply Chain Management, má stejné číslo prodejní objednávky v modulu Supply Chain Management. Chcete-li zajistit, aby číslo prodejní objednávky nebylo duplikováno, je nutné ve dvou aplikacích používat různé systémy číselných řad.

Například číselná řada v Supply Chain Management je **1, 2, 3, 4, 5,...** a číselná řada v Sales je **100, 99, 98,...**. Pokud vytvoříte prodejní objednávky 100 v prodeji, bude nakonec vygenerováno i číslo objednávky, které již existuje v Supply Chain Management. Jinak řečeno, dvě číselné řady se nakonec překryjí při vytváření prodejních objednávek v Supply Chain Management a Sales. Místo toho můžete použít číselnou řadu, jako například **F1, F2, F3,...** v Supply Chain Management a v číselnou řadě jako například **C1, C2, C3,...** v Sales. Tyto číselné řady nikdy nevydávají duplicitní čísla prodejních objednávek.

## <a name="sales-quotations"></a>Prodejní nabídky

Prodejní nabídky mohou být vytvořeny v aplikaci Sales nebo Supply Chain Management. Pokud vytvoříte nabídku v Sales, bude synchronizována se Supply Chain Management v reálném čase. Stejným způsobem, pokud vytvoříte nabídku v Supply Chain Management, bude synchronizována se Sales v reálném čase. Mějte na paměti následující body:

+ Na nabídku můžete přidat slevu. V takovém případě bude sleva synchronizována se Supply Chain Management. Sloupce **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolovány nastavením v aplikaci Supply Chain Management. Toto nastavení nepodporuje mapování integrace. Místo toho jsou sloupce **Cena**, **Sleva**, **Účtování** a **Daň** ponechány a zpracovány aplikací Supply Chain Management.
+ Sloupce **Sleva %**, **Sleva** a **Částka dopravného** jsou v záhlaví prodejní nabídky jen pro čtení.
+ Sloupce **Podmínky přepravy**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tyto sloupce mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je tabulka synchronizována.

Používáte-li také řešení Field Service, ujistěte se, že jste znovu povolili parametr **Rychlé vytvoření řádky nabídky**. Opětovná aktivace parametru umožňuje pokračovat ve vytváření řádků nabídky pomocí funkce rychlého vytvoření.
1. Přejděte k aplikaci Dynamics 365 Sales.
2. V horním navigačním pruhu vyberte ikonu nastavení.
3. Vyberte možnost **Rozšířená nastavení**.
4. Zvolte možnost **Přizpůsobit systém**.
5. V nabídce vyberte položku **Řádek nabídky**.
6. Přejděte na oddíl **Datové služby** a zaškrtněte políčko **Povolit rychlé vytváření**.

## <a name="sales-orders"></a>Prodejní objednávky

Prodejní obědnávky mohou být vytvořeny v aplikaci Sales nebo Supply Chain Management. Pokud vytvoříte prodejní objednávku v Sales, bude synchronizována se Supply Chain Management v reálném čase. Stejným způsobem, pokud vytvoříte prodejní objednávku v Supply Chain Management, bude synchronizována se Sales v reálném čase. Mějte na paměti následující body:

+ Produkty nezahrnuté do katalogu v Dynamics 365 Sales se zobrazí jako kategorie produktů v Dynamics 365 Supply Chain Management.
+ Výpočet slevy a zaokrouhlení:

    - Model výpočtu slevy v aplikaci Sales se liší od modelu výpočtu slevy v aplikaci Supply Chain Management. V aplikaci Supply Chain Management konečná částka slevy na řádku prodeje může být výsledkem kombinace částky slevy a procent slevy. Pokud je tato celková částka slevy podělená množstvím na řádku, může dojít k zaokrouhlení. Toto zaokrouhlení však není bráno v potaz, pokud je zaokrouhlená částka slevy na jednotku synchronizována do aplikace Sales. Chcete-li zaručit, že celková částka slevy z řádku prodeje v aplikaci Supply Chain Management je správně synchronizována do aplikace Sales, musí být celá částka synchronizována, aniž by byla podělena množstvím řádku. Proto je nutné definovat v aplikaci Sales možnost Metoda výpočtu slevy jako **Položku řádku**.
    - Při synchronizaci řádku prodejní objednávky z aplikace Sales do aplikace Supply Chain Management se používá celková částka řádkové slevy. Protože aplikace Supply Chain Management nemá žádné sloupce pro uložení celé částky slevy pro řádek, je částka podělená množstvím a uložená ve sloupci **Řádková sleva**. Jakékoliv zaokrouhlování, ke kterému dojde při tomto dělení, je uloženo ve sloupci **Prodejní náklady** na řádku prodeje.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Příklad: Synchronizace ze Sales do Supply Chain Management

Máte k dispozici následující prodejní objednávky:

+ **Prodej:** množství = 3, sleva na řádek = 10 USD
+ **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek = -$0,01

Pokud provádíte synchronizaci ze Supply Chain Management do Sales, dostanete následující výsledek:

+ **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek = -$0,01
+ **Prodej:** množství = 3, sleva na řádek = (3 × 3,33 USD) + $0,01 USD = 10 USD

## <a name="dual-write-solution-for-sales"></a>Řešení dvojího zapisování pro Sales

Nové sloupce byly přidána do tabulky **Objednávka** a zobrazí na stránce. Většina z těchto sloupců je zobrazena na kartě **Integrace** v modulu Sales. Další informace o tom, jak jsou mapovány stavové sloupce, najdete v tématu [Nastavení mapování pro sloupce stavu prodejní objednávky](sales-status-map.md).

+ Tlačítka **Vytvořit fakturu** a **Storno objednávky** na stránce **Prodejní objednávka** jsou v Sales skryta.
+ Hodnota **Stav prodejní objednávky** zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Supply Chain Management mohou být odeslány do prodejní objednávky v aplikaci Sales. Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní**.

## <a name="invoices"></a>Faktury

Prodejní faktury jsou vytvořeny v aplikaci Supply Chain Management a jsou synchronizovány do aplikace Sales. Mějte na paměti následující body:

+ Sloupec **Číslo faktury** byl přidán do tabulky **Faktura** a zobrazí se na stránce.
+ Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Supply Chain Management a synchronizovány do aplikace Sales. Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Supply Chain Management.
+ Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Supply Chain Management do aplikace Sales. Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury. Vlastník prodejní objednávky tudíž může zobrazit fakturu.
+ Sloupce **Dopravní podmínky**, **Dodací podmínky** a **Způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tyto sloupce mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je tabulka synchronizována.

## <a name="templates"></a>Šablony

Zpeněžení potenciálního zákazníka zahrnují kolekce map základních tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Aplikace Customer Engagement | popis |
|-----------------------------|-----------------------------------|-------------|
| Záhlaví prodejní faktury V2    | faktury                          | Tabulka záhlaví prodejní faktury V2 v aplikaci Finance and Operations obsahuje faktury za prodejní objednávky a faktury s volným textem. Je použit filtr v Dataverse pro duální zápis, který odfiltruje veškeré dokumenty s volným textem na faktuře. |
| Řádky prodejní faktury V2      | invoicedetails                    |             |
| Záhlaví prodejní objednávky CDS     | salesorders                       |             |
| Řádky prodejní objednávky CDS       | salesorderdetails                 |             |
| Kódy původu prodejních objednávek    | msdyn\_salesorderorigins          |             |
| Záhlaví prodejní nabídky CDS  | nabídky                            |             |
| Řádky prodejní nabídky CDS   | quotedetails                      |             |

Zde jsou přidružená mapování základních tabulek pro zpeněžení potenciálního zákazníka:

+ [Zákazníci V3 do accounts](customer-mapping.md#customers-v3-to-accounts)
+ [CDS kontakty V2 do contacts](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Zákazníci V3 do contacts](customer-mapping.md#customers-v3-to-contacts)
+ [Uvolněné produkty V2 do msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Všechny produkty do msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Ceník](product-mapping.md)

## <a name="limitations"></a>Omezení
- Vrácené objednávky nejsou podporovány.
- Dobropisy nejsou podporovány.
- Je třeba nastavit finanční dimenze pro kmenová data, například zákazníka a dodavatele. Když je zákazník přidán do nabídky nebo prodejní objednávky, finanční dimenze přidružené k záznamu zákazníka se automaticky dostanou do objednávky. V současné době duální zápis nezahrnuje data finančních dimenzí pro kmenová data. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

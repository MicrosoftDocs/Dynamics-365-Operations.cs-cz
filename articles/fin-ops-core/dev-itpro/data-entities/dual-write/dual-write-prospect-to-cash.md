---
title: Zpeněžení potenciálního zákazníka ve dvojím připisování
description: Toto téma obsahuje informace o Zpeněžení potenciálního zákazníka ve dvojím zapisování.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 12a0e07d1c60a359b3ba6c0d20176927ffe89431
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172801"
---
# <a name="prospect-to-cash-in-dual-write"></a>Zpeněžení potenciálního zákazníka ve dvojím připisování

[!include [banner](../../includes/banner.md)]



Důležitým cílem většiny společností je převod potenciálních zákazníků na odběratele a následný obchodní vztah s těmito odběrateli. V aplikacích Microsoft Dynamics 365 se proces zpeněžení potenciálního zákazníka uskutečňuje prostřednictvím nabídek nebo workflowů zpracování objednávek a finanční záznamy jsou odsouhlaseny a uznány. Integrace zpeněžení potenciálního zákazníka s dvojím zapisováním vytvoří workflow, který přebírá nabídku a objednávku, která pochází z produktu Dynamics 365 Sales nebo Dynamics 365 Supply Chain Management a zpřístupňuje nabídku a objednávku v obou aplikacích.

V rozhraní aplikace můžete přistupovat ke stavům zpracování a informacím o fakturách v reálném čase. Z tohoto důvodu je možné snadněji spravovat funkce, jako je například výdeje produktu, zpracování zásob a splnění v modulu Supply Chain Management, aniž by bylo nutné znovu vytvářet nabídky a objednávky.

![Datový tok s dvojím zápisem ve zpeněžení potenciálního zákazníka](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

Než bude možné synchronizovat prodejní nabídky, je nutné aktualizovat následující nastavení.

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

V Sales přejděte na **Nastavení \> Správa \> Nastavení systému \> Prodej** a ujistěte se, že se používají následující nastavení:

- Systémová možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
- Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.

### <a name="sites-and-warehouses"></a>Pracoviště a sklady

V Supply Chain Management jsou pole **Pracoviště** a **sklad** vyžadována pro řádky nabídky a řádky objednávky. Pokud nastavíte pracoviště a sklad ve výchozím nastavení objednávky, tato pole budou automaticky nastavena při přidání produktu do řádku nabídky nebo řádku objednávky. 

### <a name="number-sequences-for-quotations-and-orders"></a>Číselné řady pro nabídky a objednávky

Číselné řady pro Supply Chain Management a Sales nejsou propojeny, když jsou nabídky a objednávky vytvořeny a synchronizovány v modulu Sales a Supply Chain Management. Je-li prodejní objednávka vytvořená v Sales a synchronizována se Supply Chain Management, má stejné číslo prodejní objednávky v modulu Supply Chain Management. Chcete-li zajistit, aby číslo prodejní objednávky nebylo duplikováno, je nutné ve dvou aplikacích používat různé systémy číselných řad.

Například číselná řada v Supply Chain Management je **1, 2, 3, 4, 5,...** a číselná řada v Sales je **100, 99, 98,...**. Pokud vytvoříte prodejní objednávky 100 v prodeji, bude nakonec vygenerováno i číslo objednávky, které již existuje v Supply Chain Management. Jinak řečeno, dvě číselné řady se nakonec překryjí při vytváření prodejních objednávek v Supply Chain Management a Sales. Místo toho můžete použít číselnou řadu, jako například **F1, F2, F3,...** v Supply Chain Management a v číselnou řadě jako například **C1, C2, C3,...** v Sales. Tyto číselné řady nikdy nevydávají duplicitní čísla prodejních objednávek.

## <a name="sales-quotations"></a>Prodejní nabídky

Prodejní nabídky mohou být vytvořeny v aplikaci Sales nebo Supply Chain Management. Pokud vytvoříte nabídku v Sales, bude synchronizována se Supply Chain Management v reálném čase. Stejným způsobem, pokud vytvoříte nabídku v Supply Chain Management, bude synchronizována se Sales v reálném čase. Mějte na paměti následující body:

+ Na nabídku můžete přidat slevu. V takovém případě bude sleva synchronizována se Supply Chain Management. Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována nastavením v aplikaci Supply Chain Management. Toto nastavení nepodporuje mapování integrace. Místo toho jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** ponechána a zpracována aplikací Supply Chain Management.
+ Pole **Sleva %**, **Sleva** a **Částka dopravného** jsou v záhlaví prodejní nabídk jen pro čtení.
+ Pole **Podmínky přepravy**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

## <a name="sales-orders"></a>Prodejní objednávky

Prodejní obědnávky mohou být vytvořeny v aplikaci Sales nebo Supply Chain Management. Pokud vytvoříte prodejní objednávku v Sales, bude synchronizována se Supply Chain Management v reálném čase. Stejným způsobem, pokud vytvoříte prodejní objednávku v Supply Chain Management, bude synchronizována se Sales v reálném čase. Mějte na paměti následující body:

+ Objednávky můžete aktivovat a synchronizovat pouze z Sales, pokud všechny produkty v objednávce pocházení z aplikací Finance and Operations. Z tohoto důvodu může existovat žádný zápis produktů.
+ Výpočet slevy a zaokrouhlení:

    - Model výpočtu slevy v aplikaci Sales se liší od modelu výpočtu slevy v aplikaci Supply Chain Management. V aplikaci Supply Chain Management konečná částka slevy na řádku prodeje může být výsledkem kombinace částky slevy a procent slevy. Pokud je tato celková částka slevy podělená množstvím na řádku, může dojít k zaokrouhlení. Toto zaokrouhlení však není bráno v potaz, pokud je zaokrouhlená částka slevy na jednotku synchronizována do aplikace Sales. Chcete-li zaručit, že celková částka slevy z řádku prodeje v aplikaci Supply Chain Management je správně synchronizována do aplikace Sales, musí být celá částka synchronizována, aniž by byla podělena množstvím řádku. Proto je nutné definovat v aplikaci Sales možnost Metoda výpočtu slevy jako **Položku řádku**.
    - Při synchronizaci řádku prodejní objednávky z aplikace Sales do aplikace Supply Chain Management se používá celková částka řádkové slevy. Protože aplikace Supply Chain Management nemá žádné pole pro uložení celé částky slevy pro řádek, je částka podělená množstvím a uložená v poli **Řádková sleva**. Jakékoliv zaokrouhlování, ke kterému dojde při tomto dělení, je uloženo v poli **Prodejní náklady** na řádku prodeje.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Příklad: Synchronizace ze Sales do Supply Chain Management

Máte k dispozici následující prodejní objednávky:

+ **Prodej:** množství = 3, sleva na řádek = 10 USD
+ **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek = -$0,01

Pokud provádíte synchronizaci ze Supply Chain Management do Sales, dostanete následující výsledek:

+ **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek = -$0,01
+ **Prodej:** množství = 3, sleva na řádek = (3 × 3,33 USD) + $0,01 USD = 10 USD

## <a name="dual-write-solution-for-sales"></a>Řešení dvojího zapisování pro Sales

Nová pole byla přidána do entity **Objednávka** a zobrazí na stránce. Většina z těchto polí je zobrazena na kartě **Integrace** v modulu Sales. Existuje několik zvláštních polí:

+ Pole **Stav zpracování** ukazuje stav zpracování objednávky v aplikaci Supply Chain Management. Toto pole je uzamčeno a zobrazuje pouze stav objednávky ze Supply Chain Management. K dispozici jsou následující hodnoty:

    + **Aktivní** – Stav po aktivaci objednávky v aplikaci Sales s použitím tlačítka **Aktivovat**.
    + **Potvrzeno**
    + **Dodáno**
    + **Fakturováno**
    + **Částečně dodáno**
    + **Částečně fakturováno**
    + **Vydáno**
    + **Zrušeno**

    V následující tabulce je uvedeno, jak je stav zpracování mapován na hodnotu **stavového kódu CRM**.

    | Stav zpracování           | kód stavu CRM    |
    |-----------------------------|--------------------|
    | Aktivní                      | Nové/čekající/pozastavené |
    | Potvrzeno/vydáno            | Probíhá        |
    | Částečně dodáno         | Částečné            |
    | Dodáno                   | Dokončit           |
    | Fakturováno/částečně fakturováno | Fakturováno           |
    | Zrušeno                    | Žádné peníze           |

+ Tlačítka **Vytvořit fakturu** a **Storno objednávky** na stránce **Prodejní objednávka** jsou v Sales skryta.
+ Hodnota **Stav prodejní objednávky** zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Supply Chain Management mohou být odeslány do prodejní objednávky v aplikaci Sales. Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní**.

## <a name="invoices"></a>Faktury

Prodejní faktury jsou vytvořeny v aplikaci Supply Chain Management a jsou synchronizovány do aplikace Sales. Mějte na paměti následující body:

+ Pole **Číslo faktury** bylo přidáno do entity **Faktura** a zobrazí se na stránce.
+ Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Supply Chain Management a synchronizovány do aplikace Sales. Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Supply Chain Management.
+ Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Supply Chain Management do aplikace Sales. Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury. Vlastník prodejní objednávky tudíž může zobrazit fakturu.
+ Pole **Dopravní podmínky**, **Dodací podmínky** a **Způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

## <a name="templates"></a>Šablony

Zpeněžení potenciálního zákazníka zahrnují kolekce map základních entit, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Modelem řízené aplikace v Dynamics 365 | popis |
|-----------------------------|-----------------------------------|-------------|
| Záhlaví prodejní faktury V2    | faktury                          |             |
| Řádky prodejní faktury V2      | invoicedetails                    |             |
| Záhlaví prodejní objednávky CDS     | salesorders                       |             |
| Řádky prodejní objednávky CDS       | salesorderdetails                 |             |
| Kódy původu prodejních objednávek    | msdyn\_salesorderorigins          |             |
| Záhlaví prodejní nabídky CDS  | nabídky                            |             |
| Řádky prodejní nabídky CDS   | quotedetails                      |             |

Zde jsou přidružená mapování základních entit pro zpeněžení potenciálního zákazníka:

+ [Zákazníci V3 do accounts](customer-mapping.md#customers-v3-to-accounts)
+ [CDS kontakty V2 do contacts](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Zákazníci V3 do contacts](customer-mapping.md#customers-v3-to-contacts)
+ [Uvolněné produkty V2 do msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Všechny produkty do msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Ceník](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]

---
title: "Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Microsoft Dynamics 365 for Sales a Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Finance and Operations

[!INCLUDE [banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Microsoft Dynamics 365 for Sales a Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

Ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Finance and Operations slouží následující šablony a základní úkoly:

- **Názvy šablon v integraci dat:** 

    - Prodejní objednávky (Sales do Fin and Ops) - přímo
    - Prodejní objednávky (Fin and Ops do Sales) - přímo

- **Názvy úkolů v projektu integrace dat:**

    - OrderHeader
    - OrderLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:

- Produkty (Fin and Ops do Sales) - přímo
- Účty (Sales do Fin and Ops) - přímo (pokud se používají)
- Kontakty na zákazníky (Sales do Fin and Ops) - přímo (pokud se používají)

## <a name="entity-set"></a>Sada entit

| Finance and Operations  | Prodej.             |
|-------------------------|-------------------|
| Záhlaví prodejní objednávky CDS | SalesOrders       |
| Řádky prodejní objednávky CDS   | SalesOrderDetails |

## <a name="entity-flow"></a>Tok entity

Prodejní objednávky jsou vytvořeny v aplikaci Sales a synchronizovány do aplikace Finance and Operations při aktivaci možnosti **Spustit projekt** pro projekt na základě šablony **Prodejní objednávky (Sales do Fin and Ops) - přímo**. Můžete aktivovat a synchronizovat pouze objednávky z aplikace Sales v případě, že všechny **Produkty objednávky** se skládají z produktů, které jsou udržovány externě. Z tohoto důvodu může existovat žádný zápis produktů. Po aktivaci objednávky bude prodejní objednávka v uživatelském rozhraní jen pro čtení. V daném okamžiku se provedou aktualizace aplikace Finance and Operations. Poté, co má prodejní objednávka stav **Potvrzeno**, projekt na základě šablony **Prodejní objednávky (Fin and Ops do Sales) - přímo** umožňuje synchronizovat aktualizace nebo stav plnění z aplikace Finance and Operations do Sales.

Není nutné vytvoření objednávek v aplikaci Sales. Místo toho můžete vytvořit nové prodejní objednávky v aplikaci Finance and Operations. Poté, co má prodejní objednávka stav **Potvrzeno**, bude synchronizována do aplikace Sales, jak je popsáno ve výše uvedeném odstavci.

V aplikaci Finance and Operations pomáhají filtry v šabloně zajistit, aby byly v synchronizaci zahrnuty pouze příslušné prodejní objednávky:

- Objednávající a fakturující odběratel na prodejní objednávce musí pocházet z aplikace Sales, aby byli zahrnuti do procesu synchronizace. V aplikaci Finance and Operations se používají pole **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** k filtrování prodejních objednávek z datových entit.
- Prodejní objednávka musí být v aplikaci Finance and Operations potvrzena. Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem **Expedováno** nebo **Fakturováno**, budou synchronizovány do aplikace Sales.
- Po vytvoření nebo úpravě prodejní objednávky musí být provedena v aplikaci Finance and Operations dávková úloha **Vypočítat celkové tržby**. Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales.

## <a name="freight-tax"></a>Daň z přepravy

Aplikace Sales nepodporuje daň na úrovni záhlaví, protože daň je uložena na úrovni řádku. K podpoře daně na úrovni záhlaví z aplikace Finance and Operations, jako je daň z přepravy, systém synchronizuje daň do aplikace Sales jako zápis produktu s názvem **Daň z přepravy** a který má částku daně z aplikace Finance and Operations. Standardní kalkulace ceny v aplikaci Sales slouží pro součty, a to i v případě, kdy je daň na úrovní záhlaví z aplikace Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Výpočet slevy a zaokrouhlení

Model výpočtu slevy v aplikaci Sales se liší od modelu výpočtu slevy v aplikaci Finance and Operations. V aplikaci Finance and Operations konečná částka slevy na řádku prodeje může být výsledkem kombinace částky slevy a procent slevy. Pokud je tato celková částka slevy podělená množstvím na řádku, může dojít k zaokrouhlení. Toto zaokrouhlení však není bráno v potaz, pokud je zaokrouhlená částka slevy na jednotku synchronizována do aplikace Sales. Chcete-li zaručit, že celková částka slevy z řádku prodeje v aplikaci Finance and Operations je správně synchronizována do aplikace Sales, musí být celá částka synchronizována, aniž by byla podělena množstvím řádku. Proto je nutné definovat v aplikaci Sales možnost **Metoda výpočtu slevy** jako **Položku řádku**.

Při synchronizaci řádku prodejní objednávky z aplikace Sales do aplikace Finance and Operations se používá celková částka řádkové slevy. Protože aplikace Finance and Operations nemá žádné pole pro uložení celé částky slevy pro řádek, je částka podělená množstvím a uložená v poli **Řádková sleva**. Jakékoliv zaokrouhlování, ke kterému dojde při tomto dělení, je uloženo v poli **Prodejní náklady** na řádku prodeje.

### <a name="example"></a>Příklad

**Synchronizace z aplikace Sales do aplikace Finance and Operations**

- **Prodej:** množství = 3, sleva na řádek = 10 USD
- **Finance and Operations:** množství = 3, částka řádkové slevy = $3.33, prodejní náklady = -0.01 USD 

**Synchronizace z aplikace Finance and Operations do aplikace Sales**

- **Finance and Operations:** množství = 3, částka řádkové slevy = $3.33, prodejní náklady = -0.01 USD
- **Prodej:** množství = 3, sleva na řádek = (3 × 3,33 USD) + $0,01 USD = 10 USD

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Nová pole byla přidána do entity **Objednávka** a zobrazí na stránce:

- **Je externě spravováno** - Nastavte tuto možnost na **Ano**, když pořadí pochází z aplikace Finance and Operations.
- **Stav zpracování** - Toto pole ukazuje stav zpracování objednávky v aplikaci Finance and Operations. K dispozici jsou následující hodnoty:

    - **Návrh** – Počáteční stav při vytvoření objednávky v aplikaci Sales. V aplikaci Sales lze upravit pouze objednávky s tímto stavem zpracování.
    - **Aktivní** – Stav po aktivaci objednávky v aplikaci Sales s použitím tlačítka **Aktivovat**.
    - **Potvrzeno**
    - **Dodací list**
    - **Fakturováno**
    - **Vyskladněno**
    - **Částečně vyskladněno**
    - **Částečně zabaleno**
    - **Expedováno**
    - **Částečně expedováno**
    - **Částečně fakturováno**
    - **Zrušeno**

Nastavení **Má pouze externě udržované produkty** se používá během aktivace objednávky ke konzistentnímu sledování, zda prodejní objednávka sestává zcela z externě spravovaných produktů. Pokud prodejní objednávka sestává zcela z externě spravovaných produktů, produkty jsou evidovány v aplikaci Finance and Operations. Toto nastavení pomáhá zaručit, že neaktivujete a nepokusíte se synchronizovat řádky prodejní objednávky s produkty, které mají v aplikaci Finance and Operations neznámé produkty.

Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales. Tyto objednávky nelze upravovat, protože informace o prodejní objednávce budou synchronizovány po této aktivaci z aplikace Finance and Operations.

Stav prodejní objednávky zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Finance and Operations mohou být odeslány do prodejní objednávky v aplikaci Sales. Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní** v projektu integrace dat.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních objednávek je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení aplikace Sales přiřazen. Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá. Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.

    Přejděte na **Nastavení** &gt; **Zabezpečení** &gt; **Týmy**, vyberte příslušný tým, zvolte **Spravovat role** a vyberte roli s požadovanými oprávněními, například **Správce systému**.

- Chcete-li zajistit správné výpočty slev pv aplikacích Sales a Finance and Operations, je třeba nastavit položku **Metoda výpočtu slevy**na **Položka řádku**.
- Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Prodej** a ujistěte se, že se používají následující nastavení:

    - Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
    - Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.

### <a name="setup-in-finance-and-operations"></a>Nastavení v aplikaci Finance and Operations

- Přejděte na **Prodej a marketing** &gt; **Periodické úlohy** &gt; **Vypočítat celkové tržby**a nastavte úlohu, aby se spustila jako dávková úloha. Nastavte možnost **Vypočítat celkové částky prodejních objednávek** na **Ano**. Tento krok je důležitý, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales. Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Nastavení v prodejních objednávkách (Sales do Fin and Ops) - Přímo v projektu integrace dat

- Ujistěte se, že existuje požadované mapování pro **Shipto\_country** do **DeliveryAddressCountryRegionISOCode**. Můžete ponechat prázdnou výchozí hodnotu v mapě hodnot, abyste nemuseli zadávat zemi pro národní objednávky. Nastavte levou stranu na Prázdné a pravou stranu na požadovanou zemi nebo oblast.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí a kde prázdná hodnota = USA.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Nastavení v prodejních objednávkách (Fin and Ops do Sales) - Přímo v projektu integrace dat

#### <a name="salesheader-task"></a>Úloha SalesHeader

- Ceník je povinný pro vytvoření objednávek v aplikaci Sales. Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny. Výchozí ceník můžete použít pro jednu měnu. Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.

    Výchozí hodnota šablony pro  **pricelevelid.name \[Název ceníku\]** je **CRM služba USA (vzorek)**.

#### <a name="salesline-task"></a>Úloha SalesLine

- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.
- Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.

    Hodnota šablony, která má mapu hodnoty, je definována pro **SalesUnitSymbol** do **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat.

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations nebo naopak.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Prodejní objednávky (Fin and Ops do Sales) - přímo: OrderHeader

[![Mapování šablony v integraci dat](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Prodejní objednávky (Fin and Ops do Sales) - přímo: OrderLine

[![Mapování šablony v integraci dat](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Prodejní objednávky (Sales do Fin and Ops) - přímo: OrderHeader

[![Mapování šablony v integraci dat](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Prodejní objednávky (Sales do Fin and Ops) - přímo: OrderLine

[![Mapování šablony v integraci dat](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)


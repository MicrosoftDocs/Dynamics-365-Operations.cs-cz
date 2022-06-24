---
title: Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management
description: Tento článek se věnuje šablonám a základním úlohám, které se používají ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Dynamics 365 Sales a Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 63a9be9bedabe1f15ad8db583151aa7fa480473b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854145"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management

[!include [banner](../includes/banner.md)]



Tento článek se věnuje šablonám a základním úlohám, které se používají ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Dynamics 365 Sales a Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

Ke spuštění synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management slouží následující šablony a základní úkoly:

- **Názvy šablon v integraci dat:** 

    - Prodejní objednávky (Sales do Supply Chain Management) – Přímo
    - Prodejní objednávky (Supply Chain Management do Sales) – Přímo

- **Názvy úkolů v projektu integrace dat:**

    - OrderHeader
    - OrderLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:

- Produkty (Supply Chain Management do Sales) – Přímo
- Obchodní vztahy (Sales do Supply Chain Management) – Přímo (pokud se používá)
- Kontakty na odběratele (Sales do Supply Chain Management) – Přímo (pokud se používá)

## <a name="entity-set"></a>Sada entit

| Správa dodavatelsko-odběratelského řetězce  | Prodej.             |
|-------------------------|-------------------|
| Záhlaví prodejní objednávky Dataverse | SalesOrders       |
| Řádky prodejní objednávky Dataverse   | SalesOrderDetails |

## <a name="entity-flow"></a>Tok entity

Prodejní objednávky jsou vytvořeny v aplikaci Sales a synchronizovány do aplikace Supply Chain Management při aktivaci možnosti **Spustit projekt** pro projekt na základě šablony **Prodejní objednávky (Sales do Supply Chain Management) - přímo**. Můžete aktivovat a synchronizovat pouze objednávky z aplikace Sales v případě, že všechny **Produkty objednávky** se skládají z produktů, které jsou udržovány externě. Z tohoto důvodu může existovat žádný zápis produktů. Po aktivaci objednávky bude prodejní objednávka v uživatelském rozhraní jen pro čtení. V daném okamžiku se provedou aktualizace aplikace Supply Chain Management. Poté, co má prodejní objednávka stav **Potvrzeno**, projekt založený na šabloně **Prodejní objednávky (Supply Chain Management do Sales) - přímo** umožňuje synchronizovat aktualizace nebo stav plnění z aplikace Supply Chain Management do Sales.

Není nutné vytvoření objednávek v aplikaci Sales. Místo toho můžete vytvořit nové prodejní objednávky v aplikaci Supply Chain Management. Poté, co má prodejní objednávka stav **Potvrzeno**, bude synchronizována do aplikace Sales, jak je popsáno ve výše uvedeném odstavci.

V aplikaci Supply Chain Management pomáhají filtry v šabloně zajistit, aby byly v synchronizaci zahrnuty pouze příslušné prodejní objednávky:

- Objednávající a fakturující odběratel na prodejní objednávce musí pocházet z aplikace Sales, aby byli zahrnuti do procesu synchronizace. V aplikaci Supply Chain Management se používají sloupce **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** k filtrování prodejních objednávek z datových tabulek.
- Prodejní objednávka musí být v aplikaci Supply Chain Management potvrzena. Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem **Expedováno** nebo **Fakturováno**, budou synchronizovány do aplikace Sales.
- Po vytvoření nebo úpravě prodejní objednávky musí být provedena v aplikaci Supply Chain Management dávková úloha **Vypočítat celkové tržby**. Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales.

## <a name="freight-tax"></a>Daň z přepravy

Aplikace Sales nepodporuje daň na úrovni záhlaví, protože daň je uložena na úrovni řádku. K podpoře daně na úrovni záhlaví z aplikace Supply Chain Management, jako je daň z přepravy, systém synchronizuje daň do aplikace Sales jako zápis produktu s názvem **Daň z přepravy** a který má částku daně z aplikace Supply Chain Management. Standardní kalkulace ceny v aplikaci Sales slouží pro součty, a to i v případě, kdy je daň na úrovní záhlaví z aplikace Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Výpočet slevy a zaokrouhlení

Model výpočtu slevy v aplikaci Sales se liší od modelu výpočtu slevy v aplikaci Supply Chain Management. V aplikaci Supply Chain Management konečná částka slevy na řádku prodeje může být výsledkem kombinace částky slevy a procent slevy. Pokud je tato celková částka slevy podělená množstvím na řádku, může dojít k zaokrouhlení. Toto zaokrouhlení však není bráno v potaz, pokud je zaokrouhlená částka slevy na jednotku synchronizována do aplikace Sales. Chcete-li zaručit, že celková částka slevy z řádku prodeje v aplikaci Supply Chain Management je správně synchronizována do aplikace Sales, musí být celá částka synchronizována, aniž by byla podělena množstvím řádku. Proto je nutné definovat v aplikaci Sales možnost **Metoda výpočtu slevy** jako **Položku řádku**.

Při synchronizaci řádku prodejní objednávky z aplikace Sales do aplikace Supply Chain Management se používá celková částka řádkové slevy. Protože aplikace Supply Chain Management nemá žádné pole pro uložení celé částky slevy pro řádek, je částka podělená množstvím a uložená v poli **Řádková sleva**. Jakékoliv zaokrouhlování, ke kterému dojde při tomto dělení, je uloženo v poli **Prodejní náklady** na řádku prodeje.

### <a name="example"></a>Příklad

**Synchronizace ze Supply Chain Management**

- **Prodej:** množství = 3, sleva na řádek = 10 USD
- **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek =-$0,01 

**Synchronizace ze Supply Chain Management do Sales**

- **Supply Chain Management**: množství = 3, částka řádkové slevy = $3,33, prodejní poplatek =-$0,01
- **Prodej:** množství = 3, sleva na řádek = (3 × 3,33 USD) + $0,01 USD = 10 USD

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Nové sloupce byly přidána do tabulky **Objednávka** a zobrazí na stránce:

- **Je externě spravováno** - Nastavte tuto možnost na **Ano**, když pořadí pochází z aplikace Supply Chain Management.
- **Stav zpracování** - Tento sloupec ukazuje stav zpracování objednávky v aplikaci Supply Chain Management. K dispozici jsou následující hodnoty:

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

Nastavení **Má pouze externě udržované produkty** se používá během aktivace objednávky ke konzistentnímu sledování, zda prodejní objednávka sestává zcela z externě spravovaných produktů. Pokud prodejní objednávka sestává zcela z externě spravovaných produktů, produkty jsou evidovány v aplikaci Supply Chain Management. Toto nastavení pomáhá zaručit, že neaktivujete a nepokusíte se synchronizovat řádky prodejní objednávky s produkty, které mají v aplikaci Supply Chain Management neznámé produkty.

Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Supply Chain Management a synchronizovány do aplikace Sales. Tyto objednávky nelze upravovat, protože informace o prodejní objednávce budou synchronizovány po této aktivaci z aplikace Supply Chain Management.

Stav prodejní objednávky zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Supply Chain Management mohou být odeslány do prodejní objednávky v aplikaci Sales. Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní** v projektu integrace dat.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních objednávek je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení aplikace Sales přiřazen. Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá. Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.

    Přejděte na **Nastavení** &gt; **Zabezpečení** &gt; **Týmy**, vyberte příslušný tým, zvolte **Spravovat role** a vyberte roli s požadovanými oprávněními, například **Správce systému**.

- Chcete-li zajistit správné výpočty slev v aplikacích Supply Chain Management, je třeba nastavit položku **Metoda výpočtu slevy** na **Položka řádku**.
- Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Prodej** a ujistěte se, že se používají následující nastavení:

    - Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
    - Sloupec **Metoda výpočtu slevy** je nastaven na **Položka řádku**.

### <a name="setup-in-supply-chain-management"></a>Nastavení v Supply Chain Management

- Přejděte na **Prodej a marketing** &gt; **Periodické úlohy** &gt; **Vypočítat celkové tržby** a nastavte úlohu, aby se spustila jako dávková úloha. Nastavte možnost **Vypočítat celkové částky prodejních objednávek** na **Ano**. Tento krok je důležitý, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales. Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.

Pokud také používáte integraci s pracovními příkazy, je nutné nastavit původ prodeje. Původ prodej slouží k odlišení prodejních objednávek v Supply Chain Management, které byly vytvořeny z pracovních objednávek v modulu Field Service. Když má prodejní objednávka původ typu **Integrace pracovního příkazu**, v záhlaví prodejní objednávky se zobrazí pole **Stav externí pracovní objednávky**. Původ prodeje zajišťuje, aby během synchronizace prodejní objednávky ze Supply Chain Management do Field Service byly odfiltrovány prodejních objednávek, které byly vytvořeny z pracovních příkazů ve Field Service.

1. Přejděte na **Prodej a marketing** \> **Nastavení** \> **Prodejní objednávky** \> **Původ prodeje**.
2. Vyberte **nový** pro vytvoření nového původu prodeje.
3. Ve sloupci **Původ prodeje** zadejte název pro původ prodeje, jako je například **SalesOrder**.
4. Do sloupce **Popis** zadejte popis, například **Prodejní objednávka z obchodního oddělení**.
5. Zaškrtněte políčko **Přiřazení typů původu**.
6. Nastavte hodnotu ve sloupci **Typ původu prodeje** na **Integrace prodejní objednávky**.
7. Zvolte **Uložit**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Nastavení v prodejních objednávkách (Sales do Supply Chain Management) - Přímo v projektu integrace dat

- Ujistěte se, že existuje požadované mapování pro **Shipto\_country** do **DeliveryAddressCountryRegionISOCode**. Můžete ponechat prázdnou výchozí hodnotu v mapě hodnot, abyste nemuseli zadávat zemi pro národní objednávky. Nastavte levou stranu na Prázdné a pravou stranu na požadovanou zemi nebo oblast.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí a kde prázdná hodnota = USA.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Nastavení v prodejních objednávkách (Supply Chain Management do Sales) - Přímo v projektu integrace dat

#### <a name="salesheader-task"></a>Úloha SalesHeader

- Ceník je povinný pro vytvoření objednávek v aplikaci Sales. Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny. Výchozí ceník můžete použít pro jednu měnu. Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.

    Výchozí hodnota šablony pro  **pricelevelid.name \[Název ceníku\]** je **CRM služba USA (vzorek)**.

#### <a name="salesline-task"></a>Úloha SalesLine

- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Supply Chain Management.
- Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.

    Hodnota šablony, která má mapu hodnoty, je definována pro **SalesUnitSymbol** do **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Sloupce **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tyto sloupce mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je tabulka synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat.

> [!NOTE]
> Mapování ukazuje, jaké informace o sloupci budou synchronizovány z aplikace Sales do aplikace Supply Chain Management nebo naopak.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Prodejní objednávky (Supply Chain Management do Sales): OrderHeader

[![Mapování šablon v integraci dat, Prodejní objednávky (Supply Chain Management do Sales) - Přímo: OrderHeader.](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Prodejní objednávky (Supply Chain Management do Sales): OrderLine

[![Mapování šablon v integraci dat, Prodejní objednávky (Supply Chain Management do Sales) - Přímo: OrderLine.](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Prodejní objednávky (Sales do Supply Chain Management): OrderHeader

[![Mapování šablon v integraci dat, Prodejní objednávky (Sales do Supply Chain Management) - Přímo: OrderHeader.](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Prodejní objednávky (Sales do Supply Chain Management) - přímé: OrderLine

[![Mapování šablon v integraci dat, Prodejní objednávky (Sales do Supply Chain Management) - Přímo: OrderLine.](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-articles"></a>Související články

[Zpeněžení potenciálního zákazníka](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
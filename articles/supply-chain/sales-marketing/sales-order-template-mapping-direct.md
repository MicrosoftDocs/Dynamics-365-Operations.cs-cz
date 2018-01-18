---
title: "Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních objednávek a řádků přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních objednávek a řádků přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci hlaviček a řádků prodejních objednávek z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Prodejní objednávky (Fin and Ops do Sales) - Přímo
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

Prodejní objednávky jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.

Filtry v šabloně pomáhají zajistit, že do synchronizace jsou zahrnuty pouze příslušné prodejní objednávky:

- Objednávající a fakturující odběratel na prodejní objednávce, která pochází z aplikace Sales, budou zahrnuti do procesu synchronizace. V aplikaci Finance and Operations se používají pole **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** ke sledování ke sledování synchronizace v datových entitách.
- Prodejní objednávka musí být v aplikaci Finance and Operations potvrzena. Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem **Expedováno** nebo **Fakturováno**, budou synchronizovány do aplikace Sales.
- Po vytvoření nebo úpravě prodejní objednávky musí být provedena v aplikaci Finance and Operations dávková úloha **Vypočítat celkové tržby**. Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales.

> [!NOTE]
> Aktuálně není daň související s náklady na záhlaví prodejní objednávky zahrnuta do synchronizace z aplikace Finance and Operations do aplikace Sales. Aplikace Sales nepodporuje daňové informace na úrovni záhlaví. Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Nová pole byla přidána do entity **Objednávka** a zobrazí na stránce:

- **Je externě spravováno** - Nastavte tuto možnost na **Ano**, když pořadí pochází z aplikace Finance and Operations.
- **Stav zpracování** - Toto pole ukazuje stav zpracování objednávky v aplikaci Finance and Operations. K dispozici jsou následující hodnoty:

    - Aktivní
    - Potvrzeno
    - Dodací list
    - Fakturováno
    - Vydáno
    - Částečně vyskladněno
    - Částečně zabaleno
    - Expedováno
    - Částečně expedováno
    - Částečně fakturováno
    - Zrušeno

Nastavení **Má pouze externě udržované produkty** se používá v jiných scénářích prodejní objednávky (například při synchronizaci z aplikace Sales do aplikace Finance and Operations), aby se konzistentně sledovalo, zda je prodejní objednávka tvořena zcela z externě udržovaných produktů. Pokud prodejní objednávka sestává zcela z externě spravovaných produktů, produkty jsou evidovány v aplikaci Finance and Operations. Toto nastavení pomáhá zaručit, že se nepokusíte synchronizovat řádky prodejní objednávky s produkty, které mají v aplikaci Finance and Operations neznámé produkty.

Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales. Stránku objednávky nelze upravovat, protože informace o prodejní objednávce budou synchronizovány z aplikace Finance and Operations.

Stav prodejní objednávky zůstane **Aktivní**, aby se zajistilo, že změny z aplikace Finance and Operations mohou být odeslány do prodejní objednávky v aplikaci Sales. Chcete-li kontrolovat toto chování, nastavte hodnotu **Statecode \[Stav\]** na **Aktivní** v projektu integrace dat.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních objednávek je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení aplikace Sales přiřazen. Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá. Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.

    Přejděte na **Nastavení** > **Zabezpečení** > **Týmy**, vyberte příslušný tým, zvolte **Spravovat role** a vyberte roli s požadovanými oprávněními, například **Správce systému**.

- Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej**a ujistěte se, že se používají následující nastavení:

    - Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
    - Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.

### <a name="setup-in-finance-and-operations"></a>Nastavení v aplikaci Finance and Operations

Přejděte na  **Prodej a marketing** > **Periodické úlohy** > **Vypočítat celkové tržby** a nastavte úlohu, aby se spustila jako dávková úloha. Nastavte možnost **Vypočítat celkové částky prodejních objednávek** na **Ano**. Tento krok je důležitý, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do aplikace Sales. Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="salesheader-task"></a>Úloha SalesHeader

- Ujistěte se, že existuje požadované mapování pro **InvoiceCountryRegionId** do **BillingAddress\_Country** a pro **DeliveryCountryRegionId** do **DeliveryAddress\_Country**.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.

- Ceník je povinný pro vytvoření objednávek v aplikaci Sales. Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny. Výchozí ceník můžete použít pro jednu měnu. Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.

    Výchozí hodnota šablony pro  **pricelevelid.name \[Název ceníku\]** je **CRM služba USA (vzorek)**.

#### <a name="salesline-task"></a>Úloha SalesLine

- Ujistěte se, že existuje požadované mapování pro  **DeliveryCountryRegionId** do **DeliveryAddress\_Country**.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.

- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.

    Hodnota šablony, která má mapu hodnoty, je definována pro o**SalesUnitSymbol** do **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Mapování šablony v integrátoru dat](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Mapování šablony v integrátoru dat](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping-direct.md)

[Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales](sales-invoice-template-mapping-direct.md)





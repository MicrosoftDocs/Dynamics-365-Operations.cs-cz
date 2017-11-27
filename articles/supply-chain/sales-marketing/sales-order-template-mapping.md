---
title: "Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních objednávek z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních objednávek z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci hlaviček a řádků prodejních objednávek z aplikace Finance and Operations do aplikace Sales slouží následující šablony a základní úkoly:

- **Název šablony v integraci dat** 

    - Prodejní objednávky (Fin and Ops do Sales)
    
- **Názvy úkolů v projektu integrace dat**

    - OrderHeader
    - OrderLine

Synchronizace úkolů vyžadovaných před synchronizací záhlaví a řádků prodejní objednávky:

- Produkty (Fin and Ops do Sales)
- Účty (Sales do Fin and Ops) (pokud se používají)
- Kontakty na zákazníky (Sales do Fin and Ops) (pokud se používají)

## <a name="entity-set"></a>Sada entit

| Finance and Operations |    Common Data Service (CDS)         |     Prodej.      |
|------------------------|----------------|----------------|
| Záhlaví prodejní objednávky CDS| SalesOrder     | SalesOrders |
| Řádky prodejní objednávky CDS  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Tok entity

Prodejní objednávky jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.

Filtry v šabloně zajišťují, že do synchronizace jsou zahrnuty pouze příslušné prodejní objednávky:

- Objednávající a fakturující odběratel na prodejní objednávce, která pochází z aplikace Sales, budou zahrnuti do procesu synchronizace. V aplikaci Finance and Operations se používají pole **OrderingCustomerIsExternallyMaintained** a **InvoiceCustomerIsExternallyMaintained** ke sledování ke sledování synchronizace v datových entitách.

- **Prodejní objednávka** musí být v aplikaci Finance and Operations potvrzena. Pouze potvrzené prodejní objednávky nebo prodejní objednávky s vyšším stavem zpracování, například stavem Expedováno nebo Fakturováno, budou synchronizovány do aplikace Sales.

- Po vytvoření nebo úpravě prodejní objednávky, musí být provedena v aplikaci Finance and Operations dávková úloha **Vypočítat celkové tržby**. Pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do CDS a aplikace Sales.

> [!NOTE]
> Daně související s náklady na **Záhlaví prodejní objednávky** aktuálně nejsou zahrnuty do synchronizace z aplikace Finance and Operations do aplikace Sales. Důvodem je skutečnost, že aplikace Sales nepodporuje daňové informace na úrovni záhlaví. Je zahrnuta daň související s náklady na úrovni řádku.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Nová pole se přidají do entity **Objednávka** a zobrazí na stránce:

- **Je externě spravováno** - Nastavte na **Ano**, když pořadí pochází z aplikace Finance and Operations.

- **Stav zpracování** - Používá se k zobrazení stavu zpracování objednávky v aplikaci Finance and Operations. Hodnoty jsou:

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

Nastavení **Má pouze externě udržované produkty** se používá v jiných scénářích prodejní objednávky (synchronizace z aplikace Sales do aplikace Finance and Operations), aby se konzistentně sledovalo, zda je prodejní objednávka tvořena zcela z **externě udržovaných produktů**, přičemž produkty jsou udržovány v aplikaci Finance and Operations. Toto chování pomáhá zaručit, že nezkusíte synchronizovat řádky prodejní objednávky s produkty, které nejsou známy v aplikaci Finance and Operations.
 
Tlačítka **Vytvořit fakturu**, **Zrušit objednávku**, **Přepočítat**, **Získat produkty** a **Vyhledávání adresy** na stránce **Prodejní objednávka** jsou pro externě udržované objednávky skryta, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales. Stránku objednávky nelze upravovat, protože informace o prodejních objednávkách budou synchronizovány z aplikace Finance and Operations
 
**Stav prodejní objednávky** zůstane aktivní, aby se zajistilo, že změny z aplikace Finance and Operations mohou být odeslány do **prodejní objednávky** v aplikaci Sales. Toto je kontrolováno nastavením výchozího **Statecode [stavu]** na **Aktivní** v projektu integrace dat.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů 

Před synchronizací prodejních objednávek je důležité aktualizovat systémy s následujícím nastavením:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Zajistěte oprávnění pro tým, ke kterému je uživatel (ze **sady připojení** aplikace Sales) přiřazen. Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým nikoliv. Bez toho je vygenerována chyba, která oznamuje, že chybí hlavní tým při spuštění projektu z integrátoru dat. 

    - V **Nastavení** > **Zabezpečení** > **Týmy**, vyberte příslušný tým, klikněte na **Spravovat role** a vyberte roli s požadovanými oprávněními, například správce systému.

- V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Použít systém výpočtu ceny** je nastavena na **Ano**. 

- V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Metoda výpočtu slevy** je nastavena na **Položka řádku**. 

### <a name="setup-in-finance-and-operations"></a>Nastavení v aplikaci Finance and Operations

Nastavte **Prodej a marketing** > **Periodické úlohy** > **Vypočítat celkové tržby** pro spouštění v podobě dávkové úlohy, s možností **Vypočítat celkové částky prodejních objednávek** nastavenou na **Ano**. Je to důležité, protože pouze prodejní objednávky s vypočítanými celkovými tržbami budou synchronizovány do CDS a aplikace Sales. Frekvence dávkové úlohy musí být ve shodě s frekvencí synchronizace prodejní objednávky.

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="salesheader-task"></a>Úloha SalesHeader

- Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**.

    - Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je ORG001.
    - Výchozí hodnota šablony pro **InvoiceAccount_Organization_OrganizationId** je ORG001.
    - Výchozí hodnota šablony pro **Organization_OrganizationId** je ORG001.

- Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS pro InvoiceCountryRegionId do BillingAddress_Country** a pro **DeliveryCountryRegionId do DeliveryAddress_Country**.

    - Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.

- **Ceník** je povinný pro vytvoření objednávek v aplikaci Sales. Aktualizujte **ValueMap** v **CDS** > **Cíl** pro **pricelevelid.name [název ceníku]** do **ceníku** použitého v aplikaci Sales podle měny. Můžete buď použít výchozí **ceník** pro jednu měnu nebo použít **ValueMap**, máte-li **ceníky** v různých měnách.
    
    - Výchozí hodnota šablony pro **pricelevelid.name [název ceníku]** je CRM Service USA (vzorek). 

#### <a name="salesline-task"></a>Úloha SalesLine

- Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**. 
    
    - Výchozí hodnota šablony pro **SalesOrder_Organization_OrganizationId** je ORG001.
    - Výchozí hodnota šablony pro **Product_Organization_OrganizationId** je ORG001.

- Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS** pro **DeliveryCountryRegionId** do **DeliveryAddress_Country**.

    - Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.
    
- Ujistěte se, že existuje potřebná hodnota **ValueMap** pro **SalesUnitSymbol** v aplikaci Finance and Operations v možnostech **Zdroj** > **CDS mapování**.

    - Hodnota šablony s **ValueMap** je definovaná pro **SalesUnitSymbol to Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

### <a name="orderheader"></a>OrderHeader

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Související témata

[Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping.md)

[Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping.md)

[Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping.md)

[Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales](sales-invoice-template-mapping.md)



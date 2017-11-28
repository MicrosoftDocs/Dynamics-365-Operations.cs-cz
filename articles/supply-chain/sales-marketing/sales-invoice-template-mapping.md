---
title: "Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních faktur z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček a řádků prodejních faktur z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Šablony a úkoly

K synchronizaci hlaviček a řádků prodejních faktur z aplikace Finance and Operations do aplikace Sales slouží následující šablony a základní úkoly:

- **Název šablony v integraci dat** 

     - Prodejní faktury (Fin and Ops do Sales)

- **Názvy úkolů v projektu integrace dat**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Synchronizace úkolů vyžadovaných před synchronizací záhlaví a řádků prodejní faktury:
-   Produkty (Fin and Ops do Sales)
-   Účty (Sales do Fin and Ops) (pokud se používají)
-   Kontakty (Sales do Fin and Ops) (pokud se používají)
-   Záhlaví a řádky prodejní objednávky (Fin and Ops do Sales)

## <a name="entity-set"></a>Sada entit

| Finance and Operations                               | Common Data Service (CDS)              | Prodej.          |
|------------------------------------------------------|------------------|----------------|
| Záhlaví prodejní faktury odběratele udržované externě | SalesInvoice     | Faktury       |
| Řádky prodejní faktury odběratele udržované externě   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Tok entity

Prodejní faktury jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.

> [!NOTE]
> Daně související s náklady na **Záhlaví prodejní faktury** aktuálně nejsou zahrnuty do synchronizace z aplikace Finance and Operations do aplikace Sales. Důvodem je skutečnost, že aplikace Sales nepodporuje daňové informace na úrovni záhlaví. Je zahrnuta daň související s náklady na úrovni řádku.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

-  Pole **Číslo faktury** je přidáno do entity **Faktura** a zobrazí na stránce.
 
-  Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales. Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Finance and Operations
 
-  **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Finance and Operations do aplikace Sales. Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury. To umožňuje vlastníkovi prodejní objednávky zobrazit fakturu.
 
## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních faktur je důležité aktualizovat systémy s následujícím nastavením:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Použít systém výpočtu ceny** je nastavena na **Ano**. 

- V **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** se ujistěte, že možnost **Metoda výpočtu slevy** je nastavena na **Položka řádku**. 

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="salesinvoiceheader-task"></a>Úloha SalesInvoiceHeader

- Aktualizujte mapování pro **CDS ID organizace** v možnostech **Zdroj** > **CDS**. 

    -  Výchozí hodnota šablony pro **SalesOrder_Organization_OrganizationId** je ORG001.
    -  Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je ORG001.
    -  Výchozí hodnota šablony pro **Organization_OrganizationId** je ORG001.

- Ujistěte se, že existuje potřebné mapování v možnostech **Zdroj** > **CDS pro InvoiceCountryRegionId** do **BillingAddress_Country**.

    -  Hodnota šablony je **ValueMap** s určitým počtem namapovaných zemí.

- **Ceník** je povinný pro vytvoření faktur v aplikaci Sales. Aktualizujte **ValueMap** v **CDS** > **Destination for pricelevelid.name [název ceníku]** na **ceník** použitý v aplikaci Sales podle měny. Můžete buď použít výchozí **ceník** pro jednu měnu nebo použít **ValueMap**, máte-li **ceníky** v různých měnách.

    -  Hodnota šablony pro **pricelevelid.name [název ceníku]** je **ValueMap** na základě **měny**.
    -  usd: CRM Service USA (vzorek). 

#### <a name="salesinvoiceline-task"></a>Úloha SalesInvoiceLine

- Ujistěte se, že existuje potřebné mapování v položkách **Zdroj** > **CDS pro měrnou jednotku**.

- Ujistěte se, že existuje potřebná hodnota **ValueMap** pro **SalesUnitSymbol** v aplikaci Finance and Operations v možnostech **Zdroj** > **CDS mapování**. 
    
    - Hodnota šablony s **ValueMap** je definovaná pro **SalesUnitSymbol to Quantity_UOM**.
    
-  Aktualizujte mapování pro **CDS ID organizace v možnostech Zdroj** > **CDS**. 

    -  Výchozí hodnota šablony pro **SalesInvoicer_Organization_OrganizationId** je ORG001.
    -  Výchozí hodnota šablony pro **Product_Organization_OrganizationId** je ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou součástí výchozího mapování. Mapování těchto polí vyžaduje nastavení mapování hodnoty, což je specifické pro data v organizacích, mezi kterými je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Související témata

[Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping.md)

[Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping.md)

[Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping.md)

[Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales](sales-order-template-mapping.md)



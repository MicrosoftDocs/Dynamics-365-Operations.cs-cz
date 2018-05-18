---
title: "Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních faktur a řádků z přímo aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales

[!include [banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních faktur a řádků z přímo aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci hlaviček a řádků prodejních faktur z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Prodejní faktury (Fin and Ops do Sales) - Přímo
- **Názvy úkolů v projektu integrace dat:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:

- Produkty (Fin and Ops do Sales) - přímo
- Účty (Sales do Fin and Ops) - přímo (pokud se používají)
- Kontakty (Sales do Fin and Ops) - přímo (pokud se používají)
- Záhlaví a řádky prodejní objednávky (Fin and Ops do Sales) - přímo

## <a name="entity-set"></a>Sada entit

| Finance and Operations                               | Prodej.          |
|------------------------------------------------------|----------------|
| Záhlaví prodejní faktury odběratele udržované externě | Faktury       |
| Řádky prodejní faktury odběratele udržované externě   | InvoiceDetails |

## <a name="entity-flow"></a>Tok entity

Prodejní faktury jsou vytvořeny v aplikaci Finance and Operations a jsou synchronizovány do aplikace Sales.

> [!NOTE]
> Aktuálně není daň související s náklady na záhlaví prodejní faktury zahrnuta do synchronizace z aplikace Finance and Operations do aplikace Sales. Aplikace Sales nepodporuje daňové informace na úrovni záhlaví. Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

- Pole **Číslo faktury** bylo přidáno do entity **Faktura** a zobrazí se na stránce.
- Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Finance and Operations a synchronizovány do aplikace Sales. Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Finance and Operations
- Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Finance and Operations do aplikace Sales. Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury. Vlastník prodejní objednávky tudíž může zobrazit fakturu.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních faktur je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej**a ujistěte se, že se používají následující nastavení:

- Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
- Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="salesinvoiceheader-task"></a>Úloha SalesInvoiceHeader

- Ujistěte se, že existuje požadované mapování pro  **InvoiceCountryRegionId** do **BillingAddress\_Country**.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí.

- Ceník je povinný pro vytvoření faktur v aplikaci Sales. Aktualizujte mapu hodnot pro **pricelevelid.name \[Název ceníku\]** do ceníku, použitého v aplikaci Sales podle měny. Výchozí ceník můžete použít pro jednu měnu. Popřípadě pokud máte ceníky v několika měnách, můžete použít mapu hodnot.

    Hodnota šablony pro **pricelevelid.name \[Název ceníku\]** je mapa hodnot založená na měně s USD = CRM služba USA (vzorek).  
    
#### <a name="salesinvoiceline-task"></a>Úloha SalesInvoiceLine

- Ujistěte se, že existuje požadované mapování pro položku **Měrná jednotka**.
- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.

    Hodnota šablony, která má mapu hodnoty, je definována pro o**SalesUnitSymbol** do **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping-direct.md)

[Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales](sales-order-template-mapping-direct-two-ways.md)








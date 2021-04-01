---
title: Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales
description: Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci záhlaví a řádek prodejní faktury přímo z aplikace Dynamics 365 Supply Chain Management do Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: e12b2ca0fd5df3b2acf6b84d7ff51967e1acc93e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231761"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synchronizace záhlaví a řádků prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales

[!include [banner](../includes/banner.md)]

Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci záhlaví a řádek prodejní faktury přímo z aplikace Dynamics 365 Supply Chain Management do Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci hlaviček a řádků prodejních faktur z aplikace Supply Chain Management do aplikace Sales slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Prodejní faktury (Fin and Ops do Sales) - Přímo
- **Názvy úkolů v projektu integrace dat:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní faktury a mohou se objevit řádky:

- Produkty (Supply Chain Management do Sales) – Přímo
- Obchodní vztahy (Sales do Supply Chain Management) – Přímo (pokud se používá)
- Kontakty (Sales do Supply Chain Management) – Přímo (pokud se používá)
- Hlavička a řádky prodejní objednávky (Supply Chain Management do Sales): OrderHeader

## <a name="entity-set"></a>Sada entit

| Správa dodavatelsko-odběratelského řetězce                              | Prodej.          |
|------------------------------------------------------|----------------|
| Záhlaví prodejní faktury odběratele udržované externě | Faktury       |
| Řádky prodejní faktury odběratele udržované externě   | InvoiceDetails |

## <a name="entity-flow"></a>Tok entity

Prodejní faktury jsou vytvořeny v aplikaci Supply Chain Management a jsou synchronizovány do aplikace Sales.

> [!NOTE]
> Aktuálně není daň související s náklady na záhlaví prodejní faktury zahrnuta do synchronizace z aplikace Supply Chain Management do aplikace Sales. Aplikace Sales nepodporuje daňové informace na úrovni záhlaví. Daň, která souvisí s náklady na úrovni řádku, bude zahrnuta do procesu synchronizace.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

- Pole **Číslo faktury** bylo přidáno do entity **Faktura** a zobrazí se na stránce.
- Tlačítko **Vytvořit fakturu** je na stránce **Prodejní objednávka** skryto, protože faktury budou vytvořeny v aplikaci Supply Chain Management a synchronizovány do aplikace Sales. Stránku **Faktura** nelze upravovat, protože faktury budou synchronizovány z aplikace Supply Chain Management.
- Hodnota **Stav prodejní objednávky** se změní automaticky na **Vyfakturováno**, když byla související faktura synchronizována z aplikace Supply Chain Management do aplikace Sales. Vlastník prodejní objednávky, ze které byla faktura vytvořena, je přiřazen jako vlastník faktury. Vlastník prodejní objednávky tudíž může zobrazit fakturu.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních faktur je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

Přejděte na **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** a ujistěte se, že se používají následující nastavení:

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
- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Supply Chain Management.

    Hodnota šablony, která má mapu hodnoty, je definována pro o **SalesUnitSymbol** do **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Mapování šablony v integraci dat](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Související témata

[Zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.](accounts-template-mapping-direct.md)

[Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales](products-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management](contacts-template-mapping-direct.md)

[Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
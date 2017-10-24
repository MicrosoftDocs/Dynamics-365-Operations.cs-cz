---
title: "Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 9117b5af3beff7290816586f63091b12e357339c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci hlaviček a řádků prodejních nabídek v aplikaci Finance and Operations slouží následující šablony a základní úkoly:

- **Název šablony:** Sales Quotes (Sales to Fin and Ops)
- **Názvy úkolů v projektu:**

    - QuoteHeader
    - QuoteLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:

- Produkty (Fin and Ops do Sales)
- Účty (Sales do Fin and Ops) (pokud se používají)
- Kontakty na zákazníky (Sales do Fin and Ops) (pokud se používají)

## <a name="entity-set"></a>Sada entit

| Prodej.        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Citáty       | Nabídka     | Záhlaví prodejní nabídky   |
| QuoteDetails | QuotationLine | Řádky prodejní nabídky CDS |

## <a name="entity-flow"></a>Tok entity

Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do aplikace Finance and Operations

Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:

- Jsou externě zachovány všechny produkty v řádcích prodejní nabídky.
- Prodejní nabídka je aktivní nebo aktivovaná.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Pole **Má pouze externě udržované produkty** bylo přidáno do entity Nabídka ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů. Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Finance and Operations. Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které nejsou známy v aplikaci Finance and Operations.

Všechny produkty a řádky nabídky jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví nabídky. Tyto informace lze najít v poli **Nabídka má pouze externě udržované produkty** v entitě Řádek nabídky.

Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** řízena s zpracována aplikací Finance and Operations.

V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Finance and Operations:

- **Pole jen pro čtení v záhlaví prodejní nabídky:** % slevy, Sleva, částka dopravného
- **Pole jen pro čtení pro řádky prodejní nabídky:** Daň

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních objednávek je důležité aktualizovat systémy s následujícím nastavením:

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Sales** a ujistěte se, že je pole **Metoda výpočtu slevy** nastaveno na **Jednotkové**. Toto nastavení pomáhá zajistit, že sleva položky řádku z aplikace Sales odpovídá nastavení v aplikaci Finance and Operations. V opačném případě nebude sleva opravena v aplikaci Finance and Operations, protože aplikace Finance and Operations bude číst slevu jako slevu podle jednotky i když byla v aplikaci Sales slevou podle řádku.

### <a name="setup-in-finance-and-operations"></a>Nastavení v aplikaci Finance and Operations

- Přejděte do **Pohledávky** &gt; **Nastavení** &gt; **Parametry pohledávek**. Na kartě **Číselná řada** vyberte číselné řady pro prodejní nabídky a klepněte na tlačítko **Zobrazit podrobnosti**. Poté v části **Obecné nastavení**, nastavte pole **Ruční** na **Ano**.
- Přejděte do nabídky **Pohledávky** &gt; **Nastavení** &gt; **Parametry pohledávek**. Poté na kartě **dodávky** nastavte hodnotu v poli **řízení data dodání** na **žádná**. Toto nastavení pomáhá předcházet selháním synchronizace pro prodejní nabídky.

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="quoteheader"></a>QuoteHeader

- Pole **Požadované datum dodání** je v aplikaci Finance and Operations povinné a synchronizace se nezdaří, když je toto pole prázdné. Aby se tomuto problému předešlo, je v případě, že je toto pole prázdné, výchozí datum převzato z pole **Zdroj &gt; CDS**. Datum by mělo být aktualizováno na preferovanou hodnotu. V současné době nelze zadat hodnotu jako **Dnes** představující dnešní datum. Je nutné zadat konkrétní datum. Výchozí hodnota šablony pro **Požadovat datum doručení** je **1/1/2020**.
- Pole **Kód země/oblasti pro adresu** je v aplikaci Finance and Operations povinné. Aby nedocházelo k chybám synchronizace, můžete určit výchozí hodnotu, která se použije v případě, že pole v aplikaci Sales zůstane prázdné. Tato výchozí hodnota je rovněž užitečná, protože není nutné ručně zadat hodnotu do pole **Země** pro místní adresy. Neexistuje žádná výchozí hodnota šablony pro **DeliveryAddressCountryRegionISOCode**.
- Aktualizujte mapování pro **ID organizace CDS** v okně **Zdroj &gt; CDS** tak, aby odpovídala hodnotě **Organizace CDS** v entitě Organizace:

    - Výchozí hodnota šablony pro **Organization_OrganizationId** je **ORG001**.
    - Výchozí hodnota šablony pro **Account_Organization_OrganizationId** je **ORG001**.
    - Výchozí hodnota šablony pro **InvoiceAccount_OrganizationId** je **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Aktualizujte mapování pro **ID organizace CDS** v okně **Zdroj &gt; CDS** tak, aby odpovídala hodnotě **Organizace CDS** v entitě Organizace:

    - Výchozí hodnota šablony pro **Organization_OrganizationId** je **ORG001**.
    - Výchozí hodnota šablony pro **Product_Organization_Organization_OrganizationId** je **ORG001**.
    - Výchozí hodnota šablony pro **Quotation_Organization_Organization_OrganizationId** je **ORG001**.

- Pole **Požadované datum dodání** je v aplikaci Finance and Operations povinné a synchronizace se nezdaří, když je toto pole prázdné. Aby se tomuto problému předešlo, je v případě, že je toto pole prázdné, výchozí datum převzato z pole **Zdroj &gt; CDS**. Datum by mělo být aktualizováno na preferovanou hodnotu. V současné době nelze zadat hodnotu jako **Dnes** představující dnešní datum. Je nutné zadat konkrétní datum. Výchozí hodnota šablony pro **Požadovat datum doručení** je **1/1/2020**.
- Můžete přidat následující mapování z okna **CDS &gt; Cíl** na pomoc při zajištění, že budou řádky nabídky importovány do aplikace Finance and Operations, pokud neexistují žádné výchozí informace od odběratele nebo produktu:

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Neexistuje žádná výchozí hodnota šablony pro **SiteId**.
    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations. Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.

- Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje (MJ) v modulu Finance and Operations existuje v mapování **CDS &gt; Cíl** pro **Quantity_UOM** na **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> - Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Finance and Operations.
> - Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

### <a name="quoteheader"></a>QuoteHeader

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Mapování šablony v integrátoru dat](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Související témata

[Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping.md)

[Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping.md)

[Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping.md)




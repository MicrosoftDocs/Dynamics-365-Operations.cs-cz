---
title: "Synchronizace hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z přímo aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Synchronizace hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci hlaviček prodejních nabídek a řádků z přímo aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).

## <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Prodejní nabídky (Sales do Fin and Ops) - Přímo
- **Názvy úkolů v projektu integrace dat:**

    - QuoteHeader
    - QuoteLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:

- Produkty (Fin and Ops do Sales) - přímo
- Účty (Sales do Fin and Ops) - přímo (pokud se používají)
- Kontakty na zákazníky (Sales do Fin and Ops) - přímo (pokud se používají)

## <a name="entity-set"></a>Sada entit

| Prodej.        | Finance and Operations     |
|--------------|----------------------------|
| Citáty       | Záhlaví prodejní nabídky CDS |
| QuoteDetails | Řádky prodejní nabídky CDS  |

## <a name="entity-flow"></a>Tok entity

Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do aplikace Finance and Operations

Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:

- Jsou externě zachovány všechny nabídky produktu na prodejní nabídce.
- Po kliknutí na tlačítko **Aktivovat nabídku** bude prodejní nabídka aktivní.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Pole **Má pouze externě udržované produkty** bylo přidáno do entity **Nabídka** ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů. Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Finance and Operations. Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které mají v aplikaci Finance and Operations neznámé produkty.

Všechny produkty nabídky na prodejní nabídce jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví prodejní nabídky. Tato informace se nachází v poli **Nabídka má pouze externě udržované produkty** v entitě **QuoteDetails**.

Slevu lze přidat k produkt nabídky a tato sleva bude synchronizována do aplikace Finance and Operations. Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována nastavením v aplikaci Finance and Operations. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Náklady** a **Daň** udržována a zpracovávána v aplikaci Finance and Operations.

V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Finance and Operations:

- Pole jen pro čtení v záhlaví prodejní nabídky: **Sleva %**, **Sleva** a **Částka dopravného**
- Pole jen pro čtení u produktů nabídky: **Daň**

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací prodejních nabídek je důležité, abyste aktualizovali následující nastavení.

### <a name="setup-in-sales"></a>Nastavení v aplikaci Sales

- Zajistěte, že jsou nastavena oprávnění pro tým, ke kterému je uživatel ze sady připojení v aplikaci Sales přiřazen. Používáte-li ukázková data, má obvykle uživatel přístup správce, ale tým ho nemá. Pokud nemá tým přístup správce při spuštění projektu z integrace dat, dostanete chybovou zprávu s oznámením, že hlavní tým chybí.

    Chcete-li nastavit oprávnění pro tým, přejděte na **Nastavení** &gt; **Zabezpečení** &gt; **Týmy**a vyberte příslušný tým. Vyberte **Spravovat role**a poté vyberte roli, která má požadovaná oprávnění, jako je například **Správce systému**.

- Přejděte na **Nastavení** &gt; **Správa** &gt; **Nastavení systému** &gt; **Prodej** a ujistěte se, že se používají následující nastavení:

    - Možnost **Použít systém výpočtu ceny** je nastavena na **Ano**.
    - Pole **Metoda výpočtu slevy** je nastaveno na **Položka řádku**.

### <a name="setup-in-the-data-integration-project"></a>Nastavení projektu integrace dat

#### <a name="quoteheader"></a>QuoteHeader

- Ujistěte se, že existuje požadované mapování pro **Shipto\_country** do **DeliveryAddressCountryRegionISOCode**. V mapě hodnot můžete definovat výchozí hodnotu, která se používá v případě, že je ponechána prázdná. Pouze ponechte levou stranu prázdnou a pravou stranu nastavte na požadovanou zemi nebo oblast. Tímto způsobem nemusíte zadávat zemi nebo oblast pro národní objednávky.

    Hodnota šablony je mapa hodnot, kde je namapováno několik zemí nebo oblastí a kde prázdná hodnota se rovná **US**.

#### <a name="quoteline"></a>QuoteLine

- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Finance and Operations.
- Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.

    Hodnota šablony, která má mapu hodnoty, je definována pro **oumid.name** do **SalesUnitSymbol**.

- Volitelné: Můžete přidat následující mapování na pomoc při zajištění, že budou řádky prodejní nabídky importovány do aplikace Finance and Operations, pokud neexistují žádné výchozí informace od odběratele nebo produktu:

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Neexistuje žádná výchozí hodnota šablony pro **SiteId**.
    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations. Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> - Pole **Slevy**, **náklady**, a **daň** jsou kontrolovány složitým nastavením aplikace Finance and Operations. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Finance and Operations.
> - Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

### <a name="quoteheader"></a>QuoteHeader

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)



---
title: Synchronizace hlaviček a řádků prodejní nabídky přímo z aplikace Sales do Supply Chain Management
description: Toto téma se věnuje šablonám a základním úlohám, které se používají k synchronizaci záhlaví a řádek prodejní nabídky přímo z aplikace Dynamics 365 Sales do Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6b4f0006e4cacc2897d2b6c9c9dde88d0aafa4ad
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653172"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Synchronizace hlaviček a řádků prodejní nabídky přímo z aplikace Sales do Supply Chain Management

[!include [banner](../includes/banner.md)]

Toto téma se věnuje šablonám a základním úlohám, které se používají k synchronizaci záhlaví a řádek prodejní nabídky přímo z aplikace Dynamics 365 Sales do Dynamics 365 Supply Chain Management.

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Supply Chain Management slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Prodejní nabídky (Sales do Supply Chain Management) - Přímo
- **Názvy úkolů v projektu integrace dat:**

    - QuoteHeader
    - QuoteLine

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní nabídky a mmohou se objevit řádky:

- Produkty (Supply Chain Management do Sales) – Přímo
- Obchodní vztahy (Sales do Supply Chain Management) – Přímo (pokud se používá)
- Kontakty na odběratele (Sales do Supply Chain Management) – Přímo (pokud se používá)

## <a name="entity-set"></a>Sada entit

| Prodej.        | Správa dodavatelsko-odběratelského řetězce     |
|--------------|----------------------------|
| Citáty       | Záhlaví prodejní nabídky CDS |
| QuoteDetails | Řádky prodejní nabídky CDS  |

## <a name="entity-flow"></a>Tok entity

Prodejní nabídky jsou vytvořeny v aplikaci Sales a jsou synchronizovány do Supply Chain Management.

Prodejní nabídky z aplikace Sales jsou synchronizovány pouze v případě, že jsou splněny následující podmínky:

- Jsou externě zachovány všechny nabídky produktu na prodejní nabídce.
- Po kliknutí na tlačítko **Aktivovat nabídku** bude prodejní nabídka aktivní.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Pole **Má pouze externě udržované produkty** bylo přidáno do entity **Nabídka** ke konzistentnímu sledování, zda prodejní nabídka sestává zcela z externě spravovaných produktů. Pokud má prodejní nabídka pouze externě spravované produkty, produkty jsou evidovány v modulu Supply Chain Management. Toto chování pomáhá zaručit že nezkusíte synchronizovat řádky prodejní nabídky s produkty, které mají v aplikaci Supply Chain Management neznámé produkty.

Všechny produkty nabídky na prodejní nabídce jsou aktualizovány informacemi z pole **Má pouze externě udržované produkty** ze záhlaví prodejní nabídky. Tato informace se nachází v poli **Nabídka má pouze externě udržované produkty** v entitě **QuoteDetails**.

Slevu lze přidat k produkt nabídky a tato sleva bude synchronizována do aplikace Supply Chain Management. Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována nastavením v aplikaci Supply Chain Management. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Náklady** a **Daň** udržována a zpracovávána v aplikaci Supply Chain Management.

V aplikaci Sales způsobuje toto řešení, že jsou následující pole jen pro čtení, protože hodnoty nejsou synchronizovány s aplikací Supply Chain Management:

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

- Ujistěte se, že existuje požadovaná mapa hodnot pro **SalesUnitSymbol** v aplikaci Supply Chain Management.
- Ujistěte se, že požadované jednotky jsou definovány v aplikaci Sales.

    Hodnota šablony, která má mapu hodnoty, je definována pro **oumid.name** do **SalesUnitSymbol**.

- Volitelné: Můžete přidat následující mapování na pomoc při zajištění, že budou řádky prodejní nabídky importovány do aplikace Supply Chain Management, pokud neexistují žádné výchozí informace od odběratele nebo produktu:

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Supply Chain Management. Neexistuje žádná výchozí hodnota šablony pro **SiteId**.
    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Supply Chain Management. Neexistuje žádná výchozí hodnota šablony pro **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> - Pole **Slevy**, **Náklady**, a **Daň** v hlavičce jsou kontrolována složitým nastavením v aplikaci Supply Chain Management. Toto nastavení v současné době nepodporuje mapování integrace. V aktuálním designu jsou pole **Cena**, **Sleva**, **Účtování** a **Daň** zpracována aplikací Supply Chain Management.
> - Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou součástí výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

### <a name="quoteheader"></a>QuoteHeader

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Mapování šablony v integrátoru dat](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)


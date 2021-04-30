---
title: Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Sales.
author: ChristianRytt
ms.date: 06/10/2019
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8976bc69f63fe5b05ab7dcb8d415515436902658
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909077"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci produktů přímo z Dynamics 365 Supply Chain Management do Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://admin.powerapps.com/dataintegration). Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci účtů z aplikace Supply Chain Management do aplikace Sales slouží následující šablony a základní úkoly:

- **Název šablony v integraci dat:** Produkty (Supply Chain Management do Sales) - Přímo
- **Název úkolu v projektu integrace dat:** Produkty

Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci produktu.

## <a name="entity-set"></a>Sada entit

| Správa dodavatelsko-odběratelského řetězce    | Prodej.    |
|----------------------------|----------|
| Prodejné uvolněné produkty | Produkty |

## <a name="entity-flow"></a>Tok entity

Produkty se spravují v aplikaci Supply Chain Management a synchronizují se do aplikace Sales. Datová entita **Prodejné uvolněné produkty** v aplikaci Supply Chain Management exportuje pouze produkty, které jsou *prodejné*. Prodejné produkty jsou produkty, které mají informace potřebné k tomu, aby mohly být použity na prodejní objednávce. Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Uvolněný produkt**.

Číslo produktu je použito jako klíč. Proto při synchronizaci variant produktu do aplikace Sales má každá variantu produktu individuální ID produktu.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

V aplikaci Sales je přidáno u produktů nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě. Hodnota je ve výchozím nastavení při importu do aplikace Sales nastavena na **Ano**. K dispozici jsou následující hodnoty:

- **Ano** – Produkt pochází z aplikace Supply Chain Management a nebude ho možné upravovat v aplikaci Sales.
- **Ne** – Produkt byl zadána přímo do aplikace Sales.
- **(Prázdné)** – Produkt existoval v aplikaci Sales před povolením řešení zpeněžení potenciálního zákazníka.

Pole **Je externě spravován** pomáhá zajistit, že se do aplikaci Supply Chain Management budou synchronizovat pouze nabídky a prodejní objednávky, které mají externě spravované produkty.

Externě spravované produkty jsou automaticky přidány k prvnímu platnému ceníku se stejnou měnou. Ceníky jsou uspořádány abecedně podle názvu. Jako cena v ceníku se používá prodejní cena produktu z aplikace Supply Chain Management. Proto musí být v aplikaci Sales ceník pro každou prodejní měnu produktu v aplikaci Supply Chain Management. Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.

> [!NOTE]
> - Synchronizaci produktů se nezdaří, pokud neexistuje ceník se shodnou měnou.
> - Můžete kontrolovat použitý ceník s integrací pomocí mapování pricelevelid.name [výchozí ceník (název)] v projektu integrace dat. Vstup musí být pouze malými písmeny. Například výchozí hodnota pro ceník v aplikaci Sales s názvem 'Standardní' bude: Cílové pole:pricelevelid.name [Výchozí ceník (název)] a typ mapování: [ { "transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Před spuštěním první synchronizace je třeba vyplnit tabulku Jedinečný produkt pro existující produkty v aplikaci Supply Chain Management. Stávajících produkty nebudou synchronizovány před dokončením této úlohy.

    1. V aplikaci Supply Chain Management použijte funkci hledání pro **Naplnění tabulky různých produktů**.
    2. Zvolte možnost **Vyplnit tabulku jedinečných produktů** ke spuštění úlohy. Tato úloha musí být spuštěna pouze jednou.

- Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje mezi aplikacemi Supply Chain Management a Sales existuje v mapování **SalesUnitSymbol** na **DefaultUnit (Name)**.
- Aktualizujte mapu hodnot pro položku **Skupina jednotky** (**defaultuomscheduleid.name**), aby odpovídala položce **Skupiny jednotek** v aplikaci Sales.

    Výchozí hodnota šablony je **Výchozí jednotka**.

- Ujistěte se, že všechny prodejní měrné jednotky pro všechny produkty z aplikace Supply Chain Management existují v aplikaci Sales.
- Ujistěte se, že existují ceníky v aplikaci Sales pro každou prodejní měnu produktu v aplikaci Supply Chain Management.
- Při vytváření produktů v aplikaci Sales mohou mít stav **Koncept** nebo **Aktivní**. Chování se řídí pomocí **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** v aplikaci Sales.

    Produkty, které mají při vytváření stav **Koncept** musí být aktivovány předtím, než mohou být přidány do nabídek nebo prodejních objednávek.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.

![Mapování šablony v integrátoru dat](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Související témata

[Zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.](accounts-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management](contacts-template-mapping-direct.md)

[Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
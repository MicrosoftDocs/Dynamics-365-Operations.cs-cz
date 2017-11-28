---
title: "Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Synchronizace produktů přímo z aplikace Finance and Operations na produkty v aplikaci Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů přímo z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition do aplikace Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci produktů z aplikace Finance and Operations do aplikace Sales slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Produkty (Fin and Ops do Sales) - Přímo
- **Název úkolu v projektu integrace dat:** Produkty

Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci produktu.

## <a name="entity-set"></a>Sada entit

| Finance and Operations     | Prodej.    |
|----------------------------|----------|
| Prodejné uvolněné produkty | Produkty |

## <a name="entity-flow"></a>Tok entity

Produkty se spravují v aplikaci Finance and Operations a synchronizují s aplikací Sales. Datová entita **Prodejné uvolněné produkty** v aplikaci Finance and Operations exportuje pouze produkty, které jsou *prodejné*. Prodejné produkty jsou produkty, které mají informace potřebné k tomu, aby mohly být použity na prodejní objednávce. Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Uvolněný produkt**.

Číslo produktu je použito jako klíč. Proto při synchronizaci variant produktu do aplikace Sales má každá variantu produktu individuální ID produktu.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

V aplikaci Sales je přidáno u produktů nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě. Hodnota je ve výchozím nastavení při importu do aplikace Sales nastavena na **Ano**. K dispozici jsou následující hodnoty:

- **Ano** – Produkt pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.
- **Ne** – Produkt byl zadána přímo do aplikace Sales.
- **(Prázdné)** – Produkt existoval v aplikaci Sales před povolením řešení zpeněžení potenciálního zákazníka.

Pole **Je externě spravován** pomáhá zajistit,, že se do aplikaci Finance and Operations budou synchronizovat pouze nabídky a prodejní objednávky, které mají externě spravované produkty.

Externě spravované produkty jsou automaticky přidány k prvnímu platnému ceníku se stejnou měnou. Ceníky jsou uspořádány abecedně podle názvu. Jako cena v ceníku se používá prodejní cena produktu z aplikace Finance and Operations. Proto musí být v aplikaci Sales ceník pro každou prodejní měnu produktu v aplikaci Finance and Operations. Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.

> [!NOTE]
> Synchronizaci produktů se nezdaří, pokud neexistuje ceník se shodnou měnou.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Před spuštěním první synchronizace je třeba vyplnit tabulku Jedinečný produkt pro existující produkty v aplikaci Finance and Operations. Stávajících produkty nebudou synchronizovány před dokončením této úlohy.

    1. V aplikaci Finance and Operations použijte funkci hledání pro **Naplnění tabulky různých produktů**.
    2. Zvolte možnost **Vyplnit tabulku jedinečných produktů** ke spuštění úlohy. Tato úloha musí být spuštěna pouze jednou.

- Ujistěte se, že požadovaná mapa hodnot pro měrnou jednotku prodeje mezi aplikacemi Finance and Operations a Sales existuje v mapování **SalesUnitSymbol** na **DefaultUnit (Name)**.
- Aktualizujte mapu hodnot pro položku **Skupina jednotky** (**defaultuomscheduleid.name**), aby odpovídala položce **Skupiny jednotek** v aplikaci Sales.

    Výchozí hodnota šablony je **Výchozí jednotka**.

- Ujistěte se, že všechny prodejní měrné jednotky pro všechny produkty z aplikace Finance and Operations existují v aplikaci Sales.
- Ujistěte se, že existují ceníky v aplikaci Sales pro každou prodejní měnu produktu v aplikaci Finance and Operations.
- Při vytváření produktů v aplikaci Sales mohou mít stav **Koncept** nebo **Aktivní**. Chování se řídí pomocí **Nastavení** > **Správa** > **Nastavení systému** > **Prodej** v aplikaci Sales.

    Produkty, které mají při vytváření stav **Koncept** musí být aktivovány předtím, než mohou být přidány do nabídek nebo prodejních objednávek.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.

![Mapování šablony v integrátoru dat](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Související témata

[zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do aplikace Sales](sales-order-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales](sales-invoice-template-mapping-direct.md)





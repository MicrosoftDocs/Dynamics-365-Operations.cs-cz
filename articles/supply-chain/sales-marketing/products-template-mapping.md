---
title: "Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Šablona a úkol

Následující šablony a základní úlohy se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) do aplikace Microsoft Dynamics 365 for Sales (Sales).

-   Název šablony: Products (Fin and Ops to Sales)

-   Název úkolu v projektu: Produkty

Synchronizace úkolů vyžadovaných před synchronizací produktů: žádná

## <a name="entity-set"></a>Sada entit

| **Finance and Operations** | **CDS** | **Prodej**  |
|----------------------------|---------|------------|
| Prodejné uvolněné produkty | Produkt | Produkty   |

## <a name="entity-flow"></a>Tok entity

Produkty se spravují v aplikaci Finance and Operations a synchronizují s aplikací Sales. Entita dat **Sellable uvolněných produktů** na penále a operace exportuje pouze produkty, které jsou prodejnosti, což znamená, že produkty požadované informace pro použití v prodejní objednávce. Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Vydaný produkt**.

**Číslo produktu** slouží jako klíč, tj. varianty produktu budou synchronizovány se službou CDS a aplikací Sales u jednotlivých **ID produktu** podle **varianty produktu**.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

V aplikaci Sales je přidáno nové pole **Je externě spravováno** k označení, že je daný produkt spravován externě. Hodnota je ve výchozím nastavení při importu prodeje nastavena na **Ano**.

-   **Je externě spravována = Ano**: produkt pochází z aplikace Finance and Operations a nebude možné ho upravovat v aplikaci Sales.

-   **Je externě spravován = Ne**: Produkt je zadán přímo v aplikaci Sales.

-   **Je externě spravován = prázdné**: produkt existuje v aplikaci Sales před povolením řešení Zpeněžnění potenciálního zákazníka.

Informace **Je externě spravován** slouží k zajištění, že se v aplikaci Finance and Operations budou synchronizovat pouze pole **Nabídky** a **Prodejní objednávky** s možností **Externě spravované produkty**.

**Externě spravované produkty** jsou automaticky přidány k prvnímu platnému **ceníku** ve stejné měně. Všimněte si, že je seznam seřazený abecedně podle **názvu**. Jako cena v **ceníku** se používá prodejní cena produktu z aplikace Finance and Operations. To znamená, že je třeba mít **ceník** v aplikaci Sales pro každou **Prodejní měnu produktu** v aplikaci Finance and Operations. Měna pro uvolněné prodejné produkty je nastavena na zúčtovací měnu v právnické osobě, z níž je exportován produkt.

> [!NOTE]
> Synchronizace produktu se nezdaří bez **ceníku** v odpovídající měně.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

-   Před spuštěním úplně první synchronizace he třeba naplnit **tabulka odlišného produktu** pro existující produkty v aplikaci Finance and Operations. Stávajících produkty nebudou synchronizovány před dokončením této úlohy.

    -   V aplikaci Finance and Operations použijte funkci hledání pro **Naplnění tabulky různých produktů**.

    -   Kliknutím na **Naplnit tabulku různých produktů** spusťte úlohu. Tuto úlohu je nutné spustit pouze jednou.

-   Ujistěte se, že existuje potřebný parametr **ValueMap** pro **Měrnou jednotku** (MJ) prodeje v aplikaci Finance and Operations v části **Zdroj -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Aktualizujte **CDS Organization ID Organization_OrganizationId** v poli **Zdroj -\> CDS**.

    -   Výchozí hodnota šablony je ORG001.

-   Aktualizujte hodnotu **ValueMap** pro **skupinu jednotky** (**defaultuomscheduleid.name**) v poli **CDS -\> Cíl** tak, aby odpovídala **skupinám jednotek** v modulu Sales.

    -   Hodnota šablony je nastavena na **Výchozí jednotka**.

-   Ověřte, že všechny produkty prodávající MJ ze modulu Finance and Operations existují v aplikaci Sales s hodnotou **Seznamy vyskladnění CDS**.

-   Zkontrolujte, zda **ceníky** existují v aplikaci Sales pro každou prodejní měnu produktu v aplikaciFinance and Operations.

-   V aplikaci Sales lze vytvářet produkty se stavem **Koncept** nebo **Aktivní**. To se řídí v **Nastavení systému** pod možností **Sales** v aplikaci Sales.

    -   Produkty, které jsou vytvořeny se stavem konceptu, je třeba aktivovat před jejich přidáním do pole **nabídka** nebo **prodejní objednávka**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

![mapování šablony v integrátoru dat](./media/products-template-mapping-data-integrator-1.png)

![mapování šablony pro produkty v integrátoru dat](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Související témata

[Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping.md)

[Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping.md)

[Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales](sales-order-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales](sales-invoice-template-mapping.md)



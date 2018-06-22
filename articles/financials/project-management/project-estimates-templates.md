---
title: "Synchronizace projektových odhadů z Project Service Automation přímo do projektových prognóz v aplikaci Finance and Operations."
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci odhadů projektových hodin a projektových výdajů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Synchronizace projektových odhadů z Project Service Automation přímo do projektových prognóz v aplikaci Finance and Operations.

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci odhadů projektových hodin a projektových výdajů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations.

> [!NOTE]
> Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o odhadech projektových hodin a výdajů z aplikace Project Service Automation do Finance and Operations.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci odhadů projektových hodin z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:

-  **Název šablony v integraci dat:** Odhady projektových hodin (PSA do Fin and Ops)

-  **Název úkolů v projektu:** 
    - Vztahy transakce 
    - Odhady výdajů

## <a name="entity-set"></a>Sada entit

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projektové úkoly                   | Entita integrace pro odhady hodin projektu   |

## <a name="entity-flow"></a>Tok entity

Odhady projektových hodin jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových hodin.

## <a name="preconditions"></a>Předpoklady

Než dojde k synchronizaci odhadů projektových hodin, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

## <a name="power-query"></a>Power Query

Je nutné použít Microsoft Power Query v šabloně odhadů hodin projektu pro:
- Nastavení **ID modelu prognózy**, které se použije, když integrace vytvoří nové prognózy hodin.
- Filtrování libovolných záznamů specifických pro zdroj v rámci úkolu, který neumožní integraci do prognóz hodin
- Filtrování prázdných řádků kategorie transakce. Neučiníte-li tak, může to způsobit chybné hodinové prognózy.

### <a name="forecast-model-id"></a>ID modelu prognózy
Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, klikněte na šipku **Mapa** a otevřete mapování. Otevřete filtrování a rozšířený dotaz.
- Pokud použijete výchozí šablonu odhadu hodin Microsoft Project (PSA do Fin and Ops), vyberte **Vložená podmínka** v části **Použité kroky**. V zadání **Funkce** nahraďte **O_forecast** názvem **ID modelu prognózy**, které má být použito s integrací. Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.
- Při vytváření nové šablony je nutné přidat tento sloupec. Vyberte **Přidat podmíněný sloupec** a přiřaďte název sloupce, například ModelID. Zadejte podmínku pro sloupec, kde pokud úloha projektu nemá hodnotu null, pak<enter the forecast model ID>; jinou hodnota null.

### <a name="filter-out-resource-specific-records"></a>Filtrování záznamů specifických pro zdroj
Šablona odhadu hodin projektu odhadů (PSA do Fin and Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro zdroj. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr. Ve formuláři filtrování a rozšířeného dotazu zvolte filtrovat na sloupci **msdyn_islinetask**, aby zahrnovalo pouze záznamy **False**.

### <a name="filter-out-empty-transaction-category-rows"></a>Filtrování prázdných řádků kategorie transakce
Je nutné přidat filtr k odstranění všech řádků s prázdnými kategoriemi transakce. To je nutné bez ohledu na to, jestli používáte výchozí šablonu nebo vytváříte vlastní šablonu. Tento filtr odebere všechny souhrnné řádky pocházející z Project Service Automation, které by mohly způsobit, že prognózy hodin v Finance and Operations budou nesprávné. Ve formuláři filtrování a v rozšířeném dotazu zvolte vyfiltrování nulových záznamů ve sloupci **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

K synchronizaci odhadů projektových výdajů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkol:

-  **Název šablony v integraci dat:** Odhady projektových výdajů (PSA do Fin and Ops)
-  **Název úkolů v projektu:** 
     - Vztahy transakce 
     - Odhady výdajů

## <a name="entity-set"></a>Sada entit

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Připojení transakce         | Entita integrace pro vztahy transakce projektu.   |
| Řádky odhadu                  | Entita integrace pro odhady nákladu projektu.           |

## <a name="entity-flow"></a>Tok entity

Odhady projektových výdajů jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových výdajů.

## <a name="prerequisites"></a>Požadavky

Než dojde k synchronizaci odhadů projektových výdajů, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

## <a name="power-query"></a>Power Query

Je nutné použít Microsoft Power Query v šabloně odhadů výdajů projektu pro:
- Filtrování, aby byly zahrnuty pouze záznamy řádku odhadu výdajů
- Nastavení **ID modelu prognózy**, které se použije, když integrace vytvoří nové prognózy hodin.
- Převod typu účtování.
- Převod typů transakcí.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrování, aby byly zahrnuty pouze řádky odhadu výdajů
Šablona odhadů výdajů projektu (PSA do Fin and Ops) má výchozí filtr, který zahrnuje pouze řádky výdajů v integraci. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr. Vyberte úlohu vztahů transakcí a klikněte na šipku **Mapa**. Zvolte **Rozšířený dotaz a filtrování** Vyfiltrujte sloupec **msdyn_transactiontype1**, aby obsahoval pouze **msdyn_estimateline**.

### <a name="forecast-model-id"></a>ID modelu prognózy
Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, pro úlohu odhadu výdajů, klikněte na šipku **Mapa** a otevřete mapování. Otevřete filtrování a rozšířený dotaz.
- Pokud použijete výchozí šablonu odhadu výdajů Microsoft Project (PSA do Fin and Ops), vyberte nejdříve **Vložená podmínka** v části **Použité kroky**. V zadání **Funkce** nahraďte **O_forecast** názvem **ID modelu prognózy**, které má být použito s integrací. Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.
- Při vytváření nové šablony je nutné přidat tento sloupec. Vyberte **Přidat podmíněný sloupec** a přiřaďte název sloupce, například ModelID. Zadejte podmínku pro sloupec, kde pokud ID řádku odhadu není null, pak < ID modelu prognózy >; jinou hodnotu než null.

### <a name="transform-the-billing-types"></a>Převod typu účtování
Šablona odhadů výdajů projektu (PSA do Fin and Ops) má podmíněný sloupec přidaný k převodu typů účtování přijatých z Project Service Automation během integrace
- Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec. Ve formuláři filtrování a rozšířeném dotazu vyberte **Přidat podmíněný sloupec**. Zadejte název sloupce, například BillingType. Zadaná podmínka vypadá takto:

    If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**

### <a name="transform-the-transaction-types"></a>Převod typů transakcí
Šablona odhadů výdajů projektu (PSA do Fin and Ops) má podmíněný sloupec přidaný k převodu typů transakcí přijatých z Project Service Automation během integrace
- Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec. Ve formuláři filtrování a rozšířeném dotazu vyberte **Přidat podmíněný sloupec**. Zadejte název sloupce, například TransactionType. Zadaná podmínka je následující: If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapování šablony](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)





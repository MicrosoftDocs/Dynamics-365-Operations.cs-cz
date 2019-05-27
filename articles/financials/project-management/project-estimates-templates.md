---
title: Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556545"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace odhadů projektu přímo z Project Service Automation do aplikace Finance and Operations.

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.
> - Integrace skutečných hodnot je k dispozici v Microsoft Dynamics 365 for Finance and Operations verze 8.0.1 nebo pozdější.
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o odhadech projektových hodin a výdajů z aplikace Project Service Automation do Finance and Operations.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Odhady hodin projektů

### <a name="template-and-tasks"></a>Šablona a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci odhadů projektových hodin z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Odhady projektových hodin (PSA do Fin and Ops)
- **Název úkolů v projektu:**

    - Vztahy transakce
    - Odhady výdajů

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Projektové úkoly              | Entita integrace pro odhady hodin projektu |

### <a name="entity-flow"></a>Tok entity

Odhady projektových hodin jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových hodin.

### <a name="prerequisites"></a>Požadavky

Než dojde k synchronizaci odhadů projektových hodin, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

### <a name="power-query"></a>Power Query

V šabloně odhadů hodin projektu je nutné použít Microsoft Power Query pro Excel za účelem dokončení těchto úkolů:

- Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.
- Filtrování libovolných záznamů specifických pro zdroj v úkolu, který neumožní integraci do prognóz hodin.
- Filtrování prázdných řádků kategorie transakce. Když nedokončíte tento úkol, může to způsobit chybné hodinové prognózy.

#### <a name="set-the-default-forecast-model-id"></a>Nastavení výchozího ID modelu prognózy

Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, klikněte na šipku **Mapa** a otevřete mapování. Poté zvolte odkaz na **Filtrování a rozšířený dotaz**.

- Pokud použijete výchozí šablonu odhadu hodin Microsoft Project (PSA do Fin and Ops), vyberte **Vložená podmínka** v seznamu **Použité kroky**. V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací. Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.
- Při vytváření nové šablony je nutné přidat tento sloupec. V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**. Zadejte podmínku pro sloupec, kde pokud úloha projektu není null, pak \<enter the forecast model ID\> má jinou hodnotu než null.

#### <a name="filter-out-resource-specific-records"></a>Filtrování záznamů specifických pro zdroj

Šablona odhadu hodin projektu odhadů (PSA do Fin and Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro zdroj. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr. Zvolte odkaz **Filtrování a rozšířený dotaz** pro filtrování na sloupci **msdyn\_islinetask**, aby byly zahrnuty pouze záznamy **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrování prázdných řádků kategorie transakce

Je nutné přidat filtr k odstranění všech řádků s prázdnými kategoriemi transakce. Tento úkol je povinný, bez ohledu na to, jestli používáte výchozí šablonu nebo vytváříte vlastní šablonu. Tento filtr odebere všechny souhrnné řádky pocházející z Project Service Automation, které by mohly způsobit, že prognózy hodin v Finance and Operations budou nesprávné. Zvolte odkaz **Filtrování a rozšířený dotaz** pro odfiltrování nulových záznamů ve sloupci **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Odhady výdajů projektu

### <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci odhadů projektových výdajů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Odhady projektových výdajů (PSA do Fin and Ops)
- **Název úkolů v projektu:**

    - Vztahy transakce 
    - Odhady výdajů

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Připojení transakce    | Entita integrace pro vztahy transakce projektu |
| Řádky odhadu             | Entita integrace pro odhady nákladu projektu         |

### <a name="entity-flow"></a>Tok entity

Odhady projektových výdajů jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako prognózy projektových výdajů.

### <a name="prerequisites"></a>Požadavky

Než dojde k synchronizaci odhadů projektových výdajů, je nutné synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

### <a name="power-query"></a>Power Query

Je nutné použít Power Query v šabloně odhadů výdajů projektu pro dokončení následujících úkolů:

- Filtrování, aby byly zahrnuty pouze záznamy řádku odhadu výdajů.
- Nastavení výchozího ID modelu prognózy, které se použije, když integrace vytvoří nové prognózy hodin.
- Převod typu účtování.
- Převod typů transakcí.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrování, aby byly zahrnuty pouze řádky odhadu výdajů

Šablona odhadů výdajů projektu (PSA do Fin and Ops) má výchozí filtr, který zahrnuje pouze řádky výdajů v integraci. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr. Vyberte úlohu **Vztah transakcí** a klikněte na šipku **Mapa** pro otevření mapování. Zvolte odkaz na **Filtrování a rozšířený dotaz**. Vyfiltrujte sloupec **msdyn\_transactiontype1**, aby obsahoval pouze **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Nastavení výchozího ID modelu prognózy

Chcete-li aktualizovat výchozí ID modelu prognózy v šabloně, pro úlohu **Odhady výdajů** a poté klikněte na šipku **Mapa** a otevřete mapování. Zvolte odkaz na **Filtrování a rozšířený dotaz**.

- Pokud použijete výchozí šablonu odhadu výdajů projektu (PSA do Fin and Ops), vyberte nejdříve v Power Query možnost **Vložená podmínka** v části **Použité kroky**. V zadání **Funkce** nahraďte **O\_forecast** názvem ID modelu prognózy, které má být použito s integrací. Výchozí šablona obsahuje ID modelu prognózy z ukázkových dat.
- Při vytváření nové šablony je nutné přidat tento sloupec. V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**. Zadejte podmínku pro sloupec, kde pokud ID řádku odhadu není null, pak \<enter the forecast model ID\>; jinou hodnotu než null.

#### <a name="transform-the-billing-types"></a>Převod typu účtování

Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů účtování přijatých z Project Service Automation během integrace Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec. Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**. Zadejte název pro nový sloupec, jako je například **BillingType**. Poté zadejte následující podmínku:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Převod typů transakcí

Šablona odhadů výdajů projektu (PSA do Fin and Ops) obsahuje podmíněný sloupec použitý k převodu typů transakcí přijatých z Project Service Automation během integrace Pokud vytvoříte vlastní šablony, je nutné přidat tento podmíněný sloupec. Zvolte odkaz **Filtrování a rozšířený dotaz** a pak vyberte **Přidat podmíněný sloupec**. Zadejte název pro nový sloupec, jako je například **TransactionType**. Poté zadejte následující podmínku:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapování šablony](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)

---
title: Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838360"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation.

> [!NOTE]
> - Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.
> - Integrace skutečných hodnot je k dispozici v Microsoft Dynamics 365 for Finance and Operations verze 8.0.1 nebo pozdější.
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation a Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o kategoriích transakcí projektových výdajů mezi aplikacemi Project Service Automation a Finance and Operations.

Pokud jsou kategorie výdajů projektu řízeny v Finance and Operations, tok integrace je nejdříve z Finance and Operations do Project Service Automation. ID integrace kategorií výdajů projektu se poté aktualizují pomocí synchronizace z Project Service Automation do Finance and Operations.

Pokud jsou kategorie výdajů projektu řízeny v Project Service Automation, tok integrace je nejdříve z Prroject Service Automation do Finance and Operations. Kategorie projektu musí být již nakonfigurována v aplikaci Finance and Operations před synchronizací z Project Service Automation. Poté se synchronizuje z Finance and Operations zpět do Project Service Automation a poté znovu z Project Service Automation do Finance and Operations. Tímto způsobem pomůžete zajistit, aby byly kategorie propojeny a aby nebyly vytvořeny žádné duplicity.

> [!NOTE]
> Obvykle jsou kategorie výdajů projektu řízeny v aplikaci Finance and Operations. Pokud však nejsou v aplikaci Finance and Operations řízeny nebo pokud byly v aplikaci Project Service Automation vytvořeny kategorie výdajů, musíte nejprve synchronizovat pomocí šablony kategorií transakcí nákladů projektu (PSA do Fin and Ops). Poté synchronizujte pomocí šablony kategorií transakcí projektových výdajů (Fin and Ops do PSA). Poté spusťte synchronizaci z Project Service Automation do Finance and Operations ještě jednou.
>
> Pokud synchronizujete nejprve z Project Service Automation, musí být splněny následujíc požadavky v Finance and Operations před spuštěním synchronizace:
>
> - Musí existovat sdílená kategorie, která odpovídá nastavené kategorii projektu v aplikaci Project Service Automation, a musí být povolena pro obě položky **Projekt** a **Výdaje**.
> - Pro každou právnickou osobu Finance and Operations, se kterou je třeba integrovat, musí existovat následující kategorie projektu:
>
>     - **Kategorie projektu** existuje. 
>     - **Použít ve výdajích** je povoleno.
>     - **Aktivní v denících** je povoleno.
>     - **Typ transakce** je nastaven na **Výdaje**.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Synchronizace kategorie projektových výdajů z Finance and Operations do Project Service Automation

### <a name="template-and-task"></a>Šablona a úkol

Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci kategorií projektových výdajů z aplikace Finance and Operations do aplikace Project Service Automation slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (Fin and Ops do PSA)
- **Název úkolu v projektu:** Synchronizace kategorií do PSA

### <a name="entity-set"></a>Sada entit

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Entita integrace pro kategorie | Kategorie transakcí     |

### <a name="entity-flow"></a>Tok entity

Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.

### <a name="power-query"></a>Power Query

Musíte použít Microsoft Power Query pro Excel pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation. Šablona kategorie transakce výdajů projektu (Fin and Ops do PSA) poskytuje výchozí sloupec a mapování. Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupe v Power Query. Postupujte následovně.

1. Kliknutím na šipku otevřete mapování úlohy kategorie výdajů projektu v šabloně kategorií transakcí výdajů projektu (Fin and Ops do PSA).
2. Klikněte na odkaz **Filtrování a rozšířený dotaz** pro otevření Power Query.
2. Vyberte **Přidat podmíněný sloupec**.
3. Zadejte název pro nový sloupec, jako je například **BillingType**.
4. Zadejte následující podmínku: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klikněte na **OK** na sloupci.
6. Ujistěte se, že mapujete tento nový sloupec na stránce mapování.

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance and Operations do Project Service Automation.

[![Mapování šablony](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Synchronizace kategorie projektových výdajů z Project Service Automation do Finance and Operations

### <a name="template-and-task"></a>Šablona a úkol

K synchronizaci kategorií projektových výdajů z aplikace Project Service Automation do Finance and Operations slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (PSA do Fin and Ops)
- **Název úkolu v projektu:** Synchronizace kategorií do Fin Ops

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Kategorie transakcí     | Entita integrace pro kategorie |

### <a name="entity-flow"></a>Tok entity

Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí. Synchronizace zpět do Finance and Operations aktualizuje kategorie projektu v aplikaci Finance and Operations s ID integrace z aplikace Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

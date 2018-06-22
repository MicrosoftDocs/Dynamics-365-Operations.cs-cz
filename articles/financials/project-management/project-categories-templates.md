---
title: "Synchronizace kategorií nákladů projektu z Project Service Automation"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kategorií projektových nákladů mezi Microsoft Dynamics 365 for for Finance and Operations a Dynamics 365 for Project Service Automation."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci kategorií projektových nákladů mezi Microsoft Dynamics 365 for for Finance and Operations a Dynamics 365 for Project Service Automation.

> [!NOTE]
> Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation a Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o kategoriích transakcí projektových výdajů mezi aplikacemi Project Service Automation a Finance and Operations.

Pokud jsou kategorie výdajů projektu řízeny v aplikaci Finance and Operations, tok integrace je nejprve z Finance and Operations do Project Service Automation, a poté se aktualizují ID integrace kategorií projektových výdajů synchronizací z Project Service Automation do Finance and Operations.

Pokud jsou kategorie výdajů projektu řízeny v Project Service Automation, tok integrace je nejdříve z Prroject Service Automation do Finance and Operations. Kategorie projektu musí být již nakonfigurována v aplikaci Finance and Operations před synchronizací z Project Service Automation. Poté se synchronizuje z Finance and Operations zpět do Project Service Automation a poté znovu z Project Service Automation do Finance and Operations. Tím zajistíte, že jsou kategorie propojeny a nejsou vytvořeny duplicitní položky.

> [!NOTE]
> Obvykle budou kategorie výdajů projektu řízeny v aplikaci Finance and Operations. Pokud se nejedná o tuto situaci nebo již máte kategorie výdajů vytvořeny v Project Service Automation, musíte nejprve synchronizovat pomocí kategorií transakcí výdajů projektu (PSA do Fin and Ops) a poté synchronizovat pomocí kategorií transakce výdajů projektu (Fin and OPS do PSA). Pak spusťte synchronizaci z PSA do Fin and Ops ještě jednou.

> Při synchronizaci nejprve z Project Service Automation musí být již kategorie projektu nastaveny v aplikaci Finance and Operations a všechny projektové kategorie, které musí být synchronizovány s kategoriemi transakcí Project Service Automation musí být nastaveny tak, aby byly **Aktivní v denících**.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci kategorií projektových výdajů z aplikace Finance and Operations do aplikace Project Service Automation slouží následující šablona a základní úkol:

-  **Název šablony v integraci dat:** Kategorie transakcí projektových výdajů (Fin and Ops do PSA)
-  **Název úkolu v projektu:** Synchronizace kategorií do PSA

## <a name="entity-set"></a>Sada entit

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Entita integrace pro kategorie    | Kategorie transakcí        |

## <a name="entity-flow"></a>Tok entity

Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí.

## <a name="power-query"></a>Power Query

Musíte použít Microsoft Power Query pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation. Šablona kategorie transakce výdajů projektu (Fin and Ops do PSA) má výchozí sloupec a mapování je již zadáno. Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupe v Power Query.
- Otevřete formulář filtrování a rozšířeného dotazu z mapování úkolu kategorie výdajů projektu.
- Vyberte **Přidat podmíněný sloupec**.
- Zadejte nový název sloupce, například BillingType.
- Zadejte následující podmínku: pokud **CATEGORYID se nerovná null, pak 19235001, jinak null**.
- Klikněte na **OK** na sloupci.
- Ujistěte se, že mapujete tento nový sloupec na stránce mapování.

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance and Operations do Project Service Automation.

[![Mapování šablony](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

K synchronizaci kategorií projektových výdajů z aplikace Project Service Automation do aplikace inance and Operations slouží následující šablona a základní úkol:

-**Název šablony v integraci dat:** Kategorie transakcí výdajů projektu (PSA do Fin and Ops) -**Název úkolu v projektu:** Synchronizace kategorií do Fin and Ops

## <a name="entity-set"></a>Sada entit

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Kategorie transakcí          | Entita integrace pro kategorie  | 

## <a name="entity-flow"></a>Tok entity

Kategorie projektových výdajů jsou spravovány v Finance and Operations a jsou synchronizovány do Project Service Automation jako kategorie transakcí. Synchronizace zpět do Finance and Operations aktualizuje ID integrace Project Service Automation na kategorie projektu Finance and Operations.

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


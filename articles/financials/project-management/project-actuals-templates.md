---
title: "Synchronizace skutečných hodnot projektu z Project Service Automation přímo do deníku integrace projektu pro zaúčtování v aplikaci Finance and Operations."
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skutečných hodnot projektu přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronizace skutečných hodnot projektu z Project Service Automation přímo do deníku integrace projektu pro zaúčtování v aplikaci Finance and Operations.

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skutečných hodnot projektu přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations.

Šablona synchronizuje transakce z Project Service Automation do tabulek fázování v Finance and Operations. Po dokončení synchronizace je nutné importovat z tabulky fázování do deníku integrace.

> [!NOTE]
> Integrace skutečných hodnot projektu je dostupná v aplikaci Dynamics 365 Finance and Operations, verze 8.01.

> [!NOTE]
> Pokud zadáváte částku DPH na čas nebo transakce výdajů v Project Service Automation, je nutné nainstalovat aktualizaci 7 Project Service Automation. Pokud není nainstalována, skutečné hodnoty daně nebudou propojeny k přidruženému času nebo skutečným výdajům a nebudou synchronizovány do aplikace Finance and Operations. Pro další informace kontaktujte podporu.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o skutečných hodnotách projektu z aplikace Project Service Automation do Finance and Operations.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci skutečných hodnot projektu z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:

-  **Název šablony v integraci dat:** Skutečné hodnoty projektu (PSA do Fin and Ops)

-  **Název úkolů v projektu:** 
    - Skutečné hodnoty 
    - TransactionConnections

## <a name="entity-set"></a>Sada entit

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Skutečné hodnoty                         | Entita integrace pro skutečné hodnoty projektu                      |
| Připojení transakce         | Entita integrace pro vztahy transakce projektu    |

## <a name="entity-flow"></a>Tok entity

Skutečné úkoly projektu jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations do deníku integrace projektu. Účetnictví bude použito na základě výchozí finanční dimenze a nastavení účtování.

## <a name="preconditions"></a>Předpoklady

Než dojde k synchronizaci skutečných hodnot, musíte nastavit parametry integrace Project Service Automation a synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

## <a name="power-query"></a>Power Query

Je nutné použít Microsoft Power Query v šabloně skutečných hodnot projektu pro:
- Transformaci **typu transakce** Project Service Automation na správný **typ transakce** v Finance and Operations. Šablona skutečných hodnot projektu (PSA do Fin and Ops) již má tuto transformaci definovánu.
- Transformaci **typu účtování** Project Service Automation na správný **typ účtování** v Finance and Operations. Šablona skutečných hodnot projektu (PSA do Fin and Ops) již má tuto transformaci definovánu. Typ účtování je pak namapován na **vlastnost řádku** podle konfigurace ve formuláři integrace Dynamics 365 for Project Service Automation.
- Filtrujte na konkrétní **Organizační jednotky zdroje**, které mají být synchronizovány s touto šablonou.
- Pokud budou **mezipodnikový čas a mezipodnikové skutečné výdaje** synchronizovány do Finance and Operations, musíte převést **organizační jednotku smlouvy** na správnou **právnickou osobu** v aplikaci Finance and Operations. Šablona skutečných hodnot projektu (PSA do Fin and Ops) má podmíněný sloupec definovaný podle ukázkových dat. Musíte aktualizovat poslední vložených podmíněný sloupec na správné právnické osoby. Pokud tak neučiníte, může dojít k integrační chybě nebo nesprávným skutečným transakcím importovaným do Finance and Operations.
- Pokud **mezipodnikový čas nebo mezipodnikové skutečné výdaje** nebudou synchronizovány do Finance and Operations, je nutné odstranit poslední vložený podmíněný sloupec z vaší šablony. Pokud tak neučiníte, může dojít k integrační chybě nebo nesprávným skutečným transakcím importovaným do Finance and Operations.

### <a name="contract-organizational-unit"></a>Organizační jednotka smlouvy
Chcete-li aktualizovat vložený podmíněný sloupec v šabloně, klikněte na šipku **Mapa** a otevřete mapování. Otevřete filtrování a rozšířený dotaz.
- Pokud použijete výchozí šablonu skutečných hodnot Microsoft Project (PSA do Fin and Ops), vyberte **Vložená podmínka** v části **Použité kroky**. V zadání **Funkce** nahraďte **USSI** názvem **právnické osoby**, která má být použita s integrací. Přidejte další podmínky podle potřeby do zadání **Funkce** a aktualizujte podmínku **jiné** z **USMF** na správnou **právnickou osobu**.
- Při vytváření nové šablony je nutné přidat tento sloupec k podpoře mezipodnikových času a nákladů. Vyberte **Přidat podmíněný sloupec** a přiřaďte název sloupce, například LegalEntity. Zadejte podmínku pro sloupec, kde pokud msdyn_contractorganizationalunitid.msdyn_name je <organizational unit>, pak <enter the Legal entity>; jiné než null.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapování šablony](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Import z tabulky fázování

Import z periodického procesu tabulky fázování musí být spuštěn po synchronizaci skutečných hodnot z Project Service Automation to Finance and Operations. Tento proces bude importovat transakce projektu z tabulky fázování do deníku integrace Project Service Automation, kde se používá účetnictví a importované transakce lze zaúčtovat. Doporučujeme spustit tento proces v dávkovém režimu a volitelně lze nastavit tak, aby byl spouštěn jako opakovaná dávka.

## <a name="update-actuals"></a>Aktualizace skutečných hodnot

K synchronizaci čísla dokladu a DPH pro zaúčtované transakce projektu z aplikace Finance and Operations do aplikace Project Service Automation slouží následující šablona a základní úkoly:

-  **Název šablony v integraci dat:** Aktualizace skutečných hodnot projektu (Fin and Ops do PSA)
-  **Název úkolů v projektu:** 
     - Skutečné hodnoty 
     - TransactionConnections

## <a name="entity-set"></a>Sada entit

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Entita integrace pro skutečné hodnoty projektu                         | Skutečné hodnoty                           |
| Entita integrace pro vztahy transakce projektu       | Připojení transakce           |

## <a name="entity-flow"></a>Tok entity

Skutečné úkoly projektu jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations do deníku integrace projektu. Po zaúčtování v aplikaci Finance and Operations se skutečné hodnoty aktualizují v Project Service Automation s číslem dokladu z Finance and Operations. Pokud DPH bylo přidáno do Finance and Operations, vytvoří se v Project Service Automation nové skutečné hodnoty DPH.

## <a name="power-query"></a>Power Query

Je nutné použít Microsoft Power Query v šabloně aktualizace skutečných hodnot projektu pro:
- Transformaci **typu transakce** Finance and Operations na správný **typ transakce** v Project Service Automation. Šablona aktualizace skutečných hodnot projektu (Fin and Ops do PSA) již má tuto transformaci definovánu.
- Transformaci **typu účtování** Finance and Operations na správný **typ účtování** v Project Service Automation. Šablona aktualizace skutečných hodnot projektu (Fin and Ops do PSA) již má tuto transformaci definovánu.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance and Operations do Project Service Automation.

[![Mapování šablony](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapování šablony](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)





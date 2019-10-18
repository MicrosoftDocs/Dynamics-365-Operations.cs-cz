---
title: Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu pro zaúčtování v aplikaci Finance and Operations.
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektů přímo z Microsoft Dynamics 365 Project Service Automation do Finance and Operations.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250523"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu pro zaúčtování v aplikaci Finance and Operations.

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektů přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

Šablona synchronizuje transakce z Project Service Automation do tabulek fázování ve Finance. Po dokončení synchronizace **je nutné** importovat z tabulky fázování do deníku integrace.

> [!NOTE]
> - Integrace skutečných hodnot projektu je k dispozici od verze 8.0.1.
> - Pokud používáte Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.
> - Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, aby byly tyto poplatky zahrnuty ve faktuře projektu.
> - Pokud zadáváte částku DPH na čas nebo transakce výdajů v Project Service Automation, je nutné nainstalovat Project Service Automation Update 7. V opačném případě skutečné hodnoty daně nebudou propojeny k přidruženému času nebo skutečným výdajům a nebudou synchronizovány do aplikace Finance. Pro další informace kontaktujte podporu.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok dat pro Project Service Automation a aplikaci Finance

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation a Finance. Šablony integrace, které jsou k dispozici s funkcí integrace dat, umožňují tok dat o skutečných hodnotách projektu z aplikace Project Service Automation do Finance.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Skutečné hodnoty projektu z Project Service Automation

### <a name="template-and-tasks"></a>Šablona a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci projektových skutečných hodnot z aplikace Project Service Automation do aplikace Finance slouží následující šablona a základní úkol:

- **Název šablony v integraci dat:** Skutečné hodnoty projektu (PSA do Fin and Ops)
- **Název úkolů v projektu:**

    - Skutečné hodnoty
    - TransactionConnections

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Skutečné hodnoty                    | Entita integrace pro skutečné hodnoty projektu                   |
| Připojení transakce    | Entita integrace pro vztahy transakce projektu |

### <a name="entity-flow"></a>Tok entity

Skutečné úkoly projektu jsou spravovány v Project Service Automation a jsou synchronizovány do deníku integrace projektu v aplikaci Finance. Účetnictví bude použito na základě výchozí finanční dimenze a nastavení účtování.

### <a name="prerequisites"></a>Požadavky

Než dojde k synchronizaci skutečných hodnot, musíte nastavit parametry integrace Project Service Automation a synchronizovat projekty, úlohy projektu a kategorie transakce výdajů projektu.

### <a name="power-query"></a>Power Query

V šabloně skutečných hodnot projektu je nutné použít Microsoft Power Query pro Excel za účelem dokončení těchto úkolů:

- Transformaci typu transakce v Project Service Automation na správný typ transakce v Finance. V šabloně skutečných hodnot projektu (PSA do Fin and Ops) je již tato transformace definována.
- Transformaci typu účtování v Project Service Automation na správný typ účtování v Finance. V šabloně skutečných hodnot projektu (PSA do Fin and Ops) je již tato transformace definována. Typ účtování je pak namapován na vlastnost řádku podle konfigurace na stránce **Parametry integrace Project Service Automation**.
- Filtrujte na konkrétní organizační jednotky zdroje, které musí být synchronizovány s touto šablonou.
- Pokud budou mezipodnikový čas a mezipodnikové skutečné výdaje synchronizovány do Finance, musíte převést organizační jednotku smlouvy na správnou právnickou osobu v aplikaci Finance. V šabloně skutečných hodnot projektu (PSA do Fin and Ops) je podmíněný sloupec definovaný podle ukázkových dat. Musíte aktualizovat poslední vložený podmíněný sloupec na správné právnické osoby. V opačném případě může dojít k integrační chybě nebo mohou být importovány nesprávné skutečné transakce do Finance.
- Pokud mezipodnikový čas nebo mezipodnikové skutečné výdaje nebudou synchronizovány do Finance, je nutné odstranit poslední vložený podmíněný sloupec z vaší šablony. V opačném případě může dojít k integrační chybě nebo mohou být importovány nesprávné skutečné transakce do Finance.

#### <a name="contract-organizational-unit"></a>Organizační jednotka smlouvy
Chcete-li aktualizovat vložený podmíněný sloupec v šabloně, klikněte na šipku **Mapa** a otevřete mapování. Zvolte odkaz **Filtrování a rozšířený dotaz** pro otevření Power Query.

- Pokud použijete výchozí šablonu skutečných hodnot Microsoft Project (PSA do Fin and Ops), vyberte v Power Query **Vložená podmínka** z části **Použité kroky**. V zadání **Funkce** nahraďte **USSI** názvem právnické osoby, která má být použita s integrací. Přidejte další podmínky podle potřeby do zadání **Funkce** a aktualizujte podmínku **else** z **USMF** na správnou právnickou osobu.
- Při vytváření nové šablony je nutné přidat sloupec k podpoře mezipodnikových času a nákladů. Vyberte **Přidat podmíněný sloupec** a zadejte název sloupce, například **LegalEntity**. Zadejte podmínku pro sloupec, kde if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.

### <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujících obrázcích je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.

[![Mapování šablony](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapování šablony](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Import z tabulky fázování po integraci z Project Service Automation

Import z periodického procesu tabulky fázování musí být spuštěn po synchronizaci skutečných hodnot z Project Service Automation to Finance. Tento proces bude importovat transakce projektu z tabulky fázování do deníku integrace Project Service Automation, kde se používá účetnictví a importované transakce lze zaúčtovat. Doporučujeme spustit tento proces v dávkovém režimu a volitelně ho lze nastavit tak, aby byl spouštěn jako opakovaná dávka.

## <a name="update-actuals-from-finance"></a>Aktualizace skutečných hodnoty z aplikace Finance

### <a name="template-and-tasks"></a>Šablona a úkoly

K synchronizaci čísla dokladu a DPH pro zaúčtované transakce projektu z aplikace Finance do aplikace Project Service Automation slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Aktualizace skutečných hodnot projektu (Fin and Ops do PSA)
- **Název úkolů v projektu:**

    - Skutečné hodnoty 
    - TransactionConnections

### <a name="entity-set"></a>Sada entit

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entita integrace pro skutečné hodnoty projektu                   | Skutečné hodnoty                    |
| Entita integrace pro vztahy transakce projektu | Připojení transakce    |

### <a name="entity-flow"></a>Tok entity

Skutečné úkoly projektu jsou spravovány v Project Service Automation a jsou synchronizovány do deníku integrace projektu v aplikaci Finance. Po zaúčtování skutečných hodnot v aplikaci Finance se skutečné hodnoty aktualizují v Project Service Automation s číslem dokladu z Finance. Pokud DPH bylo přidáno do Finance, vytvoří se v Project Service Automation nové skutečné hodnoty daně.

### <a name="power-query"></a>Power Query

V šabloně aktualizace skutečných hodnot projektu je nutné použít Power Query za účelem dokončení těchto úkolů:

- Transformaci typu transakce ve Finance na správný typ transakce Project Service Automation. V šabloně aktualizace skutečných hodnot projektu (Fin Ops do PSA) je již tato transformace definována.
- Transformaci typu účtování ve Finance na správný typ účtování v Project Service Automation. V šabloně aktualizace skutečných hodnot projektu (Fin Ops do PSA) je již tato transformace definována.

### <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Finance do Project Service Automation.

[![Mapování šablony](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapování šablony](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)

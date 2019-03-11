---
title: Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "312501"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synchronizace seznamu projektů z aplikace Finance and Operations do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy slouží ke spuštění synchronizace projektů z Microsoft Dynamics 365 for Finance and Operations k Microsoft Dynamics 365 for Field Service.

**Šablona v integraci dat**
- Projekty (z aplikace Finance and Operations do služby Field Service)

**Úkol v projektu integrace dat**
- Projekty

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:
- Účty (Sales do aplikace Finance and Operations) 

## <a name="entity-set"></a>Sada entit
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekty                |

## <a name="entity-flow"></a>Tok entity
Projekty jsou vytvářeny v aplikaci Finance and Operations. Projekty s **typem projektu** nastaveným na **Čas a materiál** a **fází projektu** nastavenou na **probíhá** bude synchronizován s entitou **Externí projekt** entity ve službě Field Service, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele. Seznam **Externí projekt** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Finance and Operations.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Entita **Externí projekt** získá všechny projekty z aplikace Finance and Operations. Pole **Externí projekt** bylo přidáno do entity **pracovního příkazu**. Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem. Po změně pole **Stav systému** na **Otevřít – Probíhá (690,970,000)** na vyšší status se pole **Externí projekt** uzamkne a nebude dále možné přidávat, odebírat ani měnit jeho hodnotu.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů
### <a name="finance-and-operations"></a>Finance and Operations
Povolte sledování změn pro projekty datové entity.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekty (z aplikace Finance and Operations do služby Field Service): projekty

[![Mapování šablony v integraci dat](./media/FSProject1.png)](./media/FSProject1.png)

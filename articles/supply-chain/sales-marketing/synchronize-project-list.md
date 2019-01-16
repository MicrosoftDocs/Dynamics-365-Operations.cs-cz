---
title: "Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.

**Název šablony v integraci dat:**
- Projekty (z aplikace Finance and Operations do služby Field Service)

**Názvy úkolů v projektu integrace dat:**
- Projekty

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:
- Účty (Sales do aplikace Finance and Operations) 

## <a name="entity-set"></a>Sada entit
Služba Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekty                |

## <a name="entity-flow"></a>Tok entity
Projekty jsou vytvářeny v aplikaci Finance and Operations. Probíhající projekty s **typem projektu** časem a materiálem a **fází projektu** se synchronizují do **externích projektů** entity ve službě Field Serivce, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele. Seznam **externích projektů** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Finance and Operations.
Řešení CRM služby Field Service Externí projekt je nová entita, která získá všechny projekty z operací.
Pole Externí projekt bylo přidáno do entity pracovního příkazu. Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci operací propojena s projektem. Jakmile se stav systému změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole externích projektů se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů
### <a name="in-finance-and-operations"></a>V aplikaci Finance and Operations
Povolit sledování změn pro projekty datové entity.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekty (z aplikace Finance and Operations do služby Field Service): projekty

[![Mapování šablony v integraci dat](./media/FSProject1.png)](./media/FSProject1.png)


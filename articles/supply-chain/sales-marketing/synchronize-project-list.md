---
title: Synchronizace seznamu projektů z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 920c3741ab45f4ae88ea5febba583d34b5a1230cd25316226db850730927798d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717836"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Synchronizace seznamu projektů z aplikace Supply Chain Management do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy se používají ke spuštění synchronizace projektů ze Supply Chain Management do Field Service.

**Šablona v integraci dat**
- Projekty (z aplikace Supply Chain Management do služby Field Service)

**Úkol v projektu integrace dat**
- Projekty

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:
- Obchodní vztahy (Sales do Supply Chain Management) 

## <a name="entity-set"></a>Sada entit
| Field Service           | Správa dodavatelsko-odběratelského řetězce  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekty                |

## <a name="entity-flow"></a>Tok entity
Projekty se vytvářejí v Supply Chain Management. Projekty s **typem projektu** nastaveným na **Čas a materiál** a **fází projektu** nastavenou na **probíhá** bude synchronizován s entitou **Externí projekt** entity ve službě Field Service, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele. Seznam **Externí projekt** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Supply Chain Management.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Entita **Externí projekt** získá všechny projekty z aplikace Supply Chain Management. Pole **Externí projekt** bylo přidáno do entity **pracovního příkazu**. Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Supply Chain Management propojena s projektem. Po změně pole **Stav systému** na **Otevřít – Probíhá (690,970,000)** na vyšší status se pole **Externí projekt** uzamkne a nebude dále možné přidávat, odebírat ani měnit jeho hodnotu.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů
### <a name="supply-chain-management"></a>Správa dodavatelsko-odběratelského řetězce
Povolte sledování změn pro projekty datové entity.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projekty (z aplikace Supply Chain Management do služby Field Service): Projekty

[![Mapování šablony v integraci dat.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
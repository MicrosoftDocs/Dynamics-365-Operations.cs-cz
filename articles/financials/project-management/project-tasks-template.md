---
title: "Synchronizace projektových úloh přímo z Project Service Automation do aplikace Finance and Operations."
description: "Toto téma popisuje šablonu a základní úlohu, které se používají k synchronizaci projektových úkolů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace projektových úloh přímo z Project Service Automation do aplikace Finance and Operations.

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablonu a základní úlohu, které se používají k synchronizaci projektových úkolů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučili jsme nainstalovat též KB 4131710.
> - Integrace skutečných hodnot je dostupná v aplikaci Microsoft Dynamics 365 for Finance and Operations, verze 8.01 nebo novější.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablona integrace, která je k dispozici s funkcí integrace dat, umožňuje tok dat o úlohách projektu z aplikace Project Service Automation do Finance and Operations.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablona a úkol

Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci projektových úkolů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkol:

- **Název šablony v integraci dat:** Úlohy projektu (PSA do Fin and Ops)
- **Název úkolu v projektu:** Úlohy projektu

Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.

## <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| Projektové úkoly              | Entita integrace pro úlohu projektu |

## <a name="entity-flow"></a>Tok entity

Projektové úkoly jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako projektové aktivity.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.

## <a name="power-query"></a>Power Query

K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud je splněna tato podmínka:

- Máte záznamy specifické pro zdroj v úloze projektu.

Pokud musíte použít Power Query, postupujte podle těchto pokynů:

- Šablona projektového úkolu (PSA do Fin and Ops) má výchozí filtr, který vyloučí záznamy specifické pro zdroje z úkolu projektu nastavením filtru **IsLineTask** na **False** Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


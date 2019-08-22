---
title: Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843402"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Používaná šablona **Pracovní příkazy s projektem (Field Service do Fin and Ops)** je založena na šabloně **Pracovní příkazy (Field Service to Fin and Ops)**. Více informací naleznete v části [Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:
- **Pracovní příkazy s projektem (Field Service do Fin and Ops)**
- **Pracovní příkazy (Field Service do Fin and Ops)**

Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Finance and Operations zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace. Kromě toho šablona používá pokročilé dotazování a filtrování.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Pracovní příkazy s projektem (Field Service do Fin and Ops)

**Název úkolu v projektu integrace dat:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Pole **Externí projekt** bylo přidáno do entity pracovního příkazu. Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem. Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderHeader

[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderHeaderProject

[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderProduct

[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderService

[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)

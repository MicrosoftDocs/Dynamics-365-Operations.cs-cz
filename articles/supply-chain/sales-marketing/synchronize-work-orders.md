---
title: Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "329843"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Používaná šablona **Produkty Field Service (z aplikace Finance and Operations do služby Field Service)** je založena na šabloně **Produkty (z aplikace Finance and Operations do Sales) – Direct** z modulu Prospect to Cash. Další informace naleznete v tématu [Produkty (Finance and Operations do Sales) – přímé](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Finance and Operations do Field Service)** a je založeno na šabloně **Field Service (Finance and Operations do Sales) – přímé**.

Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Finance and Operations zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace. Kromě toho šablona používá pokročilé dotazování a filtrování.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Pracovní příkazy s projektem (Field Service do Finance and Operations)

**Název úkolu v projektu integrace dat:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Pole **Externí projekt** bylo přidáno do entity pracovního příkazu. Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem. Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderHeader

[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderHeaderProject

[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderProduct

[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderService

[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)

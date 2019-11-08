---
title: Synchronizace pracovních příkazů s projektem z aplikace Field Service do Supply Chain Management
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Dynamics 365 Field Service do prodejních objednávek v Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 5c57b8d1e09fd57611accec83ec3da4bc596fd00
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627544"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Synchronizace pracovních příkazů s projektem z aplikace Field Service do Supply Chain Management

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Dynamics 365 Field Service do prodejních objednávek v Dynamics 365 Supply Chain Management.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Používaná šablona **Pracovní příkazy s projektem (Field Service do Supply Chain Management)** je založena na šabloně **Pracovní příkazy (Field Service do Supply Chain Management)**. Více informací naleznete v části [Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:
- **Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management)**
- **Pracovní příkazy (Field Service do Supply Chain Management)**

Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Supply Chain Management zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace. Kromě toho šablona používá pokročilé dotazování a filtrování.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management)

**Název úkolu v projektu integrace dat:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Pole **Externí projekt** bylo přidáno do entity pracovního příkazu. Toto pole je vyhledávací hodnota určená k označení nákupu v pracovním příkazu s projektem, a prodejní objednávka pak bude v rámci aplikace Supply Chain Management propojena s projektem. Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderHeader

[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderHeaderProject

[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderProduct

[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderService

[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)

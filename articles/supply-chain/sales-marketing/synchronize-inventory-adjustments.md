---
title: Synchronizace převodů a úprav zásob ze služby Field Service do Supply Chain Management
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552226"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Synchronizace převodů a úprav zásob ze služby Field Service do Supply Chain Management

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy se používají k synchronizaci úprav skladů a převodů z Field Service do Supply Chain Management.

**šablony v integraci dat**
- Úprava produktu (z aplikace Field Service do Supply Chain Management)
- Převody zásob (z aplikace Field Service do Supply Chain Management)

**úkoly v projektech integrace dat**
- Množstevní úpravy zásob
- Převody zásob

## <a name="entity-set"></a>Sada entit
| Field Service                     | Správa dodavatelsko-odběratelského řetězce                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS záhlaví a řádky deníku úprav zásob |
| msdyn_inventoryadjustmentproducts | CDS záhlaví a řádky deníku převodu zásob   |

## <a name="entity-flow"></a>Tok entity
Úpravy zásob a převodů provedené ve službě Field Service se synchronizují s aplikací Supply Chain Management, poté, co se změní **stav zaúčtování** z hodnoty **vytvořeno** na **zaúčtováno**. V tomto případě se úprava nebo převodní příkaz uzamknou a budou jen pro čtení. To znamená, že úpravy převodů lze v aplikaci Supply Chain Management zaúčtovat, ale ne změnit. V aplikaci Supply Chain Management můžete nastavit dávkovou úlohu, aby automaticky zaúčtovala a úpravy a převedla deníky zásob generované při integraci. Další informace o tom, jak povolit dávkovou úlohu, naleznete v předpokladech níže.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM 
Pole **Jednotka zásob** bylo přidáno do entity **produkt**. Toto pole je třeba, jelikož jednotka prodeje a zásob není v aplikaci Supply Chain Management vždy stejná a skladová jednotka je potřeba pro skladové zásoby v aplikaci Supply Chain Management.
Při nastavování produktu v poli úprava zásob produktu pro úpravy zásob a převody zásob bude jednotka získána z hodnoty produktových zásob produktu. Pokud je hodnota nalezena, pole **Jednotka** bude v rámci úpravy zásob produktu zamčené.

Pole **Stav zaúčtování** bylo přidáno jak k entitě **Úprava zásob**, tak k entitě **Převod zásob**. Toto pole slouží jako filtr, když je úprava nebo převod odeslán do aplikace Supply Chain Management. Výchozí hodnota v tomto poli je Vytvořeno (1), není však odeslána do aplikace Supply Chain Management. Jakmile hodnotu aktualizujete na Zaúčtováno (2), je odeslána do aplikace Supply Chain Management, ale pak už nebude možné provádět úpravy, převod ani přidávat nové řádky.

Pole **Číselná řada** bylo přidáno do entity **Produkt úpravy zásob**. Toto pole zajišťuje, aby integrace měla jedinečné číslo, takže může vytvořit a aktualizovat úpravu. Při vytvoření prvního produktu úprav zásob dojde k vytvoření nového záznamu v entitě **P2C AutoNumber** za účelem zachování číselné řady a předpony, která se používá.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="supply-chain-management"></a>Správa dodavatelsko-odběratelského řetězce
Deníky zásob integrace generované integrací lze zaúčtovat automaticky pomocí dávkové úlohy. To můžete povolit zde: **Řízení zásob > Periodické úlohy > CDS integrace > Zaúčtovat skladové deníky integrace**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Úprava zásob (Field Service do Supply Chain Management): Úprava zásob

[![Mapování šablony v integraci dat](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Převod zásob (Field Service do Supply Chain Management): Převod zásob

[![Mapování šablony v integraci dat](./media/FSTrans1.png)](./media/FSTrans1.png)

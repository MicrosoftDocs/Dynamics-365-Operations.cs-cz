---
title: Synchronizujte převody zásob a množstevních úprav ze služby Field Service do aplikace Finance and Operations
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/14/2019
ms.locfileid: "842408"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synchronizujte množstevní úpravy zásob a ze služby Field Service do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablony a základní úkoly se používají k synchronizaci úprav zásob a převodů z Microsoft Dynamics 365 for Field Service do Microsoft Dynamics 365 for Finance and Operations.

**šablony v integraci dat**
- Úprava zásob (Field Service do Fin and Ops)
- Převody zásob (Field Service do Fin and Ops)

**úkoly v projektech integrace dat**
- Množstevní úpravy zásob
- Převody zásob

## <a name="entity-set"></a>Sada entit
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS záhlaví a řádky deníku úprav zásob |
| msdyn_inventoryadjustmentproducts | CDS záhlaví a řádky deníku převodu zásob   |

## <a name="entity-flow"></a>Tok entity
Úpravy zásob a převodů provedené ve službě Field Service se synchronizují s aplikací Finance and Operations, poté, co se změní **stav zaúčtování** z hodnoty **vytvořeno** na **zaúčtováno**. V tomto případě se úprava nebo převodní příkaz uzamknou a budou jen pro čtení. To znamená, že úpravy převodů lze v aplikaci Finance and Operations zaúčtovat, ale ne změnit. V aplikaci Finance and Operations můžete nastavit dávkovou úlohu, aby automaticky zaúčtovala a úpravy a převedla deníky zásob generované při integraci. Další informace o tom, jak povolit dávkovou úlohu, naleznete v předpokladech níže.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM 
Pole **Jednotka zásob** bylo přidáno do entity **produkt**. Toto pole je třeba, jelikož jednotka prodeje a zásob není v aplikaci Finance and Operations vždy stejná a skladová jednotka je potřeba pro skladové zásoby v aplikaci Finance and Operations.
Při nastavování produktu v poli úprava zásob produktu pro úpravy zásob a převody zásob bude jednotka získána z hodnoty produktových zásob produktu. Pokud je hodnota nalezena, pole **Jednotka** bude v rámci úpravy zásob produktu zamčené.

Pole **Stav zaúčtování** bylo přidáno jak k entitě **Úprava zásob**, tak k entitě **Převod zásob**. Toto pole slouží jako filtr, když je úprava nebo převod odeslán do aplikace Finance and Operations. Výchozí hodnota v tomto poli je Vytvořeno (1), není však odeslána do aplikace Finance and Operations. Jakmile hodnotu aktualizujete na Zaúčtováno (2), je odeslána do aplikace Finance and Operations, ale pak už nebude možné provádět úpravy, převod ani přidávat nové řádky.

Pole **Číselná řada** bylo přidáno do entity **Produkt úpravy zásob**. Toto pole zajišťuje, aby integrace měla jedinečné číslo, takže může vytvořit a aktualizovat úpravu. Při vytvoření prvního produktu úprav zásob dojde k vytvoření nového záznamu v entitě **P2C AutoNumber** za účelem zachování číselné řady a předpony, která se používá.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="finance-and-operations"></a>Finance and Operations
Deníky zásob integrace generované integrací lze zaúčtovat automaticky pomocí dávkové úlohy. To můžete povolit zde: **Řízení zásob > Periodické úlohy > CDS integrace > Zaúčtovat skladové deníky integrace**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Množstevní úpravy (Field Service do Fin and Ops): Množstevní úpravy

[![Mapování šablony v integraci dat](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Převod zásob (Field Service do Fin and Ops): převod zásob

[![Mapování šablony v integraci dat](./media/FSTrans1.png)](./media/FSTrans1.png)

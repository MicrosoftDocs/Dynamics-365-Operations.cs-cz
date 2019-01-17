---
title: "Synchronizujte převody zásob a množstevních úprav ze služby Field Service do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synchronizujte množstevní úpravy zásob a ze služby Field Service do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Field Service do aplikace Microsoft Dynamics 365 for Finance and Operations.

**Název šablon v integraci dat:**
- Množstevní úpravy zásob (ze služby Field Service do aplikace Finance and Operations)
- Převody zásob (ze služby Field Service do aplikace Finance and Operations)

**Názvy úkolů v projektech integrace dat:**
- Množstevní úpravy zásob
- Převody zásob

## <a name="entity-set"></a>Sada entit
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS záhlaví a řádky deníku úprav zásob |
| msdyn_inventoryadjustmentproducts | CDS záhlaví a řádky deníku převodu zásob   |

## <a name="entity-flow"></a>Tok entity
Úpravy zásob a převodů provedené ve službě Field Service se synchronizují s aplikací Finance and Operations, jakmile se změní **stav zaúčtování** z hodnoty vytvořeno na zaúčtováno. Když k tomu dojde, úprava nebo převodní příkaz budou uzamčeny a bude jen pro čtení, jelikož úpravy a převody mohou být zaúčtovány v aplikaci Finance and Operations, a proto je nelze měnit.
V aplikaci Finance and Operations můžete nastavit dávkovou úlohu, aby automaticky zaúčtovala a převedla deníky zásob generované s integrací. Další informace o tom, jak povolit tuto dávkovou úlohu, naleznete v předpokladu níže.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM 
Pole Jednotka zásob bylo přidáno do entity produktu. Toto pole je třeba, jelikož prodejní jednotka a jednotka zásob nejsou vždy v operacích totožné a pro skladové zásoby v operacích je zapotřebí jednotka zásob.
Při nastavování produktu v poli úprava zásob produktu pro úpravy zásob a převody zásob bude jednotka získána z hodnoty produktových zásob produktu. Pokud je hodnota nalezena, pole jednotky bude v rámci úpravy zásob produktu zamčené.

Pole Stav zaúčtování bylo přidáno jak k entitě úprav zásob, tak k entitě převodu zásob. Toto pole slouží jako filtr, když je úprava nebo převod odeslán do Operací. Pole je přednastaveno jako Vytvořené (1) a poté není odesláno do Operací. Jakmile pole změníte na Zaúčtováno (2), je odesláno do operací, ale už nebude možné provádět úpravy, převod ani přidávat nové řádky.
Pole Číselná řada bylo přidáno do entity úpravy zásob produktu. Toto pole umožňuje integraci mít jedinečné číslo, takže integrace pozná, kdy se vytvářet a kdy aktualizovat. Při vytvoření prvního produktu úprav zásob dojde k vytvoření nového záznamu v entitě P2C AutoNumber za účelem zachování číselné řady a předpony, která se používá.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="in-finance-and-operations"></a>V aplikaci Finance and Operations
Deníky zásob integrace generované integrací lze zaúčtovat automaticky pomocí dávkové úlohy. To můžete povolit zde: Řízení zásob > Periodické úlohy > CDS integrace > Zaúčtovat skladové deníky integrace

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Množstevní úpravy (služba Field Service do aplikace Finance and Operations): Množstevní úpravy

[![Mapování šablony v integraci dat](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Převod zásob (služba Field Service do aplikace Finance and Operations): převod zásob

[![Mapování šablony v integraci dat](./media/FSTrans1.png)](./media/FSTrans1.png)


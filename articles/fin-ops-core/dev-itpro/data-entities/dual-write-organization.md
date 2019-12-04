---
title: Organizační hierarchie v Common Data Service
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769653"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organizační hierarchie v Common Data Service

[!include [banner](../includes/banner.md)]

Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Common Data Service bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z aplikací Finance and Operations do Common Data Service.

![Obrázek architektury](media/dual-write-data-flow.png)

## <a name="templates"></a>Šablony

Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Common Data Service.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map entit pro synchronizaci produktů a souvisejících informací.

Finance and Operations | Jiné aplikace Dynamics 365 | Popis
-----------------------|--------------------------------|---
Účely organizační hierarchie | msdyn_internalorganizationhierarchypurposes | Tato šablona poskytuje jednosměrnou synchronizaci entity účelu hierarchie organizace.
Typ organizační hierarchie | msdyn_internalorganizationhierarchytypes | Tato šablona poskytuje jednosměrnou synchronizaci entity typu hierarchie organizace.
Organizační hierarchie - publikovaná | msdyn_internalorganizationhierarchies | Tato šablona poskytuje jednosměrnou synchronizaci entity publikované hierarchie organizace.
Provozní jednotka | msdyn_internalorganizations | 
Právnické osoby | msdyn_internalorganizations | 
Právnické osoby | cdm_companies | Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Interní organizace

Informace o interní organizaci v Common Data Service pocházejí ze dvou entit, **provozní jednotka** a **právnická osoba**.

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]


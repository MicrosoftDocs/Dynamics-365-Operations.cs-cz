---
title: Organizační hierarchie v Dataverse
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750805"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizační hierarchie v Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Dataverse, bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z aplikací Finance and Operations do Dataverse.

![Obrázek architektury](media/dual-write-data-flow.png)

Mapování tabulky organizační hierarchie je k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Dataverse.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365 | popis
-----------------------|--------------------------------|---
Účely organizační hierarchie | msdyn_internalorganizationhierarchypurposes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky účelu hierarchie organizace.
Typ organizační hierarchie | msdyn_internalorganizationhierarchytypes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky typu hierarchie organizace.
Organizační hierarchie - publikovaná | msdyn_internalorganizationhierarchies | Tato šablona poskytuje jednosměrnou synchronizaci tabulky publikované hierarchie organizace.
Provozní jednotka | msdyn_internalorganizations |
Právnické osoby | msdyn_internalorganizations |
Právnické osoby | cdm_companies | Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Interní organizace

Informace o interní organizaci v Dataverse pocházejí ze dvou tabulek, **provozní jednotka** a **právnická osoba**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572442"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organizační hierarchie v Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Common Data Service bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z aplikací Finance and Operations do Common Data Service.

![Obrázek architektury](media/dual-write-data-flow.png)

## <a name="templates"></a>Šablony

Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Interní účel hierarchie organizací

Tato šablona poskytuje jednosměrnou synchronizaci entity účel hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Typ interní organizační hierarchie

Tato šablona poskytuje jednosměrnou synchronizaci entity Typ hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.

<!-- ![architecture image](media/dual-write-type.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NÁZEV | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Interní organizační hierarchie

Tato šablona poskytuje jednosměrnou synchronizaci entity Publikovaná hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.

<!-- ![architecture image](media/dual-write-organization.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Interní organizace

Informace o interní organizaci v Common Data Service pocházejí ze dvou entit, **provozní jednotka** a **právnická osoba**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Provozní jednotka

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NÁZEV | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Právnická osoba

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NÁZEV | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
žádná | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Společnost

Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti) mezi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![architecture image](media/dual-write-company.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NÁZEV | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode

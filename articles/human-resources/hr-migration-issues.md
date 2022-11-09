---
title: Známé problémy při slučování infrastruktury Dynamics 365 Human Resources
description: Tento článek obsahuje seznam problémů, které mohou nastat během slučování infrastruktury Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733441"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Známé problémy při slučování infrastruktury Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Sdílená prostředí Dataverse

Rámec duálního zápisu nepodporuje propojení dvou prostředí finanční a provozní aplikace se stejným prostředím Dataverse. Pokud máte prostředí Dataverse, které je sdíleno s oběma následujícími položkami, musíte buď duplikovat prostředí Dataverse, nebo je rozdělit:

- Finanční a provozní aplikace
- Stávající prostředí lidských zdrojů

## <a name="environment-type-requirements"></a>Požadavky na typ prostředí

Před provedením migrace jsou vyžadovány následující typy prostředí:

- Pokud nemáte žádná samostatná prostředí sandbox, musíte je vytvořit, abyste ověřili migraci.
- Pokud máte více produkčních samostatných prostředí, jedno z nich lze migrovat. Obraťte se na podporu společnosti Microsoft a požádejte o povolení prostředí jako sandboxy.

## <a name="teams-integration"></a>Integrace Teams

Stávající aplikace Lidské zdroje v Teams se aktuálně přesouvá do řešení Microsoft Power Platform. Další informace viz [Aplikace Human Resources v Teams](hr-admin-teams-leave-app.md).

## <a name="licensing"></a>Licence

V licencování nejsou žádné změny Dynamics 365 Human Resources v následujících oblastech: 

- **Minimální počet požadavků na zakoupení licence**
- **Licence na produkční prostředí a prostředí sandbox** – Máte-li stávající samostatné licence pro lidské zdroje, které zahrnují jedno produkční prostředí a jedno prostředí sandbox, bude stejný počet licencí k dispozici pro finanční a provozní infrastrukturu.
- **Další licence sandboxu** – Pokud jste zakoupili další licence sandbox pro samostatnou aplikaci Human Resources, bude stejný počet licencí k dispozici pro prostředí sandbox na finanční a provozní infrastruktuře. 

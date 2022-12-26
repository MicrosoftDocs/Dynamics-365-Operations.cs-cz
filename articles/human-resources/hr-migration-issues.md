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
ms.openlocfilehash: 3fe21df8be010ace3070ad08ed95f3d3efc7b01d
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838548"
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

## <a name="dual-write-integration"></a>Integrace dvojitého zápisu

Duální zápis je předpřipravená infrastruktura poskytující interakci mezi aplikacemi pro zapojení zákazníků a finančními a provozními aplikacemi prakticky v reálném čase. Pokud vaše organizace používá integraci pomocí duálního zápisu, mohou se vás týkat některé známé problémy. Další informace o tabulkách Dataverse a problémech naleznete v části [Tabulky Dataverse](hr-developer-entities.md).


---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování v duálním zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683491"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Věrnostní karty a odměny zákazníka

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků. Například Dynamics 365 Commerce má infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách. Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují do Dataverse, aplikace pro zapojení zákazníka mohou tato data použít. Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.

## <a name="templates"></a>Šablony

| Aplikace Finance and Operations | Modelem řízené aplikace v Dynamics 365 | popis |
|-----------------------------|-----------------------------------|-------------|
| Věrnostní karta                | msdyn\_loyaltycards               | Tato šablona synchronizuje informace o věrnostních kartách zákazníků. |
| Body věrnostní odměny       | msdyn\_loyaltyrewardpoints        | Tato šablona synchronizuje informace o bodech odměn zákazníků. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
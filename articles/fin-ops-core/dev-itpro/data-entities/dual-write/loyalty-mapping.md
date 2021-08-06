---
title: Věrnostní karty a odměny zákazníka
description: Tohle téma popisuje integraci údajů o věrnostních kartách odběratelů a bodů odměňování v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d70fc6fea0e4e4e8f4ad73de5699b6b3fd481613
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542606"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Věrnostní karty a odměny zákazníka

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Podniky klasifikují zákazníky a poskytující sofistikované služby na základě vzorců nakupování a utrácení zákazníků. Například Dynamics 365 Commerce má infrastrukturu a funkce pro podporu a zpracování věrnostních karety zákazníků, bodů odměny, věrnostních cen a nákupů založených na cenách. Když se data o věrnostních kartách zákazníků a body odměny v Commerce synchronizují do Dataverse, aplikace pro zapojení zákazníka mohou tato data použít. Například uživatelé Dynamics 365 Customer Service mohou pomocí těchto dat poskytovat stejně propracované služby prostřednictvím technické podpory.

## <a name="templates"></a>Šablony

Aplikace Finance and Operations | Aplikace Customer Engagement     | popis
|-----------------------------|-----------------------------------|-------------|
[Věrnostní karta](mapping-reference.md#149) | msdyn_loyaltycards | Tato šablona synchronizuje informace o věrnostních kartách zákazníků. |
[Úrovně věrnosti](mapping-reference.md#226) | msdyn_loyaltylevels | Tato šablona synchronizuje informace o bodech odměn zákazníků. |
[Body věrnostní odměny](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

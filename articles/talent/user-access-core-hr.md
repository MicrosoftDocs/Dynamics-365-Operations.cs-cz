---
title: Uživatel má přístup k aplikaci Core HR, ale nikoliv k aplikacím Onboard nebo Attract
description: Toto téma vysvětluje, jak vyřešit problém, kdy má uživatel přístup k aplikaci Dynamics 365 for Talent Core HR, nikoliv však k aplikacím Attract nebo Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517536"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Uživatel má přístup k Core HR, ale nikoliv k aplikacím Onboard nebo Attract

[!include [banner](includes/banner.md)]

**Podrobnosti o prostředí**

- Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.
- Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 for Talent Core HR.

**Výdej**

Uživatel B má přístup do Core HR, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard. Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.

**Řešení**

Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft PowerApps, které vytvořil uživatel A během procesu zřizování.

Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Dlouhodobé řešení**

Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Core HR.

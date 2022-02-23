---
title: Uživatel má přístup k Human Resources, ale nikoliv k aplikacím Onboard nebo Attract
description: Toto téma vysvětluje, jak vyřešit problém, kdy má uživatel přístup k aplikaci Microsoft Dynamics 365 Talent - Human Resources, nikoliv však k aplikacím Attract nebo Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460550"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Uživatel má přístup k Human Resources, ale nikoliv k aplikacím Onboard nebo Attract

[!include [banner](includes/banner.md)]

**Podrobnosti o prostředí**

- Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.
- Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 Human Resources.

**Vydání**

Uživatel B má přístup do Human Resources, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard. Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.

**Řešení**

Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft Power Apps, které vytvořil uživatel A během procesu zřizování.

Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Dlouhodobé řešení**

Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Human Resources.

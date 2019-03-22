---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/01/2019
ms.locfileid: "773199"
---
# <a name="workflow-system"></a>Systémový workflowu

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Oznámení

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Proč je při odmítnutí pracovní položky doručeno více oznámení?
Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá. Jiná pracovní položka je vytvořena a přiřazena původci. To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou. 

Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek. Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.

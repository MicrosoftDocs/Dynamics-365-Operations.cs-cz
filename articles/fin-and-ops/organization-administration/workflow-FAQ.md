---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509284"
---
# <a name="workflow-system"></a>Systémový workflowu

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Oznámení

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Proč je při odmítnutí pracovní položky doručeno více oznámení?
Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá. Jiná pracovní položka je vytvořena a přiřazena původci. To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou. 

Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek. Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.

### <a name="why-are-my-workflow-exports-failing"></a>Proč se nedaří exporty mých workflow?
V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků. Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru. Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

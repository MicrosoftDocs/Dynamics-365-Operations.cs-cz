---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/19/2019
ms.locfileid: "1688993"
---
# <a name="workflow-faq"></a>Workflow – Často kladené otázky

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Proč je při odmítnutí pracovní položky doručeno více oznámení?
Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá. Jiná pracovní položka je vytvořena a přiřazena původci. To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou. 

Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek. Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.

## <a name="why-are-my-workflow-exports-failing"></a>Proč se nedaří exporty mých workflow?
V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků. Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru. Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Může odesílatel workflow také schválit workflow?
Ano, odesílatel workflow může také schválit workflow, pokud je to tímto způsobem nakonfigurováno. Chcete-li předejít tomuto chování, nastavte **Parametry workflow > Obecné > Schvalovatel > Nepovolit schválení odesílatelem** na hodnotu **Ano**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Mohu přidat výstrahy do workflow a poskytnout tak uživatelům upozornění?
Zde je několik klíčových oblastí, které je třeba vzít do úvahy při přidávání výstrah do workflow za účelem poskytování oznámení:
- Výstrahy a mechanismy oznamování workflow
    - Výstrahy lze nastavit pro změny záznamů. Workflow mění záznamy, takže je možné nastavit výstrahu související se změnou záznamu způsobenou workflow. Protože však workflow mají jiné předdefinované možnosti oznámení, není použití výstrah ideální.
- Standardní oznámení z workflow 
    - Workflow obsahují e-mailová oznámení. Zákazník může nakonfigurovat oznámení tak, aby se uživatelům odesílaly e-maily. Tato oznámení nemají za následek zprávy centra akcí pro uživatele.
    - V budoucí aktualizaci bude přidána zpráva centra akcí, takže uživateli bude přiřazena pracovní položka workflow. 
- Přidání oznámení do workflow
    - Zprávy centra akcí lze vytvářet pro konkrétní uživatele, například zprávu vytvořenou z workflow v jazyce X + +.
    - [Workflow mají obchodní události](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), které může odběratel použít ke spuštění aplikace Flow s oznámeními, která hledají.   

V souhrnu, pokud uživatel neobdrží správné oznámení z centra akcí, když jsou mu přiřazeny pracovní položky workflow, využijte [obchodní události workflow](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) s aplikací Microsoft Flow s cílem poskytovat další nebo odlišná oznámení.

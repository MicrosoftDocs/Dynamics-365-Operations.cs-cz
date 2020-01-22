---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow.
author: ChrisGarty
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: cdddd26a662e9334f6d3c9806871df5b58ec03c7
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934902"
---
# <a name="workflow-faq"></a>Workflow – Často kladené otázky

[!include [banner](../includes/banner.md)]

Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Proč je při odmítnutí pracovní položky doručeno více oznámení?
Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá. Jiná pracovní položka je vytvořena a přiřazena původci. To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou. 

Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek. Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.

## <a name="why-are-my-workflow-exports-failing"></a>Proč se nedaří exporty mých workflow?
V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků. Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru. Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Může odesílatel workflow také schválit workflow?
Ano, odesílatel workflow může také schválit workflow, pokud je to tímto způsobem nakonfigurováno. Chcete-li předejít tomuto chování, nastavte **Správa systému > Workflow > Parametry workflow > Obecné > Schvalovatel > Nepovolit schválení odesílatelem** na hodnotu **Ano**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Mohu přidat výstrahy do workflow a poskytnout tak uživatelům upozornění?
Zde je několik klíčových oblastí, které je třeba vzít do úvahy při přidávání výstrah do workflow za účelem poskytování oznámení:
- Výstrahy a mechanismy oznamování workflow
    - Výstrahy lze nastavit pro změny záznamů. Workflow mění záznamy, takže je možné nastavit výstrahu související se změnou záznamu způsobenou workflow. Protože však workflow mají jiné předdefinované možnosti oznámení, není použití výstrah ideální.
- Standardní oznámení z workflow 
    - Workflow obsahují e-mailová oznámení. Zákazník může nakonfigurovat oznámení tak, aby se uživatelům odesílaly e-maily. Tato oznámení nemají za následek zprávy centra akcí pro uživatele.
    - V budoucí aktualizaci bude přidána zpráva centra akcí, takže uživateli bude přiřazena pracovní položka workflow. 
- Přidání oznámení do workflow
    - Zprávy centra akcí lze vytvářet pro konkrétní uživatele, například zprávu vytvořenou z workflow v jazyce X + +.
    - [Workflow mají obchodní události](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), které může odběratel použít ke spuštění aplikace Flow s oznámeními, která hledají.   

V souhrnu, pokud uživatel neobdrží správné oznámení z centra akcí, když jsou mu přiřazeny pracovní položky workflow, využijte [obchodní události workflow](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) s aplikací Microsoft Power Automate s cílem poskytovat další nebo odlišná oznámení.

## <a name="workflow-editor-has-trouble-starting-under-adfs"></a>Editor workflow má potíže s spuštěním v rámci ADFS 
Při spuštění v rámci služby AD FS (Active Directory Federation Services) v inovovaném prostředí může mít editor workflow potíže se spuštěním. Pokud tomu tak je, ujistěte se, že adresa URL "https://dynamicsaxworkfloweditor/" je přidána k vlastnosti **Microsoft Dynamics 365 for Operations On-premises - Workflow - Nativní aplikace** v nastavení ADFS.

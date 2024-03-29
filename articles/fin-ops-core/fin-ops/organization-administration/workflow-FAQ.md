---
title: Workflow – Často kladené otázky
description: Tento článek poskytuje odpovědi na časté otázky týkající se systému workflow.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72fd141bb1178a3a83385c512d1a655064d5b00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896572"
---
# <a name="workflow-faq"></a>Workflow – Často kladené otázky

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tento článek poskytuje odpovědi na časté otázky týkající se systému workflow.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Proč je při odmítnutí pracovní položky doručeno více oznámení?
Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá. Jiná pracovní položka je vytvořena a přiřazena původci. To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou. 

Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek. Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.

## <a name="why-are-my-workflow-exports-failing"></a>Proč se nedaří exporty mých workflow?
V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků. Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru. Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting).

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
    - [Workflow mají obchodní události](../../dev-itpro/business-events/business-events-workflow.md), které může odběratel použít ke spuštění aplikace Flow s oznámeními, která hledají.   

V souhrnu, pokud uživatel neobdrží správné oznámení z centra akcí, když jsou mu přiřazeny pracovní položky workflow, využijte [obchodní události workflow](../../dev-itpro/business-events/business-events-workflow.md) s aplikací Microsoft Power Automate s cílem poskytovat další nebo odlišná oznámení.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Proč nelze editor workflowu spustit v rámci služby AD FS?
Při spuštění v rámci služby AD FS (Active Directory Federation Services) v inovovaném prostředí může mít editor workflow potíže se spuštěním. Pokud tomu tak je, ujistěte se, že adresa URL "https://dynamicsaxworkfloweditor/" je přidána k vlastnosti **Microsoft Dynamics 365 for Operations On-premises - Workflow - Nativní aplikace** v nastavení ADFS.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Proč se při zpracování workflowu vyskytla zablokování SQL? 
Výchozí hodnota pole **Počet položek workflowu na dávkový úkol** na stránce **Parametry workflowu** je 0. Hodnota 0 způsobí, že se výchozí nastavení změní na 20 položek na dávku. Při úpravě této hodnoty buďte opatrní, protože vysoký počet položek na dávku (> 40) může vést k zablokování SQL.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Co je funkce Rozšířená chyba pracovního postupu?
Funkce Rozšířená chyba pracovního postupu ve verzi 10.0.13 přidává chybové kódy k rozlišení různých tříd chyb pracovního postupu. Hlášené chybové zprávy budou většinou podobné, s menšími rozdíly, aby byly jasnější.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

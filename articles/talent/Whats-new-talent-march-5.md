---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (5. března 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2019
ms.locfileid: "782809"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (5. března 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="extending-option-sets-in-attract"></a>Rozšíření sad možností v aplikaci Attract

V aplikaci Attract existuje několik polí, která jsou sadami možností v rámci aplikace Common Data Service (CDS). Byly zavedeny nové možnosti pro rozšíření sad možností, počínaje polem důvodu **Zamítnutí**, polem **Typ zaměstnání** a polem **Typ služebního věku**.

> [!IMPORTANT]
> Funkce publikování pracovní nabídky na LinkedIn vyžaduje použití polí **Typ zaměstnání** a **Typ služebního věku** na stránce **Podrobnosti práce**. Výchozí hodnoty v těchto polích jsou podporovány službou LinkedIn a jsou zobrazeny při publikování nabídky práce. Pokud publikujete nabídku práce na LinkedIn a upravujete existující hodnoty sady možností pro tato pole, práce bude nadále publikována, ale LinkedIn nezobrazí vlastní hodnoty **Typ zaměstnání** a **Typ služebního věku**.

## <a name="changes-in-onboarding"></a>Změny v aplikaci Onboard

### <a name="private-preview-for-onboard-teams"></a>Soukromá verze Preview pro týmy aplikace Onboard
Nyní můžete snadno sdílet a spolupracovat na šablonách napříč celou organizací. Další informace naleznete v tématu [Sdílení doporučených postupů napříč vaší organizací pomocí zaškolovacích týmů](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Soukromá verze Preview pro zástupné texty zmocněnce
Šablony můžete obohatit přiřazením aktivit rolím namísto jednotlivců. Role jsou pak přiřazeny jednotlivcům v době vytvoření průvodce. Další informace naleznete v tématu [Zefektivnění správy průvodců přiřazením aktivit rolím](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Změny v Core HR
**Sestavení 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Konfigurace workflow pro automatické schvalování nebo následování workflow, když manažer lidských zdrojů nebo úsekový manažer odešle nebo aktualizuje žádosti o volno
Byly přidány nové podmínky workflow, aby mohly být žádosti o volno automaticky schváleny, pokud je předloží manažer zaměstnance nebo oddělení lidských zdrojů. Jedním ze způsobů, jak dosáhnout tohoto automatického schválení na workflow, je povolení automatické akce na schválení workflow.

Podmínky, které byly přidány, zahrnují:

- Odesláno kým – Použitá se k vyhodnocení ID systémového uživatele, který odeslal požadavek do workflow.
- Odesláno jménem - Používá se k vyhodnocení toho, zda byl požadavek odeslán jménem pracovníka přiřazeného k požadavku.
- Odesláno oddělením lidských zdrojů - Používá se k vyhodnocení, zda je systémový uživatel, který odeslal požadavek do workflow, v roli lidských zdrojů.
- Odesláno nadřízeným - Používá se k vyhodnocení, zda je uživatel, který odeslal žádost o volno do workflow, hierarchicky přímý nadřízený pracovníka přidruženého k požadavku.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Povolení fixní kompenzace zaměstnance pro budoucí přiřazení pozice
Je obvyklé, že zaměstnanec je přijat do organizace s budoucím počátečním datem. Tato změna umožňuje definování fixní kompenzace pro zaměstnance s budoucími přiřazeními pozice.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Při úpravě pozice jsou pole mzdy pozice prázdná
Při této změně se při požadavku na změny stávajících pozic pole mzdy nastaví na ve výchozím nastavení na aktuální hodnoty.

### <a name="other-miscellaneous-bug-fixes"></a>Ostatní různé opravy chyb
V této verzi existují jiné menší opravy chyb.

### <a name="upgrade-to-cds-for-apps"></a>Upgrade na CDS for Apps
Konečné termíny pro upgrade na CDS for Apps se rychle blíží. Přihlaste se do centra pro správu PowerApps k určení, zda je třeba provést upgrade databáze. Další informace o konečných termínech a nutných krocích k upgradu naleznete v tématu [Upgrade na Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Již brzy

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)
V mnoha organizacích mohou manažeři kompenzací a zaměstnaneckých výhod získat přístup pouze k určitým záznamům o kompenzacích, jako jsou záznamy pro vedoucí pracovníky nebo regionální zaměstnance. Díky této změně můžete spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s plány, jako jsou například záznamy o mzdě nebo bonusech. Kompenzace pro tyto zaměstnance budou moci zpracovávat pouze role s daným přístupem.

###  <a name="platform-update-24"></a>Aktualizace platformy 24
Další podrobnosti o aktualizaci Platform Update 24 naleznete v tématu [Co je nového a co se změnilo v aplikaci Finance and Operations, Platform Update 24 (březen 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

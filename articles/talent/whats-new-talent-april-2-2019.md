---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (2. dubna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 04b5a006d4580fe419d81986a90851bc8d611722
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528212"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (2. dubna 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="approval-emails-in-attract"></a>Schválení e-mailů v aplikaci Attract
Nové schvalovací e-maily zlepšují viditelnost do procesu schvalování. E-maily se odesílají schvalovatelům, když nastane některý z následujících scénářů:

- Žadatele odešle práci ke schválení.
- Práce je buď zamítnuta nebo schválena.
- Schvalovatel nereagoval na žádost o schválení do 24 hodin.

Obsah schvalovacích e-mailů lze upravit pomocí nových šablon.

### <a name="application-and-profile-attachments"></a>Přílohy žádosti a profilu
Vylepšení karty **Dokumenty** v profilech žádostí a skupin talentů nyní zobrazují název i typ dokumentu.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="coming-soon-attract-and-onboard"></a>Připravuje se (Attract a Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integrace Lifecycle Services (LCS) s nahlášením problému
V aplikacích Attract a Onboard problémy zaznamenané koncovými uživateli pomocí funkce nahlášení problému nyní automaticky vytváří problémy pro podporu v projektu LCS zákazníka. Správci pak mohou tyto problémy roztřídit a v případě potřeby je odeslat společnosti Microsoft. To odpovídá způsobu, kterým Core HR zpracovává problémy podpory koncových uživatelů.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2216.

### <a name="platform-update-25-for-finance-and-operations"></a>Aktualizace Platform 25 pro Finance and Operations
Další informace o aktualizaci Platform Update 25 pro Finance and Operations naleznete v tématu [Funkce Preview v aktualizaci Platform Update 25 aplikace Dynamics 365 for Finance and Operations (duben 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)
V mnoha organizacích mohou mít manažeři kompenzací a zaměstnaneckých výhod přístup pouze k určitým záznamům o kompenzacích. To může zahrnovat záznamy pro vedoucí pracovníky nebo regionální zaměstnance. Díky této změně může oddělení lidských zdrojů spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Můžete přiřadit role zabezpečení fixním i variabilním plánům. Tyto role zabezpečení určují přístup k plánům a souvisejícím zaměstnaneckým datům, jako jsou záznamy o platech nebo bonusech, takže pouze tyto role mohou zpracovávat kompenzace pro skupiny zaměstnanců.

### <a name="upgrade-to-common-data-service"></a>Upgrade na Common Data Service
Konečné termíny pro upgrade na Common Data Service se rychle blíží. Přihlaste se do centra pro správu Microsoft Power Apps k určení, zda je třeba provést upgrade databáze. Další informace o konečných termínech a nutných krocích k upgradu naleznete v tématu [Upgrade na Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Náhled

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Povolení určení kódů důvodů na typech pracovního volna
Organizace mohou potřebovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro určité typy pracovního volna na požadavcích na volno
Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Může to být způsobeno zásadami společnosti nebo právními požadavky. Nyní můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

## <a name="coming-soon"></a>Již brzy

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Vylepšení uživatelského rozhraní pro duplicitní kontrolu zaměstnanců
S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.

###  <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
S aktualizací Platform Update 25 Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěny událostí. 

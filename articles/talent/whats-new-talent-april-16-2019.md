---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (16. dubna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0781a479ebf37334d8eba18ea6d69d7cfb9db9ea
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024130"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (16. dubna 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="process-auditing"></a>Auditování procesů

Nyní můžete sledovat změny kandidátů, otevřených pracovních pozic a žádostí o práci. Další informace naleznete v tématu [Sledování změn v náborových datech](process-auditing.md).

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2239. Čísla v závorkách se vztahují na čísla podpory v Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Entity oblast kompenzace, úroveň kompenzace, možnost zaměstnaneckých výhod a typ dovedností v Common Data Service jsou aktualizovány a zahrnují podporu polí odběratelů

V tomto vydání byly tyto entity Common Data Service aktualizovány tak, aby obsahovaly možnost zahrnout vlastní pole přidané prostřednictvím aplikace Talent: Core HR.

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a>Nová entita Common Data Service podporuje: pravidla připsání kompenzace, plán variabilní kompenzace, variabilní kompenzaci

V této verzi byly do Common Data Service přidány entity pravidla připsání kompenzace, plánu variabilní kompenzace a variabilní kompenzace. Tyto entity rovněž podporují vlastní pole přidaná prostřednictvím aplikace Talent: Core HR.

### <a name="powerbi-refresh-issues-314342"></a>Problémy s aktualizací PowerBI (314342)

Tato změna opravuje problém se správnou aktualizací sestav PowerBI.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Nelze kliknout přímo na převodní úkoly v rámci samoobsluhy zaměstnanců (303309)

Tato změna umožňuje uživatelům s rolí zaměstnance vybrat a aktualizovat převodní úkoly ze seznamu úkolů aplikace Talent.

### <a name="performance-feedback-email-message-updated-309615"></a>E-mailová zpráva zpětné vazby k výkonnosti byla aktualizována (309615)

Při této změně se při úspěšném odeslání zpětné vazby zobrazí potvrzovací zpráva.

### <a name="missing-tables-in-word-template-308048"></a>Chybějící tabulky v šabloně aplikace Word (308048)

S touto změnou se při vytváření šablony aplikace Word s informacemi o zaměstnancích a dovednostech v dokumentu aplikace Word zobrazí pouze dovednosti pro vybraného zaměstnance.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Při použití kontrolního seznamu odchodu se zobrazí chyba. (299877)

Tato změna opravuje problém při použití kontrolního seznamu odchodu přímo z formuláře pracovníka.

## <a name="in-preview"></a>Náhled

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Povolení určení kódů důvodů na typech pracovního volna

Organizace mohou potřebovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro určité typy pracovního volna na požadavcích na volno

Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Může to být způsobeno zásadami společnosti nebo právními požadavky. Nyní můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů

Sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby vidělo příčiny zůstatků.

## <a name="coming-soon"></a>Již brzy

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Vylepšení uživatelského rozhraní pro duplicitní kontrolu zaměstnanců

S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.

### <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy

V aktualizaci Platform Update 25 for Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěna událostí.



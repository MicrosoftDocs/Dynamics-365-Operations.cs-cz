---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (9. dubna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
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
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460622"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (9. dubna 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integrace Lifecycle Services (LCS) s nahlášením problému
V aplikacích Attract a Onboard problémy zaznamenané koncovými uživateli pomocí funkce nahlášení problému nyní automaticky vytváří problémy pro podporu v projektu LCS zákazníka. Správci pak mohou tyto problémy roztřídit a v případě potřeby je odeslat společnosti Microsoft. To odpovídá způsobu, kterým Core HR zpracovává problémy podpory koncových uživatelů.

### <a name="relevance-search"></a>Vyhledávání podle relevance
Ve skupinách talentů můžete nyní prohledávat celou databázi kandidátů ohledně konkrétních dovedností, jmen nebo vzdělání. Již nemusíte specifikovat, kterou část profilu kandidáta chcete prohledat. Attract prohledá celý profil a zvýrazní všechny nalezené shody. Attract také prohledává všechny dokumenty, které jsou pro kandidáta k dispozici, a inteligentně řadí výsledky vyhledávání. Kromě toho můžete výsledky filtrovat podle zdroje nebo podle toho, zda jsou druhými v pořadí. Další informace naleznete v tématu [Vyhledávání a zobrazení profilů kandidáta](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Doporučení potenciálního uchazeče
Attract může pomoci k nastartování hledání zdroje pro práci, jakmile ho aktivujete tím, že vytvoříte inteligentní doporučení kandidáta z databáze kandidátů vaší organizace. Doporučení zahrnují informace o dovednostech a vzdělání, které byly zjištěny při hledání relevantních potenciálních uchazečů. Tato doporučení se zobrazí na kartě **Potenciální uchazeči** pod prací, pokud ho povolíte během náborového procesu pro práci. Další informace naleznete v tématu [Doporučení potenciálního uchazeče](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Stavy dostupnosti tazatele
Plánovači pohovoru budou moci brzy zobrazit stavy **Mimo kancelář, práce jinde** pro tazatele, které pomohou plánovat časy, které budou tazatelům lépe vyhovovat.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Zkušenost kandidáta s pohovorem: Uložení pozvánek kalendáře
Kandidáti si nyní mohou stáhnout a uložit své události pohovorů do svých osobních kalendářů pomocí souboru .ics připojeného k souhrnnému e-mailu pohovoru zaslanému kandidátovi.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integrace Lifecycle Services (LCS) s nahlášením problému
V aplikacích Attract a Onboard problémy zaznamenané koncovými uživateli pomocí funkce nahlášení problému nyní automaticky vytváří problémy pro podporu v projektu LCS zákazníka. Správci pak mohou tyto problémy roztřídit a v případě potřeby je odeslat společnosti Microsoft. To odpovídá způsobu, kterým Core HR zpracovává problémy podpory koncových uživatelů.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Procenta základních variabilních plánů načítají nesprávnou částku
Verze z tohoto týdne opravuje problém, kdy načítání odměn variabilních kompenzací používá procento základních plánů.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Výběr data pro poslední pracovní den nefunguje správně
Tato změna opravuje problém: Když uživatelé opravují **Koncové datum zaměstnání** a vyberou datum pomocí ovládacího prvku kalendáře, přidá se k výběru den.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Omezení typů akcí personálu podle provedené akce
Tato změna omezuje typy akcí, které se zobrazí při provedení konkrétních akcí. Například při požadavku na novou pozici se zobrazí pouze nové akce pozice v seznamu akcí k výběru. Dříve se zobrazovaly jak nová akce, tak akce úpravy. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Převod zaměstnance s kompenzací v druhé právnické osobě
Tato verze umožňuje ukončení kompenzace v druhé právnické osobě, pokud se jedná o převod mezi společnostmi.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Nelze vybrat kompenzaci pro budoucí zaměstnání během přenosu
Při převodu zaměstnance do nové právnické osoby můžete nyní nastavit kompenzaci pro novou právnickou osobu během procesu převodu.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Uživatel není schopen přiřadit kompenzaci během přiřazení pozice
Přidání přiřazení nové pozice nyní umožní nastavení záznamů fixních kompenzací. 

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

###  <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
S aktualizací Platform Update 25 Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěny událostí. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
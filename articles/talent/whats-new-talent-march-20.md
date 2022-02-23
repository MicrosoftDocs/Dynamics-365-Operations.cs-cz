---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (20. března 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460556"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (20. března 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="setting-the-audience-on-activities"></a>Nastavení cílové skupiny na aktivitách
Aktivity v systému mohou mít nyní definovanou cílovou skupinu. Aktivity související s procesem (například pohovor, plán, zpětná vazba a EEO) lze nastavit na možnosti Všichni kandidáti, Interní kandidáti a Externí kandidáti. Vlastní aktivity, jako jsou například Microsoft Forms, YouTube videa a webový obsah lze doručit všem kandidátům, interním kandidátům, externím kandidátům nebo náborovému týmu.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Vylepšení vyhledávání práce na kariérním webu: optimalizace webového vyhledávače
Tato funkce umožňuje nástrojům pro indexaci dat ve vyhledávačích najít a indexovat publikované práce na kariérním webu aplikace Attract. Pomáhá kandidátům vyhledat pracovní nabídky publikované na kariérní web aplikace Attract pomocí populárních vyhledávačů.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Zobrazení nápovědy pro přihlášení kandidátům, kteří zapomněli své přihlašovací údaje
Pokud kandidát zapomněl přihlašovací údaje, které používal pro žádost o práci při otevírání odkazu, který mu byl uložen nebo odeslán e-mailem, zobrazí se nyní nápověda se jménem poskytovatele a uživatelským jménem (zakrytým). To pomůže kandidátům použít správné přihlašovací údaje pro přístup k jejich žádostem o práci.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Pomoc interním kandidátům při hledání interních pracovních nabídek
Byl vyřešen problém, kdy externí uchazeči mohli vidět jméno náborového pracovníka nebo náborového manažera. Nyní mohou vidět členy náborového týmu u práce pouze interní kandidáti. Je rovněž snazší pro interní kandidáty zobrazit pouze interní páce a zažádat o ně. Pokud se kandidát pokusí o přístup k odkazu na zobrazení nebo žádost o interní práci, je nucen se ověřit pomocí přihlašovacích údajů služby Azure Active Directory. Interní kandidáti mají také možnost kontaktovat člena náborového týmu a projevit zájem o práci nebo se o ní dozvědět více. Tato možnost je k dispozici pro všechny práce pro pouze interní kandidáty. Další informace naleznete v tématu [Nastavení kariérního webu v aplikaci Microsoft Dynamics 365 Talent - Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Označení druhých v pořadí pro přiřazení vysoce ceněných žadatelů pro budoucí práce
Náboroví pracovníci a náboroví manažeři si často udržují aktuální seznam žadatelů, kteří byli vhodnými kandidáty na pozici, ale nemohli dostat nabídku, protože pozice byla již obsazena. Tito uchazeči, označovaní jako druzí v pořadí, jsou užiteční, protože při příštím náboru, když se otevře podobná pozice, mohou snížit dobu potřebnou k přijetí. Attract nyní umožňuje náborovým pracovníkům a náborovým manažerům určit druhé v pořadí na seznamu uchazečů, pokud uchazeč prošel do fáze nabídky. Určení druhých v pořadí se zobrazí na seznamu uchazečů o práci, ale rovněž v zobrazení skupiny talentů, když jsou tito uchazeči členy jakýchkoliv skupin náborových pracovníků nebo náborových manažerů. Kromě toho se toto označení objeví v historii práce jako součást profilu skupiny talentů kandidáta. Tuto funkci můžete vyzkoušet v náhledu, když ji zapne správce pomocí [Správy funkcí v centru pro správu](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Přidání uchazečů do skupin talentů
Nyní je snazší přidat uchazeče do skupin talentů vytvořením nové akce v seznamu uchazečů. Výběrem ikony **Přidat do skupiny talentů** si mohou náboroví pracovníci nebo manažeři vybírat ze svého seznamu skupin talentů a snadno přidávat uchazeče do skupin talentů přímo ze seznamu uchazečů o práci.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigurace nutnosti životopisu pro žádost o konkrétní práci
Na základě zpětné vazby od zákazníků mohou nyní náboráři konfigurovat, zda je při podání žádosti o určitou práci nutné poskytnout životopis ve formě nahraného souboru. Tato konfigurace je součástí aktivity Žádost, dostupné v náborovém procesu. Když je povolena, každý potenciální uchazeč bude vyzván k odeslání životopisu při žádosti o tuto pozici. Žádost nebude považována za dokončenou, dokud nebude odeslán životopis. To pomáhá snižovat nedostatek informací ve skupině uchazečů tím, že se zajistí, aby každý uchazeč poskytl dostatek informací, které by umožnily náborovému pracovníkovi jejich roztřídění.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidáti se mohou ucházet o práci pomocí svého profilu LinkedIn
Kandidáti, kteří již mají svůj aktuální profil na LinkedIn, se mohou ucházet o pracovní místa jedním kliknutím pomocí tohoto profilu.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Sledujte, jak profil uchazeče vznikl v systému a kde vaši uchazeči naleznou pracovní místa, o která požádali
Nyní se můžete dozvědět, jak profil konkrétního kandidáta vznikl v systému Attract, a to tak, že se podíváte na zdroj profilu v podrobnostech kandidáta na stránce **Profil** žádosti nebo profilu skupiny talentu. Podobně můžete zjistit, jak každý uchazeč nalezl práci, a to tak, že se podíváte na zdroj žádosti uvedený v **Aktivitě žádosti** v kanálu aktivity žádosti. Tyto informace jsou také k dispozici v historii práce v profilu skupiny talentů. Když náboroví pracovníci nebo manažeři přidávají kandidáty ručně, budou také vyzváni k určení zdroje žádosti nebo profilu kandidáta. Pokud kandidát žádá poprvé, bude jeho zdroj profilu stejný jako původ jeho žádosti. Tuto funkci můžete vyzkoušet v náhledu, když ji zapne správce pomocí [Správy funkcí v centru pro správu](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Mějte na paměti, že existující kandidáti a uchazeči nebudou mít žádnou informaci o zdroji. Náboroví pracovníci však mohou tyto údaje přidat ručně.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Integrace s aplikací Attract hlásí chybu duplicitního záznamu pro žádosti
V této aktualizaci byl problém s duplicitními záznamy opraven. Tento problém se objevuje při otevírání pracovního prostoru **Správa zaměstnanců**.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Nelze zavřít formulář při úpravách pořadí jmen
Byly provedeny změny pro nápravu tohoto problému při úpravách pořadí jmen na formuláři pracovníka.

## <a name="coming-soon"></a>Již brzy

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)
V mnoha organizacích mohou mít manažeři kompenzací a zaměstnaneckých výhod přístup pouze k určitým záznamům o kompenzacích. Tyto záznamy mohou být pro vedoucí pracovníky nebo regionální zaměstnance. Díky této změně může oddělení lidských zdrojů spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s plány, jako jsou například záznamy o mzdě nebo bonusech. Kompenzace pro tyto zaměstnance mohou zpracovávat pouze role, kterým byl udělen přístup.

###  <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
S aktualizací Platform Update 24 Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěny událostí.

### <a name="duplicate-employee-check-interface-changes"></a>Kontrola duplicitních zaměstnanců: změny rozhraní
S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.



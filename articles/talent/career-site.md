---
title: Funkce kariérního webu v aplikaci Attract
description: Toto téma poskytuje přehled funkce kariérního webu vystaveného kandidátům v aplikaci Attract
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: e51fb00536884d2b3815c05a0968714d8b9326f2
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729696"
---
# <a name="career-site-functionality-in-attract"></a>Funkce kariérního webu v aplikaci Attract

[!include[banner](../includes/banner.md)]

Toto téma poskytuje přehled funkce kariérního webu vystaveného kandidátům v aplikaci Microsoft Dynamics 365 for Talent: Attract. Také vysvětluje, jak tuto funkci nastavit.

Attract poskytuje jeden kariérní web pro každé prostředí v klientovi. Pokud například organizace používá prostředí pro vývoj a testovací prostředí, je zřízen jeden kariérní web pro vývojové prostředí a jiný pro testovací prostředí. Každý kariérní web je zcela nezávislý a má vlastní mechanismus ověřování. Mezi kariérními weby nejsou sdíleny pracovní pozice a profily kandidátů.

Ve výchozím nastavení je kariérní web veřejný. Proto mohou kandidáti zobrazit všechna pracovní místa, která jsou označena jako externí, aniž by se museli přihlásit. Všechny ostatní akce však vyžadují, aby se uchazeči přihlásili.

## <a name="career-site-management"></a>Správa kariérního webu

Pokud chcete nastavit hodnoty pro následující položky, přihlaste se k systému Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** nabídky (symbol ozubeného kola) a pak vyberte kartu **informace o společnosti**.

-   **Název organizace:** - Název organizace se objevuje v navigačním panelu v horní části kariérního webu. Když uchazeč vybere název organizace, přejde na stránku se seznamem všech otevřených pracovních míst.

-   **Logo organizace:** - V levém horním rohu kariérního webu se zobrazuje obrázek loga organizace. Když uchazeč vybere obrázek loga, přejde na stránku se seznamem všech otevřených pracovních míst.

    > [!NOTE] 
    > Obrázek loga, který se zobrazí na stránce kariérního webu, má pevnou výšku 20 pixelů (px). Obrázek, který přidáte do Centra pro správu, se přizpůsobuje stránce. Proto se může šířka měnit v závislosti na obrázku.
 
Pokud chcete nastavit hodnoty pro následující položky, přihlaste se k aplikaci Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** a poté zvolte kartu **Správa kariérního webu**.

-   **Optimalizace pro vyhledávače** - Pokud je povolena, budou všechny nabídky práce publikované na kariérním webu Attract vyhledávatelné pomocí vyhledávačů, jako jsou Bing a Google. 

    > [!NOTE] 
    > Může dojít ke zpoždění mezi zapnutím tohoto nastavení a zobrazením výsledků vyhledávání, v závislosti na používaném vyhledávači.
    
-   **Smluvní podmínky** – Pokud je to povoleno, musí všichni uchazeči při žádosti o zaměstnání souhlasit se smluvními podmínkami organizace. Správce systému Attract je schopen nakonfigurovat vlastní text souhlasu a odkaz na stránku Smluvní podmínky. 

        
## <a name="career-site-urls"></a>URL adresy kariérního webu

Následující seznam obsahuje běžně používané URL adresy kariérního webu a způsob přístupu.

-   **Adresa URL domovské stránky kariérního webu** – Chcete-li zobrazit adresu URL domovské stránky kariérního webu, přihlaste se k aplikaci Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** a poté vyberte kartu **Správa kariérního webu**.

-   **URL adresa individuální žádosti o publikování práce** - Když [publikujete externí práci](Creating-jobs-Attract.md#postings) poprvé, můžete zkopírovat odkaz **Požádat** z aplikace Attract. Adresa URL pro tento odkaz bude v následujícím formátu: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **URL adresa individuálního publikování práce** – Adresa URL publikování práce je dílčí řetězec žádosti. Sestává ze všech položek až k číslu práce. Proto je pro předchozí adresu URL žádosti URL adresa publikování práce [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Možnosti ověřování

Uchazeči mají k dispozici následující možnosti přihlašování ke kariérním webu Attract:

-   Osobní účet:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Pracovní nebo školní účet:

    -   Microsoft Azure Active Directory (Azure AD)

Přihlašování ke službě Azure AD je určeno pouze pro interní kandidáty. Proto funguje pouze pro interní uchazeče, kteří používají své přihlašovací údaje služby Azure AD. Například uchazeč, který je aktuálně zaměstnancem společnosti Contoso Ltd., chce zažádat o zaměstnání v nesouvisející společnost Alpine Ski House. V takovém případě přihlášení nebude úspěšné, pokud se zaměstnanec pokusí použít své přihlašovací údaje ke službě Azure AD od společnosti Contoso Ltd. 

Zájemci se musí přihlásit s použitím Azure AD, pokud je práce, kterou zobrazují nebo o niž žádají, uvedena pouze jako interní.

## <a name="create-and-maintain-a-profile"></a>Vytvoření a správa profilu

Poté, co se uchazeči přihlásí ke kariérnímu webu, mohou vybrat **Můj profil** na navigačním panelu v horní části stránky, kde mohou vytvořit a spravovat svůj profil.
Profil obsahuje osobní údaje, údaje o pracovních zkušenostech, podrobnostech o vzdělání, dokumenty, odkazy a informace o kvalifikačních předpokladech. Po vytvoření lze profil použít k zažádání o pracovní místa, o která má uchazeč zájem. Profily také pomáhají systému Attract doporučit správná pracovní místa uchazečům.

> [!NOTE]
> Pokud kandidát použije ID e-mailu k přihlášení pomocí jednoho z výše uvedených poskytovatelů ověřování, toto e-mailové ID bude standardně nastaveno na ID e-mailu kontaktu přidruženého k profilu. Ty druhé však mohou být kdykoliv změněny a jsou zcela nezávislé na prvním. Attract vždy použije ID e-mailu kontaktu pro přidružení k vašemu profilu pro všechny e-mailové komunikace.

## <a name="find-the-right-job"></a>Vyhledání správné práce

Na stránce se seznamem práce mohou uchazeči vyhledat určité pracovní místo zadáním hledaných pojmů. Funkce vyhledávání vyhledá hledané termíny v názvech a popisech pracovní pozice a zobrazí jako výsledky relevantní pracovní místa. Uchazeči mohou kdykoli filtrovat výsledky na základě místa výkonu práce nebo pracovní funkce.

Uchazeči také mohou zobrazit sadu doporučených pracovních míst na kariérním webu. Pracovní místa, která jsou uchazeči doporučena, jsou založena na minulých žádostech uchazeče, profilu a životopisech.

> [!NOTE] 
> Doporučení pracovních míst se zobrazí pouze v případě, že je na kariérním webu zveřejněno nejméně 10 pracovních míst, a pokud uchazeč vyplnil svůj profil.

Interní uchazeči se také mohou podívat, kdo je náborový manažer nebo pracovník u dané práce, pro případ, že by tyto členy náborového týmu chtěli kontaktovat. Externí uchazeči se však nemohou podívat, kdo jsou členové náborového týmu u jakékoli zakázky.

## <a name="contact-the-hiring-team"></a>Kontaktovat náborový tým
Pouze interní uchazeči mohou kontaktovat náborový tým. Toto omezení se vztahuje na všechny práce, bez ohledu na to, jestli jsou jenom interní nebo byly zveřejněny.

Zájemci mohou chtít kontaktovat náborový tým, aby vyjádřili zájem o práci, která byla zveřejněna, nebo aby o ní získali více informací. Mohou kontaktovat kohokoli z náborového týmu, kdo je uveden (náboroví manažeři nebo pracovníci). Ke zprávě mohou také volitelně připojit životopis nebo mohou vybrat současný životopis, který předtím nahráli v rámci svého profilu.

Poté, co interní uchazeč vybere členy náborového týmu ke kontaktování, Attract pošle těmto lidem e-mail jménem uchazeče. Současně je profilu uchazeče přidán do fáze **potenciální zaměstnanec**, pokud je tato fáze pro práci dostupná. Ve fázi **potenciální zaměstnanec** mohou náboroví pracovníci nebo manažeři zobrazovat uchazeče, kteří je kontaktovali. Mohou také prohlížet profily uchazečů a pozvat potenciální uchazeče, aby o práci zažádali.

Uchazeči mohou zažádat o práci, ohledně které už kontaktovali členy náborového týmu. Jakmile podají žádost, nemohou dále kontaktovat náborový tým prostřednictvím kariérního webu.

## <a name="apply-for-jobs"></a>Žádost o práci

Poté, co uchazeči najdou správnou práci, mohou o ni zažádat pomocí tlačítka **Požádat**  na stránce **Podrobnosti o práci**. V tomto okamžiku mohou uchazeči vytvořit nový profil nebo zkontrolovat informace ve svém existujícím profilu.
Uchazeči také mohou nahrát podle potřeby životopis a odeslat žádost o práci.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Povolení žádostí o práci s profily na webu LinkedIn

Uchazečům můžete usnadnit žádost o pracovní místa konfigurací aplikace Attract tak, aby jim umožnila podávat žádosti prostřednictvím webu LinkedIn.

> [!NOTE] 
> K tomu je potřeba jedna nebo více licencí náborových pracovníků LinkedIn předtím, než budou moci podat žádost pomocí webu LinkedIn.

1. Přihlaste se do aplikace Attract jako správce.
2. Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.
3. Vyberte kartu **Integrace LinkedIn** a připojte se k účtu LinkedIn Recruiter.
4. V části **Integrace LinkedIn Recruiter System Connect** vyberte **Povoleno** pro nastavení **Zažádat pomocí webu LinkedIn**.

Poté, co jste povolili toto nastavení, mohou uživatelé k žádosti použít svá stávající data profilu LinkedIn. Když uživatelé zažádají pomocí tlačítka **Zažádat pomocí služby LinkedIn**, jsou ožádáni o ověření ve službě LinkedIn, zda nejsou přihlášení. Po ověření nahradí jejich profil LinkedIn existující data profilu zobrazená na stránce aplikace. Zájemci mohou podle potřeby upravovat informace a následně odeslat žádost Pokud uchazeč přejde mimo stránku bez žádosti o práci, data profilu se neaktualizují v Attract.

## <a name="check-application-status"></a>Kontrola stavu žádosti

Poté, co uchazeči zažádají o jedno nebo více pracovních míst, mohou na navigačním panelu v horní části stránky vybrat možnost **Žádosti** k zobrazení otevřených a uzavřených žádostí. Jakmile uchazeči otevřou některou ze svých žádostí, uvidí aktuální fázi a jakékoli čekající položky akcí, které je nutné dokončit. Pokud musí například uchazeč poskytnout potenciální data pro pohovor mezi čtyřma očima, na stránce se zobrazí dostupné možnosti.

## <a name="internal-jobs"></a>Interní pracovní pozice

V současné době se pracovní pozice, které jsou označeny jako interní a publikované na kariérním webu Attract, na kariérním webu nezobrazují. Jsou přístupné pouze prostřednictvím přímé adresy URL **Požádat**, kterou lze kopírovat z aplikace Attract.

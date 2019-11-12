---
title: Přístup k funkcím náhledu v aplikaci Microsoft Dynamics 365 Talent
description: Toto téma popisuje, jak může správce povolit funkce náhledu, a uvádí seznam funkcí v aplikaci Microsoft Dynamics 365 Talent, které jsou nyní povoleny pro náhled.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551583"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Přístup k funkcím náhledu v aplikaci Microsoft Dynamics 365 Talent

[!include[banner](../includes/banner.md)]

V rámci našeho průběžného přidávání schopností cyklu správy lidského kapitálu v aplikaci Microsoft Dynamics 365 Talent chceme, aby zákazníci co nejdříve měli k dispozici nové funkce. Správci mohou zobrazit a používat funkce náhledu v rámci prostředí. Tyto funkce jsou téměř připraveny k obecné dostupnosti a prošly rozsáhlým testováním. Právě hledáme další z zpětnou vazbu od zákazníků a ověření před tím, než budou dostupné široké veřejnosti.

Toto téma popisuje, jak lze povolit funkce náhledu, a uvádí seznam funkcí, které jsou nyní k dispozici pro náhled. Tento seznam bude aktualizován s tím, jak budou vydávány nové funkce pro všeobecnou dostupnost a nové funkce, které budou uvolněny k zobrazení náhledu. Při uvolnění funkcí k náhledu není vydáno žádné upozornění. Uživatelé jen uvidí funkce. Další informace o nových funkcích v aplikaci Talent získáte v části [Co je nového nebo změněného v aplikaci Dynamics 365 Talent](./whats-new.md) a [Poznámky k verzi Dynamics 365 a Power Platform](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Povolit nebo zakázat funkce náhledu

Chcete-li získat přístup k funkcím náhledu, je nutné je nejprve povolit ve vašem prostředí. Povolení nebo zakázání funkcí náhledu se vztahuje ke konkrétnímu prostředí.

> [!IMPORTANT]
> Když zapnete nastavení **Funkce náhledu**, povolíte tím funkce Náhledu pro všechny uživatele ve vaší organizaci, kteří jsou v prostředí. Vypnutím nastavení zakážete funkce náhledu a způsobíte, že budou uživatelům nepřístupné. Funkce náhledu mají v aplikaci Talent omezenou podporu. Mohou používat méně opatření pro soukromí a bezpečnostních opatření a nejsou zahrnuty do smlouvy o úrovni služeb (SLA) aplikace Talent. Neměli byste je používat ke zpracování osobních údajů (to znamená všech informací, které vás mohou identifikovat), nebo ke zpracování jiných dat, které podléhají požadavkům na vyhovění zákonům nebo předpisům.

### <a name="attract"></a>Attract

1. Přihlaste se do aplikace Microsoft Dynamics 365 Talent: Attract.
2. V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **Centrum pro správu**.
3. Na kartě **Správa funkcí** vyberte možnost vedle položky **náhled funkce**, aby se zbarvila modře a uváděla informaci **Zapnuto**.

    ![Povolení nebo zákaz ukázkových funkcí v systému Attract](./media/attract-enable-preview-features.png)

4. Vyberte nebo zrušte výběr jednotlivých funkcí náhledu. Pokud neprovedete žádnou akci, budou povoleny všechny funkce náhledu, které jsou k dispozici.
5. Aktualizujte prohlížeč tak, abyste viděli nové funkce. Všichni uživatelé, kteří jsou již přihlášeni, uvidí funkce při příštím přihlášení, nebo mohou aktualizovat svůj prohlížeč, aby funkce viděli okamžitě.

> [!NOTE]
> Některé funkce náhledu mohou vyžadovat další konfiguraci. Pomocí odkazů vedle funkce náhledu dokončete její instalaci.

### <a name="core-hr"></a>Základní lidské zdroje

1. Přihlaste se do aplikace Talent.
2. Vyberte **Správa systému** a poté vyberte kartu **Odkazy**.
3. Na stránce **Správa systému** v části **Nastavení** vyberte **Parametry systému**.
4. Na stránce **Parametry systému** vyberte kartu **Funkce náhledu**.
5. Chcete-li zpřístupnit funkce náhledu, nastavte volbu **Povolit režim náhledu pro všechny uživatele** na **Ano**.

    ![Povolení nebo zákaz ukázkových funkcí v systému Core HR](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Chcete-li zakázat funkce náhledu, použijte stejný postup, ale nastavte volbu **Povolit režim náhledu pro všechny uživatele** na **Ne**. Když funkce náhledu zakážete, budou nepřístupné pro uživatele a v procesech, které jsou spojeny s funkcemi, může dojít k chybám.

### <a name="onboard"></a>Zaškolení

V současné době nejsou k dispozici žádné funkce náhledu pro Microsoft Dynamics 365 Talent: Onboard.

## <a name="features-that-are-currently-in-preview"></a>Funkce, které jsou aktuálně v náhledu

### <a name="attract"></a>Attract

- [Doporučení uchazeče](./intelligent-recommendations.md#candidate-recommendations) – Pokud je více než deset kandidátů nebo uchazečů, kteří mají životopisy nebo kompletní profily, se kandidáti nebo uchazeči, kteří nejvíce splňují požadavky na práci, objeví v části **Uchazeči k uvážení** na stránce dané práce.
- [Doporučení práce](./intelligent-recommendations.md#job-recommendations) – Pokud je na vašem kariérním webu zveřejněno více než deset nabídek práce, Attract nabízí potenciálním uchazečům návrhy práce.
- [Integrace Broadbean](./posting-jobs-external.md#post-jobs-to-broadbean) – práci je možné zveřejňovat ze systému Attract do Broadbean, což je externí web pro nabídku práce. Po povolení této funkce náhledu je nutné dokončit nastavení zadáním uživatelského jména, ID klienta a šifrovacího tokenu pro Broadbean.
- [Analytika](./analytic-reports.md) – Náborové týmy mohou zobrazit klíčové metriky pro jednu práci pomocí analytiky práce a agregované metriky napříč všemi pracemi v centru analytiky.
- [EEO](./activities-attract.md) – nové typy aktivit umožňují použití předdefinovaného formuláře pro shromažďování údajů o rovných zaměstnaneckých příležitostech (EEO) a kanceláře programu kompatibility pro federální smlouvy (OFCCP) od uchazeče. Předdefinovaný formulář nelze upravovat.
- [Doporučení potenciálního zaměstnance](./intelligent-recommendations.md#prospect-recommendations) – aplikace Attract prověří minulé uchazeče a současné uchazeče a vytvoří seznam potenciálních zaměstnanců pro danou pozici.
- [Vyhledávání podle relevance](./attract-talent-pools.md#search-and-view-candidate-profiles) – můžete prohledat celou kandidátskou databázi na konkrétní dovednosti, jména nebo historii vzdělávání. Attract prohledá celý profil a zvýrazní všechny shody, které najde. Attract také prohledává všechny dokumenty, které jsou pro kandidáta k dispozici, a inteligentně řadí výsledky vyhledávání.
- [Cílová skupina aktivity](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – Můžete nastavit cílovou skupinu aktivit (jako pohovor, plán nebo zpětná vazba) na **Všichni uchazeči**, **Interní uchazeči** nebo **Externní uchazeči**. Můžete dodávat vlastní aktivity, jako jsou například YouTube videa, webový obsah a Microsoft Forms všem uchazečům, pouze interním uchazečům, pouze externím uchazečům nebo náborovému týmu.
- [Zažádat pomocí LinkedIn](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Na svém kariérním webu Attract můžete nastavit možnost umožňující uchazečům zažádat pomocí služby LinkedIn. Tato funkce zjednodušuje proces žádosti pro vaše uchazeče tím, že jim umožní používat jejich profil ve službě LinkedIn, který automaticky vyplní jejich žádosti na vašem kariérním webu.
- [Sledování zdroje](./source-tracking.md) – Attract sleduje zdroje žádostí uchazečů a poskytuje cenné informace, které vám mohou pomoci zaměřit se na vaše úsilí při náboru. Můžete také vybrat zdroj žádosti při ručním přidávání kandidáta k práci nebo skupině talentů.
- [Stříbrný medailista](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – Pokud se uchazeči zdají pro vaši organizaci skvěle vhodní, ale nabídku pro aktuální pozici nerozšiřujete, můžete je označit jako stříbrná medailisty. Tato funkce pomáhá zkrátit čas věnovaný náboru při příštím zpřístupnění podobné pozice.

### <a name="core-hr"></a>Základní lidské zdroje

- [Ověřit data hierarchie pozic](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – můžete ověřit manažerskou hierarchii pro všechny cyklické odkazy, které byly neúmyslně importovány.
- [Určení kódů důvodů pro typy odchodu](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – můžete zadat kódy důvodů pro typy odchodu.
- [Vyžadovat kódy důvodu v žádostech o volno](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – Kromě určení kódů důvodu pro typy dovolených můžete požadovat kódy důvodu pro požadavky na odchod.
- [Zadání seznamu transakcí volna a absence pro HR](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – můžete zobrazit seznam transakcí volna a absencí, které vám pomohou poskytnout přehledy do zůstatků volna.

### <a name="onboard"></a>Zaškolení

V současné době nejsou k dispozici žádné funkce náhledu pro Onboard.

## <a name="feedback"></a>Zpětná vazba

Rádi bychom se o vás dozvěděli něco o zkušenostech s těmito funkcemi náhledu. Doporučujeme vám pravidelně zveřejňovat zpětnou vazbu na následujících webech během používání těchto a dalších funkcí:

- [Komunita](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – tento web je skvělým zdrojem, kde mohou uživatelé diskutovat o případech použití, ptát se a získat nápovědu komunity.
- Dejte nám vědět, jaké funkce chcete zobrazit v produktu nebo o jakýchkoli změnách, které by měly podle vašeho názoru být provedeny u existujících funkcí. Pomocí následujících webů navrhujte nápady k produktům:

    - [Nápady Attract](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Nápady Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Nápady Onboard](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Neuvádějte ve zpětné vazbě nebo recenzích na produkty své osobní údaje (některé informace, které by vás mohly identifikovat). Shromážděné informace mohou být dále analyzovány a nebudou použity k odpovídání na žádosti v rámci platných zákonů o ochraně osobních údajů. Osobní údaje, které jsou získány samostatně v rámci těchto programů, se řídí [Prohlášením společnosti Microsoft o ochraně osobních údajů](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Toto téma si uložte do záložek a často se vracejte, abyste měli informace o nových funkcích náhledu, když je vydáme.

## <a name="see-also"></a>Viz také

- [Vyzkoušení nebo nákup aplikací Talent](https://dynamics.microsoft.com/talent/overview/)
- [Novinky](./whats-new.md)
- [Poznámky k verzi](https://docs.microsoft.com/business-applications-release-notes/index)
- [Získání podpory pro Talent](./talent-support.md)

---
title: Přístup k funkcím náhledu v aplikaci Talent
description: Toto téma popisuje, jak může správce povolit funkce náhledu, a uvádí seznam funkcí, které jsou nyní povoleny pro náhled.
author: andreabichsel
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 060a36185641d5bb7912631b7c857c5c4331c8b7
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "856317"
---
# <a name="access-preview-features-in-talent"></a>Přístup k funkcím náhledu v aplikaci Talent

[!include[banner](../includes/banner.md)]

V rámci našeho průběžného přidávání schopností produktu chceme, aby zákazníci co nejdříve měli k dispozici nové funkce. Správci mohou zobrazit a používat funkce náhledu v rámci prostředí. Tyto funkce jsou téměř připraveny k obecné dostupnosti a prošly rozsáhlým testováním. Právě hledáme další z zpětnou vazbu od zákazníků a ověření před tím, než je vydáme do všeobecného oběhu.

Toto téma popisuje, jak může správce povolit funkce náhledu, a uvádí seznam funkcí, které jsou nyní k dispozici pro náhled. Tento seznam bude aktualizován s tím, jak budou vydávány nové funkce pro všeobecnou dostupnost a nové funkce, které budou uvolněny k zobrazení náhledu. Při uvolnění funkcí k náhledu není vydáno žádné upozornění. Uživatelé jen uvidí funkce.

## <a name="enable-or-disable-preview-features"></a>Povolit nebo zakázat funkce náhledu

Nastavení **funkcí náhledu** můžete použít v centru pro správu aplikace Microsoft Dynamics 365 for Talent pro povolení nebo zakázání funkcí náhledu. Ve výchozím nastavení je toto nastavení vypnuté. Akce povolení nebo zakázání funkcí náhledu se vztahuje ke konkrétnímu prostředí.

> [!IMPORTANT]
> Zapnutím nastavení **Funkce náhledu** povolíte funkce Náhledu pro všechny uživatele ve vaší organizaci, kteří jsou v prostředí. Vypnutím nastavení zakážete funkce náhledu a způsobíte, že budou uživatelům nepřístupné. Funkce náhledu mají v aplikaci Talent omezenou podporu. Mohou používat méně opatření pro soukromí a bezpečnostních opatření a nejsou zahrnuty do smlouvy o úrovni služeb aplikace Talent. Neměli byste je používat ke zpracování osobních údajů (to znamená všech informací, které vás mohou identifikovat), nebo ke zpracování jiných dat, které podléhají požadavkům na vyhovění zákonům nebo předpisům.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Povolit nebo zakázat funkce náhledu ve vaší organizaci

#### <a name="attract"></a>Upoutat

1. Přihlaste se do aplikace Microsoft Dynamics 365 for Talent: Attract.
2. V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **nastavení pro správu**.
3. Na kartě **správa funkcí** vyberte možnost vedle položky **náhled funkce**, aby se zbarvila modře.
4. Volitelně můžete ovládat konkrétní povolením/zakázáním konkrétních funkcí na této stránce.
5. Aktualizujte prohlížeč tak, abyste viděli nové funkce. (Všichni uživatelé, kteří jsou již přihlášeni, uvidí funkce při příštím přihlášení, nebo mohou aktualizovat svůj prohlížeč, aby funkce viděli okamžitě.)

#### <a name="core-hr"></a>Základní lidské zdroje

1. Přihlaste se do aplikace Talent. Otevře se pracovní prostoru základní lidské zdroje, ze kterého provedete další kroky. 
2. Vyberte **Správa systému \> Odkazy na systémové parametry**.
3. Na stránce **systémové parametry** na kartě **funkce náhledu** nastavte možnost **Povolit režim náhledu pro všechny uživatele** na možnost k **Ano** pro zpřístupnění funkcí náhledu.

> [!NOTE]
> Při zakázání náhledu funkce použijte stejné základní kroky. Když funkce náhledu zakážete, budou nepřístupné pro uživatele a v procesech, které jsou spojeny s funkcemi, může dojít k chybám.

## <a name="features-that-are-currently-in-preview"></a>Funkce, které jsou aktuálně v náhledu

### <a name="attract"></a>Upoutat

- **Relevantní uchazeči o pozici** – náboráři a manažeři náboru se mohou snadno podívat, kteří uchazeči ze všech mohou být nejvhodnější pro danou pozici. Je uvedeno nejlepších 5 uchazečů na základě relevantnosti jejich životopisu/profilu vůči popisu práce.
- **Relevantní pracovní pozice** – uchazeči nyní uvidí seznam dalších pracovních pozic, které jsou pro ně relevantní, na základě jejich životopisu/ profilu a popisů práce.  Aktuálně se zobrazuje uchazečům, jakmile zažádají o návrh dalších pracovních příležitostí.
- **Podpora EEO/OFCCP** – nové typy aktivit umožňují použití předdefinovaného formuláře pro shromažďování údajů o rovných zaměstnaneckých příležitostech (EEO) a kanceláře programu kompatibility pro federální smlouvy (OFCCP) od uchazeče.  Tento formulář je předdefinovaný a nelze ho upravovat.

    > [!NOTE]
    > Zveřejněná pracovní místa se zobrazí pouze zákazníkům, kteří mají předplacený jeden nebo více produktů seznamu volných míst ve službě LinkedIn. Jinak zákazníci pracovní místo uvidí pouze v případě, že je explicitně hledají. Při zveřejnění pracovního místa na webu LinkedIn nastalo zpoždění. Po zveřejnění z aplikace Abstract může trvat několik hodin, než se pracovní místo objeví.

- **Žádost uchazeče** – interní i externí uchazeči nyní mohou žádat o místa přímo ze stránky pracovních míst na kariérním webu.
- **Správa nabídek** – uživatelé mohou nyní vytvářet nabídkové dopisy ze šablony, které obsahují zástupné symboly. S tím, jak uživatelé procházejí fázemi nabídky, náboráři a manažeři pro zaměstnance mohou pomocí nástroje Nabídka připravit formální nabídku pro uchazeče pomocí šablon pro zaslání nabídek na interní schválení a nakonec odeslat nabídku zájemci k podpisu. Do nástroje Nabídka budou průběžně přidávány nové možnosti a funkce náhledu bude o tyto možnosti aktualizována, jak budeme připraveni je vydávat k náhledu.

### <a name="core-hr"></a>Základní lidské zdroje

- **Otevřená registrace** Otevřená registrace výhod zaměstnancům dává jednoduché, samoobslužné možnosti výběru výhod. Správci lidských zdrojů (HR) mohou konfigurovat proces zaměstnaneckých výhod pro svou organizaci a možnosti registrace pro zaměstnance s použitím snadno řízeného řešení.

## <a name="feedback"></a>Zpětná vazba

Bez ohledu na to, zda je zpětná vazba kladná nebo záporná, chceme znát váš názor o vašem používání funkcí náhledu. Doporučujeme vám pravidelně zveřejňovat zpětnou vazbu na následujících webech během používání těchto a dalších funkcí.

- [Komunita](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – tento web je skvělým zdrojem, kde mohou uživatelé diskutovat o případech použití, ptát se a získat nápovědu komunity.
- Pomocí následujících webů můžete navrhovat nápady k produktům. Dejte nám vědět, jaké funkce chcete zobrazit v produktu, a také o jakýchkoli změnách, které by měly podle vašeho názoru být provedeny u existujících funkcí.

    - [Nápady](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Základní lidské zdroje](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Neuvádějte ve zpětné vazbě nebo recenzích na produkty své osobní údaje (některé informace, které by vás mohly identifikovat). Shromážděné informace mohou být dále analyzovány a nebudou použity k odpovídání na žádosti v rámci platných zákonů o ochraně osobních údajů. Osobní údaje, které jsou získány samostatně v rámci těchto programů, se řídí [Prohlášením společnosti Microsoft o ochraně osobních údajů](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Toto téma si uložte do záložek a často se vracejte, abyste měli informace o nových funkcích náhledu, když je vydáme.

---
title: "Funkce kariérního webu v systému Attract"
description: "Tento článek uvádí přehled funkce kariérního webu určené pro uchazeče v aplikaci Microsoft Dynamics 365 for Talent - Attract. Také popisuje postup nastavení této funkce."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: cs-cz
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Funkce kariérního webu v systému Attract

[!include [banner](includes/banner.md)]

Tento článek uvádí přehled funkce kariérního webu určené pro uchazeče v aplikaci Microsoft Dynamics 365 for Talent: Attract. Také popisuje postup nastavení této funkce.

## <a name="overview"></a>Přehled

Attract poskytuje jeden kariérní web pro každé prostředí v klientovi. Pokud například organizace používá prostředí pro vývoj a testovací prostředí, je poskytován jeden kariérní web pro vývojové prostředí a jiný pro testovací prostředí. Každý kariérní web však je **zcela nezávislý** a má vlastní mechanismus ověřování. Mezi kariérními weby nejsou sdíleny pracovní pozice a profily uchazečů.

Ve výchozím nastavení je kariérní web veřejný. Proto mohou kandidáti zobrazit všechna pracovní místa, která jsou označena jako externí, aniž by se museli přihlásit. Všechny ostatní akce však vyžadují, aby se uchazeči přihlásili.

## <a name="career-site-management"></a>Správa kariérního webu

Následující položky na kariérním webu jsou řízeny nastaveními:

- **Název organizace:** Název organizace se objevuje v navigačním panelu v horní části kariérního webu. Když uchazeč vybere název organizace, přejde na stránku se seznamem všech otevřených pracovních míst.
- **Logo organizace:** V levém horním rohu kariérního webu se zobrazuje obrázek loga organizace. Když uchazeč vybere obrázek loga, přejde na stránku se seznamem všech otevřených pracovních míst.

Pokud chcete nastavit hodnoty pro název a logo organizace, přihlaste se k systému Attract jako správce, vyberte **Centrum pro správu** v nabídce **Nastavení** nabídky (symbol ozubeného kola) a pak vyberte kartu **informace o společnosti**.

> [!NOTE]
> Obrázek loga, který se zobrazí na stránce kariérního webu, má pevnou výšku 20 pixelů (px). Obrázek, který přidáte do Centra pro správu, se přizpůsobuje stránce. Proto se může šířka měnit v závislosti na obrázku.

## <a name="career-site-url"></a>Adresa URL kariérního webu

Když [zveřejníte externí pracovní pozici](./Creating-jobs-Attract.md#postings) poprvé, můžete zkopírovat odkaz **Použít** z aplikace Attract. Adresa URL pro tento odkaz bude v následujícím formátu: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Adresa URL kariérního webu je dílčí řetězec pro **použití** adresy URL. Sestává ze všech položek až k názvu společnosti. Proto je pro předchozí adresu URL pro **použití** adresa URL kariérního webu `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Možnosti ověřování

Uchazeči mají k dispozici následující možnosti přihlašování ke kariérním webu Attract:

- Osobní účet:

    - LinkedIn
    - Microsoft 
    - Google
    - Facebook

- Pracovní nebo školní účet:

    - Microsoft Azure Active Directory (Azure AD)

Přihlašování ke službě Azure AD je určeno pouze pro interní uchazeče. Proto funguje pouze pro interní uchazeče, kteří používají své přihlašovací údaje služby Azure AD. Například uchazeč, který je aktuálně zaměstnancem společnosti Contoso Ltd., chce zažádat o zaměstnání v nesouvisející společnost Alpine Ski House. V takovém případě přihlášení nebude úspěšné, pokud se zaměstnanec pokusí použít své přihlašovací údaje ke službě Azure AD od společnosti Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Vytvoření a správa profilu

Poté, co se uchazeči přihlásí ke kariérnímu webu, mohou vybrat **Můj profil** na navigačním panelu v horní části stránky, kde mohou vytvořit a spravovat svůj profil. Profil obsahuje osobní údaje, údaje o pracovních zkušenostech, podrobnostech o vzdělání, dokumenty, odkazy a informace o kvalifikačních předpokladech. Po vytvoření lze profil použít k zažádání o pracovní místa, o která má uchazeč zájem. Profily také pomáhají systému Attract doporučit správná pracovní místa uchazečům.

## <a name="find-the-right-job"></a>Vyhledání správné práce

Na stránce se seznamem práce mohou uchazeči vyhledat určité pracovní místo zadáním hledaných pojmů. Funkce vyhledávání vyhledá hledané termíny v názvech a popisech pracovní pozice a zobrazí jako výsledky relevantní pracovní místa. Uchazeči mohou kdykoli filtrovat výsledky na základě místa výkonu práce nebo pracovní funkce.

Uchazeči také mohou zobrazit sadu doporučených pracovních míst na kariérním webu. Pracovní místa, která jsou uchazeči doporučena, jsou založena na minulých žádostech uchazeče, profilu a životopisech.

> [!NOTE]
> Doporučení pracovních míst se zobrazí pouze v případě, že je na kariérním webu zveřejněno nejméně 10 pracovních míst, a pokud uchazeč vyplnil svůj profil.

## <a name="apply-for-jobs"></a>Žádost o práci

Poté, co uchazeči najdou správnou práci, mohou o ni zažádat pomocí tlačítka **použít** na stránce podrobností o pracovním místě. V tomto okamžiku mohou uchazeči vytvořit zcela nový profil nebo zkontrolovat informace ve svém existujícím profilu. Uchazeči také mohou nahrát podle potřeby životopis a odeslat žádost o práci.

## <a name="check-application-status"></a>Kontrola stavu žádosti

Poté, co uchazeči zažádají o jedno nebo více pracovních míst, mohou na navigačním panelu v horní části stránky vybrat možnost **Žádosti** k zobrazení otevřených a uzavřených žádostí. Jakmile uchazeči otevřou některou ze svých žádostí, uvidí aktuální fázi a jakékoli čekající položky akcí, které je nutné dokončit. Pokud musí například uchazeč poskytnout potenciální data pro pohovor mezi čtyřma očima, na stránce se zobrazí jeho možnosti.

## <a name="internal-jobs"></a>Interní pracovní pozice

V současné době se pracovní pozice, které jsou označeny jako interní a publikované na kariérním webu Attract, na kariérním webu nezobrazují. Jsou přístupné pouze prostřednictvím přímé adresy URL **Použít**, kterou lze kopírovat z aplikace Attract.


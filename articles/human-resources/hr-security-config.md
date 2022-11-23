---
title: Koncepce konfigurace zabezpečení pro integrace založené na virtuálních tabulkách
description: Tento článek vysvětluje architekturu pro vytváření integrace mezi Microsoft Dynamics 365 Human Resources a další systémy.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759648"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Koncepce konfigurace zabezpečení pro integrace založené na virtuálních tabulkách

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje architekturu pro použití [virtuálních tabulek Microsoft Dataverse (entit)](/dev-itpro/power-platform/virtual-entities-overview) k vytvoření integrace mezi Dynamics 365 Human Resources a systémem třetí strany. Článek se zaměřuje na konfiguraci zabezpečení a na aspekty ověřování a autorizace, které jsou vyžadovány mezi hranicemi systému k vybudování funkčního a bezpečného systému.

## <a name="prerequisite-reference-articles"></a>Nezbytné referenční články

Další informace konceptech v tomto článku jsou uvedeny v následujících článcích:

- [Přehled virtuálních entit](/dev-itpro/power-platform/virtual-entities-overview)
- [Začínáme s virtuálními tabulkami (entitami)](/developer/data-platform/virtual-entities/get-started-ve)
- [Používání ověřování mezi servery pro více tenantů (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Použivání ověřování OAuth s Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [Tok přihlašovacích údajů klienta OAuth 2.0 na platformě Microsoft identity](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Ověřování a autorizace](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Architektura 

Následující architektonické schéma ukazuje hlavní koncepty, které jsou součástí integrace využívající virtuální tabulky (entity).

![Integrace založená na virtuálních tabulkách.](./media/Hosts.jpg)

Zde je vysvětlení některých prvků v předchozím diagramu:

- **Microsoft** – Microsoft hostuje a provozuje různé produkty Dynamics 365 jménem zákazníků.

    - **Azure Active Directory (Azure AD) tenant C** – Tenant Azure AD, který je ve vlastnictví společnosti Microsoft. Je to tenant, ve kterém jsou aplikace Dynamics 365 registrovány.

- **Integrující partner**

    - **Integrující systém** – Systém, který je integrován s Dynamics 365. Může to být mzdový systém nebo jakýkoli systém, který se spoléhá na data uložená v Dynamics 365.
    - **Adaptér** – Software nebo služba, která je zodpovědná za interakci s Dynamics 365 a integrujícím systémem.

        > [!NOTE]
        > Pokud je adaptér zamýšlen pro použití více zákazníky Dynamics 365, očekává se, že bude registrován jako aplikace pro více klientů v Azure AD.

    - **Azure AD tenant A** – Tenant Azure AD, který je ve vlastnictví integrujícího partnera. Je to tenant, ve kterém je registrováno ID aplikace adaptéru.

- **Vzájemný zákazník** – Zákazník, který implementuje Dynamics 365 Human Resources a řešení integrujícího partnera.

    - **Dynamics 365 Finance nebo Human Resource** – Instance Dynamics 365 Finance nebo Human Resources specifická pro zákazníka, která obsahuje zákaznická data, která integrující systém vyžaduje.
    - **Dataverse** – Prostředí Dataverse specifické pro zákazníka, které je propojeno buď s Financemi, nebo Human Resources. Dataverse poskytuje webové rozhraní API pro interakci s daty Dynamics 365.
    - **Azure AD tenant B** – Tenant Azure AD zákazníka. Funguje jako poskytovatel identity (autorizační server) a vydává tokeny, které opravňují volající volat instanci Dataverse zákazníka.

## <a name="basic-request-flow"></a>Základní tok požadavku

Tato část popisuje základní tok typického požadavku, který je součástí integrace. Odkazuje na architektonické schéma dříve v tomto článku.

Typický požadavek vyžaduje, aby se adaptér dotazoval Dynamics 365 na data a poté tato data uložil a synchronizoval s integrujícím systémem.

1. Adaptér volá webové rozhraní API Dataverse pro dotazování na relevantní data.

    > [!NOTE]
    > Nezbytnou podmínkou je ověření a získání tokenu je hlavní součástí procesu. Ověřování bude popsáno v části [Ověřování a autorizace na hranicích systému](#authentication-and-authorization-at-system-boundaries).

    Toto volání je provedeno proti webovému rozhraní API Dataverse pro dotazování na data aplikace, která jsou vystavena prostřednictvím virtuální tabulky. (Viz „2. Počáteční synchronizace“ a „3. Rozdílová synchronizace“ v diagramu.)

2. Dataverse zpracuje požadavek dotazem na virtuální tabulku prostřednictvím pluginu virtuální entity („Proxy virtuální tabulky“ v diagramu). Požadavek Dataverse je předán do služby virtuální entity Finance nebo Human Resources za účelem dotazu na data, která jsou fyzicky uložena v databázi Finance nebo Human Resources.
3. Služba virtuální entity Finance nebo Human Resources převede požadavek na virtuální entitu do dotazu na entitu Finance nebo Human Resources, která podporuje virtuální entitu Dataverse. Data jsou načtena z databáze, přeložena zpět do reprezentace entity Dataverse a vrácena volajícímu.
4. Adaptér dokončí veškeré požadované mapování a překlad dat a zavolá integračnímu systému, aby data uchoval v databázi integračního systému. (Viz „4. Uložit data“ v diagramu.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Ověřování a autorizace na hranicích systému

*Ověřování* ověřuje, že totožnost uživatele nebo aplikace byla prokázána, a potvrzuje, že uživatel nebo aplikace jsou tím, za koho se vydávají. *Autorizace* uděluje uživateli nebo aplikaci právo přístupu ke konkrétním oprávněním na úrovni aplikace. Více informací viz [Ověřování vs. autorizace](/azure/active-directory/develop/authentication-vs-authorization).

Většina volání mezi systémy v architektonickém diagramu dříve v tomto článku zahrnuje adaptér. Adaptér se musí sám ověřit, aby mohl provést následující volání:

- Volání Dataverse
- Volání do integračního systému

Podívejte se na hranice systému v diagramu. Každý webový požadavek mezi systémy musí být ověřen a před vrácením dat volajícímu musí projít autorizační kontroly na úrovni aplikace. U požadavku na virtuální tabulku Dynamics 365, která je podporována Finance nebo Human Resources, jsou kontroly ověřování a autorizace vynuceny na následujících hranicích systému:

- Hovor mezi adaptérem a koncovým bodem webového rozhraní API Dataverse (OData)
- Volání mezi modulem plug-in virtuální entity Dataverse a službou virtuální entity Finance nebo Human Resources

V obou případech se nejprve provádějí kontroly ověřování. Poté se provedou kontroly autorizace na úrovni aplikace, aby se zajistilo, že ověřený uživatel nebo aplikace má správná oprávnění na úrovni aplikace k načtení požadovaných dat.

Autentizace pro volání Dataverse je zpracována prostřednictvím nosného tokenu, který musí být zahrnut jako hlavička HTTP ve webovém požadavku na Dataverse. Adaptér musí získat token od instance Azure AD tenanta B. (Viz „1. Získat token“ v diagramu.) Azure AD působí jako poskytovatel identity v toku ověřování.

Adaptér se ověřuje poskytnutím identity své aplikace (netajné, jak je registrováno v tenantu A Azure AD) a tajného klíče nebo certifikátu aplikace, který má pouze aplikace adaptéru.

Poté, co byl uživatel nebo aplikace ověřena pro volání Dataverse, u každého požadavku se provádějí kontroly autorizace na úrovni Dataverse. Tyto kontroly zajišťují, že volající (identita aplikace adaptéru, která je označena „\<guid A\>“ v diagramu) má příslušná oprávnění aplikace. Autorizace na úrovni aplikace je spravována v Dataverse prostřednictvím uživatele aplikace, který představuje ID aplikace adaptéru. Oprávnění na úrovni aplikace se spravují udělením přístupu konkrétním rolím aplikace definovaným v Dataverse Tyto role poskytují aplikaci podrobná oprávnění.

Podrobnější návod viz [Použijte ověřování typu mezi servery pro více klientů](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Pokud projdou kontroly oprávnění aplikace na úrovni Dataverse, plugin virtuální entity zavolá koncový bod služby virtuální entity v prostředí Finance nebo Human Resources. K tomuto volání se používá ověřování mezi servery (S2S). Používá identitu a tajný klíč, které jsou nakonfigurovány v záznamu konfigurace virtuálního zdroje dat Finance a provoz.

![Záznam konfigurace virtuálního zdroje dat Finance a provoz v prostředí sandbox.](./media/sandbox.jpg)

Další informace viz [Konfigurace virtuálních entit Dataverse](/dev-itpro/power-platform/admin-reference).

Volání z pluginu virtuální entity Dataverse pro Finance nebo Human Resources obsahuje identitu adaptéru původního volání do Dataverse z adaptéru (identita, která je označena „\<guid A\>“ v architektonickém schématu). Pokud je zdroj dat virtuální entity správně nakonfigurován a kontroly autentizace S2S projdou, služba virtuální entity ve Finance nebo Human Resources spustí dotaz v kontextu původního volajícího (adaptér, \<guid A\>). Budou provedeny kontroly oprávnění aplikace (autorizace) na úrovni Finance nebo Human Resources, aby se zajistilo, že adaptér má oprávnění, která jsou vyžadována pro přístup k datovým entitám požadovaným prostřednictvím dotazu.

Zabezpečení Finance a Human Resources je řízeno následujícími způsoby:

1. Mapováním identity adaptéru (\<guid A\>) konkrétnímu uživateli Finance a Human Resources. Toto mapování se provádí na stránce **Aplikace Azure Active Directory**. Další informace naleznete v tématu [Registrace externí aplikace](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Udělením příslušných rolí, povinností a oprávnění na úrovni aplikace uživateli Finance and Human Resources. Další informace viz [Zabezpečení na základě rolí](/dev-itpro/sysadmin/role-based-security).

Pokud jsou aplikaci adaptéru (\<guid A\>) udělena oprávnění, která jsou vyžadována pro přístup k požadovaným datům, dojde k následujícím událostem:

1. Je spuštěn dotaz.
2. Data jsou přeložena zpět na stránku entity Dataverse.
3. Data jsou vrácena do adaptéru.

> [!IMPORTANT]
> Během vývoje lze adaptér spustit pomocí uživatele Finance nebo Human Resources, který má roli správce. V produkčním prostředí by však adaptér nikdy neměl být spouštěn s oprávněními správce.

## <a name="key-takeaways"></a>Klíčové poznatky

Zde jsou některé důležité důsledky architektury virtuální tabulky nebo entity:

- Konfigurace zabezpečení pro virtuální tabulky, které jsou podporovány Human Resources, je spravována v Human Resources.
- Zákazník („Vzájemný zákazník“ v architektonickém diagramu dříve v tomto článku) má plnou kontrolu nad tím, jaká oprávnění jsou udělena identitě integrujícího adaptéru (označené „\<guid A\>“ ve schématu).
- Zákazník je odpovědný za správnou konfiguraci zabezpečení svého prostředí Human Resources. Integrující partner, který vytváří adaptér, musí poskytnout pokyny ohledně oprávnění, která adaptér vyžaduje.

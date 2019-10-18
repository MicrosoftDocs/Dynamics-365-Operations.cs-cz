---
title: Rozšíření aplikace Talent pomocí PowerApps a Microsoft Flow - příkladové scénáře
description: Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent používající Microsoft PowerApps a Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7bc3a18327f2d32770176eddcb7200681f0fb0da
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008052"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Rozšíření aplikace Talent pomocí PowerApps a Microsoft Flow - příkladové scénáře

Toto téma popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent používající Microsoft PowerApps a Microsoft Flow. Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí PowerApps. Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.

> [!IMPORTANT]
> Pokud chcete používat šablony a aplikaci, které jsou popsány v tomto tématu „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.


## <a name="prerequisites"></a>Předpoklady

- Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.
- Pro export nebo import aplikací musí mít uživatelé licenci PowerApps Plan 2 nebo zkušební licenci PowerApps Plan 2.

## <a name="flow--form-connect"></a>Tok – připojení k formuláři

Šablonu **Tok – připojení k formuláři** lze použít ke čtení dat z Microsoft Forms a ukládat je do entity Common Data Service.

Tuto šablonu lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře. Několik příkladů:

- Zaznamenání hodnocení kandidáta.
- Zaznamenání výsledků z dotazníků kurzu.
- Kompilace knihovny otázek na pohovoru pro správce lidských zdrojů.
- Zaznamenání hodnocení kandidáta z procesu pohovoru

V aplikaci Microsoft Dynamics 365: Attract lze zobrazit formuláře na portálu kandidáta a kandidáti mohou vyplnit podrobnosti. Formuláře lze také integrovat jako aktivity do šablony práce.

Když kandidát odešle formulář, Microsoft Flow zaznamená odeslání formuláře, přečte data a uloží je do entity Common Data Service.

Chcete-li stáhnout šablonu **Flow – Form Connect** a strukturu vlastní entity, přejděte na [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) v Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Zahájení a extrakce parametrů předaných do Powerapps

Šablonu **Zahájení a extrakce parametrů předaných do Powerapps** lze použít jako výchozí bod pro všechny scénáře PowerApps specifické pro aplikaci Attract. Obsahuje všechny výchozí parametry, které jsou předávány aplikací Attract, jako je například **Žádost o práci**, **ID kandidáta** a **ID práce**.

Tato šablona může být použita k získání hodnotícího formuláře kandidáta, aby náborový manažer mohl zobrazit hodnocení, které kandidát vyplnil.

Aplikace, které jsou vytvořeny s použitím PowerApps lze vložit do šablony práce v aplikaci Attract.

Chcete-li stáhnout šablonu **Zahájení a extrakce parametrů předaných do Powerapps** a strukturu vlastní entity, přejděte na [Zahájení a extrakce parametrů předaných do Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) v Microsoft Download Center.

## <a name="integration-with-office-365"></a>Integrace s aplikací Office 365

Aplikaci **Integrace s Office 365** lze použít k extrakci informací o týmu pro přihlášené uživatele z Microsoft Office 365. Odkazuje zaměstnance v aplikaci Talent na extrakci podrobností příchodu a odchodu a záznamy výjimek. Podrobnosti příchodu a odchodu jsou uloženy ve vlastních entitách Common Data Service. Předpokladem je, že tyto údaje jsou vyplňovány ze systémů třetích stran prostřednictvím integrace.

Tuto aplikaci lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře. Například ji lze použít pro zobrazení informací o dovolené týmu, událostech kalendáře a jakýchkoliv událostech specifických pro tým.

Chcete-li stáhnout aplikaci **Integrace s Office 365** a Strukturu entity zákazníka, přejděte na [Integrace s Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) v Microsoft Download Center.

## <a name="flow--email-notification"></a>Tok – E-mailové oznámení

Šablonu **Tok – E-mailové oznámení** lze použít pro scénáře e-mailových oznámení. Slouží ke spouštění e-mailových oznámení pro kandidáty, které náborový tým odmítl během jakékoliv fáze náborového procesu.

Tuto šablonu můžete rozšířit ke sledování změn fáze kandidáta průběhu náborového procesu a k odesílání oznámení náborovému týmu a kandidátovi.

Obecně lze nastavit toky pro entity, které jsou uloženy v Common Data Service, pro odesílání oznámení pro události, které nastanou v aplikacích Core HR, Attract, nebo Onboard.

Chcete-li stáhnout šablonu **Tok – e-mailové oznámení**, přejděte na [Tok – e-mailové oznámení](https://go.microsoft.com/fwlink/?linkid=2082103) v Microsoft Download Center.

## <a name="flow--sql-connect-and-execute"></a>Tok – připojení k SQL a provedení

Šablona **Tok – připojení k SQL a provedení** se připojuje k serveru Microsoft SQL Server a povoluje spuštění SQL dotazů.

I když je tato šablona určena ke čtení a aktualizaci tabulek SQL, lze ji rozšířit tak, aby ji bylo možné použít pro jiné scénáře. Například ji můžete použít k vyplnění tabulky fázování v Common Data Service záznamy z SQL Serveru a pravidelné synchronizaci tabulky fázování pomocí přírůstkového nabízení z SQL Serveru.

Chcete-li stáhnout šablonu **Tok – připojení k SQL a provedení**, přejděte na [Tok – připojení k SQL a provedení](https://go.microsoft.com/fwlink/?linkid=2081789) v Microsoft Download Center.

## <a name="flow--sharepoint-integration"></a>Tok - Integrace SharePoint

Šablonu **Tok – Integrace SharePoint** lze použít ke čtení dat ze seznamu aplikace Microsoft SharePoint, porovnání seznamu s hodnotami polí pro všechny entity Common Data Service a odesílání výsledků porovnání e-mailovým oznámením. 

Organizace může míst sadu dovedností, které naléhavě vyžaduje. Tyto dovednosti mohou být uloženy v aplikaci SharePoint jako seznam SharePoint. Když kandidát požádá o práci, u které je uvedena sada požadovaných dovedností, dojde k odeslání e-mailového oznámení, pokud existuje významná shoda mezi dovednostmi kandidáta, a dovednostmi, které jsou uloženy v aplikaci SharePoint. Tímto způsobem se obsadí naléhavě požadované pozice rychleji, protože oznámení pomáhají náborovým pracovníkům kontaktovat a interně najmout kandidáty v rámci organizace.

Tuto šablonu lze rozšířit, aby ji bylo možné použít pro všechny scénáře, které zahrnují integraci SharePoint.

Chcete-li stáhnout šablonu **Tok - Integrace SharePoint**, přejděte na [Tok - Integrace SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) v Microsoft Download Center.

## <a name="referral-app"></a>Referenční aplikace
Pomocí Referenční aplikace můžete přidat kandidáty do sdílené skupiny talentů. Poskytovatel reference může zadat **Křestní jméno**, **Příjmení**, **E-mail** a **Adresa URL LinkedIn** při odesílání uchazeče. Zdrojová metadata kandidáta jsou poté naplněna informacemi o poskytovateli reference.

Tuto aplikaci můžete vložit do samoobsluhy zaměstnanců (ESS) pro odesílání poskytovatelů reference nebo ji můžete použít jako hypertextový odkaz na podnikovém portálu a spustit jako samostatnou aplikaci.

Chcete-li stáhnout **Referenční aplikaci**, přejděte na [Řešení rozšiřitelnosti Dynamics 365 Talent: Referenční aplikace](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) na webu Microsoft Download Center. Chcete-li přidat další funkce, můžete tuto aplikaci importovat a přizpůsobit ji.

## <a name="additional-resources"></a>Další zdroje

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Migrace aplikace mezi klienty a prostředími](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

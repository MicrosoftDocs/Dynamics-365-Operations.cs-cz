---
title: Rozšíření aplikace Talent o Power Apps a Power Automate
description: Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent - Attract používající Microsoft Power Apps a Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529627"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Rozšíření aplikace Talent o Power Apps a Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Talent: Attract používající Microsoft Power Apps a Microsoft Power Automate. Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí Power Apps. Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.

> [!IMPORTANT]
> Pokud chcete používat šablony a aplikaci, které jsou popsány v tomto článku „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.


## <a name="prerequisites"></a>Předpoklady

- Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.
- Pro export nebo import aplikací musí mít uživatelé licenci Power Apps Plan 2 nebo zkušební licenci Power Apps Plan 2.

## <a name="power-automate--form-connect"></a>Power Automate – připojení k formuláři

Šablonu **Power Automate – připojení k formuláři** lze použít ke čtení dat z Microsoft Forms a ukládat je do entity Common Data Service.

Tuto šablonu lze rozšířit tak, aby ji bylo možné použít pro jiné scénáře. Několik příkladů:

- Zaznamenání hodnocení kandidáta.
- Zaznamenání výsledků z dotazníků kurzu.
- Kompilace knihovny otázek na pohovoru pro správce lidských zdrojů.
- Zaznamenání hodnocení kandidáta z procesu pohovoru

V aplikaci Microsoft Dynamics 365: Attract můžete použít formuláře na portálu kandidáta, kde kandidáti vyplňují své detaily. Formuláře lze také integrovat jako aktivity do šablony práce.

Když kandidát odešle formulář, Microsoft Power Automate zaznamená odeslání formuláře, přečte data a uloží je do entity Common Data Service.

Chcete-li stáhnout šablonu **Power Automate – připojení k formuláři** a Struktur vlastní entity, přejděte na [Power Automate – připojení k formuláři](https://go.microsoft.com/fwlink/?linkid=2081988) v Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – integrace se službou SharePoint

Šablonu **Power Automate – Integrace SharePoint** lze použít ke čtení dat ze seznamu aplikace Microsoft SharePoint porovnání seznamu s hodnotami polí pro všechny entity Common Data Service a odesílání výsledků porovnání e-mailovým oznámením. 

Organizace může míst sadu dovedností, které naléhavě vyžaduje. Tyto dovednosti mohou být uloženy v aplikaci SharePoint jako seznam SharePoint. Když kandidát požádá o práci, u které je uvedena sada požadovaných dovedností, dojde k odeslání e-mailového oznámení, pokud existuje významná shoda mezi dovednostmi kandidáta, a dovednostmi, které jsou uloženy v aplikaci SharePoint. To pomáhá obsadit naléhavě požadované pozice rychleji, protože oznámení pomáhají náborovým pracovníkům kontaktovat a interně najmout kandidáty v rámci organizace.

Tuto šablonu lze rozšířit, aby ji bylo možné použít pro všechny scénáře, které zahrnují integraci SharePoint.

Chcete-li stáhnout šablonu **Power Automate – Integrace SharePoint**, přejděte na [Power Automate – Integrace SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) v Microsoft Download Center.

## <a name="referral-app"></a>Referenční aplikace

Pomocí Referenční aplikace můžete přidat kandidáty do sdílené skupiny talentů. Poskytovatel reference může zadat **Křestní jméno**, **Příjmení**, **E-mail** a **Adresa URL LinkedIn** při odesílání uchazeče. Zdrojová metadata kandidáta jsou poté naplněna informacemi o poskytovateli reference.

Tuto aplikaci můžete vložit do samoobsluhy zaměstnanců pro odesílání poskytovatelů reference nebo ji můžete použít jako hypertextový odkaz na podnikovém portálu a spustit jako samostatnou aplikaci.

Chcete-li stáhnout **Referenční aplikaci**, přejděte na [Řešení rozšiřitelnosti Dynamics 365 Talent: Referenční aplikace](https://www.microsoft.com/download/details.aspx?id=58497) na webu Microsoft Download Center. Chcete-li přidat další funkce, můžete tuto aplikaci importovat a přizpůsobit ji.

## <a name="additional-resources"></a>Další zdroje

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Migrace aplikace mezi klienty a prostředími](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

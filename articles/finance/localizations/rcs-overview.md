---
title: Regulatory Configuration Service
description: Toto téma poskytuje přehled schopností Regulatory Configuration Service (RCS) a vysvětluje, jak ke službě přistupovat.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890793"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) je samostatná služba návrhu a správy životního cyklu pro funkce globalizace bez kódování / s malým množstvím kódování. RCS umožňuje zúčastněným stranám globalizace rozšířit a přizpůsobit klíčové oblasti globalizace v oblasti daní, elektronické fakturace, regulačních zpráv, bankovnictví a obchodních dokumentů, aniž by bylo nutné zapojovat vývojáře. Tento globalizační přístup bez kódování / s malým množstvím kódování umožňuje globalizaci snazší, rychlejší a nákladově efektivnější při vytváření nebo rozšiřování.

RCS poskytuje následující možnosti:

- Podpora všech funkcí, které poskytuje elektronické výkaznictví (ER).
- Předpoklad ke konfiguraci nových globálních mikroslužeb.
- Podpora elektronické fakturace. Další informace získáte v tématu [Elektronická fakturace](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Podporuje výpočet daně. Další informace naleznete v tématu [Daňová služba](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Podpora nových funkcí globalizačních funkcí, která zjednodušuje správu životního cyklu vícekomponentních funkcí a poskytuje další možnosti konfigurace akcí a nastavení parametrů funkcí. Další informace viz [Regulatory Configuration Service – zjednodušená správa funkcí globalizace pro globalizační služby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Podpora centralizovaného publikování, ukládání a sdílení vlastních konfigurací v globálním úložišti pro zjednodušení správy konfigurace bez nutnosti použití Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Přístup k RCS

Můžete se zaregistrovat nebo přihlásit do RCS ze [stránky Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![Registrace/přihlášení k RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Na stránce **Regulatory Configuration Service** zkontrolujte a přijměte doplňkové podmínky pro používání služby a poté vyberte jedno z následujících tlačítek:

- **Zaregistrovat se**, pokud službu používáte poprvé a používáte pracovní e-mailovou adresu k zajištění prostředí služby vaší organizaci
- **Přihlásit se**, pokud jste se již do služby zaregistrovali a chcete přistupovat k prostředí vaší organizace

## <a name="regional-availability"></a>Regionální dostupnost

RCS je obecně k dispozici v následujících oblastech:

- Spojené státy americké
- Indie
- Francie
- Evropa

Úplný seznam oblastí najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="related-rcs-documentation"></a>Související dokumentace RCS

Další informace o souvisejících komponentech naleznete v následující dokumentaci:

- **Globální úložiště:**

    - [Vytvoření konfigurace ER a nahrání do globálního úložiště](rcs-global-repo-upload.md)
    - [Sdílení konfigurace v globálním úložišti](rcs-global-repo-share-configuration.md)
    - [Rozšířené filtrování v globálním úložišti](enhanced-filtering-global-repo.md)
    - [Stažení konfigurací elektronického výkaznictví z globálního úložiště](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Ukončení konfigurací v globálním úložišti](discontinuing-configurations-rcs-global-repo.md)

- **Globalizační funkce:**

    - [Regulatory Configuration Service (RCS) – Globalizační funkce](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)
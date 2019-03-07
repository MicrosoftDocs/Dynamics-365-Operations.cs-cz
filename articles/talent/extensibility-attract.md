---
title: Rozšiřitelnost v aplikaci Attract
description: Toto téma popisuje, jak můžete rozšířit aplikaci Microsoft Dynamics 365 for Talent - Attract pomocí Microsoft Power Platform.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303555"
---
# <a name="extensibility-in-attract"></a>Rozšiřitelnost v aplikaci Attract

[!include[banner](../includes/banner.md)]

Aplikace Dynamics 365 for Talent je vytvořen na platformě Common Data Service (CDS) for Apps a lze ji rozšířit různými způsoby pomocí Microsoft Power Platform a možností, které nabízí Common Data Service for Apps. Proto můžete konfigurovat a přizpůsobit systém pomocí Microsoft PowerApps a Microsoft Flow. Můžete rovněž získat další analýzy o osobách pomocí Microsoft Power BI. Kromě toho je díky novým vlastním aktivitám, jako jsou například PowerApps a Webový obsah (iframe), proces náboru přizpůsobitelní více, než kdy dříve. Díky těmto aktivitám můžete proces náboru přizpůsobit potřebám a procesům vaší firmy a zajistit, aby náborový tým i kandidáti měli bezproblémový a přizpůsobený zážitek

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Využijte výhody Microsoft Power Platform 

Protože se všechna data z aplikace Attract nachází v Common Data Service for Apps, můžete použít nástroje z Microsoft Power Platform pro začlenění vašich jedinečných firemních potřeb do aplikace Attract.

### <a name="powerapps"></a>PowerApps

Pomocí PowerApps můžete snadno vytvořit aplikace, které se připojí k datům aplikace Attract a které používají stejné výrazy jako Microsoft Excel. Aplikace, které vytvoříte pomocí PowerApps, můžete spustit na webu a na zařízení Apple iOS a Google Android.

Například můžete zjednodušit univerzitní trhy práce pro náboráře tak, že vytvoříte jednoduchou aplikaci, která jim umožní skenovat životopisy a přiřazovat kandidáty na pozici v aplikaci Attract. Popřípadě můžete vytvořit aplikaci umožňující splnění potřeb organizace na shodu s předpisy. Další informace o PowerApps a způsobu použití pro vytváření aplikací naleznete v části [Integrace dat Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Můžete použít Microsoft Flow pro vytvoření automatizovaných workflow, která běží nad daty aplikace Attract. Můžete se snadno připojit ke stovkám oblíbených aplikací a služeb, aniž by bylo nutné psát kód. Vytvářením toků, které v Common Data Service for Apps interagují s entitami Práce, Kandidát a Žádost v aplikaci Attracts můžete automatizovat různé akce. Například když kandidát přijme nabídku, může být náborovému týmu odesláno oznámení, nebo může být oznámena novinka na Twitteru. Další informace o tocích naleznete v [dokumentaci k aplikaci Microsoft Flow](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI vám umožňuje vytvořit a zobrazit vlastní sestavy a řídicí panely, které vám dávají podrobnější přehled o datech v aplikaci Attract. Další informace o Power BI a způsobu vytváření interaktivních sestav a řídicích panelů naleznete v části [Dokumentace k Power BI](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Custom activities 

Můžete přidávat vlastní aktivity, jako jsou například aplikace PowerApps a Webový obsah (iframe) na úrovni šablony procesu práce nebo při vytváření nové práce. Tyto aktivity umožňují přizpůsobení náborového procesu a přinášejí do aplikace Attract obchodní logiku, která je jedinečná pro vaši organizaci.

#### <a name="powerapps-activity"></a>Aktivity PowerApps 

Aktivita PowerApps umožňuje autorovi práce nebo šablony procesu práce integrovat aplikaci PowerApps do toku náboru. Po vytvoření a publikování aplikace můžete zadat její ID aplikace v konfiguracích aktivity. Pomocí aplikace PowerApps lze číst a zapisovat data do Common Data Service for Apps. Můžete dokonce připojit aplikaci do toku. Například máte aplikaci, kterou náboráři používají k vyplnění formuláře během provádění svých telefonních pohovorů. V takovém případě můžete propojit aplikaci do toku, který vyhodnotí, zda žadatel může být posunut dále v procesu žádosti o práci. Tento typ aktivity mohou zobrazit pouze členové náborového týmu. Další informace o nakonfigurování aktivity PowerApps naleznete v části [Aktivity v aplikaci Attract](./activities-attract.md).

> [!NOTE]
> Aktivita PowerApps je dostupná pouze s doplňkem Komplexní nábor.

#### <a name="web-content-iframe-activity"></a>Aktivita webového obsahu (iframe)

Aktivita webového obsahu (iframe) vám umožňuje vložit vlastní webové řešení, které jste vytvořili v náborovém procesu nebo na portálu kandidátů. Můžete číst a zapisovat data přímo z Common Data Service for Apps. Můžete také upravit řešení tak, aby spustilo toky nebo využilo výhod funkcí Microsoft Azure. Další informace o nakonfigurování aktivity webového obsahu naleznete v části [Aktivity v aplikaci Attract](./activities-attract.md).

> [!NOTE]
> Aktivita Webový obsah je dostupná pouze s doplňkem Komplexní nábor.

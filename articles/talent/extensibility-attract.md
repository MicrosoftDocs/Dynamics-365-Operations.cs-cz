---
title: Rozšiřitelnost v aplikaci Attract
description: Toto téma popisuje, jak můžete rozšířit aplikaci Microsoft Dynamics 365 for Talent - Attract pomocí Microsoft Power Platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505857"
---
# <a name="extensibility-in-attract"></a>Rozšiřitelnost v aplikaci Attract

[!include[banner](../includes/banner.md)]

Aplikace Microsoft Dynamics 365 for Talent je vytvořena na platformě Common Data Service a lze ji rozšířit mnoha způsoby pomocí Microsoft Power Platform a možností, které nabízí Common Data Service. Proto můžete konfigurovat a přizpůsobit systém pomocí Microsoft PowerApps a Microsoft Flow. Můžete rovněž získat další analýzy o osobách pomocí Microsoft Power BI. Kromě toho je díky novým vlastním aktivitám, jako jsou například PowerApps a Webový obsah (iframe), proces náboru přizpůsobitelní více, než kdy dříve. Díky těmto aktivitám můžete proces náboru přizpůsobit potřebám a procesům vaší firmy a zajistit, aby náborový tým i kandidáti měli bezproblémový a přizpůsobený zážitek

## <a name="extending-option-sets-in-attract"></a>Rozšíření sad možností v aplikaci Attract

**Sada možností** (rozevírací seznam) je typem pole, který může být zahrnut do entity. Definuje sadu možností. Když se sada možností zobrazí ve formuláři, používá ovládací prvek rozevíracího seznamu.  V aplikaci Attract existuje více polí, která jsou sadami možností.  Začínáme zavádět funkce pro rozšíření sad možností, počínaje polem Důvodu zamítnutí, polem Typ zaměstnání a polem Typ služebního věku.   Můžete také přidat lokalizované zobrazované popisky možnosti, které přidáte. Další informace naleznete v tématu [Přizpůsobení popisků sady možností](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Funkce publikování pracovní nabídky na LinkedIn vyžaduje použití polí **Typ zaměstnání** a **Typ služebního věku** na stránce **Podrobnosti práce**. Výchozí hodnoty v těchto polích jsou podporovány službou LinkedIn a jsou zobrazeny při publikování nabídky práce. Proto pokud publikujete nabídku práce na LinkedIn a upravujete existující hodnoty sady možností pro tato pole, práce bude nadále publikována, ale LinkedIn nezobrazí vlastní hodnoty **Typ zaměstnání** a **Typ služebního věku**.  

V následujícím seznamu jsou uvedeny kroky k aktualizaci pole **Důvod zamítnutí** s hodnotami, které jsou specifické pro váš podnik.  

1. Pokud chcete rozšířit sadu možnosti **Důvod odmítnutí**, přejděte na [web pro správu PowerApps](https://admin.powerapps.com).
2. Můžete být vyzvání k přihlášení se ke svému účtu. Zadejte své ID uživatele a heslo, které používáte pro přihlášení k Dynamics365 anebo Office365 a poté klikněte na tlačítko **Další**.
3. Na kartě **Prostředí** vyberte prostředí, které chcete spravovat, a dvakrát klikněte, abyste se dostali na kartu **Podrobnosti**.
4. Na kartě **Podrobnosti** zvolte **Centrum pro správu Dynamics 365**.
5. Vyberte instanci, kterou chcete změnit, a zvolte **Otevřít**.
6. Přejděte na **Nastavení**a pak **Přizpůsobení** a zvolte **Přizpůsobit systém**.
7. Vyhledejte entitu, pro kterou chcete rozbalit sadu možností, výběrem možnosti **Entity** a rozbalením skupiny. V tomto příkladu to bude **entita žádosti o práci**.
8. Přejděte na pole, pro které chcete rozšířit sadu možností, výběrem možnosti **Pole**. V tomto příkladu to bude **msdyn_rejectionreason**. Dvakrát klikněte na pole.
9. V poli **Sada možností** vyberte **Upravit**.
10. Vyberte ikonu **+**.
11. Zadejte **Popisek**.  (Musí to být jedinečná hodnota – žádné duplicity).
12. Zvolte **Uložit**.
13. Vyberte **Publikovat** v horní části stránky.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Využijte výhody Microsoft Power Platform 

Protože se všechna data z aplikace Attract nacházejí v Common Data Service, můžete použít nástroje z Microsoft Power Platform pro začlenění vašich jedinečných firemních potřeb do aplikace Attract.

### <a name="powerapps"></a>PowerApps

Pomocí PowerApps můžete snadno vytvořit aplikace, které se připojí k datům aplikace Attract a které používají stejné výrazy jako Microsoft Excel. Aplikace, které vytvoříte pomocí PowerApps, můžete spustit na webu a na zařízení Apple iOS a Google Android.

Například můžete zjednodušit univerzitní trhy práce pro náboráře tak, že vytvoříte jednoduchou aplikaci, která jim umožní skenovat životopisy a přiřazovat kandidáty na pozici v aplikaci Attract. Popřípadě můžete vytvořit aplikaci umožňující splnění potřeb organizace na shodu s předpisy. Další informace o PowerApps a způsobu použití pro vytváření aplikací naleznete v části [Integrace dat do Common Data Service](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Můžete použít Microsoft Flow pro vytvoření automatizovaných workflow, která běží nad daty aplikace Attract. Můžete se snadno připojit ke stovkám oblíbených aplikací a služeb, aniž by bylo nutné psát kód. Vytvářením toků, které v Common Data Service interagují s entitami Práce, Kandidát a Žádost v aplikaci Attracts můžete automatizovat různé akce. Například když kandidát přijme nabídku, může být náborovému týmu odesláno oznámení, nebo může být oznámena novinka na Twitteru. Další informace o tocích naleznete v [dokumentaci k aplikaci Microsoft Flow](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI vám umožňuje vytvořit a zobrazit vlastní sestavy a řídicí panely, které vám dávají podrobnější přehled o datech v aplikaci Attract. Další informace o Power BI a způsobu vytváření interaktivních sestav a řídicích panelů naleznete v části [Dokumentace k Power BI](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Custom activities 

Můžete přidávat vlastní aktivity, jako jsou například aplikace PowerApps a Webový obsah (iframe) na úrovni šablony procesu práce nebo při vytváření nové práce. Tyto aktivity umožňují přizpůsobení náborového procesu a přinášejí do aplikace Attract obchodní logiku, která je jedinečná pro vaši organizaci.

#### <a name="powerapps-activity"></a>Aktivity PowerApps 

Aktivita PowerApps umožňuje autorovi práce nebo šablony procesu práce integrovat aplikaci PowerApps do toku náboru. Po vytvoření a publikování aplikace můžete zadat její ID aplikace v konfiguracích aktivity. Pomocí aplikace PowerApps lze číst a zapisovat data do Common Data Service. Můžete dokonce připojit aplikaci do toku. Například máte aplikaci, kterou náboráři používají k vyplnění formuláře během provádění svých telefonních pohovorů. V takovém případě můžete propojit aplikaci do toku, který vyhodnotí, zda žadatel může být posunut dále v procesu žádosti o práci. Tento typ aktivity mohou zobrazit pouze členové náborového týmu. Další informace o nakonfigurování aktivity PowerApps naleznete v části [Aktivity v aplikaci Attract](./activities-attract.md).

> [!NOTE]
> Aktivita PowerApps je dostupná pouze s doplňkem Komplexní nábor.

#### <a name="web-content-iframe-activity"></a>Aktivita webového obsahu (iframe)

Aktivita webového obsahu (iframe) vám umožňuje vložit vlastní webové řešení, které jste vytvořili v náborovém procesu nebo na portálu kandidátů. Můžete číst a zapisovat data přímo z Common Data Service. Můžete také upravit řešení tak, aby spustilo toky nebo využilo výhod funkcí Microsoft Azure. Další informace o nakonfigurování aktivity webového obsahu naleznete v části [Aktivity v aplikaci Attract](./activities-attract.md).

> [!NOTE]
> Aktivita Webový obsah je dostupná pouze s doplňkem Komplexní nábor.

---
title: Přehled výstrah
description: Toto téma obsahuje obecné informace o výstrahách. Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 12fadd8387054db3e19d4136555724c23548e05c
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031012"
---
# <a name="alerts-overview"></a>Přehled výstrah

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>O výstrahách
Výstrahy tvoří systém oznámení pro kritické události v systému. Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne. Můžete snadno vytvořit vlastní pravidla výstrah, abyste byli upozorněni na zpožděné dodávky, smazané objednávky, změny cen nebo jiné události, na které musíte reagovat.

Při plánování podnikových zdrojů (ERP) existují některé typické scénáře, kde lze použít funkci výstrahy. Několik příkladů:

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Scénář 1: Vytvoření pravidla výstrahy pro nové prodejní objednávky

1. Otevřete stránku **Všechny prodejní objednávky**.
2. V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit vlastní oznámení**.
3. V dialogovém okně **vytvořit pravidlo výstrahy** na pevné záložce **Upozornit mě při** v poli **Událost** vyberte **Záznam byl vytvořen**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Scénář 2: Vytvoření pravidla výstrahy pro odložení data doručení

1. Otevřete stránku **Všechny nákupní objednávky**.
2. Vyberte ID nákupní objednávky pro přístup k podrobnostem o nákupní objednávce.
3. Rozbalte pevnou záložku **Záhlaví nákupní objednávky**.
4. V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit vlastní oznámení**.
5. V dialogovém okně **vytvořit pravidlo výstrahy** na pevné záložce **Upozornit mě při** v poli **Událost** vyberte **Datum doručení**.
6. V poli **Událost** vyberte **Bylo odloženo**.
    
Po ukončení dialogového okna **Vytvořit pravidlo výstrahy** se zobrazí vaše pravidlo zobrazí na stránce **Správa pravidel výstrah**. Můžete použít stránku **Správa pravidel výstrah** k aktualizaci existujících pravidel výstrah. Můžete například upravit aktivační události, aktualizovat události oznámení a aktualizovat data vypršení platnosti. Chcete-li otevřít stránku **Správa pravidel výstrah**, použijte tlačítko **Upozornit mě** na kartě **Možnosti** podokna akcí.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Co se stane, když se vytvoří pravidlo výstrahy?

Při vytváření pravidel výstrah můžete přidružit k určitému poli předem definované události. Například nastane datum zadané v poli nebo se změní obsah pole. Rovněž je možné přiřadit událost záznamům na konkrétní stránce. Například je vytvořen záznam nebo odstraněn záznam.

Vyskytne-li se u daného pole nebo u záznamu na stránce vybraná událost, odešle se vám výstraha. Například vytvoříte pravidlo, ve kterém přiřadíte **datum dodání** na řádek specifické nákupní objednávky s událostí **splatnost před určitou dobou**. Časový rámec nastavíte na pět dní. V tomto případě se výstraha odešle pět dnů po datu doručení tohoto řádku nákupní objednávky.

Dále můžete upřesnit pravidla výstrah nastavením podmínek. Například můžete být informováni o nových nákupních objednávkách vytvořených pro konkrétní dodavatele.

## <a name="preparing-for-an-alert"></a>Příprava pro výstrahu

Před nastavením pravidla výstrahy rozhodněte, kdy nebo za jakých situací chcete přijímat výstrahy. Pokud víte, o kterých událostech chcete být vyrozuměni, vyhledejte v aplikaci stránku, kde se zobrazují data, která událost způsobila. Událost může být nadcházející datum nebo nastalá specifická změna. Musíte tedy vyhledat stránku, kde je zadáno datum, nebo kde se objevuje pole, které se změní, nebo nový záznam, který je vytvořen. Jakmile máte tyto informace k dispozici, můžete vytvořit pravidlo výstrahy.

## <a name="components-of-an-alert-rule"></a>Komponenty pravidla výstrahy

Pravidlo výstrahy obsahuje pět komponent:

- **Událost** – událost, která spouští pravidlo výstrahy, může být datum nebo nastalá specifická změna, ke které dochází. Události definujete na pevné záložce **Odeslat e-mailové výstrahy pro změny stavu úlohy** dialogového okna **vytvořit pravidlo výstrahy**.
- **Podmínka** – na pevné záložce **Upozornit mě na** v dialogovém okně **Vytvořit pravidlo výstrahy** můžete vybrat rozsah podmínky, chcete-li řídit, kdy budete upozorňováni na události. Můžete použít pravidlo buď pouze pro aktuální záznam nebo na všechny viditelné záznamy na stránce. Pokud se pravidlo platí mezi právnickými osobami, můžete nastavit **celoorganizační** možnost na **Ano**.
- **Uplynutí platnosti pravidla** – na pevné záložce **Upozornit mě do** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, jak dlouho má být pravidlo výstrahy aktivní.
- **Obsah** – na pevné záložce **Upozornit mě pomocí** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit text předmětu a text zprávy, kterou by zprávy s výstrahou měly používat.
- **Uživatel** – na pevné záložce **Příjemce výstrahy** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, který uživatel by měl přijímat zprávy s výstrahou. ID uživatele je ve výchozím nastavení vybráno.

    > [!NOTE]
    > Tato možnost je omezen na správce organizace.

## <a name="email-notifications-from-alerts"></a>E-mailová oznámení z výstrah

E-mailová oznámení z výstrah dosud nejsou povolena. To bude k dispozici v budoucí aktualizaci.

## <a name="videos"></a>Videa

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Jak používat výstrahy ke sledování filtrovaných dat

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

Video [Jak používat výstrahy ke sledování filtrovaných dat](https://youtu.be/ZYKMcv6kl9s) (zobrazeno výše) je zahrnuto v [Playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupné na YouTube.

### <a name="alert-rule-options"></a>Možnosti pravidla výstrahy

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

Video [Možnosti pravidel výstrah](https://youtu.be/cpzimwOjicM)  (zobrazené výše) je zahrnuto do [Playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.



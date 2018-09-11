---
title: "Výstrahy"
description: "Toto téma poskytuje obecné informace o výstrahách v aplikaci Microsoft Dynamics 365 for Finance and Operations. Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne."
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 38309e986c1d284ed63be760745b20a5415adb4c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="alerts"></a>Výstrahy

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>O výstrahách
Výstrahy představují systém oznámení kritické události v aplikaci Microsoft Dynamics 365 for Finance and Operations. Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne. Můžete snadno vytvořit vlastní pravidla výstrah, abyste byli upozorněni na zpožděné dodávky, smazané objednávky, změny cen nebo jiné události, na které musíte reagovat.

Při plánování podnikových zdrojů (ERP) existují některé typické scénáře, kde lze použít funkci výstrahy v modulu Finance and Operations. Několik příkladů:

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
Před nastavením pravidla výstrahy rozhodněte, kdy nebo za jakých situací chcete přijímat výstrahy. Pokud víte, o kterých událostech chcete být vyrozuměni, vyhledejte v aplikaci Finance and Operations stránku, kde se zobrazují data, která událost způsobila. Událost může být nadcházející datum nebo nastalá specifická změna. Musíte tedy vyhledat stránku, kde je zadáno datum, nebo kde se objevuje pole, které se změní, nebo nový záznam, který je vytvořen. Jakmile máte tyto informace k dispozici, můžete vytvořit pravidlo výstrahy.

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

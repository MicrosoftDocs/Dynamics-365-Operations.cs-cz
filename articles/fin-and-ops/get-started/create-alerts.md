---
title: "Vytvoření výstrah"
description: "Toto téma obsahuje informace o výstrahách a vysvětluje postup při vytvoření pravidla výstrahy, abyste byli upozorněni na události, jako je například následné datum nebo nastalá specifická změna."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 5bcd02e08a4ce5b601615b39bf95362cf92d3fec
ms.contentlocale: cs-cz
ms.lasthandoff: 03/23/2018

---

# <a name="create-alerts"></a>Vytvoření výstrah

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

## <a name="getting-started"></a>Začínáme
Před nastavením pravidla výstrahy rozhodněte, kdy nebo za jakých situací chcete přijímat výstrahy. Pokud víte, o kterých událostech chcete být vyrozuměni, vyhledejte v aplikaci Microsoft Dynamics 365 for Finance and Operations stránku, kde se zobrazují data, která událost způsobila. Událost může být nadcházející datum nebo nastalá specifická změna. Musíte tedy vyhledat stránku, kde je zadáno datum, nebo kde se objevuje pole, které se změní, nebo nový záznam, který je vytvořen. Jakmile máte tyto informace k dispozici, můžete vytvořit pravidlo výstrahy.

Když vytváříte pravidlo výstrahy, je třeba definovat kritéria, která je třeba splnit dříve, než bude spuštěna výstraha. Kritérium můžete považovat například za shodu mezi výskytem události a splněním specifické podmínky. Když dojde k události, systém provede kontrolu podle podmínek, které jsou nastaveny v aplikaci Finance nd Operations..

## <a name="events"></a>Události
Událost, která spouští pravidlo výstrahy, může být datum nebo nastalá specifická změna, ke které dochází. Spouštěče událostí jsou definovány na pevné záložce **Upozornit mě při** dialogového okna **Vytvořit pravidlo výstrahy**. Dostupné události pro konkrétní pole závisí na zvoleném spouštěči.

Například když nastavujete pravidlo výstrahy pro pole **počáteční datum**, události po termínu splnění jsou vhodné. Proto je typ události **je splatno za** pro toto pole k dispozici. Pro pole, jako je například **Nákladové středisko** například není událost data splatnosti vhodná. Proto není typ události **je splatno za** k dispozici. Namísto toho je k dispozici typ události **Došlo ke změně**.

## <a name="event-types"></a>Typy událostí
Může dojít ke třem typům událostí:

- **Události typu vytvoření a odstranění** – tyto události spustí výstrahu, když je vytvořen nebo odstraněn záznam.
- **Události typu aktualizace** – tyto události vyvojají výstrahu při změně údajů určitého pole.
- **Události typu datum splatnosti** – tyto události spouští výstrahu při získání data.
    
Uživatel může provést změny. Například uživatel změní datum dodání nákupní objednávky. Alternativně mohou být provedeny změny jako součást procesu. Například pole **sstav** na stránce se změní na odráží cyklus životnosti různých procesů v systému.

## <a name="conditions"></a>Podmínky
Na pevné záložce **Upozornit mě na** v dialogovém okně **Vytvořit pravidlo výstrahy** můžete použít podmínky k řízení, kdy budete upozorňováni na události.

Můžete například určit, že systém by vás měl upozornit na změnu stavu nákupní objednávky změny, ale pouze v případě, že stav odpovídá konkrétní sadě podmínek. Konkrétně předpokládejme, že chcete být upozorněni na okamžik, kdy je stav nákupní objednávky nastaven na **Přijato**. Tato změna stavu je událostí, která spouští výstrahu.

Dále je nutné určit, na které nákupní objednávky chcete být upozorněni. Můžete například vybrat jednu z následujících možností: Tyto možnosti je definují podmínky pravidel výstrah.

- **Aktuální vybraný záznam** – obdržíte výstrahu, když se změní stav určité nákupní objednávky na **přijato**.
- **Všechny záznamy** – obdržíte výstrahu při změně stavu nákupní objednávky pro položku v aktivním zobrazení stránky. Můžete použít rozšířené filtrování dostupné na stránce k vytvoření pravidel pro konkrétní sadu záznamů. Můžete například vytvořit upozornění, které je spouštěno pro všechny nákupní objednávky pro odběratele ve skupině specifického odběratele.
    
## <a name="expiry-of-rule"></a>Uplynutí platnosti pravidla
Na pevné záložce **Upozornit mě do** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, jak dlouho má být pravidlo výstrahy aktivní.

## <a name="alert-contents"></a>Obsah výstrahy
Na pevné záložce **Upozornit mě pomocí** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit text předmětu a text zprávy, kterou by zprávy s výstrahou měly používat.

## <a name="user-id"></a>ID uživatele
Na pevné záložce **Upozornit mě pomocí** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, který uživatel by měl přijímat zprávy s výstrahou. ID uživatele je ve výchozím nastavení vybráno. Tato možnost je omezen na správce organizace.

## <a name="create-an-alert-rule"></a>Vytvoření pravidla výstrahy
1. Otevřete stránku obsahující data, která chcete sledovat.
2. V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit pravidlo výstrahy**.
3. V dialogovém okně **Vytvořit pravidlo výstrahy**, v poli **Pole** vyberte pole, které chcete sledovat.
4. V poli **Událost** vyberte typ události.
5. Na pevné záložce **upozornit mě na** vyberte jednu z možností.
6. Pokud by se pravidlo výstrahy mělo deaktivovat v určité datum, vyberte na pevné záložce **Upozornit mě do** koncové datum.
7. Na pevné záložce **Upozornit mě pomocí** v poli **Předmět** přijměte výchozí text předmětu e-mailové zprávy nebo zadejte nový předmět. Text se používá jako předmět e-mailové zprávy, kterou obdržíte, když se aktivuje výstraha.
8. Do pole **Zpráva** zadejte libovolnou zprávu. Text, který bude používán jako zpráva, kterou dostanete při spuštění výstrahy.
9. Zvolte **OK**, chcete-li uložit nastavení a vytvořit pravidlo výstrahy.


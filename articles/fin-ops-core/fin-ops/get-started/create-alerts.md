---
title: Vytváření pravidel výstrah
description: Toto téma obsahuje informace o výstrahách a vysvětluje postup při vytvoření pravidla výstrahy, abyste byli upozorněni na události, jako je například následné datum nebo nastalá specifická změna.
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 4fe97ca8e1eecdc064ad4d21d5acdeade9f33d9c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694488"
---
# <a name="create-alert-rules"></a>Vytváření pravidel výstrah

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Začínáme

Před nastavením pravidla výstrahy rozhodněte, kdy nebo za jakých situací chcete přijímat výstrahy. Pokud víte, o kterých událostech chcete být vyrozuměni, vyhledejte v aplikaci stránku, kde se zobrazují data, která událost způsobila. Událost může být nadcházející datum nebo nastalá specifická změna. Musíte tedy vyhledat stránku, kde je zadáno datum, nebo kde se objevuje pole, které se změní, nebo nový záznam, který je vytvořen. Jakmile máte tyto informace k dispozici, můžete vytvořit pravidlo výstrahy.

Když vytváříte pravidlo výstrahy, je třeba definovat kritéria, která je třeba splnit dříve, než bude spuštěna výstraha. Kritéria jsou v podstatě shoda mezi výskytem události a splněním specifické podmínky. Když dojde k události, systém začne provádět kontrolu podle podmínek, které jsou nastaveny.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Zkontrolujte, zda jsou spuštěny dávkové úlohy výstrah

Dávkové úlohy pro změnu dat a výstrahy s datem splatnosti musí být spuštěny, aby bylo možné zpracovat podmínky výstrah a odesílat upozornění. Chcete-li spustit dávkové úlohy, přejděte na **Správa systému** > **Periodické úkoly** > **Výstrahy** a přidejte novou dávkovou úlohu pro **Výstrahy na základě změn** a/nebo **Výstrahy založené na datu plnění**. Je-li vyžadována dlouhodobá a často spuštěná dávková úloha, vyberte **Opakování** a nastavte **Bez koncového data** se **Vzorcem opakování** **Minuty** a **Počet** **1**.

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

Na pevné záložce **Upozornit mě pomocí** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, který uživatel by měl přijímat zprávy s výstrahou. ID uživatele je ve výchozím nastavení vybráno. Možnost změny uživatele, který výstrahu obdrží, je omezena pouze na správce organizace.

## <a name="alerts-as-business-events"></a>Výstrahy jako obchodní události

Výstrahy lze externě odesílat pomocí architektury obchodních událostí. Při vytváření výstrahy nastavte **Pro celou organizaci** na **Ne** a **Odeslat externě** na **Ano**. Po aktivaci obchodní události pomocí výstrahy můžete spustit tok vestavěný v Power Automate pomocí spouštěče **Při výskytu obchodní události** v konektoru Finance and Operations nebo explicitně odeslat událost do koncového bodu obchodních událostí prostřednictvím **Katalogu obchodních událostí**.

## <a name="create-an-alert-rule"></a>Vytvoření pravidla výstrahy

0. Zkontrolujte, zda jsou spuštěny dávkové úlohy výstrah (viz výše).
1. Otevřete stránku obsahující data, která chcete sledovat.
2. V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit pravidlo výstrahy**.
3. V dialogovém okně **Vytvořit pravidlo výstrahy**, v poli **Pole** vyberte pole, které chcete sledovat.
4. V poli **Událost** vyberte typ události.
5. Na pevné záložce **Upozornit mě na** vyberte požadovanou možnost. Chcete-li odeslat výstrahu jako obchodní událost, zkontrolujte, že je možnost **Pro celou organizaci** nastavena na **Ne**.
6. Pokud by se pravidlo výstrahy mělo deaktivovat v určité datum, vyberte na pevné záložce **Upozornit mě do** koncové datum.
7. Na pevné záložce **Upozornit mě pomocí** v poli **Předmět** přijměte výchozí text předmětu e-mailové zprávy nebo zadejte nový předmět. Text se používá jako předmět e-mailové zprávy, kterou obdržíte, když se aktivuje výstraha. Chcete-li odeslat výstrahu jako obchodní událost, nastavte možnost **Odeslat externě** na **Ano**.
8. Do pole **Zpráva** zadejte libovolnou zprávu. Text, který bude používán jako zpráva, kterou dostanete při spuštění výstrahy.
9. Zvolte **OK**, chcete-li uložit nastavení a vytvořit pravidlo výstrahy.

## <a name="limitations-and-workarounds"></a>Omezení a zástupná řešení

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Řešení pro vytváření výstrah pro sekundární zdroje dat formuláře
Výstrahy nelze vytvořit pro některé sekundární zdroje dat ve formulářích. Například při vytváření výstrah ve formuláři účetních profilů odběratelů nebo dodavatelů jsou k dispozici pouze pole v záhlaví (CustLedger nebo VendLedger) a nikoli účty dimenzí. Řešením tohoto omezení je pomocí **SysTableBrowser** otevřít tuto tabulku jako primární zdroj dat. 
1. Otevřete tabulku ve formuláři **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Vytvořte výstrahu z formuláře SysTableBrowser.


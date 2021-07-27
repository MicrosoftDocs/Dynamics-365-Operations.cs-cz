---
title: Záznamník úloh a nápověda pro Retail Modern POS (MPOS) a Cloud POS
description: Toto téma popisuje, jak používat záznamník úloh v aplikacích Retail Modern POS (MPOS) a Cloud POS.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7b5f8303ea23f4f38bf27d35de0fa91ab82f4b5b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354462"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Záznamník úloh a nápověda pro Retail Modern POS (MPOS) a Cloud POS

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak používat záznamník úloh v aplikacích Retail Modern POS (MPOS) a Cloud POS.

## <a name="overview"></a>Přehled

Záznamník úloh v Retail Modern POS nebo Cloud POS je nové řešení, které nabízí vysokou míru odezvy. Poskytuje flexibilní aplikační programovací rozhraní (API) pro rozšíření a plynulou integraci se spotřebiteli záznamů obchodních procesů. Integrace Záznamníku úloh s nástrojem Modelování podnikových procesů (BPM) ve službě Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) se posunula kupředu. Proto mohou uživatelé dále vytvářet diagramy pro bohaté obchodní procesy ze záznamů pro analýzu a návrh aplikací.

## <a name="architecture"></a>Architektura

Záznamník úkolů může zaznamenávat akce uživatele v klientovi s přesnou věrností. Každý ovládací prvek je laděný tak, aby upozornil Záznamník úloh o provedení akce uživatele. Ovládací prvek oznámí Záznamníku úloh, že došlo k události, a předá všechny příslušné informace o odpovídající akci uživatele v reálném čase. Z těchto informací může Záznamník úloh zaznamenat typ akce uživatele (například kliknutí na tlačítko, zadání hodnoty nebo navigace) a veškerá data, která souvisí s akcí uživatele (například hodnota a typ vstupních dat, kontext formuláře nebo kontext záznamu). Záznamník úloh zachovává informace s dostatkem detailů k zajištění, že přehrávání nahrávky může provést nahrané akce přímo v pořadí, v jakém je uživatel provedl. (Přehrávání funkce není dosud implementováno v Retail modern POS nebo Cloud POS.)

## <a name="basic-configuration"></a>Základní konfigurace

Pokud chcete zapnout nahrávání úloh v systému POS, postupujte takto:

1. Klikněte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Registry**.
2. Klepněte na registr, pokud chcete povolit záznam úlohy.
3. Na kartě **Registr** na pevné záložce **Obecné** nastavte možnost **Povolit záznam úloh** na **Ano**.
4. Klikněte na možnost **Uložit**.
5. Přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plán distribuce**.
6. Vyberte úlohu **Registry (1090)** a klikněte na **Spustit**.

## <a name="create-a-recording"></a>Vytvoření záznamu

Tento postup slouží k vytvoření nového záznamu pomocí Záznamníku úloh.

1. Spusťte Retail Modern POS nebo Cloud POS a přihlaste se.
2. Na stránce **Nastavení** v části **Záznamník úloh** klikněte na **Otevřít záznamník úloh**. Otevře se podokno **Záznamníku úloh**. Můžete kliknout na tlačítko **Zavřít** (**X**) v pravém horním rohu pro zavření podokna **Záznamník úkolů** před zahájením nového záznamu. K opětovnému otevření podokna zopakujte krok 2.

    [![Podokno Záznamník úloh.](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Zadejte jméno a popis pro nahrávky a poté klepněte na možnost **Spustit**. Relace záznamu začne hned po klepnutí na tlačítko **Spustit**.

    > [!NOTE]
    > Pokud kliknete na tlačítko **Zavřít** (**X**) v pravém horním rohu v době, kdy probíhá nahrávání, podokno **Záznamník úloh** se zavře, ale relace nahrávání se neukončí. K opětovnému otevření podokna Záznamník úkolů klepněte na tlačítko **Nápověda** (otazník) v horní části obrazovky.
    >
    > [![Otazník.](./media/help.jpg)](./media/help.jpg)

4. Po kliknutí na tlačítko **Spustit** záznamník úloh přejde do režimu nahrávání. V podokně **Záznamník úloh** se zobrazují informace a ovládací prvky, které se vztahují k procesu záznamu.
5. Proveďte akce, které chcete provést v uživatelském rozhraní Retail Modern POS nebo Cloud POS.
6. Pokud chcete záznam zastavit, klikněte na **Stop**.

## <a name="download-options"></a>Možnosti stahování

Po ukončení relace záznamu se zobrazuje několik možností tak, abyste si mohli stáhnout záznam.

[![Možnosti stahování.](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Uložit do tohoto počítače

K přehrání Průvodce záznamem úloh, správě nahrávky nebo úpravě anotací v nahrávce můžete použít balíček nahrávky. (Tato funkce není dosud implementována v Retail Modern POS nebo Cloud POS.)

### <a name="export-as-word-document"></a>Exportovat jako dokument aplikace Word

Nahrávku můžete uložit jako dokument Microsoft Word. Dokument bude obsahovat zaznamenané kroky a snímky obrazovky, které byly zaznamenány.

### <a name="save-as-developer-recording"></a>Uložit jako vývojářský záznam

Nezpracovaný soubor záznamu je užitečný pro scénáře vývojářů, jako je generování testovacího kódu. (Tato funkce není dosud implementována.)

## <a name="recording-controls"></a>Ovládací prvky pro záznam

[![Ovládací prvky pro záznam.](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Zastavit

Pokud chcete relaci záznamu zastavit, klikněte na **Stop**. Poznámka: Relaci po dokončení nelze restartovat. Proto ověřte, že záznam bude dokončen před ukončením.

### <a name="pause"></a>Pozastavit

Klepněte na tlačítko **Pozastavit** pro dočasné ukončení relace záznamu a pokračování v operaci. Kroky provedené po kliknutí na **Pozastavit** se nezaznamenají.

### <a name="continue"></a>Pokračovat

Pokud chcete záznam po pozastavení obnovit, klikněte na **Pokračovat**.

### <a name="capture-screenshots"></a>Pořídit snímky obrazovky

Záznamník úkolů může zaznamenat snímky obrazovky uživatelského rozhraní Retail Modern POS při zaznamenávání obchodního procesu. Chcete-li aktivovat funkci pořízení snímku obrazovky, nastavte možnost **Zachytit obrazovku** na **Ano** a poté proveďte záznam. Po ukončení záznamu klikněte na tlačítko **Zastavit** a stáhněte dokument aplikace Word. Dokument bude obsahovat kroky s příslušnými snímky obrazovky.

> [!NOTE]
> Funkce zachycení obrazovky není podporována v prostředí Cloud POS.

### <a name="start-task-and-end-task"></a>Počáteční a koncový úkol

Začátek a konec sady seskupených kroků můžete určit pomocí tlačítka **Počáteční úkol** a **Koncový** **úkol**. Kliknutím na **Počáteční úkol** přidáte krok Počáteční úkol. Potom proveďte kroky, které mají být zahrnuty ve skupině. Po dokončení kroků skupiny klepněte na tlačítko **Koncový úkol**. Úlohy pomáhají uspořádat vaše postupy. Mohou být vnořeny v jiných úkolech. Tímto způsobem můžete lépe uspořádat příliš dlouhé a složité obchodní procesy.

## <a name="adding-annotations"></a>Přidání poznámek

Poznámka je doplňkový text, který přidáváte do kroku v záznamu. Můžete například použít poznámky k poskytnutí uživateli dalšího kontextu nebo pokynů. Můžete přidat poznámky před nebo za krok. Můžete přidat poznámky k jakémkoli kroku klepnutím na tlačítko **Upravit** (symbol tužky) napravo od kroku.

[![Tlačítko Upravit u kroku.](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Texty a poznámky

V polích **Texty** a **Poznámky** můžete přidat text, který by měl být přidružený ke kroku v Průvodci záznamem úloh.

[![Pole Text a Poznámky.](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Text

Text, který zadáte do pole **Text**, se zobrazí *nad* krokem v Průvodci záznamem úloh. Toto místo je vhodné pro text, který si má uživatel přečíst před dokončením kroku.

#### <a name="notes"></a>Poznámky

Text, který zadáte do pole **Poznámky**, se zobrazí *pod* krokem v Průvodci záznamem úloh. Aby si uživatel mohl přečíst text poznámky, musí rozbalit text kroku v místním okně. Toto umístění je vhodné pro volitelný materiál ke čtení nebo další informace, které mohou být pro uživatele užitečné, ale uživatel je nevyžaduje pro dokončení akce.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Nápověda v Retail Modern POS a Cloud POS

Chcete-li zobrazovat vlastní záznamy úkolů v podokně nápovědy pro Retail Modern POS a Cloud POS, aby je bylo možné přehrát jako průvodce úkolem nebo zobrazit jako text, je třeba záznamy úkolů uložit do vlastní knihovny BPM a poté aktualizovat systémové parametry nápovědy tak, aby odkazovaly na knihovnu BPM. Další informace naleznete v tématu [Připojení systému nápovědy](../fin-ops-core/fin-ops/get-started/help-connect.md). Nápověda pro Retail Modern POS a Cloud POS prohlledává LCS v reálném čase. Vyhledává ve všech knihovnách BPM, které jsou vybrány v parametrech systému nápovědy aplikace Commerce, a zobrazí příslušné výsledky. Pro přístup do nabídky **Nápověda** klikněte na tlačítko **Nápověda** (otazník) v horní části obrazovky a do vyhledávacího pole napište název procesu. Potom klikněte na tlačítko pro vyhledávání.

[![Tlačítko Nápověda.](./media/help.jpg)](./media/help.jpg)

Po kliknutí na Průvodce záznamem úloh ve výsledcích vyhledávání můžete zobrazit kroky jako téma nápovědy nebo kroky exportovat do wordového dokumentu.

> [!NOTE]
> V nápovědě pro Retail Retail Modern POS a Cloud POS se nezobrazují průvodci záznamem úloh v závislosti na tom, v jakém jste formuláři nebo jakou provádíte operaci. Je nutné v poli pro vyhledávání zadat název procesu a poté kliknout na **Hledat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
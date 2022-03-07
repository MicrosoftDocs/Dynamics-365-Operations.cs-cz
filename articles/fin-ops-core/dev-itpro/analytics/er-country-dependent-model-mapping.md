---
title: Konfigurace mapování modelu ER závislého na kontextu podle země
description: V tomto tématu je vysvětleno, jak můžete nastavit mapování modelu ER tak, aby závisela na kontextu země/oblasti právnické osoby, která řídí jejich použití.
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 5b26c605bd64b8d8e5a90f4389261e8e56825111
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605350"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Konfigurace mapování modelu ER závislého na kontextu podle země

[!include[banner](../includes/banner.md)]

Mapování modelu aplikace elektronického výkaznictví (ER) lze konfigurovat tak, aby implementovalo obecný datový model ER, ale aby bylo specifické pro Dynamics 365 Finance. V tomto tématu je vysvětleno, jak navrhnout více mapování modelů ER pro datový model ER pro řízení způsobu jejich použití odpovídajícími formáty ER, které jsou spouštěny ze společností s různými kontexty zemí nebo oblastí.

## <a name="prerequisites"></a>Předpoklady

Pro dokončení příkladů v tomto tématu musíte mít následující přístup:

- Přístup k Finance pro některou z následujících rolí:
    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako aplikace Finance, pro jednu z následujících rolí:
    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

Některé kroky v tomto tématu vyžadují spuštění formátu ER. V některých případech je zpracování formátu ER ovlivněno kontextem země nebo oblasti společnosti, k níž jste aktuálně přihlášeni. V aktuální instanci RCS můžete spustit formát ER, pokud je společnost s požadovaným kontextem země/oblasti dostupná v RCS. V opačném případě je nutné odeslat dokončenou verzi konfigurace mapování modelu ER a formátu ER, které používají datový model ER pro vaši instanci Finance, a poté ve své instanci Finance spustit formát ER. Informace o tom, jak importovat konfigurace, které se nacházejí v RCS do instance Finance, naleznete [v tématu Import konfigurací z RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Případ mapování jednoho modelu

Chcete-li navrhnout požadované součásti ER, postupujte podle kroků v [příloze 1](#appendix1) tohoto tématu. Nyní máte konfiguraci mapování modelu **mapování (obecná)**, která obsahuje mapování modelu pro definici **vstupního bodu 1**.

![Stránka konfigurací ER, formát pro naučení konfigurace mapování.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Spustit**.
2.  Vyberte **OK**.

Všimněte si, že webový prohlížeč nabízí stažení textového souboru, který byl vytvořen spuštěným formátem ER. Vzhledem k tomu, že tento formát byl nakonfigurován pro použití definice **vstupní bod 1** a v současné době je k dispozici pouze jediné mapování modelu pro základní model, který obsahuje mapování pro tuto definici, spuštěný formát ER používal mapování modelu **mapování (Obecné)** ke konfiguraci **mapování (obecná)** jako zdroj dat. Stažený soubor tedy obsahuje text **Obecná funkce 1**.

## <a name="multiple-shared-model-mappings-case"></a>Několik případů mapování sdílených modelů

Chcete-li navrhnout požadované součásti ER, postupujte podle kroků v [příloze 2](#appendix2) tohoto tématu. Nyní máte konfigurace mapování modelu **Mapování (obecné)** a **Vlastní mapování (obecné)**, z nichž každá obsahuje mapování modelu pro definici **Vstupní bod 1**.

![Stránka konfigurací ER, mapování obecné vlastní konfigurace.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Formát učení se mapování**.
2.  Na pevné záložce **Verze** vyberte **Spustit**.
3.  Vyberte **OK**.

Povšimněte si, že provedení vybraného formátu ER je neúspěšné. Chybová zpráva vás informuje o tom, že existuje více mapování modelu pro definici modelu **Model k učení se mapování** a **Vstupní bod 1** v konfiguracích mapování modelu **Mapování (obecné)** a **Vlastní mapování (obecné)**. Tato zpráva také doporučuje, abyste jako výchozí konfiguraci vybrali některou z těchto konfigurací.

![Stránka konfigurací ER s chybovou zprávou.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Definování výchozí konfigurace mapování

Pomocí následujícího postupu definujte konfiguraci mapování modelu **Vlastní mapování (obecné)** jako výchozí konfigurace, aby bylo možné jeho mapování použít jako zdroje dat pro formát ER **Formát mapování**.

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vlastní mapování (obecné)**.
2.  Podle potřeby vyberte možnost **Upravit**, aby byla aktuální stránka připravena pro úpravy.
3.  Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.
4.  Zvolte možnost **Uložit**.

![Stránka konfigurací ER, výchozí jezdec mapování modelu nastaven na Ano.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Formát učení se mapování**.
2.  Na pevné záložce **Verze** vyberte **Spustit**.
3.  Vyberte **OK**.

Povšimněte si, že provedení vybraného formátu ER je úspěšné. Webový prohlížeč nabízí stažení textového souboru, který byl vytvořen spuštěným formátem ER. Vzhledem k tomu, že tento formát byl nakonfigurován pro použití definice **Vstupní bod 1** a jako výchozí konfigurace byla vybrána konfigurace modelu mapování **Vlastní mapování (obecné)**, provedený formát ER používal mapování modelu **Kopie mapování (obecné)** konfigurace **Vlastní mapování (obecné)** jako zdroj dat. Stažený soubor tedy obsahuje text **Vlastní obecná funkce 1**.

> [!NOTE]
> Pokud změníte společnost, ke které jste aktuálně přihlášeni, a znovu spustíte tento formát ER, dostanete stejný obsah v generovaném souboru, protože výchozí konfigurace mapování modelu ER neobsahuje žádná omezení závislá na společnosti.

## <a name="multiple-mixed-model-mappings-case"></a>Několik případů mapování kombinovaných modelů

Chcete-li navrhnout požadované součásti ER, postupujte podle kroků v [příloze 3](#appendix3) tohoto tématu. Nyní máte konfigurace mapování modelu **Mapování (obecné)** a **Vlastní mapování (obecné)** a **Mapování modelu (FR)**, z nichž každá obsahuje mapování modelu pro definici **Vstupní bod 1**.

Všimněte si, že verze 1 konfigurace mapování modelu **Mapování (FR)** platí pouze pro formáty ER modelu **Model k učení mapování**, které jsou spuštěny ve společnostech Finance, které mají kontext francouzské země/oblasti.

![Stránka konfigurací ER, konfigurace mapování modelu (FR).](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Změňte společnost na **FRSI**.
2.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Formát učení se mapování**.
3.  Na pevné záložce **Verze** vyberte **Spustit**.
4.  Vyberte **OK**.

Povšimněte si, že provedení vybraného formátu ER je úspěšné. Webový prohlížeč nabízí stažení textového souboru, který byl vytvořen spuštěným formátem ER. Vzhledem k tomu, že tento formát byl nakonfigurován pro použití definice **Vstupní bod 1** a jako výchozí konfigurace byla vybrána konfigurace modelu mapování **Vlastní mapování (obecné)**, provedený formát ER používal mapování modelu **Kopie mapování (obecné)** konfigurace **Vlastní mapování (obecné)** jako zdroj dat. Stažený soubor tedy obsahuje text **Vlastní obecná funkce 1**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Definujte konfiguraci mapování specifickou pro Francii jako výchozí konfiguraci.

Pomocí následujících kroků definujte vlastní konfiguraci mapování modelu **Mapování (FR)** jako výchozí konfiguraci. Vzhledem k tomu, že toto mapování je specifické pro Francii, bude považováno za výchozí mapování mezi všemi konfiguracemi mapování modelu, které mají v poli **Kódy země/oblasti ISO** kód země **FR**.

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Mapování (FR)**.
2.  Podle potřeby vyberte možnost **Upravit**, aby byla aktuální stránka připravena pro úpravy.
3.  Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.
4.  Zvolte možnost **Uložit**.

![Stránka konfigurací ER, konfigurace mapování (FR), výchozí jezdec mapování modelu nastaven na Ano.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Formát učení se mapování**.
2.  Na pevné záložce **Verze** vyberte **Spustit**.
3.  Vyberte **OK**.

Povšimněte si, že provedení vybraného formátu ER je úspěšné. Webový prohlížeč nabízí stažení textového souboru, který byl vytvořen spuštěným formátem ER. Vzhledem k tomu, že tento formát byl nakonfigurován pro použití definice **Vstupní bod 1** a jako výchozí konfigurace byla vybrána konfigurace mapování modelu **Mapování (FR)**, provedený formát ER používal mapování modelu **Mapování (FR)** konfigurace **Mapování (FR)** jako zdroj dat. Stažený soubor tedy obsahuje text **Funkce FR 1**.

> [!NOTE]
> Pokud změníte společnost, ke které jste aktuálně přihlášeni, a znovu spustíte tento formát ER, bude výstup záviset na kontextu země nebo oblasti vybrané společnosti.

## <a name="other-model-mapping-cases"></a>Ostatní případy mapování modelu

Jak jste viděli, výběr mapování modelu pro spuštění formátu ER funguje následujícím způsobem:

- Definice mapování modelu, kterou formát ER používá, je zadána (**vstupní bod 1** v příkladech v tomto tématu).
- Všechny konfigurace mapování obsahující mapování, které má zadanou definici a které splňují všechna nakonfigurovaná omezení kontextu země nebo oblasti, mohou být potenciálně použity ke spuštění formátu (**Mapování (Obecné)**, **Vlastní mapování (obecné)** a **Mapování (FR)** v příkladech v tomto tématu).
- Jakékoli výchozí mapování modelu, které má omezení kontextu země nebo oblasti, má nejvyšší prioritu pro výběr (**Mapování (FR)** v příkladech v tomto tématu).
- Jakékoli výchozí mapování modelu, které nemá omezení kontextu země nebo oblasti, má druhou nejvyšší prioritu pro výběr (**Vlastní mapování (obecné)** v příkladech v tomto tématu).
- Jakékoli mapování modelu, které má omezení kontextu země nebo oblasti, má vyšší prioritu než mapování modelu, které nemá omezení kontextu země/oblasti.

Následující tabulka obsahuje informace o výsledcích výběru mapování modelu pro všechny možné případy nastavení mapování modelu:

- Sloupec 1 určuje, zda první mapování modelu, které nemá omezení kontextu země nebo oblasti (například sdílené mapování **Mapování (obecné)**) je prezentováno a pokud ano, zda je pro ně nastavená možnost **Výchozí pro mapování modelu** na **ano**.
- Sloupec 2 určuje, zda druhé mapování modelu, které nemá omezení kontextu země nebo oblasti (například sdílené mapování **Mapování (obecné)**) je prezentováno a pokud ano, zda je pro ně nastavená možnost **Výchozí pro mapování modelu** na **ano**.
- Sloupec 3 určuje, zda první mapování modelu, které má omezení kontextu země nebo oblasti A (například mapování **Mapování (FR) specifické pro francii**) je prezentováno a pokud ano, zda je pro ně nastavená možnost **Výchozí pro mapování modelu** na **ano**.
- Sloupec 4 určuje, zda druhé mapování modelu, které má omezení kontextu země nebo oblasti A (například mapování Mapování (FR) specifické pro francii) je prezentováno a pokud ano, zda je pro ně nastavená možnost **Výchozí pro mapování** modelu na **ano**.
- Sloupec 5 uvádí výsledek výběru mapování modelu pro provedení formátu ER v rámci kontroly společnosti, která má kontext země/oblast A.
- Sloupec 6 uvádí výsledek výběru mapování modelu pro provedení formátu ER v rámci kontroly společnosti, která má kontext země/oblast B.

V tabulce znaménko plus (+) označuje přítomnost konfigurace mapování modelu v aktuální instanci služby Microsoft Azure, která se používá ke spuštění formátu ER (Finance nebo RCS).

| Pevný obal | Mapování modelu 1 bez kontextu země/oblasti (MM1) | Mapování modelu 2 bez kontextu země/oblasti (MM2) | Mapování modelu 1 s kontextem země/oblasti A (MM1A) | Mapování modelu 2 s kontextem země/oblasti A (MM2A) | Spustit pod kontrolou společnosti, která má kontext země/oblasti A | Spustit pod kontrolou společnosti, která má kontext země/oblasti B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Chyba (mapování chybí)   | Chyba (mapování chybí)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Chyba (vícenásobné mapování) | Chyba (vícenásobné mapování)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Chyba (vícenásobné mapování) | MM1                        |
|     6   |     +   | výchozí |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | výchozí |         | MM1A                      | MM1                        |
|     8   |     +   |         | výchozí |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | výchozí | výchozí | Chyba (vícenásobné mapování) | MM1                        |
|    10   | výchozí |         |         |         | MM1                       | MM1                        |
|    11   | výchozí |    +    |         |         | MM1                       | MM1                        |
|    12   | výchozí |         |    +    |         | MM1                       | MM1                        |
|    13   | výchozí | výchozí |         |         | Chyba (vícenásobné mapování) | Chyba (vícenásobné mapování)  |
|    14   | výchozí |         | výchozí |         | MM1A                      | MM1                        |
|    15   | výchozí |         | výchozí | výchozí | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | výchozí | výchozí | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Zjistěte, jaké mapování bylo použito při provádění formátu ER.

### <a name="configure-er-user-parameters"></a>Konfigurace parametrů uživatele ER

1.  Na stránce **Konfigurace** v podokně akcí na kartě **KONFIGURACE** vyberte **Parametry uživatelů**.
2.  Nastavte možnost **Spustit v režimu ladění** na **Ano**.
4.  Vyberte **OK**.

### <a name="run-the-configured-format"></a>Spuštění konfigurovaného formátu

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Formát učení se mapování**.
2.  Na pevné záložce **Verze** vyberte **Spustit**.
3.  Vyberte **OK**.

### <a name="review-the-er-debug-log"></a>Kontrola protokolu ladění ER

1.  V navigačním podokně přejděte na **Moduly \> Správa organizace \> Elektronické vykazování \> Protokol konfigurace ladění**.
2.  Vyberte tlačítko **Znovu načíst tuto stránku**.

![Stránka spuštění protokolů ER.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Všimněte si, že do protokolu ladění ER byl přidán nový záznam pro spuštěný formát ER. Vzhledem k **tomu**, že pole úrovně tohoto záznamu je nastaveno na **Informace**, záznam je informativní. Vzhledem k tomu, že pole součásti Formát je nastaveno na **Konfigurace mapování**, záznam vás informuje o mapování modelu, které bylo použito při spuštění formátu ER **Formát k učení se mapování** (vybraný v poli **Název konfigurace**). Obsah pole **Generovaný text** vás informuje, že komponenta mapování **Mapování (FR)**, která je umístěna v konfiguraci **Mapování (FR)** byla použita ke spuštění této sestavy.p

## <a name="appendix-1"></a><a name="appendix1"></a>Dodatek 1

### <a name="configure-a-sample-data-model"></a>Konfigurace ukázkového datového modelu

Přihlaste se k instanci RCS.

V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Pro dokončení tohoto postupu musíte nejprve v RCS dokončit kroky v proceduře [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

#### <a name="create-an-er-data-model-configuration"></a>Vytvoření nové konfigurace datového modelu ER

1.  Na výchozím řídicím panelu vyberte **Elektronické vykazování**.
2.  Vyberte dlaždici **Konfigurace vykazování**.
3.  Na stránce **Konfigurace** zvolte **Vytvořit konfiguraci**.
4.  V rozevíracím dialogovém okně v poli **Název** zadejte **Model pro učení mapování**.
5.  Vyberte **Vytvořit konfiguraci**.
6.  Vyberte pevnou záložku **Komponenty konfigurace**.

Všimněte si, že verze 1 této konfigurace ER je připravena k úpravám. Tato verze obsahuje komponentu datového modelu.

#### <a name="design-a-sample-data-model"></a>Návrh ukázkového datového modelu

1.  Na stránce **Konfigurace** vyberte **Návrhář**.
2.  Zvolte **Nové**.
3.  V rozevíracím dialogovém okně do pole **Název** zadejte **Vstupní bod 1**.
4.  Vyberte **přidat**.
5.  Zvolte **Nové**.
6.  V rozevíracím dialogovém okně v poli **Název** zadejte **Popis funkce**.
7.  Vyberte **přidat**.
8.  Zvolte **Nové**.
9.  V rozevíracím dialogovém okně ve skupině polí **Nový uzel** vyberte **Modelový kořen**.
10. Do pole **Název** zadejte **Vstupní bod 2**.
11. Vyberte **Vstupní bod 2**.
12. Vyberte **přidat**.
13. Zvolte **Nové**.
14. V rozevíracím dialogovém okně v poli **Název** zadejte **Popis funkce**.
15. Vyberte **přidat**.

    ![Stránka Návrhář modelu dat ER.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Zvolte možnost **Uložit**.
17. Zavřete stránku.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Dokončení upravené verze konfigurace modelu

1.  Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Změnit stav**.

    > Změňte stav navržené konfigurace modelu z **Koncept** na **Dokončeno**, aby bylo možné ho použít k navržení požadovaných mapování a formátů modelu.

2.  Zvolte **Dokončit**.
3.  Vyberte **OK**.

Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.

### <a name="configure-a-sample-model-mapping"></a>Konfigurace ukázkového mapování modelu

#### <a name="create-an-er-model-mapping-configuration"></a>Vytvoření konfigurace mapování modelu ER

1.  Na stránce **Konfigurace** zvolte **Vytvořit konfiguraci**.
2.  V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte možnost **Mapování modelu založené na datovém modelu pro učení mapování**.
3.  Do pole **Název** zadejte **Mapování (obecné)**.
4.  V poli **Definice datového modelu** vyberte **Vstupní bod 1**.
5.  Vyberte **Vytvořit konfiguraci**.

Všimněte si, že verze 1 této konfigurace ER je připravena k úpravám. Tato verze obsahuje komponentu modelu mapování.

#### <a name="design-a-sample-model-mapping"></a>návrh ukázkového mapování modelu

1.  Na stránce **Konfigurace** zvolte **Návrhář**.

    Mapování modelu typu směru **Do modelu** bylo do této komponenty automaticky přidáno pro definici **Vstupní bod 1**.
    
2.  Vyberte **Návrhář** pro zahájení úprav přidaného mapování modelu.
3.  V části **Datový model** vyberte **Upravit**.
4.  Do pole **Vzorec** zadejte **Obecná funkce 1**.
5.  Zvolte **Uložit**.
6.  Zavřete stránku **Návrhář vzorce**.

    ![Stránka návrháře mapování modelu ER, definice vstupního bodu 1.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Zvolte možnost **Uložit**.
8.  Zavřete stránku **Návrhář mapování modelu**.
9.  Zvolte **Nové**.
10. V poli **Definice** vyberte **Vstupní bod 2**.
11. Do pole **Název** zadejte **Mapování (obecné) 2**.
12. Vyberte možnost **Návrhář**.
13. V části **Datový model** vyberte **Upravit**.
14. Do pole **Vzorec** zadejte **Obecná funkce 2**.
15. Zvolte **Uložit**.
16. Zavřete stránku **Návrhář vzorce**.

    ![Stránka návrháře mapování modelu ER, definice vstupního bodu 2.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Zvolte možnost **Uložit**.
18. Zavřete stránku **Návrhář mapování modelu**.

    ![Stránka mapování modelu ER s definicemi vstupního bodu.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Zavřete stránku **Mapování modelu**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Dokončení upravené verze konfigurace mapování modelu

1.  Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Změnit stav**.

    > Změňte stav navrženého mapování modelu z **Koncept** na **Dokončeno**, aby ho mohly používat formáty ER.

2.  Zvolte **Dokončit**.
3.  Vyberte **OK**.

Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.

### <a name="configure-a-sample-format"></a>Konfigurace vzorového formátu

#### <a name="create-an-er-format-configuration"></a>Vytvoření konfigurace formátu ER

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Model učení se mapování**.
2.  Vyberte **Vytvořit konfiguraci**.
3.  V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte možnost **Formát založený na datovém modelu pro učení mapování**.
4.  Do pole **Název** zadejte **Formát pro učení mapování**.
5.  V poli **Definice datového modelu** vyberte **Vstupní bod 1**.
6.  Vyberte **Vytvořit konfiguraci**.

Všimněte si, že verze 1 této konfigurace ER je připravena k úpravám. Tato verze obsahuje komponentu formátu.

#### <a name="design-a-sample-format"></a>Návrh ukázkového formátu

1.  Na stránce **Konfigurace** zvolte **Návrhář**.
2.  Vyberte **Přidat kořen**.
3.  Ve skupině **Text** vyberte položku **Řetězec**.
4.  Vyberte **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Vázání prvků formátu na zdroje dat

1.  Na stránce **Návrhář formátu** na kartě **Mapování** rozbalte modelový zdroj dat.
2.  Vyberte pole **Popis** funkčnosti.
3.  Vyberte možnost **vazba**.

    ![Stránka návrháře formátu ER.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Zvolte možnost **Uložit**.
5.  Zavřete stránku.

## <a name="appendix-2"></a><a name="appendix2"></a>Dodatek 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Konfigurace ukázkového mapování modelu pro obecné přizpůsobení

Můžete upravit mapování modelu, které vám bylo poskytnuto poskytovatelem konfigurace (partner), a potom použít přizpůsobenou verzi jako zdroj dat pro formáty ER. V takovém případě je nutné vytvořit vlastní konfiguraci mapování modelu ER pro provedení požadovaných změn v existujících mapováních modelu. Postupy v tomto dodatku používají jako příklad mapování modelu **Mapování (Obecné)**.

#### <a name="create-an-er-model-mapping-configuration"></a>Vytvoření konfigurace mapování modelu ER

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Mapování (obecné)**.
2.  Vyberte **Vytvořit konfiguraci**.
3.  V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte **Odvodit z názvu: Mapování (obecné), Litware, Inc.**.
4.  Do pole **Název** zadejte **Vlastní mapování (obecné)**.
5.  Vyberte **Vytvořit konfiguraci**.

Všimněte si, že verze 1 této konfigurace ER je připravena k úpravám.

#### <a name="design-a-sample-model-mapping"></a>návrh ukázkového mapování modelu

1.  Na stránce **Konfigurace** zvolte **Návrhář**.

    > Všimněte si, že mapování modelu základní konfigurace bylo automaticky zkopírováno do této konfigurace.

2.  Vyberte mapování **Kopie mapování (obecné)**.
3.  Vyberte možnost **Návrhář**.
4.  V části **Datový model** vyberte **Upravit**.
5.  Do pole **Vzorec** zadejte **Vlastní obecná funkce 1**.
6.  Zvolte možnost **Uložit**.
7.  Zavřete stránku.

    ![Stránka návrháře mapování modelu ER, obecná funkčnost 1 vlastní vzorec.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Zvolte možnost **Uložit**.
9.  Zavřete stránku.
10. Vyberte mapování **Kopie mapování (obecné) 2**.
11. Vyberte možnost **Návrhář**.
12. V části **Datový model** vyberte **Upravit**.
13. Do pole **Vzorec** zadejte **Vlastní obecná funkce 2**.
14. Zvolte možnost **Uložit**.
15. Zavřete stránku.

    ![Stránka návrháře mapování modelu ER, obecná funkčnost 2 vlastní vzorec.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Zvolte možnost **Uložit**.
17. Zavřete stránku.

    ![Stránka mapování modelu ER na zdroj dat pro mapování kopie mapování (obecné).](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Zavřete stránku.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Dokončení upravené verze konfigurace mapování modelu

1.  Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Změnit stav**.

    > Změňte stav navrženého mapování modelu z **Koncept** na **Dokončeno**, aby ho mohly používat formáty ER.

2.  Zvolte **Dokončit**.
3.  Vyberte **OK**.

Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.

## <a name="appendix-3"></a><a name="appendix3"></a>Dodatek 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Konfigurace ukázkového mapování modelu pro přizpůsobení podle země/oblasti

U některých formátů ER mohou existovat specifické požadavky na zemi nebo oblast pro přípravu dat. V takovém případě můžete spravovat samostatnou konfiguraci mapování modelu ER a izolovat implementaci specifických požadavků dané země nebo oblasti z obecné implementace. Postupy uvedené v tomto dodatku používají **formát pro získání informací o mapování** formátu ER a požadavků specifických pro Francii jako příklad.

#### <a name="create-an-er-model-mapping-configuration"></a>Vytvoření konfigurace mapování modelu ER

Nejprve vytvořte novou konfiguraci mapování modelu ER pro implementaci specifických požadavků na zemi nebo oblast. Použijte vlastní konfiguraci mapování modelu ER jako základ.

1.  Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vlastní mapování (obecné)**.
2.  Vyberte **Vytvořit konfiguraci**.
3.  V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte **Odvodit z názvu: Vlastní mapování (obecné), Litware, Inc.**.
4.  Do pole **Název** zadejte **Mapování (FR)**.
5.  Vyberte **Vytvořit konfiguraci**.

Všimněte si, že verze 1 této konfigurace ER je připravena k úpravám.

#### <a name="design-a-sample-model-mapping"></a>návrh ukázkového mapování modelu

1.  Na stránce **Konfigurace** zvolte **Návrhář**.

    > Všimněte si, že mapování modelu základní konfigurace bylo automaticky zkopírováno do této konfigurace.

2.  Vyberte mapování **Kopie mapování (obecné)**.
3.  Přejmenujte mapování na **Mapování (FR)**.
4.  Vyberte možnost **Návrhář**.
5.  V části **Datový model** vyberte **Upravit**.
6.  Do pole **Vzorec** zadejte **Funkce FR 1**.
7.  Zvolte možnost **Uložit**.
8.  Zavřete stránku.

    ![Stránka návrháře mapování modelu FR, funkčnost 1 vzorec.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Zvolte možnost **Uložit**.
10. Zavřete stránku.
11. Vyberte mapování **Kopie mapování 2 (obecné)**.
12. Přejmenujte mapování na **Mapování (FR) 2**.
13. Vyberte možnost **Návrhář**.
14. V části **Datový model** vyberte **Upravit**.
15. Do pole **Vzorec** zadejte **Funkce FR 2**.
16. Zvolte možnost **Uložit**.
17. Zavřete stránku.

    ![Stránka návrháře mapování modelu FR, funkčnost 2 vzorec.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Zvolte možnost **Uložit**.
19. Zavřete stránku.

    ![Stránka mapování modelu ER na zdroj dat.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Zavřete stránku.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Zadání omezení kontextu země/oblasti pro použití

1.  Na stránce **Konfigurace** na pevné záložce **Kódy země/oblasti ISO** vyberte **Nová**.
2.  V poli **ISO** vyberte **FR**.
3.  Zvolte **Uložit**.

Nezapomeňte, že je nutné se přihlásit ke konkrétní společnosti v modulu Finance, aby byl spuštěn formát ER. Proto lze tuto společnost považovat za stranu, která řídí zpracování formátu ER a výběr správného mapování modelu ER základního datového modelu ER. Přidáním kódu země **FR** určíte, že toto mapování modelu bude k dispozici pro výběr ve formátu ER základního datového modelu pouze v případě, že je tento formát spuštěn pod kontrolou společnosti, která má v kontextu francouzské země/oblasti.

Pro jednu verzi konfigurace mapování modelu ER lze přidat více kódů zemí nebo oblastí. Tímto způsobem lze mapování modelů, která jsou umístěna v konfiguraci mapování modelu, použít pro formát ER, který je spuštěn pod kontrolou společností, které mají jiný kontext země/oblasti.

Všimněte si, že seznam kódů zemí nebo oblastí je určen pro každou verzi konfigurace mapování modelu ER a může se lišit od verze k verzi.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Dokončení upravené verze konfigurace mapování modelu

1.  Na stránce **Konfigurace** na pevné záložce **Verze** vyberte **Změnit stav**.

    > Změňte stav navrženého mapování modelu z **Koncept** na **Dokončeno**, aby ho mohly používat formáty ER.

2.  Zvolte **Dokončit**.
3.  Vyberte **OK**.

Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Správa mapování modelu elektronického výkaznictví v samostatných konfiguracích elektronického výkaznictví](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Použití kontextu země nebo oblasti](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Časté dotazy

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Nakonfiguroval jsem dvě sdílené konfigurace mapování modelu ER v RCS a označil jeden z nich jako výchozí konfiguraci mapování modelu. Úspěšně jsem spustil formát ER, který byl vytvořen pro stejnou základní konfiguraci datového modelu ER, pro testování mapování modelu. Pak jsem importoval celé řešení ER (datový model ER, dvě konfigurace mapování modelů ER a konfiguraci formátu ER) do modulu Finance Proč se při pokusu o spuštění stejného formátu ER v modulu finance zobrazí chybová zpráva?
Výchozí nastavení mapování modelu je specifické pro dané prostředí. Je konfigurováno v RCS, ale není exportováno do financí. Chcete-li úspěšně spustit tento formát ER, je nutné označit jednu z konfigurací mapování modelu ER jako výchozí konfiguraci mapování modelu v i modulu Finance.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Bylo nakonfigurováno jedno mapování modelu jako sdílené mapování modelu a byla dokončena verze konceptu. Poté jsem přidal novou konfiguraci mapování modelu pro stejný datový model a nakonfiguroval ji jako specifickou pro francouzštinu. Proč je mapování sdílených modelů vybráno při spuštění formátu ER, přestože tento formát ER používá správnou kořenovou definici a provádění je probíhá pod kontrolou společnosti, která je v kontextu francouzské země/oblasti?
Zkontrolujte, zda není jako výchozí konfigurace mapování modelu označena konfigurace mapování sdílených modelů. V opačném případě bude mít vyšší prioritu při výběru mapování. Rovněž se ujistěte, že konfigurace mapování modelu specifická pro Francii je zvažována, když je mapování vybráno během spouštění formátu ER. Konfiguraci mapování modelu ER lze vybrat pouze v případě, že je splněna alespoň jedna z následujících podmínek:
- Nejméně jedna verze konfigurace mapování modelu ER má stav **Dokončeno** nebo **Sdíleno**. V tomto případě bude pro provádění formátu ER použita verze s nejvyšším číslem verze.
- Možnost **Spuštění konceptu** pro konfiguraci mapování modelu ER je zapnuta. V tomto případě bude pro provádění formátu ER použita verze se stavem **Koncept**.
> Možnost **Spustit koncept** bude dostupná na stránce **Konfigurace** pro každou konfiguraci mapování modelu ER, když je zapnutý parametr uživatele ER **Spustit nastavení**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Místa určení elektronického výkaznictví
description: Tento článek obsahuje informace o správě cílů elektronického výkaznictví, podporovaných cílech a o možnostech zabezpečení.
author: kfend
ms.date: 08/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: DocuType, ERSolutionTable
ms.openlocfilehash: b1bf6289e80769dfe8858f307cbb9b217b42dbb4
ms.sourcegitcommit: f2edc193003564c5bee1747f9c2b800feee342bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/29/2022
ms.locfileid: "9360972"
---
# <a name="electronic-reporting-er-destinations"></a>Místa určení elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Pro každou konfiguraci formátu elektronického výkaznictví (ER) a její komponenty (složku nebo soubor) lze konfigurovat cíl. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. Tento článek popisuje správu cílů EV, typy podporovaných cílů a důležité informace o zabezpečení.

Konfigurace formátu elektronického výkaznictví obvykle obsahuje alespoň jednu součást výstupu: soubor. Konfigurace obvykle obsahují více součástí výstupního souboru různých typů (například XML, TXT, XLSX, DOCX nebo PDF), které jsou seskupeny do buď jedné složky nebo více složek. Správa destinací EV umožňuje předem nastavit, co se stane při spuštění každé ze součástí. Ve výchozím nastavení se při spuštění konfigurace uživateli zobrazí dialogové okno, které vám umožní uložit nebo otevřít soubor. Ke stejnému chování dochází při importu konfigurace EV, když pro ně nechcete konfigurovat žádné konkrétní cíle. Po vytvoření cíle pro hlavní součást výstupu daný cíl potlačí výchozí chování a soubor nebo složka je odeslána podle nastavení cíle.

## <a name="availability-and-general-prerequisites"></a>Dostupnost a obecné požadavky

Funkce cíle elektronického výkaznictví není k dispozici ve verzi Microsoft Dynamics AX 7.0 (únor 2016). Proto je nutné nainstalovat Microsoft Dynamics 365 for Operations verzi 1611 (listopad 2016) nebo novější, aby bylo možné použít následující typy cílů:

- [E-mail](er-destination-type-email.md)
- [Archivovat](er-destination-type-archive.md)
- [Soubor](er-destination-type-file.md)
- [Obrazovka](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Případně můžete nainstalovat jeden z následujících požadovaných softwarů. Upozorňujeme však, že tyto alternativy poskytují omezené možnosti cíle ER.

- Verze aplikace Microsoft Dynamics AX 7.0.1 (květen 2016)
- [Oprava hotfix pro aplikaci správy cílů elektronického výkaznictví](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Je zde také typ cíle [tisku](er-destination-type-print.md). Chcete-li ho použít, je nutné nainstalovat Microsoft Dynamics 365 Finance verze 10.0.9 (duben 2020).

## <a name="overview"></a>Přehled

Cíle můžete nastavit pouze pro konfigurace elektronického výkaznictví, které byly [importovány](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) do aktuální instance Finance, a u formátů, které jsou k dispozici na stránce **Konfigurace elektronického výkaznictví**. Funkce správy cílů elektronického výkaznictví je k dispozici v nabídce **Správa organizace** \> **Elektronické výkaznictví** \> **Cíl elektronického výkaznictví**.

### <a name="default-behavior"></a>Výchozí chování

Výchozí chování pro konfiguraci formátu ER závisí na typu provádění, který zadáte při spuštění formátu ER.

Pokud v dialogovém okně **Zpráva Intrastat** na pevné záložce **Spustit na pozadí** nastavíte možnost **Dávkové zpracování** na **Ne**, formát ER se okamžitě spustí v interaktivním režimu. Po úspěšném dokončení tohoto spuštění je generovaný odchozí dokument zpřístupněn ke stažení.

Pokud nastavíte možnost **Dávkové zpracování** na **Ano**, formát ER se spustí v [dávkovém](../sysadmin/batch-processing-overview.md) režimu. Příslušná dávková úloha je vytvořena na základě parametrů, které zadáte na kartě **Spustit na pozadí** dialogového okna **Parametry elektronického výkaznictví**.

> [!NOTE]
> Popis úlohy vás informuje o průběhu mapování formátu elektronického výkaznictví. Zahrnuje také název provedené komponenty ER.

[![Spuštění formátu ER.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Informace o této úloze najdete na několika místech:

- V části **Společné** \> **Dotazy** \> **Dávkové úlohy** \> **Moje dávkové úlohy** ověřte stav naplánované úlohy.
- Přejděte na **Organizační správa** \> **Elektronické výkaznictví** \> **Úlohy elektronického výkaznictví** a zkontrolujte stav naplánované úlohy a výsledky provedení u dokončené úlohy. Po úspěšném dokončení úlohy vyberte **Zobrazit soubory** na stránce **Úlohy elektronického výkaznictví** pro získání generovaného odchozího dokumentu.

    > [!NOTE]
    > Tento dokument je uložen jako příloha aktuálního záznamu úlohy a je řízen rámcem [Správa dokumentů](../../fin-ops/organization-administration/configure-document-management.md). [Typ dokumentu](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), který se používá k ukládání artefaktů ER tohoto typu, je nakonfigurován v okně [Parametry ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Na stránce **Úlohy elektronického výkaznictví** vyberte **Zobrazit souboru** k zobrazení seznamu případných chyb a varování generovaných v průběhu provádění úlohy.

    [![Prohlížení seznamu úloh ER.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Uživatelem nakonfigurované chování

Na stránce **Cíl elektronického výkaznictví** můžete přepsat výchozí chování pro konfiguraci. Importované konfigurace na této stránce nejsou zobrazeny, dokud nezvolíte **Nový** a pak v poli **Odkaz** nevyberete konfiguraci, pro kterou chcete vytvořit nastavení cíle.

[![Výběr konfigurace v poli Odkaz.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Po vytvoření odkazu můžete vytvořit cíl souboru pro každou výstupní komponentu **složky** nebo **souboru** odkazovaného formátu elektronického výkaznictví.

[![Vytvoření cíle souboru.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Poté lze povolit nebo zakázat jednotlivé cíle pro cíl souboru v dialogovém okně **Nastavení cíle**. Tlačítko **Nastavení** se používá k řízení všech cílů pro vybraný cíl souboru. V dialogovém okně **Nastavení cíle** lze ovládat samostatně každý cíl nastavením možnosti **Povoleno**.

Ve verzích Finance **před verzí 10.0.9** můžete vytvořit **jeden cíl souboru** pro každou komponentu výstupu ve stejném formátu, jako je složka nebo soubor vybraný v poli **Název souboru**. Ve **verzi 10.0.9 a novější** však můžete vytvořit **více cílů souboru** pro každou výstupní součást stejného formátu.

Pomocí této funkce můžete například konfigurovat cíle souborů pro součást souboru, která se používá ke generování odchozího dokumentu ve formátu aplikace Excel. Jeden cíl ([archiv](er-destination-type-archive.md)) lze nakonfigurovat tak, aby ukládal původní soubor aplikace Excel do archivu úloh elektronického výkaznictví, a další místo určení ([E-mail](er-destination-type-email.md)) lze nakonfigurovat tak, aby současně [převedl](#OutputConversionToPDF) soubor Excel do formátu PDF a odeslal soubor PDF e-mailem.

[![Konfigurace více cílů pro jeden prvek formátu.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Při spuštění formátu ER se vždy spustí všechny cíle, které byly nakonfigurovány pro komponenty formátu. Kromě toho v aplikaci Finance **verze 10.0.17 a novější** byla vylepšena funkčnost cílů ER a nyní vám umožňuje konfigurovat různé sady cílů pro jeden formát ER. Tato konfigurace označí každou sadu jako nakonfigurovanou pro konkrétní akci uživatele. Rozhraní API ER bylo [prodlouženo](er-apis-app10-0-17.md), takže lze poskytnout akci, kterou uživatel provede, spuštěním formátu ER. Poskytnutý kód akce je předán cílům ER. Můžete spustit různé cíle ve formátu ER, v závislosti na poskytnutém kódu akce. Další informace viz [Konfigurace cílů ER závislých na akci](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Typy cílových míst

Pro formáty elektronického výkaznictví jsou nyní podporovány následující cíle. Můžete zakázat nebo povolit všechny typy současně. Tímto způsobem můžete neprovádět žádnou akci, nebo poslat součásti do všech nakonfigurovaných cílů.

- [E-mail](er-destination-type-email.md)
- [Archivovat](er-destination-type-archive.md)
- [Soubor](er-destination-type-file.md)
- [Obrazovka](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Vytisknout](er-destination-type-print.md)

## <a name="applicability"></a>Použitelnost

Cíle můžete nastavit pouze pro konfigurace EV, které byly importovány, a u formátů, které jsou k dispozici na stránce **Konfigurace elektronického výkaznictví**.

> [!NOTE]
> Nakonfigurované cíle jsou specifické pro konkrétní společnost. Pokud plánujete použití formátu elektronického výkaznictví v různých společnostech aktuální instance Finance, je nutné pro každou z těchto společností nakonfigurovat cíle pro tento formát elektronického výkaznictví.

Když konfigurujete cíle souboru pro vybraný formát, nakonfigurujete je pro celý formát.

[![Odkaz na konfiguraci.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Zároveň můžete mít více verzí formátu, které byly importovány do aktuální instance Finance. Můžete je zobrazit, pokud vyberete odkaz **Konfigurace**, který je nabídnutý při výběru pole **Odkaz**.

[![Verze konfigurace.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Ve výchozím nastavení jsou konfigurované cíle použity pouze při spuštění verze formátu elektronického výkaznictví, jejíž stav je buď **Dokončeno** nebo **Sdíleno**. V některých případech je však nutné použít nakonfigurované cíle při spuštění verze formátu elektronického výkaznictví. Například upravíte verzi konceptu vašeho formátu a chcete použít nakonfigurované cíle pro otestování, jak bude vygenerovaný výstup poskytnut. Chcete-li použít cíle pro formát elektronického výkaznictví při spuštění verze konceptu, postupujte podle následujících kroků.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte volbu **Použít cíle pro stav konceptu** na **Ano**.

[![Možnost Použít cíle pro stav konceptu.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Chcete-li použít verzi konceptu ve formátu elektronického výkaznictví, musíte odpovídajícím způsobem označit formát elektronického výkaznictví.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte možnost **Spustit nastavení** na **Ano**.

[![Možnost Spustit nastavení.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Po dokončení tohoto nastavení bude k dispozici možnost **Spustit koncept** pro formáty elektronického výkaznictví, které jste změnili. Tuto možnost nastavte na **Ano**, chcete-li při spuštění formátu použít verzi konceptu formátu.

[![Možnost Spustit koncept.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Zpracování selhání cíle

Formát elektronického výkaznictví je obvykle spuštěn v rozsahu určitého obchodního procesu. Doručení odchozího dokumentu, který je generován při spuštění formátu elektronického výkaznictví, však musí být někdy považováno za součást tohoto obchodního procesu. V takovém případě, pokud je doručení vygenerovaného odchozího dokumentu do konfigurovaného cíle neúspěšné, musí být provádění obchodního procesu zrušeno. Chcete-li nakonfigurovat příslušný cíl elektronického výkaznictví, vyberte možnost **Zastavit zpracování při selhání**.

Například konfigurujete zpracování plateb dodavatele, aby byl spuštěn formát elektronického výkaznictví **Převod kreditu ISO20022** pro generování souboru plateb a doplňkových dokumentů (například průvodní dopis a kontrolní sestava). Pokud má být platba považována za úspěšnou pouze v případě, že průvodní dopis byl úspěšně doručen e-mailem, je nutné zaškrtnout políčko **Zastavit zpracování při selhání** pro komponentu **Průvodní dopis** v příslušném cíli souboru, jak je znázorněno na následujícím obrázku. V tomto případě bude stav platby, která je vybrána ke zpracování, změněn z **Žádný** na **Odesláno** pouze v případě, že vygenerovaný dopis je úspěšně přijat pro doručení poskytovatelem e-mailu, který je konfigurován v instanci Finance.

[![Konfigurace zpracování procesu pro selhání cíle souboru.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Pokud odškrtnete políčko **Zastavit zpracování při selhání** pro komponentu **Průvodní dopis** v cíli souboru, bude platba považována za úspěšně zpracovanou i tehdy, když nebude průvodní dopis úspěšně odeslán e-mailem. Stav platby bude změněn z **Žádný** na **Odesláno** i v případě, že průvodní dopis nelze odeslat, protože například chybí e-mailová adresa příjemce nebo odesílatele, nebo jsou adresy nesprávné.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Výstupní převod do souboru PDF

Chcete-li převést výstup ve formátu Microsoft Office (Excel nebo Word) do formátu PDF, můžete použít volbu převodu do PDF.

### <a name="make-pdf-conversion-available"></a>Zpřístupnění převodu do PDF

Chcete-li, aby byla v aktuální instanci modulu Finance k dispozici možnost převodu PDF, otevřete pracovní prostor **Správa funkcí** a zapněte funkci **Převod odchozích dokumentů elektronického výkaznictví z formátů Microsoft Office do PDF**.

[![Zapnutí funkce převodu odchozích dokumentů do PDF ve správě funkcí.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Použitelnost

Ve verzích Finance **před verzí 10.0.18** možnost převodu PDF lze zapnout pouze pro komponenty **Excel\\Soubor**, které se používají ke generování výstupu ve formátu Office (Excel nebo Word). Je-li tato možnost zapnuta, bude výstup vygenerovaný ve formátu Office automaticky převeden do formátu PDF. Nicméně ve **verzi 10.0.18 a novější** můžete také zapnout tuto možnost pro komponenty typu **Běžný\\Soubor**.

> [!NOTE]
> Věnujte pozornost varovné zprávě, kterou obdržíte při zapnutí možnosti převodu PDF pro komponentu ER typu **Běžný\\Soubor**. Tato zpráva vás informuje, že neexistuje způsob, jak v době návrhu zaručit, že vybraná komponenta souboru za běhu vystaví obsah ve formátu PDF nebo obsah převáděný do formátu PDF. Tuto možnost byste proto měli zapnout, pouze pokud jste si jisti, že vybraná komponenta souboru byla nakonfigurována tak, aby za běhu vystavovala obsah ve formátu PDF nebo obsah převáděný do formátu PDF.
> 
> Pokud zapnete možnost převodu PDF pro komponentu formátu, pokud tato komponenta vystavuje obsah v jiném formátu než PDF a pokud vystavený obsah nelze převést do formátu PDF, dojde za běhu k výjimce. Zpráva, kterou obdržíte, vás informuje, že vygenerovaný obsah nelze převést do formátu PDF.

### <a name="limitations"></a>Omezení

Ve Finance **verze 10.0.9** je možnost převodu PDF k dispozici pouze pro nasazení v cloudu. Počínaje verzí Finance **10.0.27** možnost převodu PDF je k dispozici pro jakékoli místní nasazení, které má povolené [Internetové připojení](../user-interface/client-disconnected.md).

Vtvořený dokument PDF je omezen na maximální počet 300 stránek.

Ve Finance **verze 10.0.9**, vytvořeném z výstupu z aplikace Excel, je podporována pouze orientace stránky na šířku. Počínaje verzí Finance **10.0.10** můžete [určit orientaci stránky](#SelectPdfPageOrientation) v dokumentu PDF, který je vytvořen z výstupu aplikace Excel při konfiguraci cíle ER.

Pro převod výstupu, který neobsahuje žádná vložená písma, se používají pouze běžná systémová písma operačního systému Windows.

### <a name="resources"></a>Prostředky

Před verzí Finance 10.0.29 bylo možné převod PDF provést pouze mimo aktuální instanci Finance. Vygenerovaný soubor byl odeslán z Finance do konverzní služby a tato služba pak vrátila převedený dokument. Nicméně ve verzi **10.0.29 a pozdější** navíc k funkcí **Převést odchozí dokumenty elektronického vykazování z formátů Microsoft Office do PDF** můžete aktivovat funkci **Využít prostředky aplikace k provedení převodu dokumentů CBD z Wordu do formátu PDF**. Tato funkce umožňuje převádět vygenerované dokumenty Wordu do formátu PDF lokálně pomocí prostředků aplikačního serveru v aktuální instanci Finance. 

Zde jsou výhody místního převodu PDF, když je aktivní funkce **Využít prostředky aplikace k provedení převodu dokumentů CBD z Wordu do formátu PDF**.

- Vytvořený dokument PDF není [omezen](#limitations) na maximální počet stránek.
- Dokument aplikace Word, který je převeden, může obsahovat [velké množství ovládacích prvků obsahu](https://fix.lcs.dynamics.com/Issue/Details?bugId=647877&dbType=3).
- V místním nasazení není vyžadováno připojení k internetu.

### <a name="use-the-pdf-conversion-option"></a>Použití možnosti převodu do PDF

Chcete-li zapnout převod do PDF pro cíl souboru, zaškrtněte políčko **Převést do PDF**.

[![Zapnutí převodu do PDF pro cíl souboru.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Výběr orientace stránky pro převod do PDF</a>

Vygenerujete-li konfiguraci ER ve formátu aplikace Excel a chcete ji převést do formátu PDF, můžete explicitně určit orientaci stránky v dokumentu PDF. Když zaškrtnete políčko **Převést do PDF** pro povolení převodu PDF pro cíl souboru, který vytváří výstupní soubor ve formátu aplikace Excel, bude pole **Orientace stránky** k dispozici na pevné záložce **Nastavení převodu PDF**. V poli **Orientace stránky** vyberte upřednostňovanou orientaci.

[![Výběr orientace stránky pro převod do PDF.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Chcete-li mít možnost vybrat orientaci stránky PDF, musíte nainstalovat Finance verze 10.0.10 nebo novější. Ve verzích Finance **před verzí 10.0.23** tato možnost nabízí následující možnosti orientace stránky:

- Na výšku
- Na šířku

Vybraná orientace stránky se použije pro všechny stránky odchozího dokumentu, který jsou generován ve formátu aplikace Excel a následně převedeny do formátu PDF.

Nicméně ve **verzi 10.0.23 a novější** byl seznam možností orientace stránky rozšířen takto:

- Na výšku
- Na šířku
- Specifické pro list

Když vyberete možnost **Specifické pro pracovní list**, je každý list vygenerovaného excelového sešitu převeden do PDF pomocí orientace stránky, která byla pro tento list nakonfigurována v použité šabloně Excelu. Můžete tedy mít konečný dokument PDF obsahující stránky na výšku a na šířku. 

Pokud je konfigurace ER ve formátu aplikace Word převedena na PDF, bude orientace dokumentu PDF vždy vzata z dokumentu aplikace Word.

## <a name="output-unfolding"></a>Rozbalení výstupu

Když konfigurujete cíl pro komponentu **Složka** vašeho formátu ER, můžete určit, jak je výstup této komponenty doručen do nakonfigurovaného cíle.

### <a name="make-output-unfolding-available"></a>Zpřístupnění výstupu

Chcete-li zpřístupnit možnost rozložení výstupu v aktuální instanci Finance, otevřete praconví prostor **Správa funkcí** a zapněte funkci **Povolte konfiguraci cílů ER k odesílání obsahu složek jako samostatných souborů**.

### <a name="applicability"></a>Použitelnost

Možnost rozložení výstupu lze konfigurovat pouze pro komponenty formátu typu **Složka**. Když začnete konfigurovat komponentu **Složka**, pevná záložka **Všeobecné** bude k dispozici na stránce **Cíl elektronického hlášení**. 

### <a name="use-the-output-unfolding-option"></a>Použijte možnost rozložení výstupu

Na pevné záložce **Všeobecné** v poli **Odeslat složku jako** vyberte jednu z následujících hodnot:

- **ZIP archiv** - Doručit vygenerovaný soubor jako soubor zip.
- **Oddělit soubory** - Doručit každý soubor vygenerovaného souboru zip jako samostatný soubor.

    > [!NOTE]
    > Když vyberete **Oddělte soubory**, generovaný výstup se shromažďuje v paměti ve stavu zip. Proto maximální [limit velikosti souboru](er-compress-outbound-files.md) se použije pro výstup ZIP, když skutečná velikost souboru může překročit tento limit. Doporučujeme vybrat tuto hodnotu, pokud očekáváte, že velikost generovaného výstupu bude příliš velká.

[![Konfigurace cíle pro komponentu Formát složky.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Omezení

Pokud nastavíte pole **Odeslat složku jako** na **Jednotlivé soubory** pro komponentu **Složka**, která obsahuje další vnořené komponenty **Složka**, nastavení se rekurzivně nepoužije na vnořené komponenty **Složka**.

## <a name="change-page-layout-properties-of-a-template"></a><a name="change-page-layout-properties-of-a-template"></a> Změna vlastnosti rozložení stránky šablony

Můžete konfigurovat cíl ER pro komponentu formátu ER, která je navržena pro použití šablony ve formátu Microsoft Office (Excel nebo Word) pro generování sestav. Pokud nejste vlastníkem tohoto formátu a potřebujete změnit vlastnosti rozložení stránky šablony formátu ve verzích Finance starších než verze 10.0.29, musíte vytvořit odvozený formát a upravit vlastnosti šablony. Poté musíte zachovat konfiguraci odvozeného formátu. Ve verzi 10.0.29 a novější však můžete změnit vlastnosti rozložení stránky šablony za běhu, abyste se vyhnuli vytváření a údržbě odvozené konfigurace formátu. Chcete-li to provést, nastavte požadované vlastnosti jako součást nastavení konfigurovaného cíle ER. Když spustíte formát ER a provedete cíl ER, který je konfigurován pro použití určitých vlastností rozložení stránky, hodnoty vlastností rozložení stránky spouštěného cíle se použijí na šablonu, kterou používáte, a nahradí vlastnosti původní šablony. U komponenty stejného formátu můžete konfigurovat různá umístění a konfigurovat různé vlastnosti rozložení stránky pro používanou šablonu.

Následující vlastnosti lze konfigurovat v cíli ER pro komponentu formátu, která je navržena pro použití šablony ve formátu Excel nebo Word:

- Orientace stránky
    - Na výšku
    - Na šířku
- Formát papíru
    - A3
    - A4
    - A5
    - B4
    - B5
    - Executive
    - Právní informace
    - Písmeno
    - Statement
    - Tabloid
- Okraje stránky
    - Horní
        - Hlavička
    - Dolní
        - Zápatí
    - Levý
    - Pravý

> [!NOTE]
> Orientace stránky šablony, která je konfigurována tímto způsobem, musí být stejná s [orientací stránky pro převod PDF](#select-a-page-orientation-for-pdf-conversion), pokud je konfigurován převod do PDF.

Musíte vybrat jednotku délky pro nastavení okrajů stránky:

- Palce
- Centimetry
- Milimetry

![Nastavte vlastnosti rozložení stránky na cílové stránce elektronického výkaznictví.](./media/er_destinations-set-page-layout-properties.png)

> [!TIP]
> Když je hodnota okraje určena v centimetrech s přesností na více desetinných míst, je za běhu zaokrouhlena na nejbližší hodnotu s 1 desetinnou čárkou.
>
> Když je hodnota okraje určena v milimetrech s přesností v desetinných místech, je za běhu pro aplikaci Excel zaokrouhlena na nejbližší celočíselnou hodnotu bez desetinné čárky.
>
> Když je hodnota okraje určena v milimetrech s přesností na více desetinných míst, je za běhu pro aplikaci Word zaokrouhlena na nejbližší hodnotu s 1 desetinnou čárkou.

## <a name="security-considerations"></a>Na co brát ohled při zabezpečení

Pro cíle EV se používají dva typy oprávnění a povinností. Jeden typ ovládá celkovou schopnost uživatele udržovat celkové cíle, které jsou nakonfigurovány pro právnickou osobu (to znamená, že kontroluje přístup ke stránce **Cíle elektronického výkaznictví**). Druhý typ určuje, zda uživatel aplikace může přepsat v době běhu nastavení cíle, které upravil vývojář elektronického výkaznictví nebo funkční konzultant EV.

| Role (název stromu AOT)                     | Název role                                  | Funkční oprávnění (název stromu AOT)                     | Název funkčního oprávnění                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Návrhář elektronického výkaznictví             | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| ERFunctionalConsultant              | Funkční konzultant elektronického výkaznictví | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| PaymAccountsPayablePaymentsClerk    | Úředník plateb závazků            | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |
| PaymAccountsReceivablePaymentsClerk | Úředník plateb pohledávek         | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |

> [!NOTE]
> V předchozích úkolech jsou použita dvě oprávnění. Tato oprávnění mají stejné názvy jako odpovídající role: **ERFormatDestinationConfigure** a **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Provedl(a) jsem import elektronických konfigurací a vidím je na stránce s konfiguracemi elektronického výkaznictví. Proč je ale nevidím na stránce Cíle elektronického výkaznictví?

Ujistěte se, že jste zvolili **Nový** a potom zvolte konfiguraci v poli **Odkaz**. Stránka **Místa určení elektronického výkaznictví** zobrazuje pouze konfigurace, pro které byly nakonfigurovány cíle.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Existuje nějaký způsob, jak určit, který účet úložiště Microsoft Azure a úložiště Azure Blob se bude používat?

Č. Používá se výchozí úložiště Microsoft Azure Blob definované a používané pro systém správy dokumentů.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Jaký je účel cíle souboru v nastavení cíle? Co toto nastavení dělá?

Cíl **Soubor** se používá k ovládání dialogového okna webového prohlížeče, když spustíte formát ER v interaktivním režimu. Pokud povolíte tento cíl, nebo pro konfiguraci není definován žádný cíl, zobrazí se po vytvoření výstupního souboru ve webovém prohlížeči dialogové okno uložení nebo otevření.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Můžete dát příklad vzorce, který odkazuje na účet dodavatele, aby mu bylo možné odeslat e-mail?

Vzorec je specifický pro konfiguraci EV. Například pokud použijete konfiguraci „platební převod ISO 20022“, můžete pomocí konfigurace **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** nebo **model.Payments.Creditor.Identification.SourceID** získat účet přidruženého dodavatele.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Jedna z mých konfigurací formátu obsahuje více souborů, které jsou seskupeny do jedné složky (například složka1 obsahuje soubor1, soubor2 a soubor3). Jak mohu nastavit cíle tak, aby se soubor složka1.zip nebyl nevytvořil, soubor1 byl odeslán prostřednictvím e-mailu, soubor2 byl odeslán na server SharePoint a soubor3 bylo možné otevřít ihned po spuštění konfigurace?

Váš formát musí být nejdříve k dispozici v konfiguracích elektronického výkaznictví. Když je splněn požadavek, otevřete stránku **Místo určení elektronického výkaznictví** a vytvořte nový odkaz na tuto konfiguraci. Pak je třeba mít k dispozici čtyři cíle souboru, jeden pro každou součást výstupu. Vytvořte první cíl souboru, pojmenujte jej např. jako **Složka** a vyberte název souboru, který představuje složku ve vaší konfiguraci. Poté zvolte **Nastavení** a ujistěte se, že jsou zakázány všechny cíle. Pro tento cíl souboru se složka nevytvoří. Ve výchozím nastavení se soubory budou chovat stejným způsobem díly hierarchickým závislostem mezi soubory a nadřazenými složkami. Jinými slovy se nikam neodešlou. Chcete-li přepsat výchozí chování, je nutné vytvořit tři další cíle souborů, jeden pro každý soubor. V nastavení cíle pro každý ze souborů je nutné povolit cíl, na který má být soubor odeslán.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Konfigurace cílů ER závislých na akci](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

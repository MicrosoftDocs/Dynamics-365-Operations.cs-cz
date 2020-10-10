---
title: Generování formulářů FTI k tisku
description: Toto téma vysvětluje, jak použít architekturu elektronického výkaznictví pro vygenerování formulářů volné faktury k tisku jako dokumentů sady Microsoft Office.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 4412fb08c8548c8ebe8455db0547618578e5e5b4
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893356"
---
# <a name="generate-printable-fti-forms"></a>Generovat formulářů FTI k tisku

[!include[banner](../includes/banner.md)]

Architektura elektronického výkaznictví vám umožní vygenerování formulářů volné faktury k tisku jako dokumentů sady Microsoft Office. Toto téma poskytuje informace o tom, jak vytvořit vlastní konfigurace, stejně jako podrobnosti o dostupných konfiguračních šablonách.

## <a name="overview"></a>Přehled

Kromě existující funkce generování tisknutelných formulářů FTI pomocí služeb Microsoft SQL Server Reporting Services (SSRS) můžete nyní použít architekturu elektronického výkaznictví. Můžete spravovat tisknutelné FTI formuláře v aplikaci Microsoft Office Excel a Word. Rozložení, tok dat a formátování můžete také upravit tak, aby splňovaly konkrétní požadavky, aniž by došlo k změnám kódu.

> [!NOTE]
> Pokud chcete začít s přehledem stávajících konfigurací elektronického výkaznictví pro tento vzorek řešení tisknutelných formulářů FTI, lze přejít přímo do oddílu **Stažení vzorové konfigurace elektronického výkaznictví pro generování tisknutelných formulářů FTI** dále v tomto tématu.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Vytvoření přizpůsobených konfigurací pro tisknutelné formuláře FTI
V rámci svého přizpůsobeného řešení pro tisknutelné formuláře FTI je nutné vytvořit sadu konfigurací elektronického výkaznictví.

### <a name="configure-the-er-data-model"></a>Konfigurace datového modelu elektronického výkaznictví
Vaše aplikace musí zahrnovat konfiguraci datového modelu elektronického výkaznictví, která obsahuje datový model, který popisuje obchodní doménu fakturace odběratele. Jako požadavek musí být název datového modelu **CustomersInvoicing**. Informace o návrhu datových modelů elektronického výkaznictví naleznete v tématu [Návrh datového modelu specifického pro doménu pro elektronické výkaznictví](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Konfigurace mapování modelu elektronického výkaznictví
Aplikace musí obsahovat mapování modelu elektronického výkaznictví pro datový model CustomersInvoicing. Mapování modelu může být buď konfigurace datového modelu elektronického výkaznictví nebo konfigurace mapování modelu elektronického výkaznictví. Název kořenového popisovače mapování modelu musí být **FreeTextInvoice**.

Mapování musí obsahovat následující zdroje dat:

- Typ zdroje dat: **Záznamy tabulky**

    - Tento zdroj dat musí mít název **CustInvoiceJour**.
    - Musí odkazovat na tabulku aplikace CustInvoiceJour.
    - Používá se při běhu pro přechod z aplikace do mapování modelu elektronického výkaznictví na seznam faktur, které byly vybrány pro tisk.

- Typ zdroje dat: **Objekt**

    - Tento zdroj dat musí mít název **PrintMgmtPrintSettingDetail**.
    - Musí odkazovat na třídu aplikace **PrintMgmtPrintSettingDetail**.
    - Používá se při běhu k přechodu z aplikace na podrobnosti mapování modelu elektronického výkaznictví nastavení správy tisku pro spuštěný formát elektronického výkaznictví.

Podrobnosti o integraci aplikace s architekturou elektronického výkaznictví najdete v třídě **ERPrintMgmtReportFormatSubscriber** (model integrace sady aplikace elektronického výkaznictví) ve zdrojovém kódu aplikace.

Další informace o návrhu mapování modelu elektronického výkaznictví naleznete v tématu [Definování mapování modelu a volba datových zdrojů pro elektronické výkaznictví](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>Konfigurace formátu elektronického výkaznictví
V instanci aplikace musíte mít konfiguraci formátu elektronického výkaznictví, která bude použita k vygenerování FTI formulářů. 

> [!NOTE]
> Tato konfigurace formátu musí být vytvořena pro datový model CustomersInvoicing a musí používat mapování modelu, které má kořenový popisovač **FreeTextInvoice**.

Více informací o konfiguraci formátů elektronického výkaznictví naleznete v části [Vytvoření konfigurace formátů pro elektronické výkaznictví (listopad 2016)](tasks/er-format-configuration-2016-11.md). Informace o tom, jak navrhovat formáty elektronického výkaznictví pro generování sestav ve formátu OpenXML, naleznete v části [Návrh konfigurace pro generování sestav ve formátu OPENXML pro elektronické výkaznictví (listopad 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Konfigurace správy tisku
Chcete-li generovat formuláře FTI pomocí architektury elektronického výkaznictví, můžete přiřadit formáty elektronického výkaznictví stejným způsobem jako sestavy SSRS. Chcete-li přidružit formát elektronického výkaznictví ke všem FTI pohledávek, přejděte na **Pohledávky** \> **Nastavení** \> **Formuláře** \> **Nastavení formuláře** \> **Obecné** \> **Správa tisku** \> **Volná faktura** \> **Originál**. Chcete-li přidružit formát elektronického výkaznictví ke konkrétnímu odběrateli nebo faktuře, postupujte podle následujících kroků.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Vyberte volnou fakturu, ke které se přidruží formát elektronického výkaznictví, a otevřete stránku **Nastavení správy tisku**.
3. Vyberte úroveň dokumentu k určení rozsahu faktury ke zpracování.
4. Vyberte formát elektronického výkaznictví pro konkrétní úroveň dokumentu.

![Nastavení správy tisku](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Pouze formáty elektronického výkaznictví, které používají kořenový popisovač **FreeTextInvoice** datvého modelu **CustomersInvoicing** se objeví v poli **Vyhledání formátu sestavy** pro zvolený formát.

## <a name="generate-fti-forms"></a>Generování formulářů FTI
Formuláře FTI se generují v architektuře elektronického výkaznictví stejným způsobem jako sestavy SSRS.

Chcete-li generovat formuláře FTI, můžete vybrat faktury podle rozsahu nebo podle výběru. 

![Volba faktury](media/FTIbyGER-InvoiceSelection.png)

![Náhled faktury](media/FTIbyGER-InvoiceExcelPreview.png)

Pokud používáte formáty elektronického výkaznictví pro tisk formulářu FTI tímto způsobem, použijí se výchozí cíloví umístění souboru elektronického výkaznictví. Cílové umístění nelze změnit. Více informací o konfiguraci cílových umístění elektronického výkaznictví pro formáty elektronického výkaznictví (ER) naleznete v části [Cílová umístění elektronického výkaznictví](electronic-reporting-destinations.md).

Můžete také generovat formuláře FTI při zaúčtování FTI zapnutím možnosti **Tisknout fakturu** a vypnutím možnoti **Použít cílová umístění správy tisku**.

> [!NOTE]
> Pokud používáte formáty elektronického výkaznictví pro tisk formulářu FTI tímto způsobem, použijí se výchozí cíloví umístění souboru elektronického výkaznictví. Cílové umístění můžete změnit za běhu, pokud již bylo nakonfigurováno. Chcete-li změnit cílové umístění, musíte mít následující oprávnění zabezpečení:
>
> - **Název:** ERFormatDestinationRuntimeMaintain
> - **Popisek:** Spravovat cílové umístění formátu elektronického výkaznictví za běhu

![Místo určení elektronického výkaznictví](media/FTIbyGER-ERFileDestinationSetting.png)

![Cílové umístění formátu elektronického výkaznictví](media/FTIbyGER-ERFileDestinationUsage.png)

Architektura elektronického výkaznictví aktuálně podporuje následující cílová umístění pro vygenerované dokumenty:

- **Stažený soubor** – vygenerované formuláře jsou k dispozici jako stažené soubory, které můžete uložit pomocí prohlížeče.
- **Obrazovka** – Použije se Microsoft 365 Excel k zobrazení náhledu generovaných formulářů FTI ve formátu aplikace Excel.
- **Složka SharePoint** – vygenerované formuláře jsou uloženy na základě nastavení architektury správy dokumentů.
- **Archiv aplikace** – vygenerované formuláře jsou uloženy jako přílohy záznamů protokolů provádění v úložišti Microsoft Azure.
- **E-mail** – vygenerované formuláře jsou odeslány jako e-mailové přílohy.

> [!NOTE]
> Nemůžete odeslat FTI formuláře, které jsou generovány, přímo na tiskárnu, protože přímý tisk používající agenta směrování tisku aplikace Dynamics není aktuálně podporován.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Stažení vzorové konfigurace elektronického výkaznictví pro generování tisknutelných formulářů FTI
Můžete si stáhnout vzorové konfigurace elektronického výkaznictví pro jejich použití jako šablony pro vaše řešení FTI. Tyto konfigurace jsou uloženy v knihovně sdíleného majetku v aplikaci Microsoft Dynamics Lifecycle Services. Konfigurace zahrnují:

- Konfigurace **Model fakturace odběratele** obsahuje požadovaný datový model a mapování modelu.
- Konfigurace **Sestava FTI odběratele (GER)** obsahuje vzorový formát.

> [!NOTE]
> Tyto konfigurace byly vytvořeny jako vzorové, aby vám pomohly ujasnit možné scénáře. Budoucnost těchto konfigurací závisí na výsledcích tohoto hodnocení a přijaté zpětné vazbě.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Funkce, které jsou implementovány ve vzorovém formátu elektronického výkaznictví
Ve vzorové konfiguraci formátu elektronického výkaznictví je použit jako šablona pro generování formulářů FTI soubor Excel.

![Návrhář formátu](media/FTIbyGER-ERFormat.png)

Aktuálně tento vzorový formát elektronického výkaznictví podporuje následující funkce pro generování FTI formulářů:

- Formuláře FTI jsou generovány jak pro původní faktury zaúčtované i nezaúčtované faktury. Opravené faktury a dobropisy nejsou podporovány.
- Formuláře FTI jsou generovány v jazyce faktury. Formát hodnot a dat v generovaných formulářích závisí na nastavení národního prostředí uživatele.
- Generované faktury zobrazují oznámení o nedostupnosti dat, pokud na fakturách, které jsou zpracovány, nejsou žádné řádky.
- Záhlaví generovaných faktur jsou založeny na formátu papíru, který byl zvolen pro formulář FTI na stránce **Parametry pohledávek**. Podrobnosti o společnosti se objeví v záhlaví generovaného formuláře faktury pouze tehdy, je-li formát papíru prázdný.
- Generované formuláře faktury uvádějí čísla společností a zákazníků osvobozených od daně, pokud byla pro formulář FTI vybrána příslušná volba na stránce **Parametry pohledávek**.
- Generované řádky faktur a části součtů faktur zobrazují měnové údaje výchozí faktury v měně registrace faktury.
- Vygenerovaná část součtu faktury zobrazuje peněžní podrobnosti v EUR a měně registrace faktury, když je povolena možnost **Vytisknout částku v měně představující euro** na stránce **Parametry pohledávek**.
- Vygenerované formuláře faktur zobrazují všechny dostupné poznámky k faktuře, na základě nastavení na stránce **Parametry pohledávek**. Poznámky jsou k dispozici pro celou fakturu a každý řádek faktury.
- Vygenerované formuláře faktur zahrnují poznámky pro formuláře FTI odběratele a jazyk zpracování faktury, když byly nakonfigurovány v seznamu poznámek formuláře pohledávek.
- V závislosti na nastavení správy tisku obsahují generované faktury vlastní text zápatí, pokud byl nakonfigurován pro jazyk fakturace, formát elektronického výkaznictví a rozsah dokumentu FTI
- Část součtů vygenerovaných formulářů faktury obsahuje veškeré informace o platební slevě, které jsou k dispozici.
- Část rozvrhu plateb vygenerovaných fakturačních formulářů obsahuje veškeré podrobnosti o rozvrhu plateb, které jsou k dispozici.
- Sekce přirážek vygenerovaných fakturačních formulářů zahrnuje veškeré dostupné transakce poplatků.
- Vygenerované formuláře faktury obsahují podrobnosti o DPH, na základě nastavení **Určení DPH** na stránce **Parametry pohledávek**. Tato část zobrazuje daňové podrobnosti buď pouze v měně registrace faktur, nebo v měně registrace faktur a zúčtovací měně společnosti současně.
- Vygenerované formuláře faktury zobrazují podrobnosti oznámení přímého inkasa. Ukazují například, kdy byl pro fakturu vybrán způsob platby, který má povinné ID zmocnění inkasa, kdy byla faktura registrována v měně EUR a kdy bylo pro fakturu definováno ID zmocnění inkasa.
- Vygenerované faktury zobrazují všechny podrobnosti zálohy, které jsou k dispozici pro zaúčtované faktury.
- Vygenerované formuláře faktury lze odesílat zákazníkovi faktury jako přílohu e-mailu. Odpovídající umístění souboru elektronického výkaznictví by mělo být nakonfigurováno pro používaný formát elektronického výkaznictví.

### <a name="countryregion-specific-features"></a>Funkce specifické pro zemi nebo oblast 
Následující funkce specifické pro zemi/oblast jsou zahrnuty ve vzorovém formátu elektronického výkaznictví, aby ukázaly, jak lze zpracovávat konkrétní požadavky v konfiguracích elektronického výkaznictví.

#### <a name="norway"></a>Norsko
Podnikový registr je vložen do hlavičky vygenerovaného formuláře faktury, když je faktura zpracována pro právnickou osobu, která je nakonfigurována následujícím způsobem:

- Použije se kontext země/oblasti pro Norsko.
- Parametr **Print Foretaksregisteret** je aktivní na prodejních dokumentech.

#### <a name="spain"></a>Španělsko
**Zvláštní režim pro metodu pokladního účetnictví** je vložen do hlavičky vygenerovaného formuláře faktury, když je faktura zpracována pro právnickou osobu, která je nakonfigurována následujícím způsobem:

- Použije se kontext země/oblasti pro Španělsko.
- Zvláštní režim pro metodu pokladního účetnictví je povolen v den zpracování faktury.

Jsou-li k dispozici údaje o platebních slevách, jako je částka platební slevy a čistá částka řádku faktury, jsou uvedeny v sekci součtů faktury vygenerovaného formuláře faktury, pokud byla zpracována pro právnickou osobu, která je nakonfigurována následujícím způsobem:

- Použije se kontext země/oblasti pro Španělsko.
- Možnost **U faktury je použita platební sleva** je pro fakturu zapnuta (**Parametry hlavní knihy** \> **Sekce DPH**).

#### <a name="italy"></a>Itálie
Značka slev na zboží je uvedena na řádcích faktur vygenerované faktury, když je zpracovávána pro právnickou osobu, která je konfigurována podle kontextu země/oblasti pro Itálii.

#### <a name="finland"></a>Finsko
Kromě vygenerovaného formuláře faktury lze vygenerovat převodní poukázky žira následujícím způsobem:

- Pro právnickou osobu, která používá kontext země/oblasti pro Finsko a má alespoň jeden bankovní účet označený jako **Žiro účet** a **Čárový kód banky**. 
- Pro fakturu, která je označena jako povinná pro **finskou** přidruženou přílohu platby

![Poukázka žira](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Vzorový formát elektronického výkaznictví byl nakonfigurován tak, aby volitelně generoval převodní poukázky žira v samostatném listu.

> [!NOTE]
> Nejprve musíte nainstalovat písmo, které se použije k vygenerování čárového kódu na místním počítači, ve kterém bude vytvořen náhled vygenerovaného formuláře faktury ve formátu aplikace Excel.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Použití vzorového formátu elektronického výkaznictví pro konfiguraci cílů e-mailu
Použijte následující prvky vzorového formátu elektronického výkaznictví pro konfiguraci cílů e-mailu:

- Na e-mailovou adresu kontaktní osoby odběratele lze přistoupit prostřednictvím následujícího výrazu elektronického výkaznictví: **model.InvoiceBase.Contact.ElectronicMail**.
- K textu předmětu e-mailu lze přistoupit prostřednictvím následujícího výrazu elektronického výkaznictví: **Emailing.TxtToUse.Subject**.
- K tělu e-mailu lze přistoupit prostřednictvím následujícího výrazu elektronického výkaznictví: **Emailing.TxtToUse.Body**.

![Nastavení cíle](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Výchozí text předmětu a textu e-mailu je definován ve vzorovém formátu elektronického výkaznictví. Jazyk závisí na popiscích formátu. Tento výchozí text se použije pro e-maily, pokud vlastní šablona e-mailu organizace s předdefinovaným ID **ERFTITMP** nebyla přidána.

> [!NOTE]
> ID šablony e-mailu **ERFTITMP** bylo definováno ve vzorovém formátu elektronického výkaznictví. Lze ho změnit podle potřeby v novém formátu elektronického výkaznictví vytvořeného z tohoto vzorového formátu.

Pokud byla pro právnickou osobu, pro kterou zpracováváte fakturu, s předdefinovaným ID **ERFTITMP**, přidána šablona e-mailu organizace, pro vygenerování e-mailu se použije šablona předmětu a těla e-mailu. 

![Šablony e-mailu organizace](media/FTIbyGER-EmailTemplate.png)

![Odeslat šablonu e-mailu](media/FTIbyGER-EmailTemplateBody.png)

Výraz elektronického výkaznictví **Emailing.TxtToUse.Subject** vzorového formátu elektronického výkaznictví je nakonfigurován pro nahrazení všech výskytů zástupce %1 identifikátorem ID faktury.

Výraz **Emailing.TxtToUse.Body** vzorového formátu je nakonfigurován pro následující nahrazení za zástupce:

- %1 je nahrazen jménem kontaktní osoby odběratele.
- %2 je nahrazen názvem společnosti.
- %3 je nahrazen jménem odběratele.
- %4 je nahrazen jménem kontaktní osoby společnosti.
- %5 je nahrazen funkcí kontaktní osoby společnosti.
- %6 je nahrazen e-mailovou adresou kontaktní osoby společnosti.

![E-mail](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Další zdroje
[Přehled elektronického výkaznictví](general-electronic-reporting.md)

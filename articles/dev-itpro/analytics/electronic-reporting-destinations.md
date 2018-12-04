---
title: "Místa určení elektronického výkaznictví"
description: "Pro každou konfiguraci formátu elektronického výkaznictví (ER) a její komponenty (složku nebo soubor) lze konfigurovat cíl. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. Tento článek popisuje správu cílů EV, typy podporovaných cílů a důležité informace o zabezpečení."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 301dccaf154c3c12bcc4d611a147cdef03b8f851
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="electronic-reporting-er-destinations"></a>Místa určení elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Pro každou konfiguraci formátu elektronického výkaznictví (ER) a její komponenty (složku nebo soubor) lze konfigurovat cíl. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. Tento článek popisuje správu cílů EV, typy podporovaných cílů a důležité informace o zabezpečení.

Konfigurace formátu pro Elektronické výkaznictví (EV) obvykle obsahuje alespoň jednu součást výstupu: soubor. Konfigurace obvykle obsahují více součástí výstupního souboru různých typů (například XML, TXT nebo XLSX), které jsou seskupeny do buď jedné složky nebo více složek. Správa destinací EV umožňuje předem nastavit, co se stane při spuštění každé ze součástí. Ve výchozím nastavení se při spuštění konfigurace uživateli zobrazí dialogové okno, které umožní uživateli uložit nebo otevřít soubor. Stejné chování se také používá při importu konfigurace EV, když pro ně nechcete konfigurovat žádné konkrétní cíle. Po vytvoření cíle pro hlavní součást výstupu daný cíl potlačí výchozí chování a soubor nebo složka je odeslána podle nastavení cíle.

## <a name="availability-and-general-prerequisites"></a>Dostupnost a obecné požadavky
Funkce cíle elektronického výkaznictví není k dispozici ve verzi Microsoft Dynamics AX 7.0 (únor 2016). Proto je třeba nainstalovat Microsoft Dynamics 365 for Operations verzi 1611 (listopad 2016), abyste mohli použít všechny funkce, které jsou popsány v tomto tématu. Případně můžete nainstalovat jeden z následujících požadovaných softwarů. Upozorňujeme však, že tyto alternativy poskytují omezené možnosti cíle ER.

- Aplikace Microsoft Dynamics AX verze 7.0.1 (květen 2016)
- [Opravy hotfix pro aktualizace](https://fix.lcs.dynamics.com/issue/results/?q=3160213) správy cílů EV

Cíle můžete nastavit pouze pro konfigurace EV, které byly importovány, a u formátů, které jsou k dispozici na stránce **Konfigurace elektronického výkaznictví**.

## <a name="overview"></a>Přehled
Funkce správy cílů EV je k dispozici v nabídce **Správa organizace** &gt; **Elektronické výkaznictví**. Zde můžete přepsat výchozí chování pro konfiguraci. Importované konfigurace zde nejsou zobrazeny, dokud neklepnete na tlačítko **Nový** a pak v poli **Odkaz** nevyberete konfiguraci, pro kterou chcete vytvořit nastavení cíle.

[![Výběr konfigurace v poli Odkaz](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg)

Poté, co jste vytvořili odkaz, můžete vytvořit cíl souboru pro každou složku nebo pro soubor.

[![Vytvoření cíle souboru](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> [!NOTE]
> Můžete vytvořit jedno místo určení souboru pro každou komponentu výstupu ve stejném formátu, jako je složka nebo soubor vybraný v poli **Název souboru**. Poté lze povolit nebo zakázat jednotlivé cíle pro cíl souboru v dialogovém okně **Nastavení cíle**. Tlačítko **Nastavení** se používá k řízení všech cílů pro vybraný cíl souboru. V dialogovém okně **Nastavení cíle** lze ovládat samostatně každý cíl nastavením možnosti **Povoleno**.

[![Dialogové okno Nastavení cíle](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Typy cílů
Podporovány jsou různé typy cílů. Můžete zakázat nebo povolit všechny typy současně. Tímto způsobem můžete neprovádět žádnou akci, nebo poslat součásti do všech nakonfigurovaných cílů. Následující část popisuje podporované cíle.

### <a name="email-destination"></a>E-mailový cíl

Nastavením možnosti **Povoleno** na **Ano** odešlete výstupní soubor prostřednictvím e-mailu. Po povolení této možnosti můžete zadat příjemce e-mailů a upravit předmět a tělo e-mailové zprávy. Můžete nastavit konstantní texty pro předmět a tělo e-mailu nebo můžete použít ER vzorce k dynamickému vytvoření textů e-mailů. E-mailové adresy pro ER lze konfigurovat dvěma způsoby. Konfiguraci lze dokončit stejným způsobem, jakou ji dokončuje funkce správy tisku v aplikaci Finance and Operations. Popřípadě můžete vyřešit e-mailovou adresu pomocí přímého odkazu na ER konfiguraci pomocí vzorce.

### <a name="email-address-types"></a>Typy e-mailových adres

Po kliknutí na tlačítko **Upravit** u pole **Komu** nebo **Kopie** se zobrazí dialogové okno **E-mail – komu**. Můžete zvolit typ e-mailové adresy, který použijete.

[![Dialogové okno E-mail - komu](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Správa tisku

Vyberete-li typ **Správa tisku – e-mail**, můžete zadat pevné e-mailové adresy do pole **Komu**. Pro použití jiných než pevných e-mailových adres je nutné vybrat typ zdroje e-mailu pro cíl souboru. Podporovány jsou následující hodnoty: **Odběratel**, **Dodavatel**, **Potenciální zákazník**, **Kontakt**, **Konkurent**, **Pracovník**, **Uchazeč**, **Potenciální dodavatel** a **Zakázaný dodavatel**. Po výběru typu zdroje e-mailu použijte tlačítko vedle pole **E-mail – zdrojový účet** a otevřete formulář **Návrhář receptur**. Tento formulář můžete použít k připojení vzorce, který představuje účet vybrané strany do cílového umístění e-mailu.

[![Konfigurace typu e-mailu správy tisku](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg)

Všimněte si, že vzorce jsou specifické pro konfiguraci EV. V poli **Vzorec** zadejte odkaz specifický pro dokument pro stranu typu Odběratel nebo Dodavatel. Namísto zadávání můžete najít uzel zdroje dat, který reprezentuje účet odběratele nebo dodavatele, a kliknutím na tlačítko **Přidat zdroj dat** aktualizovat vzorec. Příklad: Pokud používáte konfiguraci „platební převod ISO 20022“, uzel představující účet dodavatele má tvar **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. V opačném případě uložte řetězec zadáním libovolné hodnoty řetězce, jako například **DE-001**.

[![Návrhář receptur](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

V dialogovém okně **E-mail - komu** klikněte na koš vedle pole **E-mail – zdrojový účet** a trvale odstraňte vzorec pro zdrojový účet e-mailu. Popřípadě otevřete návrhář receptur, chcete-li změnit vzorec, který byl dříve uložen. Pro přiřazení e-mailové adresy klikněte na **Upravit**, čímž otevřete dialogové okno **Přiřadit e-mailové adresy**.

[![Přiřazení e-mailových adres k cíli e-mailu](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurační e-mail

Použijte tento typ e-mailu, pokud má použitá konfigurace uzel ve zdrojích dat, které představují e-mailovou adresu. Zdroje dat a funkce můžete použít v návrháři receptur, abyste získali správně naformátovanou e-mailovou adresu.

[![Přiřazení zdroje dat e-mailové adresy k cíli e-mailu](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg)

> [!NOTE]
> Server SMTP (Simple Mail Transfer Protocol) musí být nakonfigurován a být dostupný. Váš server SMTP můžete určit v aplikaci Finance and Operations v nabídce **Správa systému** &gt; **Nastavení** &gt; **E-mail** &gt; **Parametry e-mailu**.

### <a name="archive-destination"></a>Cíl archivace

Tuto možnost můžete použít k odeslání výstupu do složky Microsoft SharePoint nebo Microsoft Azure Storage. Nastavením **Povoleno** na **Ano** dojde k odeslání výstupu do cíle, který je definován pro vybraný typ dokumentu. K dispozici pro výběr jsou pouze typy dokumentu, kde je skupina nastavena na **Soubor**. Typy dokumentů definujete v části **Správa organizace** &gt; **Správa dokumentů** &gt; **Typy dokumentů**. Konfigurace pro cíle EV je stejná, jako nastavení pro systém správy dokumentů.

[![Stránka typu dokumentu](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg)

Umístění určuje, kde bude soubor uložen. Po povolení cíle **Archiv** lze výsledky spuštění konfigurace uložit do archivu úloh. Výsledky můžete zobrazit pod **Správa organizace** &gt; **Elektronické výkaznictví** &gt; **Archivované úlohy elektronického výkaznictví**.

> [!NOTE]
> Můžete vybrat typ dokumentu pro archiv úloh v aplikaci Finance and Operations pod **Správa organizace** &gt; **Pracovní prostory** &gt; **Elektronické výkaznictví** &gt; **Parametry elektronického výkaznictví**.

#### <a name="sharepoint"></a>SharePoint

Soubor můžete uložit do určené složky SharePoint. Výchozí server služby SharePoint určíte v možnostech **Správa organizace** &gt; **Správa dokumentů** &gt; **Parametry správy dokumentů** na kartě **SharePoint**. Po konfiguraci složky SharePoint ji můžete vybrat jako složku k uložení výstupu elektronického výkaznictví pro typ dokumentu.

[![Výběr složky služby SharePoint](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg)

#### <a name="azure-storage"></a>Úložiště Azure

Pokud je umístění typu dokumentu nastaveno na **Adresář archivu**, můžete soubor uložit do úložiště Azure.

### <a name="file-destination"></a>Místo určení souboru

Nastavením **Povoleno** na **Ano** zobrazíte po dokončení konfigurace dialogové okno pro otevření nebo uložení.

### <a name="screen-destination"></a>Cíl obrazovky

Nastavíte-li **Povoleno** na **Ano**, vytvoří se náhled výstupu. Některé typy souborů, například XML, TXT nebo PDF můžete zobrazit přímo v okně prohlížeče. U jiných typů souborů, jako jsou soubory aplikací Microsoft Excel nebo Word, se používá služba Microsoft Office Online.

### <a name="power-bi-destination"></a>Cíl Power BI

Nastavte **Povoleno** na **Ano** pro použití vaší konfigurace elektronického výkaznictví k uspořádání přenosu dat z instance aplikace Finance and for Operations do služeb Microsoft Power BI. Převedené soubory se ukládají na instanci serveru Microsoft SharePoint, který musí být konfigurován pro tento účel. Více informací získáte v části [Použití konfigurace elektronického výkaznictví k poskytnutí dat do Power BI z aplikace Finance and Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md)

> [!TIP]
> Chcete-li přepsat výchozí chování (tj. dialogové okno pro konfiguraci), můžete vytvořit odkaz cíle a cíl souboru pro součást hlavního výstupu, a potom zakázat všechny cíle.

## <a name="security-considerations"></a>Na co brát ohled při zabezpečení
Pro cíle EV se používají dva typy oprávnění a povinností. Jeden typ ovládá schopnost udržovat celkové cíle, které jsou nakonfigurovány pro právnickou osobu (to znamená, že kontroluje přístup ke stránce **Cíle elektronického výkaznictví**). Druhý typ určuje, zda uživatel aplikace může přepsat v době běhu nastavení cíle, které upravil vývojář EV nebo funkční konzultant EV.

| Role (název AOT)                     | Název role                                  | Funkční oprávnění (název stromu AOT)                     | Název funkčního oprávnění                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Návrhář elektronického výkaznictví             | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| ERFunctionalConsultant              | Funkční konzultant elektronického výkaznictví | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| PaymAccountsPayablePaymentsClerk    | Úředník plateb závazků            | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |
| PaymAccountsReceivablePaymentsClerk | Úředník plateb pohledávek         | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |

> [!NOTE]
> V předchozích úkolech jsou použita dvě oprávnění. Tato oprávnění mají stejné názvy jako odpovídající role: **ERFormatDestinationConfigure** a **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Provedl(a) jsem import elektronických konfigurací a vidím je na stránce s konfiguracemi elektronického výkaznictví. Proč je ale nevidím na stránce Cíle elektronického výkaznictví?

Ujistěte se, že jste kliknuli na **Nový** a potom zvolte konfiguraci v poli **Odkaz**. Na stránce **Místa určení elektronického výkaznictví** můžete zobrazit pouze konfigurace, pro které byly nakonfigurovány cíle.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Existuje nějaký způsob, jak určit, který účet úložiště Azure a úložiště Azure Blob se bude používat?

Ne. Používá se výchozí úložiště Azure Blob definované a používané pro systém správy dokumentů.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Jaký je účel cíle souboru v nastavení cíle? Co toto nastavení dělá?

Cíl **Souboru** se používá k řízení dialogového okna. Pokud povolíte tento cíl, nebo pro konfiguraci není definován žádný cíl, zobrazí se po vytvoření výstupního souboru dialogové okno uložení nebo otevření.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Můžete dát příklad vzorce, který odkazuje na účet dodavatele, aby mu bylo možné odeslat e-mail?

Vzorec je specifický pro konfiguraci EV. Například pokud použijete konfiguraci „platební převod ISO 20022“, můžete pomocí konfigurace **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** nebo **model.Payments.Creditor.Identification.SourceID** získat účet přidruženého dodavatele.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Jedna z mých konfigurací formátu obsahuje více souborů, které jsou skupiny do jedné složky (například složka1 obsahuje soubor1, soubor2 a soubor3). Jak mohu nastavit cíle tak, aby se soubor složka1.zip nebyl nevytvořil, soubor1 byl odeslán prostřednictvím e-mailu, soubor2 byl odeslán na server SharePoint a soubor3 bylo možné otevřít ihned po spuštění konfigurace?

Nezbytným předpokladem je, že formát musí být k dispozici v konfiguracích EV. Pokud máte svůj formát, otevřete stránku **Místo určení elektronického výkaznictví** a vytvořte nový odkaz na tuto konfiguraci. Pak je třeba mít k dispozici čtyři cíle souboru, jeden pro každou součást výstupu. Vytvořte první cíl souboru, pojmenujte jej např. jako **Složka** a vyberte název souboru, který představuje složku ve vaší konfiguraci. Poté klepněte na tlačítko **Nastavení** a ujistěte se, že jsou zakázány všechny cíle. Pro tento cíl souboru se složka nevytvoří. Ve výchozím nastavení se soubory budou chovat stejným způsobem díly hierarchickým závislostem mezi soubory a nadřazenými složkami. Jinými slovy se nikam neodešlou. Chcete-li přepsat výchozí chování, je nutné vytvořit tři další cíle souborů, jeden pro každý soubor. V nastavení cíle pro každý ze souborů je nutné povolit cíl, na který má být soubor odeslán.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


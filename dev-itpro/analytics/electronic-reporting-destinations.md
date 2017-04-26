---
title: "Místa určení elektronického výkaznictví"
description: "Pro každou konfiguraci formátu elektronického výkaznictví (ER) a její komponenty (složku nebo soubor) lze konfigurovat cíl. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. Tento článek popisuje správu cílů EV, typy podporovaných cílů a důležité informace o zabezpečení."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Místa určení elektronického výkaznictví

[!include[banner](../includes/banner.md)]


Pro každou konfiguraci formátu elektronického výkaznictví (ER) a její komponenty (složku nebo soubor) lze konfigurovat cíl. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. Tento článek popisuje správu cílů EV, typy podporovaných cílů a důležité informace o zabezpečení.

Konfigurace formátu pro Elektronické výkaznictví (EV) obvykle obsahuje alespoň jednu součást výstupu: soubor. Konfigurace obvykle obsahují více součástí výstupního souboru různých typů (například XML, TXT nebo XLSX), které jsou seskupeny do buď jedné složky nebo více složek. Správa destinací EV umožňuje předem nastavit, co se stane při spuštění každé ze součástí. Ve výchozím nastavení při spuštění konfigurace, zobrazí se dialogové okno, který umožňuje uživateli uložit nebo otevřít soubor. Stejné chování se také používá při importu konfigurace EV, když pro ně nechcete konfigurovat žádné konkrétní cíle. Po vytvoření cíle pro hlavní součást výstupu daný cíl potlačí výchozí chování a soubor nebo složka je odeslána podle nastavení cíle.

## <a name="availability-and-general-prerequisites"></a>Dostupnost a obecné požadavky
Funkce cíle ER není k dispozici v 365 Microsoft Dynamics pro verze 7.0 operace (únor 2016). Proto je třeba nainstalovat Microsoft Dynamics 365 operací (verze z listopadu 2016) Chcete-li použít všechny funkce, které jsou popsány v tomto tématu. Alternativně můžete nainstalovat jeden z následujících požadavků. Upozorňujeme však, že tyto alternativní poskytnout omezené zkušenosti určení ER.

-   365 Microsoft Dynamics pro operace aplikace verze 7.0.1 (květen 2016)
-   [Opravy hotfix pro aktualizace](https://fix.lcs.dynamics.com/issue/results/?q=3160213) správy cílů EV

Cíle můžete nastavit pouze pro konfigurace EV, které byly importovány, a u formátů, které jsou k dispozici na stránce **Konfigurace elektronického výkaznictví**.

## <a name="overview"></a>Přehled
Funkce správy cílové ER je k dispozici na **Správa organizace**&gt;**elektronických sestav**. Zde můžete přepsat výchozí chování pro konfiguraci. Importované konfigurace zde nejsou zobrazeny, dokud neklepnete na tlačítko **Nový** a pak v poli **Odkaz** nevyberete konfiguraci, pro kterou chcete vytvořit nastavení cíle.

[![Při výběru některé konfigurace v poli odkaz](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Poté, co jste vytvořili odkaz, můžete vytvořit soubor cíl pro každou složku nebo soubor. 

[![Vytvoření cílového souboru](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Poznámka:** Můžete vytvořit jedno místo určení souboru pro každou komponentu výstupu ve stejném formátu, jako je složka nebo soubor vybraný v poli **Název souboru**. Poté lze povolit a zakázat jednotlivé cíle pro cílový soubor v **nastavení cíle** dialogové okno. Tlačítko **Nastavení** se používá k řízení všech cílů pro vybraný cíl souboru. V dialogovém okně **Nastavení cíle** lze ovládat samostatně každý cíl nastavením možnosti **Povoleno**.

[![V dialogovém okně Nastavení cíl](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Typy cílů
Podporovány jsou různé typy cílů. Můžete zakázat nebo povolit všechny typy současně. Tímto způsobem můžete neprovádět žádnou akci, nebo poslat součásti do všech nakonfigurovaných cílů. Následující část popisuje podporované cíle.

### <a name="email-destination"></a>E-mailový cíl

Nastavením možnosti **Povoleno **na **Ano** odešlete výstupní soubor prostřednictvím e-mailu. Po povolení této možnosti můžete zadat příjemci e-mailu a upravit předmět a text e-mailové zprávy. Můžete nastavit konstantní text pro předmět e-mailu a tělo nebo ER vzorce můžete použít k dynamickému vytvoření texty e-mailů. E-mailové adresy pro ER lze konfigurovat dvěma způsoby. Konfiguraci lze provést způsobem funkce správy tisku v 365 Dynamics pro operace se dokončí. Alternativně můžete vyřešit e-mailovou adresu pomocí přímého odkazu na ER konfiguraci pomocí vzorce.

### <a name="email-address-types"></a>Typy e-mailových adres

Po klepnutí na tlačítko **upravit** pro **na** nebo **Cc** pole, **na Email** zobrazí se dialogové okno. Vyberte typ e-mailovou adresu používat.

[![E-mail dialogového okna](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Správa tisku

Vyberete-li **Správa tisku e-mailu** typ, můžete zadat pevné e-mailové adresy v **k** pole. Použití e-mailové adresy, které nejsou vyřešeny, je nutné vybrat typ zdroje e-mailu pro cílový soubor. Podporovány jsou následující hodnoty: **zákazníka**, **dodavatele**, **potenciálního zákazníka**, **kontakt**, **konkurence**, **pracovní**, **žadatel**, **potenciálního dodavatele**, a **Nepovoleno dodavatele**. Po výběru typu zdroje e-mailu použijte tlačítko vedle **e-mailu zdrojového účtu** pole otevřete ** návrháře vzorců ** formuláře. Tento formulář můžete použít vzorec, který představuje účet vybrané strany do cílového umístění e-mailu připojit.

[![Konfigurace e-mailu typu správy tisku](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Všimněte si, že vzorce jsou specifické pro konfiguraci EV. V poli **Vzorec** zadejte odkaz specifický pro dokument pro stranu typu Odběratel nebo Dodavatel. Namísto zadávání můžete najít uzel zdroje dat, který reprezentuje účet odběratele nebo dodavatele, a kliknutím na tlačítko **Přidat zdroj dat** aktualizovat vzorec. Příklad: Pokud používáte konfiguraci „platební převod ISO 20022“, uzel představující účet dodavatele má tvar **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. V opačném případě uložte řetězec zadáním libovolné hodnoty řetězce, jako například **DE-001**.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

V **e-mailu na** dialogové okno, klepněte na tlačítko Další přihrádky Koš **e-mailu zdrojového účtu** pole, odstraníte trvale vzorec pro e-mailový účet zdroje. Alternativně otevřete Návrhář receptur, chcete-li změnit vzorec, který byl dříve uložen. Přiřadit e-mailové adresy, klepněte na **úprava** otevřete **přiřadit e-mailové adresy** dialogové okno.

[![Přiřazení e-mailové adresy pro cíl e-mailu](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurační e-mail

Pokud používáte konfiguraci má uzel zdroje dat, který představuje e-mailovou adresu, použijte tento typ e-mailu. Zdroje dat a funkcí můžete použít v Návrháři vzorců správně naformátovanou e-mailovou adresu.

[![Přiřadit zdroj dat e-mailovou adresu pro cíl e-mailu](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Poznámka:** Server SMTP (Simple Mail Transfer Protocol) musí být nakonfigurován a být dostupný. Můžete zadat server SMTP v 365 Dynamics pro operace, v **Správa systému**&gt;**nastavení**&gt;**E-mail**&gt;**parametry e-mailu**.

### <a name="archive-destination"></a>Cíl archivace

Tuto možnost můžete použít k odeslání výstupu do složky Microsoft SharePoint nebo Microsoft Azure Storage. Nastavením **Povoleno** na **Ano **dojde k odeslání výstupu do cíle, který je definován pro vybraný typ dokumentu. K dispozici pro výběr jsou pouze typy dokumentu, kde je skupina nastavena na **Soubor**. Definování typů dokladů na **Správa organizace**&gt;**Správa dokumentů**&gt;**typy dokumentů,**. Konfigurace pro cíle EV je stejná, jako nastavení pro systém správy dokumentů.

[![Typy stránky dokumentu](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Umístění určuje, kde bude soubor uložen. Po **archivu** cíl je povolena, výsledky spuštění konfigurace lze uložit do archivu úloh. Můžete zobrazit výsledky v **Správa organizace**&gt;**elektronických sestav**&gt;**elektronických sestav archivovaných projektů**. **Poznámka:** můžete vybrat typ dokumentu pro úlohy archivu v 365 Dynamics pro operace, v **Správa organizace**&gt;**pracovní prostory**&gt;**elektronických sestav**&gt;**elektronické hlášení parametry**.

#### <a name="sharepoint"></a>SharePoint

Soubor můžete uložit do určené složky SharePoint. Definování výchozího serveru SharePoint na **Správa organizace**&gt;**Správa dokumentů**&gt;**parametry správy dokumentů**, dále **SharePoint** kartu. Po dokončení konfigurace složky služby SharePoint, vyberte jej jako složku uložení výstupu ER pro typ dokumentu. 

[![Výběr složky služby SharePoint](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Úložiště Azure

Pokud je umístění typu dokumentu nastaveno na **Adresář archivu**, můžete soubor uložit do úložiště Azure.

### <a name="file-destination"></a>Místo určení souboru

Nastavíte-li **povoleno** k **Ano**, otevřít nebo uložit dialogové okno se zobrazí po dokončení konfigurace.

### <a name="screen-destination"></a>Cílovou obrazovku

Nastavíte-li **povoleno** k **Ano**, je vytvořen Náhled výstupu. Některé typy souborů, například XML, TXT nebo PDF, můžete zobrazit přímo v okně prohlížeče. U jiných typů souborů, tato aplikace Microsoft Excel nebo Word, se používá službu Microsoft Office Online.

### <a name="power-bi-destination"></a>Power BI cíl

Nastavit **povoleno** k **Ano** zajistit přenos dat z vaší instance Dynamics 365 pro operace služby Microsoft Power BI pomocí konfigurace ER. Přenesené soubory jsou uloženy na serveru Microsoft SharePoint Server instanci, která musí být nakonfigurován pro tento účel. Další informace naleznete v tématu [použít konfigurace elektronických sestav Power BI s daty z Dynamics 365 pro operace](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tip:** Chcete-li přepsat výchozí chování (tj. dialogové okno pro konfiguraci), můžete vytvořit odkaz cíle a cíl souboru pro součást hlavního výstupu, a potom zakázat všechny cíle.

## <a name="security-considerations"></a>Na co brát ohled při zabezpečení
Pro cíle EV se používají dva typy oprávnění a povinností. Jeden typ ovládá schopnost udržovat celkové cíle, které jsou nakonfigurovány pro právnickou osobu (tedy řídí přístup k **elektronické hlášení míst** stránky). Druhý typ určuje, zda uživatel aplikace může přepsat v době běhu nastavení cíle, které upravil vývojář EV nebo funkční konzultant EV.

| Role (název AOT)                     | Název role                                  | Funkční oprávnění (název stromu AOT)                     | Název funkčního oprávnění                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Návrhář elektronického výkaznictví             | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| ERFunctionalConsultant              | Funkční konzultant elektronického výkaznictví | ERFormatDestinationConfigure        | Konfigurovat místo určení formátu elektronického výkaznictví                |
| PaymAccountsPayablePaymentsClerk    | Úředník plateb závazků            | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |
| PaymAccountsReceivablePaymentsClerk | Úředník plateb pohledávek         | ERFormatDestinationRuntimeConfigure | Konfigurovat místo určení formátu elektronického výkaznictví za běhu |

**Poznámka:** v předchozích úkolech jsou použita dvě oprávnění. Tato oprávnění mají stejné názvy jako odpovídající role: **ERFormatDestinationConfigure** a **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Provedl(a) jsem import elektronických konfigurací a vidím je na stránce s konfiguracemi elektronického výkaznictví. Ale Proč nevidím je na stránce elektronické vykazování cíle?

Ujistěte se, že klepnete na tlačítko **nové** a potom vyberte možnost konfigurace v **odkaz** pole. Na stránce **Místa určení elektronického výkaznictví** můžete zobrazit pouze konfigurace, pro které byly nakonfigurovány cíle.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Existuje nějaký způsob, jak určit, který účet úložiště Azure a úložiště objektů Blob Azure slouží?

Č. Je použit výchozí úložiště objektů Blob Azure, definované a používané pro systém správy dokumentů.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Jaký je účel určení souboru v nastavení cíle? Co toto nastavení dělá?

Cíl **Souboru** se používá k řízení dialogového okna. Pokud povolíte tento cíl nebo pokud je definován žádný cíl pro konfiguraci naleznete v tématu otevření nebo dialogové okno Uložit po vytvoření výstupního souboru.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Můžete dát příklad vzorce, který odkazuje na účet dodavatele, aby mu bylo možné odeslat e-mail?

Vzorec je specifický pro konfiguraci EV. Například pokud použijete konfiguraci „platební převod ISO 20022“, můžete pomocí konfigurace **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** nebo **model.Payments.Creditor.Identification.SourceID** získat účet přidruženého dodavatele.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Jedna z mých konfigurací formátu obsahuje více souborů, které jsou skupiny do jedné složky (například složka1 obsahuje soubor1, soubor2 a soubor3). Jak mohu nastavit cíle tak, aby se soubor složka1.zip nebyl nevytvořil, soubor1 byl odeslán prostřednictvím e-mailu, soubor2 byl odeslán na server SharePoint a soubor3 bylo možné otevřít ihned po spuštění konfigurace?

Nezbytným předpokladem je, že formát musí být k dispozici v konfiguracích ER. Pokud máte svůj formát, otevřete stránku **Místo určení elektronického výkaznictví** a vytvořte nový odkaz na tuto konfiguraci. Pak je třeba mít k dispozici čtyři cíle souboru, jeden pro každou součást výstupu. Vytvořte první cíl souboru, pojmenujte jej např. jako **Složka** a vyberte název souboru, který představuje složku ve vaší konfiguraci. Poté klepněte na tlačítko **Nastavení** a ujistěte se, že jsou zakázány všechny cíle. Pro tento cíl souboru se složka nevytvoří. Ve výchozím nastavení se soubory budou chovat stejným způsobem díly hierarchickým závislostem mezi soubory a nadřazenými složkami. Jinými slovy se nikam neodešlou. Chcete-li přepsat výchozí chování, je nutné vytvořit tři další cíle souborů, jeden pro každý soubor. V nastavení cíle pro každý ze souborů je nutné povolit cíl, na který má být soubor odeslán.

# <a name="see-also"></a>Viz také

[Přehled elektronického výkaznictví](general-electronic-reporting.md)





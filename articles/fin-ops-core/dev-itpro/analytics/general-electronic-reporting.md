---
title: Přehled elektronického výkaznictví
description: Toto téma poskytuje přehled o nástroji Elektronické výkaznictví. Popisuje klíčové koncepty, podporované scénáře a formáty, které jsou součástí řešení.
author: NickSelin
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 976a02f51e22c513b988e1ecfcb792d5f93a4b54
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986140"
---
# <a name="electronic-reporting-er-overview"></a>Přehled elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled o nástroji Elektronické výkaznictví (ER). Zahrnuje informace o klíčových konceptech, scénářích, které EV podporuje, a vyjmenovává formáty, které jsou navržené a vydané jako součást řešení.

Elektronické výkaznictví je konfigurovatelný nástroj, který pomáhá vytvářet a udržovat regulační elektronické výkazy a platby. Je založen na následujících třech konceptech:

- Konfigurace místo kódování:

    - Konfiguraci může provést podnikový uživatel a nevyžaduje vývojáře.
    - Datový model je definován v obchodních podmínkách.
    - K vytvoření všech součástí konfigurace elektronického výkaznictví se používají vizuální editory.
    - Jazyk, který se používá pro transformaci dat, se podobá jazyku, který používá Microsoft Excel.

- Jedna konfigurace pro více vydání Dynamics 365 Finance:

    - Spravujte jeden datový model ve vybrané doméně, který je definován v obchodních podmínkách.
    - Izolujte podrobnosti o vydání aplikace v mapováních datového modelu závislých na vydání.
    - Mějte jen jednu konfiguraci formátu pro více vydání aktuální verze na základě datového modelu.

- Snadný nebo automatický upgrade:

    - Správa verzí konfigurací elektronického výkaznictví je podporována.
    - Knihovnu majetku Microsoft Dynamics Lifecycle Services (LCS) lze použít jako úložiště konfigurací elektronického výkaznictví pro výměnu verzí.
    - Lokalizace, které jsou založeny na původních konfiguracích elektronického výkaznictví, lze zavést jako podřízené verze.
    - Konfigurační strom elektronického výkaznictví je poskytován jako nástroj, který pomáhá řídit závislosti verzí.
    - Rozdíly v lokalizaci nebo konfiguraci delty jsou zaznamenány, aby bylo možné provést automatický upgrade na novou verzi původní konfigurace elektronického výkaznictví.
    - Je snadné ručně vyřešit konflikty, které se objeví během automatického upgradu verzí lokalizace.

Elektronické výkaznictví umožňuje definovat struktury elektronického formátu a pak pomocí dat a algoritmů popsat, jak by tyto struktury měly být vyplněny. Pro transformaci dat můžete použít jazyk vzorců, který se podobá jazyku aplikace Excel. Aby bylo mapování databáze na formát lépe spravovatelné, opakovaně použitelné a nezávislé na změnách formátu, je zaveden koncept přechodného datového modelu. Tento koncept umožňuje skrýt detaily implementace z mapování formátu a umožňuje opětovné použití jediného datového modelu pro více mapování formátů.

Elektronického výkaznictví můžete použít ke konfiguraci formátů pro příchozí i odchozí elektronické dokumenty v souladu s právními požadavky různých zemí a oblastí. Elektronické výkaznictví umožňuje spravovat tyto formáty během jejich životního cyklu. Můžete například přijímat nové právní požadavky nebo generovat obchodní dokumenty v požadovaném formátu pro elektronickou výměnu informací s orgány veřejné správy, bankami a jinými stranami.

Modul EV je zaměřen na obchodní uživatele, nikoli na vývojáře. Vzhledem k tomu, že místo kódu konfigurujete formáty, jsou procesy vytváření a úpravy formátů pro elektronické dokumenty rychlejší a jednodušší.

Eelektronické výkaznictví v současné době podporuje formáty listů TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel a OPENXML.

## <a name="capabilities"></a>Schopnosti

Modul EV má následující možnosti:

- S jedním společným nástrojem pro elektronické výkaznictví v různých doménách nahrazuje 20 různých modulů pro provádění určitého typu elektronického výkaznictví pro Finance and Operations.
- Izoluje formát výkazu od aktuální implementace. Jinými slovy, formát je použitelný pro různé verze.
- Podporuje vytváření vlastního formátu, který je založen na původním formátu. Nabízí také funkce pro automatické upgradování vlastního formátu při změně původního formátu kvůli požadavkům na lokalizaci nebo přizpůsobení.
- Stane se primárním standardním nástrojem pro podporu lokalizace požadavků v elektronických sestavách – pro společnost Microsoft i pro její partnery.
- Podporuje možnost pro distribuci formátu pro partnery a zákazníky pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Klíčové koncepty

### <a name="main-data-flow"></a>Hlavní tok dat

[![Hlavní tok dat elektronického výkaznictví.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponenty

Elektronické výkaznictví podporuje následující typy komponent:

- Datový model
- Mapování modelu
- Formát
- Metadata

Další informace získáte v tématu [Komponenty elektronického výkaznictví](er-overview-components.md).


#### <a name="component-versioning"></a>Správa verzí komponent

Komponenty EV podporují správu verzí je podporována. Následující workflow je určen pro správu změn v komponentách ER:

1. Původně vytvořená verze je označena jako verze **Koncept**. Tato verze může být upravena a je k dispozici pro zkušební běh.
2. Verzi **Koncept** lze převést na verzi **Dokončeno**. Tuto verzi lze použít v místních procesů vykazování.
3. Verzi **Dokončeno** lze převést na verzi **Sdíleno**. Tato verze je publikována v LCS a lze ji použít v globálních procesech vykazování.
4. Verzi **Sdíleno** lze převést na verzi **Vyřazeno**. Tuto verzi můžete potom odstranit.

Verze ve stavu **Dokončeno** nebo **Sdíleno** jsou k dispozici pro další výměnu dat. U komponenty s těmito stavy můžete provádět následující akce:

- Komponentu lze serializovat do formátu XML a exportovat jako soubor ve formátu XML.
- Komponentu lze reserializovat ze souboru XML a importovat do aplikace jako novou verzi komponenty ER.

#### <a name="component-date-effectivity"></a>Datum platnosti komponenty

Verze komponent ER platí k určitému datu. Určením hodnoty data **Platné od** lze u komponenty ER určit datum, kdy komponenta začne platit v procesech vykazování. Datum relace aplikace slouží k definování, zda komponenta je platná pro spuštění. Poslední verze slouží k procesu vykazování při více než jedné platné verzi pro konkrétní datum.

#### <a name="component-access"></a>Přístup komponent

Přístup ke komponentám formátu EV závisí na nastavení ISO kódu země/oblasti. Pokud je toto nastavení pro vybranou verzi konfigurace formátu prázdné, k součásti formátu lze přistupovat z libovolné společnosti v době běhu. Pokud toto nastavení obsahuje ISO kódy země/oblasti, je komponenta formátu přístupná pouze ze společností, jejichž primární adresa je definována pro jednu komponentu formátu ISO kódu země/oblasti.

Různé verze součástí formátu data mají pravděpodobně různá nastavení ISO kódů země/oblasti.

#### <a name="configuration"></a><a name="Configuration"></a>Konfigurace

Konfigurace ER představuje obálku určité komponenty ER. Komponenta může být komponentou datového modelu nebo formátu. Konfigurace může obsahovat různé verze komponenty ER. Každá konfigurace je označena jako vlastněná určitou konfigurací poskytovatele. Verze **Návrh** komponent z konfigurace lze upravit po zvolení vlastníka konfigurace jako aktivního poskytovatele v nastavení EV v aplikaci.

Každá konfigurace modelu obsahuje komponentu datového modelu. Z konkrétní konfigurace datového modelu lze odvodit novou konfiguraci formátu. Ve stromu konfigurace se vytvořená konfigurace formátu zobrazí jako podřazená položka původní konfigurace datového modelu.

Vytvořená konfigurace formátu obsahuje komponentu formátu. Komponenta datového modelu původní konfigurace modelu bude automaticky vložena do komponenty formátu z podřazené konfigurace formátu jako výchozí datový zdroj.

Konfigurace EV je sdílená pro společnosti aplikace.

#### <a name="provider"></a><a name="Provider"></a>Zprostředkovatel

Poskytovatel EV je identifikací strany, která se používá k označení autora (vlastníka) každé konfigurace EV. EV umožňuje spravovat seznam zprostředkovatelů konfigurace. Konfigurace formátu vydané pro elektronické dokumenty jako součást řešení Finance and Operations jsou označeny jako vlastněné poskytovatelem konfigurace **Microsoft**.

Chcete-li zjistit, jak zaregistrovat nového poskytovatele ER, přehrajte si průvodce záznamem úloh **Elektronické výkaznictví – vytvoření poskytovatele konfigurace a jeho označení jako aktivního** (součást obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

#### <a name="repository"></a><a name="Repository"></a>Úložiště

Úložiště EV obsahuje konfigurace EV. Následující typy úložiště ER jsou aktuálně podporovány: 

- Sdílená knihovna LCS
- Projekt LCS
- Systém souborů
- RCS
- Prostředky aplikace Operations
- Globální úložiště

Úložiště **sdílené knihovny LCS** poskytuje přístup k seznamu konfigurací v rámci knihovny sdíleného majetku ve službě Lifecycle Services (LCS). Tento typ ER úložiště lze registrovat pouze pro zprostředkovatele společnosti Microsoft. Z knihovny sdíleného majetku LCS můžete importovat poslední verze konfigurace ER do aktuální instance.

Úložiště **projektu LCS** poskytuje přístup k seznamu konfigurací určitého projektu LCS (knihovny majetku projektu LCS), který byl vybrán při registraci úložiště. ER umožňuje odesílat sdílené konfigurace z aktuální instance aplikace do určitého úložiště **projektu LCS**. Můžete také importovat konfigurace z úložiště **projektu LCS** do aktuální instance aplikací Finance a Operace.

Úložiště **Systém souborů** poskytuje přístup k seznamu konfigurací, které jsou umístěny jako soubory XML ve specifické složce místního systému souborů počítače, kde je hostována služba AOS. Požadovaná složka je vybrána při fázi registrace úložiště. Můžete importovat konfigurace z úložiště **Systém souborů** do aktuální instance. 

Všimněte si, že tento typ úložiště je přístupný v následujících prostředích:

- Prostředí hostovaná v cloudu nasazená pro vývojářské účely (obsahující testovací modely přiložených sad)
- Místně nasazená prostředí (on-premises)

Další informace získáte v tématu [Import konfigurací elektronického výkaznictví](./electronic-reporting-import-ger-configurations.md).

Úložiště **RCS** poskytuje přístup k seznamu konfigurací určité instance [Služby konfigurace RCS](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration), která byla vybrána ve fázi registrace úložiště. Elektronické výkaznictví vám umožňuje importovat dokončené nebo sdílené konfigurace z vybrané instance RCS do aktuální instance, abyste je mohli použít v elektronickém výkaznictví.

Další informace získáte v tématu [Import konfigurací elektronického výkaznictví z RCS](./rcs-download-configurations.md).

**Globální úložiště** poskytuje přístup k seznamu konfigurací v globálním úložišti v [Konfigurační službě](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Tento typ ER úložiště lze registrovat pouze pro zprostředkovatele společnosti Microsoft. Z globálního úložiště můžete importovat poslední verze konfigurace ER do aktuální instance.

Další informace získáte v tématu [Import konfigurací elektronického výkaznictví z globálního úložiště konfigurační služby](./er-download-configurations-global-repo.md).

Úložiště typu **Provozní prostředky** poskytuje přístup k seznamu konfigurací, které společnost Microsoft jako poskytovatel konfigurace ER původně vydává v rámci řešení aplikace. Tyto konfigurace lze importovat do aktuální instance aplikace a používat pro elektronické sestavy nebo přehrání vzorovými průvodci záznamem úloh. Můžete je používat i pro další lokalizace a přizpůsobení. Všimněte si, že nejnovější verze poskytované konfiguracemi elektronického výkaznictví musí být importovány z knihovny sdíleného majetku LCS s použitím odpovídajícího ER úložiště.

Požadovaná úložiště **LCS projekt**, **Systém souborů** a **Regulatory Configuration Services (RCS)** lze registrovat pro jednotlivé poskytovatele konfigurace jednotlivě z aktuální instance. Každé úložiště může být určeno konkrétnímu poskytovateli konfigurace.

## <a name="supported-scenarios"></a>Podporované scénáře

### <a name="building-a-data-model"></a>Vytvoření datového modelu

EV nabízí návrháře modelu, kterého můžete použít pro vytvoření modelu dat pro určité obchodní domény. Všechny obchodních entity specifické pro domény a a vztahy mezi nimi mohou být přítomné v datovém modelu jako hierarchická struktura. 

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh datového modelu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="translating-data-model-content"></a>Překlad obsahu datového modelu

Obsah datového modelu (štítky a popisy) lze přeložit do jiných jazyků, které aplikace podporuje. Obsah datového modelu můžete chtít převést z následujících důvodů:

- V době návrhu – aby byl obsah lépe srozumitelný pro návrháře formátů mluvící cizím jazykem, kteří budou data modelu používat k mapování dat komponent formátu.
- V době spuštění – aby byl obsah lépe použitelný pro uživatele a zobrazoval výzvy, nápovědu týkající se parametrů a konfigurované zprávy ověření (chyby a upozornění) v preferovaném jazyce přihlášeného uživatele.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfigurace mapování datového modelu u odchozích dokumentů

EV poskytuje návrháře mapování modelu, který umožňuje uživatelům mapovat datové modely, které jsou navrženy pro konkrétní zdroje dat aplikace. Na základě mapování budou data importovány v operačním čase z vybraných datových zdrojů do datového modelu. Datový model se následně použije jako abstraktní zdroj dat formátů ER, které generují odchozí elektronické dokumenty. 

K seznámení se s tímto scénářem podrobněji si přehrajte průvodce úkoly **Elektronické vykazování – definování mapování modelů a výběr zdrojů dat** a **Elektronické vykazování – namapování datového modelu na vybrané zdroje dat** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfigurace mapování datového modelu u příchozích dokumentů

ER obsahuje modul návrháře mapování modelu, který umožňuje uživatelům mapovat navržené datové modely na konkrétní cíle. Je například možné mapovat datové modely na komponenty aktualizovatelných dat (tabulky, datové entity a zobrazení). Na základě mapování, se data se aktualizují v operačním čase pomocí dat z datového modelu. Jako abstraktní úložiště formátu ER se datový model vyplní daty importovanými z příchozího elektronického dokumentu. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Uložení navrženého modelu komponent jako konfigurace modelu

EV může ukládat navržený datový model společně s přiřazenými mapováními dat jako konfiguraci modelu aktuální instance. Následující obrázek znázorňuje příklad tohoto typu konfigurace datového modelu (konfigurace modelu dat pro doménu platby).

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – namapování datového modelu na vybrané zdroje dat** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Vytvoření formátu využívajícího datového modelu jako základu

ER podporuje modul návrháře formátů, pomocí kterého lze vytvořit formát elektronického dokumentu pro vybrané obchodní domény výběrem komponenty modelu jako základu. Stejný návrhář formátu EV nabízí schopnost mapování vytvořeného formátu pro výběr mapování modelu dat vybrané domény jako zdroje dat. 

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh formátu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Vytváření konfigurace pro generování elektronických dokumentů ve formátu listu OPENXML

Návrhář formátů ER slouží k vytvoření elektronických dokumentů ve formátu listu OPENXML. 

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – vytvoření konfigurace pro sestavy ve formátu OPENXML** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**). V rámci kroku průvodce záznamem úlohy pro import šablony použijte jako šablonu soubor aplikace Excel [Šablona sestavy platby (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Vytvoření konfigurace pro generování elektronických dokumentů ve formátu dokumentu aplikace Word

Návrhář formátu ER lze použít k vytvoření elektronického dokumentu ve formátu dokumentu aplikace Word. Následující obrázek znázorňuje příklad tohoto typu formátu. Tento formát znovu používá existující konfiguraci ER, která byla původně vytvořena ke generování výstupu sestavy ve formátu OPENXML.

Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu Microsoft WORD (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)). V rámci kroku průvodce záznamem úlohy pro import šablony použijte jako šablony pro formát ER následující soubory aplikace Word:

- [Šablona sestavy platby (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Vázaná šablona sestavy platby (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Vytvoření konfigurace pro import dat z příchozích elektronických dokumentů

Návrhář formátů ER lze použít k popisu elektronického dokumentu, který je součástí plánu pro import dat v textovém formátu nebo XML. Navržený formát slouží k analýze příchozího dokumentu. Návrhář mapování formátu ER lze použít k definování vazeb prvků navrženého formátu na model dat. 

Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy Elektronické vykazování – Vytvoření požadovaných konfigurací pro import dat z externího souboru (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)). Při přehrávání průvodce použijte tyto soubory:

- [Konfigurace modelu dat ER (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [Konfigurace formátu ER (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Ukázka vstupního dokumentu ve formátu XML (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Ukázka sešitu ke správě dat příchozího dokumentu (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Uložení navržené komponenty formátu do konfigurace formátu

EV umožňuje ukládat navržený formát společně s konfigurovanými mapováními dat jako konfiguraci formátu aktuální instance. Na předchozím obrázku je uveden příklad tohoto typu konfigurace formátu (**BACS (UK)**, který je podřízený konfiguraci **Platební model**). K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh formátu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Konfigurace aplikace Finance k použití interně vytvořeného formátu

Aplikaci lze použít ke spuštění za použití vytvořeného formátu pro generování elektronických sestav. Odkaz k vytvořené konfiguraci formátu by měl být definován ve specifických nastaveních určité domény. Například pokud chcete zahájit používání konfigurace formátu ER pro elektronické platby dodavatelů ve formátu BACS, na konfigurace formátu by se mělo odkazovat v určitých způsobech platby.

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – použití formátu ke generování elektronického dokumentu pro platby** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

## <a name="handling-er-components"></a>Zpracování komponent EV

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Publikování komponent EV v LCS pro jejich externímu nabízení (lokalizace)

Vlastník vytvořené součásti (modelu nebo formátu) je schopen používat EV pro publikování dokončené verze součásti do LCS. Je požadováno úložiště typu **projekt LCS** pro aktuálního zprostředkovatele konfigurací EV. Při změně stavu dokončené verze součásti z **DOKONČENO** na **SDÍLENO**, je tato verze publikována do LCS. Při publikování komponenty do LCS se vlastník této součásti stane poskytovatelem služby pro podporu této součásti. Například pokud součást formátu slouží ke generování zákonem požadovaných elektronických dokumentů (například podle scénáře lokalizace), předpokládá se, že tento formát splňuje změny právních předpisů, a že poskytovatel vydává nové verze pokaždé, když musí podporovat nové právní požadavky. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Odeslání konfigurace ER do služby Lifecycle Services**(součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Import součásti EV z LCS pro interní použití

EV umožňuje importovat komponenty EV z LCS do aktuální instance. Je požadováno úložiště typu **projekt LCS**. Při importu komponent ER ze služby LCS do aktuální instance se vlastník této instance stane spotřebitelem služby poskytované vlastníkem (autorem) importované komponenty. Například pokud tato komponenta formátu umožňuje generovat konkrétní elektronické dokumenty z aplikace v určitém formátu některé země/oblasti (scénář lokalizace), předpokládá se, že uživatel dané služby bude mít možnost získat jakoukoli aktualizaci pro tento formát, a udržován ho v souladu s právními požadavky. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Import konfigurace ER ze služby Lifecycle Services** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Vytvoření formátu výběrem jiného formátu jako základu (přizpůsobení)

EV umožňuje vytváření (odvození) nové komponenty z aktuální verze komponenty (základní), která byla importována z LCS. Například uživatel chce odvodit nový formát a implementovat tak některé zvláštní požadavky na elektronický dokument (například další pole nebo rozsáhlý popis) s cílem podpořit scénář přizpůsobení. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – aktualizace formátu osvojováním jeho nové základní verze** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Upgrade formátu výběrem nové verze základního formátu (přeskládání)

EV podporuje schopnost automaticky přijmout změny poslední verze základní komponenty v aktuální verzi konceptu odvozené komponenty. Pro tento proces je používáno označení *přeskladnění*. Například nové regulační změny zavedené v nejnovější verzi formátu importovaných z LCS mohou být automaticky sloučeny do vlastní přizpůsobené verze tohoto formátu elektronického dokumentu. Všechny změny, které nelze automaticky sloučit, jsou považovány za konflikty. Tyto konflikty jsou uvedeny a připraveny pro ruční vyřešení v nástroji Návrhář příslušné součásti. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – aktualizace formátu osvojováním jeho nové základní verze** (součástí obchodního procesu **7.5.5.3 Získání/vývoj součástí změněných IT služeb/řešení (10683)**).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Seznam konfigurací ER, které byly vydány v aplikaci Finance

Seznam konfigurací ER pro Finance se neustále aktualizuje. Otevřete [Globální úložiště](er-download-configurations-global-repo.md) ke kontrole seznamu konfigurací ER, které jsou aktuálně podporovány. Na kartě s náhledem **Podrobnosti o ukončení** můžete zkontrolovat informace o konfiguracích, které byly přerušeny nebo které již nejsou udržovány. 

![Obsah globálního úložiště na stránce úložiště konfigurace.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Další prostředky

- [Vytvoření konfigurace elektronického výkaznictví](electronic-reporting-configuration.md)
- [Správa životního cyklu konfigurace elektronického vykazování](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

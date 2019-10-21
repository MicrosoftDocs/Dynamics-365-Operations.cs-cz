---
title: Přehled elektronického výkaznictví
description: Toto téma poskytuje přehled o nástroji Elektronické výkaznictví (ER). Zahrnuje informace o klíčových konceptech, scénářích, které EV podporuje, a vyjmenovává formáty, které jsou navržené a vydané jako součást řešení.
author: NickSelin
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ce7b5418ab9e1a9abd6c3206c74c5a1cf739a3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181880"
---
# <a name="electronic-reporting-er-overview"></a>Přehled elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled o nástroji Elektronické výkaznictví (ER). Zahrnuje informace o klíčových konceptech, scénářích, které EV podporuje, a vyjmenovává formáty, které jsou navržené a vydané jako součást řešení.

ER je nástroj, který slouží ke konfiguraci formátů pro příchozí i odchozí elektronické dokumenty v souladu s právními požadavky různých zemí a oblastí. EV umožňuje spravovat tyto formáty během jejich životního cyklu. Můžete například přijímat nové právní požadavky nebo generovat obchodní dokumenty v požadovaném formátu pro elektronickou výměnu informací s orgány veřejné správy, bankami a jinými stranami.

Modul EV je zaměřen na obchodní uživatele, nikoli na vývojáře. Vzhledem k tomu, že místo kódu konfigurujete formáty, jsou procesy vytváření a úpravy formátů pro elektronické dokumenty rychlejší a jednodušší.

EV v současné době podporuje formáty listů TEXT, XML dokument Microsoft Word a OPENXML. Je k dispozici rozšíření zajišťující podporu dalších formátů.

## <a name="capabilities"></a>Schopnosti
Modul EV má následující možnosti:

- S jedním společným nástrojem pro elektronické výkaznictví v různých doménách nahrazuje 20 různých modulů pro provádění určitého typu elektronického výkaznictví pro Finance and Operations.
- Izoluje formát výkazu od aktuální implementace. Jinými slovy, formát je použitelný pro různé verze.
- Podporuje vytváření vlastního formátu, který je založen na původním formátu. Nabízí také funkce pro automatické upgradování vlastního formátu při změně původního formátu kvůli požadavkům na lokalizaci nebo přizpůsobení.
- Stane se primárním standardním nástrojem pro podporu lokalizace požadavků v elektronických sestavách – pro společnost Microsoft i pro její partnery.
- Podporuje možnost pro distribuci formátu pro partnery a zákazníky pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Klíčové koncepty
### <a name="components"></a>Komponenty

EV podporuje dva typy komponentů: **Datový model** a **Formát**.

#### <a name="data-model-components"></a>Komponenty datového modelu

Komponenta datového modelu je abstraktní reprezentací datové struktury. Slouží k popisu konkrétní oblasti obchodní domény s dostatečným množstvím podrobností, aby byly splněny požadavky na výkazy pro tuto doménu. Součást modelu dat se skládá z následujících částí:

- Datový model jako sada obchodních entit konkrétní domény a hierarchicky strukturované definice vztahů mezi nimi.
- Mapování modelu spojující vybrané zdroje dat aplikace s jednotlivými prvky datového modelu, který při spuštění určuje tok dat a pravidla naplnění obchodních dat do součásti modelu dat.

Kontejner (záznam) představuje obchodní entitu modelu dat. Vlastnosti obchodní entity jsou reprezentovány položkami dat (pole). Každá datová položka má jedinečný název, štítek, popis a hodnotu. Hodnota pro každou datovou položku může být určena tak, aby byla rozpoznána jako řetězec, celé číslo, reálné číslo, datum, výčet, logická hodnota a podobně. Kromě toho může být jiným záznamem nebo seznamem záznamů.

Jedna komponenta datového modelu může obsahovat několik hierarchií obchodních entit pro konkrétní doménu. Může také obsahovat mapování modelu, která podporují v operačním čase tok dat pro konkrétní sestavu. Hierarchie se mohou lišit podle jednotlivých záznamů, který byly vybrány jako kořen mapování modelu. Například datový model oblasti domény platby může podporovat následující mapování:

- Společnost \> Dodavatel \> Platební transakce domény závazků
- Zákazník \> Společnost \> Platební transakce pohledávek domény

Všimněte si, že obchodní entity (například společnost a platební transakce) jsou určeny jednou. Různá mapování je poté znovu využívají.

Mapování modelu, které podporuje odchozí elektronické dokumenty, má tyto funkce:

- Může využívat různé typy dat aplikace jako zdroje dat pro datový model. Například může používat tabulky, datové entity, metody nebo výčty.
- Podporuje vstupní parametry uživatele lze definovat jako datové zdroje modelu dat, když je při spuštění nutné zadat některá data.
- Podporuje transformaci dat aplikace do požadovaných skupin. Umožňuje také filtrování, řazení a sčítání dat a připojování logických vypočítaných polí určených pomocí vzorců (podobně jako v aplikaci Microsoft Excel) jako na následujícím obrázku. Další informace najdete v tématu [Návrhář receptur elektronického výkaznictví](general-electronic-reporting-formula-designer.md).

[![Návrhář receptur](./media/ER-overview-01.png)](./media/ER-overview-01.png)

Mapování modelu, které podporuje příchozí elektronické dokumenty, má tyto funkce:

- Může používat různé aktualizovatelné datové prvky jako cíle. K těmto datovým prvkům patří tabulky, datové entity a zobrazení. Data lze aktualizovat pomocí dat z příchozích elektronických dokumentů. V jednom mapování modelu lze použít více cílů.
- Podporuje vstupní parametry uživatele lze definovat jako datové zdroje modelu dat, když je při spuštění nutné zadat některá data.

Pro každou doménu je určena komponenta datového modelu, kterou je třeba používat jako jednotný zdroj dat pro vykazování, který izoluje výkaznictví od fyzické implementace datových zdrojů. Představuje obchodní koncepce a funkce konkrétní domény ve formě, která zvyšuje efektivitu úvodní struktury formátu výkaznictví a usnadňuje jeho další údržbu.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Komponenty formátu pro odchozí elektronické dokumenty

Komponenta formátu je schématem výstupu vykazování, který je generován při spuštění. Schéma se skládá z následujících prvků:

- Formát, který definuje strukturu a obsah odchozího elektronického dokumentu (generuje se při spuštění).
- Zdroje dat jako sada vstupních parametrů uživatele a datového modelu konkrétní domény s mapováním vybraného modelu.
- Formát mapování jako sada vazeb datových zdrojů formátu s jednotlivými prvky formátu, které určují při spuštění tok dat a pravidla generování formátu výstupu.
- Ověření formátu jako sada konfigurovatelných pravidel, která řídí vytváření sestav v době spuštění v závislosti na aktuálním kontextu. Může napříkad existovat pravidlo, které zastaví generování výstupu plateb dodavatele dodavatele a vytvoří výjimku, když chybí konkrétní atributy dodavatele, například číslo bankovního účtu.

Komponenta formátu podporuje následující funkce:

- Vytvoření výstupní sestavy jako samostatných souborů v různých formátech, například text, XML, dokument aplikace Microsoft Word nebo sešit.
- Vytvoření více souborů samostatně a jejich uložení do souborů ZIP.

Komponenta formátu umožňuje připojit určité soubory, které lze použít ve výstupním vykazování:

- Listy sešitů Excel obsahující listy, které lze použít jako šablonu pro výstup ve formátu listu OPENXML
- Soubory aplikace Word obsahující dokument, který lze použít jako šablonu pro výstup ve formátu dokumentu aplikace Microsoft Word
- Ostatní soubory, které mohou být zahrnuty do výstupního formátu jako předdefinovaných souborů

Následující obrázek znázorňuje tok dat u těchto formátů.

[![Tok dat pro odchozí komponenty formátu](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Chcete-li spustit jednu konfiguraci formátu ER a vygenerovat odchozí elektronický dokument, je nutné určit mapování konfigurace formátu.

#### <a name="format-components-for-incoming-electronic-documents"></a>Komponenty formátu pro příchozí elektronické dokumenty
Komponenta formátu je schématem příchozího dokumentu, které se importuje při spuštění. Schéma se skládá z následujících prvků:

- Formát, který definuje strukturu a obsah příchozího elektronického dokumentu obsahujícího data, která se importují při spuštění. Komponenta formátu, která slouží k analýze příchozích dokumentů v různých formátech (například text nebo XML).
- Mapování formátu, které spojuje jednotlivé prvky formátu s prvky datového modelu konkrétní domény. Při spuštění prvky v datovém modelu určují tok dat a pravidla pro import dat z příchozího dokumentu a následně ukládají data do datového modelu.
- Ověření formátu jako sada konfigurovatelných pravidel, která řídí import dat v době spuštění v závislosti na aktuálním kontextu. Může napříkad existovat pravidlo, které zastaví import dat bankovního výpisu s platbami dodavatele a vytvoří výjimku, když chybí konkrétní atributy dodavatele, například jeho identifikační číslo.

Následující obrázek znázorňuje tok dat u těchto formátů.

[![Tok dat pro příchozí komponenty formátu](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Chcete-li spustit jednu konfiguraci formátu ER při importu dat z příchozího elektronického dokumentu, je nutné určit požadované mapování konfigurace formátu a bod integrace mapování modelu. Pro různé typy příchozích dokumentů můžete použít stejné mapování modelu a cíle společně s různými formáty.

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

#### <a name="configuration"></a>Konfigurace

Konfigurace ER představuje obálku určité komponenty ER. Komponenta může být komponentou datového modelu nebo formátu. Konfigurace může obsahovat různé verze komponenty ER. Každá konfigurace je označena jako vlastněná určitou konfigurací poskytovatele. Verze **Návrh** komponent z konfigurace lze upravit po zvolení vlastníka konfigurace jako aktivního poskytovatele v nastavení EV v aplikaci.

Každá konfigurace modelu obsahuje komponentu datového modelu. Z konkrétní konfigurace datového modelu lze odvodit novou konfiguraci formátu. Ve stromu konfigurace se vytvořená konfigurace formátu zobrazí jako podřazená položka původní konfigurace datového modelu.

Vytvořená konfigurace formátu obsahuje komponentu formátu. Komponenta datového modelu původní konfigurace modelu bude automaticky vložena do komponenty formátu z podřazené konfigurace formátu jako výchozí datový zdroj.

Konfigurace EV je sdílená pro společnosti aplikace.

#### <a name="provider"></a>Zprostředkovatel

Poskytovatel EV je identifikací strany, která se používá k označení autora (vlastníka) každé konfigurace EV. EV umožňuje spravovat seznam zprostředkovatelů konfigurace. Konfigurace formátu vydané pro elektronické dokumenty jako součást řešení Finance and Operations jsou označeny jako vlastněné poskytovatelem konfigurace **Microsoft**.

Chcete-li zjistit, jak zaregistrovat nového poskytovatele ER, přehrajte si průvodce záznamem úloh **Elektronické výkaznictví – vytvoření poskytovatele konfigurace a jeho označení jako aktivního** (součást obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

#### <a name="repository"></a>Úložiště

Úložiště EV obsahuje konfigurace EV. Následující typy úložiště ER jsou aktuálně podporovány: 

- Sdílená knihovna LCS
- Projekt LCS
- Systém souborů
- Regulatory Configuration Services (RCS)
- Prostředky aplikace Operations


Úložiště **sdílené knihovny LCS** poskytuje přístup k seznamu konfigurací v rámci knihovny sdíleného majetku ve službě Lifecycle Services (LCS). Tento typ ER úložiště lze registrovat pouze pro zprostředkovatele společnosti Microsoft. Z knihovny sdíleného majetku LCS můžete importovat poslední verze konfigurace ER do aktuální instance.

Úložiště **projektu LCS** poskytuje přístup k seznamu konfigurací určitého projektu LCS (knihovny majetku projektu LCS), který byl vybrán ve fázi registrace úložiště. ER umožňuje odesílat sdílené konfigurace z aktuální instance aplikace do určitého úložiště **projektu LCS**. Můžete také importovat konfigurace z úložiště **projektu LCS** do aktuální instance aplikace Finance and Operations.

Úložiště **Systém souborů** poskytuje přístup k seznamu konfigurací, které jsou umístěny jako soubory XML ve specifické složce místního systému souborů počítače, kde je hostována služba AOS. Požadovaná složka je vybrána při fázi registrace úložiště. Můžete importovat konfigurace z úložiště **Systém souborů** do aktuální instance. 

Všimněte si, že tento typ úložiště je přístupný v následujících prostředích:

- Prostředí hostovaná v cloudu nasazená pro vývojářské účely (obsahující testovací modely přiložených sad)
- Místně nasazená prostředí (on-premises)

Další informace získáte v tématu [Import konfigurací elektronického výkaznictví](./electronic-reporting-import-ger-configurations.md).

Úložiště **Instance RCS** poskytuje přístup k seznamu konfigurací určité instance RCS, která byla vybrána ve fázi registrace úložiště. Elektronické výkaznictví vám umožňuje importovat dokončené nebo sdílené konfigurace z vybrané instance RCS do aktuální instance, abyste je mohli použít v elektronickém výkaznictví.

Další informace získáte v tématu [Import konfigurací elektronického výkaznictví ze služby RCS (Regulatory Configuration Services)](./rcs-download-configurations.md).

Úložiště typu **Provozní prostředky** poskytuje přístup k seznamu konfigurací, které společnost Microsoft jako poskytovatel konfigurace ER původně vydává v rámci řešení aplikace. Tyto konfigurace lze importovat do aktuální instance aplikace a používat pro elektronické sestavy nebo přehrání vzorovými průvodci záznamem úloh. Můžete je používat i pro další lokalizace a přizpůsobení. Všimněte si, že nejnovější verze poskytované konfiguracemi elektronického výkaznictví musí být importovány z knihovny sdíleného majetku LCS s použitím odpovídajícího ER úložiště.

Požadovaná úložiště **LCS projekt**, **Systém souborů** a **Regulatory Configuration Services (RCS)** lze registrovat pro jednotlivé poskytovatele konfigurace jednotlivě z aktuální instance. Každé úložiště může být určeno konkrétnímu poskytovateli konfigurace.

## <a name="supported-scenarios"></a>Podporované scénáře
### <a name="building-a-data-model"></a>Vytvoření datového modelu

EV nabízí návrháře modelu, kterého můžete použít pro vytvoření modelu dat pro určité obchodní domény. Všechny obchodních entity specifické pro domény a a vztahy mezi nimi mohou být přítomné v datovém modelu jako hierarchická struktura. Následující obrázek znázorňuje příklad tohoto typu datového modelu (model dat pro doménu platby).

[![Datový model domény platby](./media/ER-overview-04.png)](./media/ER-overview-04.png)

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh datového modelu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="translating-data-model-content"></a>Překlad obsahu datového modelu

Obsah datového modelu (štítky a popisy) lze přeložit do jiných jazyků, které aplikace podporuje. Obsah datového modelu můžete chtít převést z následujících důvodů:

- V době návrhu – aby byl obsah lépe srozumitelný pro návrháře formátů mluvící cizím jazykem, kteří budou data modelu používat k mapování dat komponent formátu.
- V době spuštění – aby byl obsah lépe použitelný pro uživatele a zobrazoval výzvy, nápovědu týkající se parametrů a konfigurované zprávy ověření (chyby a upozornění) v preferovaném jazyce přihlášeného uživatele.

Následující obrázek zobrazuje příklad toho, jak lze obsah datového modelu přeložit z angličtiny do japonštiny.

[![Obsah datového modelu v angličtině](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Obsah datového modelu přeložený do japonštiny](./media/ER-overview-06.png)](./media/ER-overview-06.png)

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfigurace mapování datového modelu u odchozích dokumentů

EV poskytuje návrháře mapování modelu, který umožňuje uživatelům mapovat datové modely, které jsou navrženy pro konkrétní zdroje dat aplikace. Na základě mapování budou data importovány v operačním čase z vybraných datových zdrojů do datového modelu. Datový model se následně použije jako abstraktní zdroj dat formátů ER, které generují odchozí elektronické dokumenty. Následující obrázek popisuje příklad tohoto typu mapování modelu dat (mapování modelu **platebního převodu SEPA** datového modelu platební domény).

[![Příklad mapování modelu dat](./media/ER-overview-07.png)](./media/ER-overview-07.png)

K seznámení se s tímto scénářem podrobněji si přehrajte průvodce úkoly **Elektronické vykazování – definování mapování modelů a výběr zdrojů dat** a **Elektronické vykazování – namapování datového modelu na vybrané zdroje dat** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfigurace mapování datového modelu u příchozích dokumentů
ER obsahuje modul návrháře mapování modelu, který umožňuje uživatelům mapovat navržené datové modely na konkrétní cíle. Je například možné mapovat datové modely na komponenty aktualizovatelných dat (tabulky, datové entity a zobrazení). Na základě mapování, se data se aktualizují v operačním čase pomocí dat z datového modelu. Jako abstraktní úložiště formátu ER se datový model vyplní daty importovanými z příchozího elektronického dokumentu. Následující obrázek znázorňuje příklad tohoto typu mapování datového modelu. V tomto příkladu se mapování modelu **Import mapování pro NETS** použije k podpoře importu bankovních výpisů ve formátu NETS pro Norsko.

[![Příklad datového modelu importu pro NETS](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Uložení navrženého modelu komponent jako konfigurace modelu

EV může ukládat navržený datový model společně s přiřazenými mapováními dat jako konfiguraci modelu aktuální instance. Následující obrázek znázorňuje příklad tohoto typu konfigurace datového modelu (konfigurace modelu dat pro doménu platby).

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – namapování datového modelu na vybrané zdroje dat** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Vytvoření formátu využívajícího datového modelu jako základu

ER podporuje modul návrháře formátů, pomocí kterého lze vytvořit formát elektronického dokumentu pro vybrané obchodní domény výběrem komponenty modelu jako základu. Stejný návrhář formátu EV nabízí schopnost mapování vytvořeného formátu pro výběr mapování modelu dat vybrané domény jako zdroje dat. Následující obrázek znázorňuje příklad tohoto typu formátu (konfigurace formátu, která podporuje formát platby **BACS** pro Spojené království).

[![Příklad formátu využívajícího datový model jako základ](./media/ER-overview-09.png)](./media/ER-overview-09.png)

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh formátu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Vytváření konfigurace pro generování elektronických dokumentů ve formátu listu OPENXML

Návrhář formátů ER slouží k vytvoření elektronických dokumentů ve formátu listu OPENXML. Následující obrázek znázorňuje příklad tohoto typu formátu (konfigurace formátu pro vygenerování listu OPENXML s podrobnostmi o vybraném deníku plateb).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – vytvoření konfigurace pro sestavy ve formátu OPENXML** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**). V rámci kroku průvodce záznamem úlohy pro import šablony použijte jako šablonu soubor aplikace Excel [Šablona sestavy platby (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Vytvoření konfigurace pro generování elektronických dokumentů ve formátu dokumentu aplikace Word
Návrhář formátu ER lze použít k vytvoření elektronického dokumentu ve formátu dokumentu aplikace Word. Následující obrázek znázorňuje příklad tohoto typu formátu. Tento formát znovu používá existující konfiguraci ER, která byla původně vytvořena ke generování výstupu sestavy ve formátu OPENXML.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu Microsoft WORD (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)). V rámci kroku průvodce záznamem úlohy pro import šablony použijte jako šablony pro formát ER následující soubory aplikace Word:

- [Šablona sestavy platby (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Vázaná šablona sestavy platby (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Vytvoření konfigurace pro import dat z příchozích elektronických dokumentů
Návrhář formátů ER lze použít k popisu elektronického dokumentu, který je součástí plánu pro import dat v textovém formátu nebo XML. Navržený formát slouží k analýze příchozího dokumentu. Návrhář mapování formátu ER lze použít k definování vazeb prvků navrženého formátu na model dat. Následující obrázky znázorňují příklad tohoto typu formátu a mapování formátu. V tomto příkladu jsou importovány bankovních výpisy NETS, které zahrnují informace o platbách dodavatelů v textovém formátu.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy Elektronické vykazování – Vytvoření požadovaných konfigurací pro import dat z externího souboru (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)). Při přehrávání průvodce použijte tyto soubory:

- [Konfigurace modelu dat ER (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Konfigurace formátu ER (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Ukázka vstupního dokumentu ve formátu XML (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Ukázka sešitu ke správě dat příchozího dokumentu (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Uložení navržené komponenty formátu do konfigurace formátu

EV umožňuje ukládat navržený formát společně s konfigurovanými mapováními dat jako konfiguraci formátu aktuální instance. Na předchozím obrázku je uveden příklad tohoto typu konfigurace formátu (**BACS (UK)**, který je podřízený konfiguraci **Platební model**). K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh formátu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Konfigurace aplikace Finance k použití interně vytvořeného formátu

Aplikaci lze použít ke spuštění za použití vytvořeného formátu pro generování elektronických sestav. Odkaz k vytvořené konfiguraci formátu by měl být definován ve specifických nastaveních určité domény. Například pokud chcete zahájit používání konfigurace formátu EV pro elektronické platby dodavatelů ve formátu BACS, na konfigurace formátu by se mělo odkazovat v určitém způsoby platby tak, jak je znázorněno na následujícím obrázku:

[![Konfigurace formátu BACS (UK)](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Odkazování na formát BACS (UK) v metodě platby](./media/ER-overview-15.png)](./media/ER-overview-15.png)

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

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-application"></a>Seznam konfigurací ER, které jsou k dispozici v řešení Finance

| Konfigurace modelu dat pro specifickou doménu: název | Doména                | Konfigurace formátu závislá na modelu dat: název | Popis                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Model souboru auditu                                 | Finanční audit       |                                                   |                                                                    |
|                                                  |                       | Soubor auditu (NL)                                   | Formát souboru auditu pro Nizozemsko                                  |
| Model BAS                                        | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | Formát BAS pro Austrálii                                           |
| Model schématu pro obor stavebnictví               | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Měsíční vratky CIS (UK)                           | Formát měsíční vratky CIS pro Spojené království                   |
| Model upomínky                          | Elektronická fakturace  |                                                   |                                                                    |
|                                                  |                       | Upomínka OIOUBL (DK)                     | Formát upomínky OIOUBL pro Dánsko                        |
| Model účetní elektronické hlavní knihy (MX)          | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Pomocná hlavní kniha XML (MX)                         | Formát sestavy transakcí v pomocné hlavní knize pro každý účet pro Mexiko |
|                                                  |                       | Účtová osnova XML (MX)                         | Formát sestavy účtové osnovy pro Mexiko                          |
|                                                  |                       | Deníky XML (MX)                                 | Formát sestavy deníku transakcí pro Mexiko                      |
|                                                  |                       | Předvaha XML (MX)                            | Formát sestavy předvahy pro Mexiko                             |
| Model Elster                                     | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Formát Elster pro Německo                                          |
| Model souhrnného hlášení – EU                              | Sestava obchodu       |                                                   |                                                                    |
|                                                  |                       | Souhrnné hlášení – EU (DE)                                | Formát souhrnného hlášení (EU) pro Německo                               |
|                                                  |                       | Souhrnné hlášení – EU (DK)                                | Formát souhrnného hlášení (EU) pro Dánsko                               |
|                                                  |                       | Souhrnné hlášení – EU (FR)                                | Formát souhrnného hlášení (EU) pro Francii                                |
|                                                  |                       | Souhrnné hlášení – EU (NL)                                | Formát souhrnného hlášení (EU) pro Nizozemsko                           |
|                                                  |                       | Souhrnné hlášení TXT – EU (UK)                            | Formát TXT souhrnného hlášení (EU) pro Spojené království                    |
|                                                  |                       | Souhrnné hlášení XML – EU (UK)                            | Formát XML souhrnného hlášení (EU) pro Spojené království                    |
|                                                  |                       | Souhrnné hlášení – EU podle sloupců                   | Souhrnné hlášení – EU podle sloupců                                    |
|                                                  |                       | Souhrnné hlášení – EU podle řádků                      | Souhrnné hlášení – EU podle řádků                                       |
| Účtovací model FEC (FR)                        | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Účetní data XML – FEC (FR)                      | Formát XML pro export účetních dat FEC pro Francii                   |
| Soubor auditu pro Německo                                | Finanční audit       |                                                   |                                                                    |
|                                                  |                       | Výstupní soubor auditu pro Německo                          | Výstupní soubor auditu pro Německo a Rakousko                          |
| Modul Intrastat                                  | Sestava obchodu       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Formát Intrastat pro Německo                                       |
|                                                  |                       | Intrastat (DK)                                    | Formát Intrastat pro Dánsko                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Formát Intrastat INTRACOM pro Francii                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Formát Intrastat SAISUNIC pro Francii                               |
|                                                  |                       | Intrastat (NL)                                    | Formát Intrastat pro Nizozemsko                               |
|                                                  |                       | Intrastat (UK)                                    | Formát Intrastat pro Spojené království                            |
|                                                  |                       | Sestava Intrastat                                  | Kontrolní sestava Intrastat aplikace Excel                                     |
| Model faktury odběratele                           | Elektronická fakturace  |                                                   |                                                                    |
|                                                  |                       | Dobropis k projektu OIOUBL (DK)                   | Formát dobropisu k projektu OIOUBL pro Dánsko                      |
|                                                  |                       | Faktura k projektu OIOUBL (DK)                       | Formát faktury k projektu OIOUBL pro Dánsko                          |
|                                                  |                       | Prodejní dobropis OIOUBL (DK)                     | Formát prodejního dobropisu OIOUBL pro Dánsko                        |
|                                                  |                       | Prodejní faktura OIOUBL (DK)                         | Formát prodejní faktury OIOUBL pro Dánsko                            |
| Model deklarace OB                             | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Prohlášení OB (NL)                               | Formát prohlášení OB pro Nizozemsko                          |
| Model platby                                    | Platby              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Formát platby Betalingsservice pro Dánsko                        |
|                                                  |                       | Úhrada směnky (FR)                  | Formát úhrady směnky pro Francii                      |
|                                                  |                       | BTL91 (NL)                                        | Formát platby dodavatele BTL91 pro Nizozemsko                    |
|                                                  |                       | CFONB Prelevements (FR)                           | Formát platby přímého debetu CFONB pro Francii                       |
|                                                  |                       | CFONB Virements (FR)                              | Formát platby domácího dodavatele CFONB pro Francii                    |
|                                                  |                       | Dodavatel Nordea (DK)                                | Formát platby korporačního dodavatele Nordea Netbank pro Dánsko         |
|                                                  |                       | Přímé platební služby ANZ (AU)                    | Formát pro přímé platební služby ANZ pro Austrálii                 |
|                                                  |                       | Přímé platební služby CBA (AU)                    | Formát pro přímé platební služby CBA pro Austrálii                 |
|                                                  |                       | Přímé platební služby NAB (AU)                    | Formát pro přímé platební služby NAB pro Austrálii                 |
|                                                  |                       | Přímé platební služby STG (AU)                    | Formát pro přímé platební služby STG pro Austrálii                 |
|                                                  |                       | Systém pro přímý vstup WBC (AU)                      | Formát systému pro přímý vstup WBC pro Austrálii                   |
|                                                  |                       | DirectLink (NZ)                                   | Formát pro DirectLink pro Nový Zéland                              |
|                                                  |                       | Soubor platby JBA (JP)                             | Formát platby JBA pro Japonsko                                       |
|                                                  |                       | Peněžní převod ISO20022                          | Formát pro peněžní převod SEPA pro Evropu                             |
|                                                  |                       | Peněžní převod ISO20022 (FR)                     | Formát pro peněžní převod SEPA pro Francii                             |
|                                                  |                       | Peněžní převod ISO20022 (DE)                     | Formát pro peněžní převod SEPA pro Německo                            |
|                                                  |                       | Peněžní převod ISO20022 (NL)                     | Formát pro peněžní převod SEPA pro Nizozemsko                    |
|                                                  |                       | Inkaso ISO20022                             | Formát inkasa SEPA pro Evropu                                |
|                                                  |                       | Inkaso ISO20022 (FR)                        | Formát inkasa SEPA pro Francii                                |
|                                                  |                       | Inkaso ISO20022 (DE)                        | Formát inkasa SEPA pro Německo                               |
|                                                  |                       | Inkaso ISO20022 (NL)                        | Formát inkasa SEPA pro Nizozemsko                       |
|                                                  |                       | BACS (UK)                                         | Formát pro platbu dodavatele BACS pro Spojené království                  |
| Stornovací poplatek                                   | Vykázání daně         |                                                   |                                                                    |
|                                                  |                       | Seznam stornovacích poplatků prodeje                         | Formát seznamu stornovacích poplatků prodeje                                   |
| Model integrace XBRL pro Nizozemsko                     | Vykazování v kódu XBRL        |                                                   |                                                                    |
|                                                  |                       | XBRL Semansys (NL)                                | Formát exportu Semansys XBRL pro Nizozemsko                    |
| Model GAF (MY)                                   | Finanční audit       |                                                   |                                                                    |
|                                                  |                       | Soubor GAF (MY)                                     | Formát GAF pro Malajsii                                         |
| Sestava sledování splatnosti dodavatele (CN)                         | Analýza dat dodavatele |                                                   |                                                                    |
|                                                  |                       | Formát sestavy sledování splatnosti dodavatele (CN)                   | Formát sestavy sledování splatnosti dodavatele pro Čínu                               |
| Model prohlášení k faktuře dodavatele                 | Analýza dat dodavatele |                                                   |                                                                    |
|                                                  |                       | Prohlášení k faktuře dodavatele (IS)                   | Formát prohlášení k faktuře dodavatele pro Island                      |
|                                                  |                       | Sestava prohlášení k faktuře dodavatele (IS)            | Sestava prohlášení k faktuře dodavatele pro Island                      |

## <a name="additional-resources"></a>Další zdroje

- [Požadavky na lokalizaci – vytvoření konfigurace elektronického výkaznictví](electronic-reporting-configuration.md)
- [Správa životního cyklu konfigurace elektronického vykazování](general-electronic-reporting-manage-configuration-lifecycle.md)

---
title: "Přehled elektronického výkaznictví"
description: "Tento článek podává přehled o nástroji Elektronické výkaznictví (ER). Zahrnuje informace o klíčových konceptech, scénářích, které EV podporuje, a vyjmenovává formáty, které jsou navržené a vydané jako součást řešení."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: abe9212372fb7429d68c1fb6b32ec1d15c20a6d7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-reporting-overview"></a>Přehled elektronického výkaznictví

[!include[banner](../includes/banner.md)]


Tento článek podává přehled o nástroji Elektronické výkaznictví (ER). Zahrnuje informace o klíčových konceptech, scénářích, které EV podporuje, a vyjmenovává formáty, které jsou navržené a vydané jako součást řešení.

Elektronické výkaznictví je nástroj, který slouží ke konfiguraci formátů pro elektronické dokumenty v souladu s právními požadavky různých zemí a oblastí. EV umožňuje spravovat tyto formáty během jejich životního cyklu. Například můžete přijímat nové právní požadavky nebo generovat obchodní dokumenty v požadovaném formátu pro elektronickou výměnu informací s orgány veřejné správy, bankami a jinými stranami. Modul EV je zaměřen na obchodní uživatele, nikoli na vývojáře. Vzhledem k tomu, že konfigurujete formáty, ne kód, jsou procesy vytváření a úpravy formátů pro elektronické dokumenty rychlejší a jednodušší. EV v současné době podporuje formáty listů TEXT, XML a OPENXML. Nicméně rozhraní rozšíření poskytuje podporu pro více formátů.

## <a name="capabilities"></a>Schopnosti
Modul EV má následující možnosti:

-   S jedním společným nástrojem pro pro elektronické vykazování v různých doménách nahrazuje 20 různých modulů pro provádění určitého elektronického vykazování Microsoft Dynamics 365 for Operations.
-   Izoluje formát výkazu od aktuální implementace Dynamics 365 for Operations. (Jinými slovy, formát je použitelný pro různé verze aplikace Microsoft Dynamics365 for Operations.)
-   Podporuje vytváření vlastního formátu, který je založen na původním formátu. Nabízí funkce pro automatické upgradování vlastního formát při změně původního formátu v případě, že se zavádějí požadavky na lokalizaci/úpravy.
-   Stane se primárním standardním nástrojem pro podporu lokalizace požadavků v elektronických sestavách – pro společnost Microsoft i pro její partnery.
-   Podporuje možnost pro distribuci formátu pro partnery a zákazníky pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Koncepty
### <a name="components"></a>Součásti

EV podporuje dva typy komponentů: **Datový model** a **Formát**.

#### <a name="data-model-components"></a>Komponenty datového modelu

Komponenta datového modelu je abstraktní znázornění struktury dat pro použití k popisu určité oblasti obchodní domény s dostatečnými podrobnostmi, aby splňovaly požadavky na výkazy v dané doméně. Součást modelu dat se skládá z následujících částí:

-   Datový model jako sadu obchodních entit specifických pro domény a hierarchicky strukturované definice vztahů mezi nimi.
-   Mapování modelu spojující vybrané zdroje dat aplikace Dynamics 365 for Operations s jednotlivými prvky datového modelu, který při spuštění určuje tok dat a pravidla naplnění obchodních dat do součásti modelu dat.

Kontejner (záznam) představuje obchodní entitu modelu dat. Vlastnosti obchodní entity jsou reprezentovány položkami dat (pole). Každá datová položka má jedinečný název, štítek, popis a hodnotu. Hodnota pro každou datovou položku může být navržena tak, aby byla rozpoznána jako řetězec, celé číslo, skutečná hodnota, datum, typ výčtu, Boolean apod. Kromě toho může být jiným záznamem nebo seznamem záznamů. Komponenta jednotlivého datového modelu může obsahovat několik hierarchií domény specifických obchodních entit, a také mapování modelu k podpoře konkrétní sestavy konkrétního toku dat při spuštění. Hierarchie se mohou lišit podle jednotlivých záznamů, který byly vybrány jako kořen mapování modelu. Například datový model oblasti domény platby může podporovat následující mapování:

-   Společnost -&gt; Dodavatel -&gt; Platební transakce domény závazků
-   Zákazník -&gt; Společnost -&gt; Platební transakce pohledávek domény

Všimněte si, že obchodní entity (například společnost a platební transakce) jsou určeny jednou. Různá mapování je poté znovu využívají. Mapování modelu má následující možnosti:

-   Může využívat různé typy dat aplikace Dynamics 365 for Operations jako zdroje dat pro datový model. Například může používat tabulky, datové entity, metody nebo výčty.
-   Podporuje vstupní parametry uživatele lze definovat jako datové zdroje modelu dat, když je při spuštění nutné zadat některá data.
-   Podporuje transformaci dat aplikace Dynamics 365 for Operations do požadovaných skupin, filtrování, řazení a součtu dat, stejně jako připojení pomocí logicky vypočítaných polí, které jsou navrženy za použití vzorců podobných jako v aplikaci Microsoft Excel (další informace naleznete v tématu [Návrhář vzorců v elektronickém vykazování](general-electronic-reporting-formula-designer.md)).

[![Editor vzorců jako v Excelu](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Komponent data modelu je určen pro každou obchodní doménu, kterou chcete použít jako sjednocení datového zdroje pro vykazování, které odděluje vykazování od fyzické implementace datových zdrojů aplikace Dynamics 365 for Operations, představuje konkrétní obchodní koncept a funkce domén v podobě, které činí počáteční návrhy sestav formátů a další údržbu efektivnější.

#### <a name="format-components"></a>Komponenty formátu

Komponenta formátu je schématem výstupu vykazování, který je generován při spuštění. Schéma se skládá z následujících prvků:

-   Formát, který definuje struktury a obsah dokumentu elektronického vykazování generovaného při spuštění
-   Zdroje dat jako sada vstupních parametrů uživatele a datového modelu specifického pro doménu s mapováním vybraného modelu
-   Formát mapování jako sada vazeb datových zdrojů formátu s jednotlivými prvky formátu, které určují při spuštění tok dat a pravidla generování formátu výstupu
-   Ověřování formátu jako sada konfigurovatelných pravidel, které řídí generování sestavy v době běhu v závislosti na kontextu daného běhu (například pravidlo, které zastaví výstupní generování plateb dodavatele a vyvolá výjimku, pokud chybí určité atributy vybraného dodavatele, jako je například bankovní číslo účtu).

Komponenta formátu podporuje následující funkce:

-   Vytváření výstupní sestavy jako samostatných souborů v různých formátech: text, XML nebo list
-   Vytvoření více souborů samostatně, ale také zapouzdření těchto souborů do souborů ZIP

Komponenta formátu umožňuje připojit určité soubory, které lze použít ve výstupním vykazování:

-   Listy sešitů Excel obsahující listy, které lze použít jako šablonu pro výstup ve formátu listu OPENXML
-   Ostatní soubory, které mohou být zahrnuty do výstupního formátu jako předdefinovaných souborů

#### <a name="component-versioning"></a>Správa verzí komponent

Komponenty EV podporují správu verzí je podporována. Následující workflow je k dispozici pro správu změn v komponentách EV:

-   Verze, která je původně vytvořena, je označena jako verze **NÁVRH**. Tato verze může být upravena a je k dispozici pro zkušební běh.
-   Verzi **NÁVRH** lze převést na verzi **DOKONČENO**. Tuto verzi lze použít v místních procesů vykazování.
-   **DOKONČENOU** verzi lze převést na **SDÍLENOU**. Tato verze je publikována v LCS a lze ji použít v globálních procesech vykazování.
-   Verzi **SDÍLENO** lze převést na verzi **UKONČENO**. Tuto verzi můžete potom odstranit.

Verze ve stavu ** DOKONČENO** nebo **SDÍLENO** jsou k dispozici jsou pro jinou výměnu dat. U komponenty s těmito stavy můžete provádět následující akce:

-   Lze je serializovat do formátu XML a exportovat z aplikace Dynamics 365 for Operations jako soubor ve formátu XML.
-   Lze je reserializovat ze souboru XML a importovat do aplikace Dynamics 365 for Operations jako novou verzi součásti EV.

#### <a name="component-date-effectivity"></a>Datum platnosti komponenty

Verze komponent EV jsou časově platná. Datum **Platné od** lze definovat pro komponentu EV, chcete-li zadat datum, od kterého tato komponenta začne být platná pro proces vykazování. Datum relace aplikace Microsoft Dynamics 365 for Operations slouží k definování, zda komponenta je platná pro spuštění. Poslední verze slouží k procesu vykazování při více než jedné platné verzi pro konkrétní datum.

#### <a name="component-access"></a>Přístup komponent

Přístup ke komponentám formátu EV závisí na nastavení ISO kódu země/oblasti. Pokud je toto nastavení pro vybranou verzi konfigurace formátu prázdné, k součásti formátu lze přistupovat z libovolné společnosti aplikace Dynamics 365 for Operations v době běhu. Pokud toto nastavení obsahuje ISO kódy země/oblasti, je komponenta formátu přístupná ze společností Dynamics 365 for Operations, jejichž primární adresa je definována pro jednu komponentu formátu ISO kódu země/oblasti. Různé verze součástí formátu data mají pravděpodobně různá nastavení ISO kódů země/oblasti.

#### <a name="configuration"></a>Konfigurace

Konfigurace EV je obal určité součásti EV: buď **Datového modelu** nebo **Formátu**. Konfiguraci mohou obalovat různé verze určitých součástí EV. Každá konfigurace je označena jako vlastní určitou konfigurací poskytovatele. Verze **NÁVRH** komponent z konfigurace lze upravit po zvolení vlastníka konfigurace jako aktivního poskytovatele v nastavení EV v aplikaci Dynamics 365 for Operations. Každá konfigurace modelu obsahuje komponentu **Datový model**. Nová konfigurace formátu může pocházet (být odvozena) z konfigurace určitého datového modelu. Konfigurace vytvořeného formátu se zobrazí ve stromové struktuře konfigurace jako konfigurace podřízená původní konfiguraci datového modelu. Konfigurace vytvořeného formátu obsahuje komponentu **Formát**. Komponenta **Datový model** původní konfigurace modelu bude automaticky vložena do komponenty **Formát** vytvořené z podřízené konfigurace formátu jako výchozího datového zdroje. Konfigurace EV je sdílená pro společnosti aplikace Dynamics 365 for Operations.

#### <a name="provider"></a>Zprostředkovatel

Poskytovatel EV je identifikací strany, která se používá k označení autora (vlastníka) každé konfigurace EV. EV umožňuje spravovat seznam zprostředkovatelů konfigurace. Konfigurace formátu vydané pro elektronické dokumenty jako součást řešení Dynamics 365 for Operations jsou označeny jako vlastněné poskytovatelem konfigurace **Microsoft**.

#### <a name="repository"></a>Úložiště

Úložiště EV obsahuje konfigurace EV. Následující typy úložiště EV jsou aktuálně podporovány: **Zdroje Operations** a **projekt LCS**. Úložiště zdrojů ** Operations** poskytuje přístup k seznamu konfigurací, které jsou dodávány jako součást řešení Dynamics 365 for Operations společností Microsoft jako zprostředkovatelem konfigurace EV. Tyto konfigurace lze importovat do aktuální instance aplikace Dynamics 365 for Operations a používat pro elektronické sestavy. Můžete je používat pro další lokalizace a přizpůsobení. Úložiště **projektu LCS** poskytuje přístup k seznamu konfigurací určitého projektu LCS (knihovny majetku projektu LCS), který byl vybrán ve fázi registrace úložiště. EV podporuje schopnost odeslat sdílené konfigurace z aktuální instance aplikace Dynamics 365 for Operations do určitého úložiště **projektu LCS**. Můžete také importovat konfigurace z určitého úložiště **projektu LCS** do aktuální instance aplikace Dynamics 365 for Operations. Požadovaná úložiště **LCS projektu** lze registrovat pro jednotlivé poskytovatele konfigurace jednotlivě z aktuální instance aplikace Dynamics 365 for Operations. Každé úložiště může být určeno konkrétnímu poskytovateli konfigurace.

## <a name="supported-scenarios"></a>Podporované scénáře
### <a name="building-a-data-model"></a>Vytvoření datového modelu

EV nabízí návrháře modelu, kterého můžete použít pro vytvoření modelu dat pro určité obchodní domény. Všechny obchodních entity specifické pro domény a a vztahy mezi nimi mohou být přítomné v datovém modelu jako hierarchická struktura. Následující obrázek znázorňuje příklad tohoto typu datového modelu (model dat pro doménu platby). [![Příklad modelu dat](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce záznamem úloh **Elektronické vykazování – návrh datového modelu pro určitou doménu** (součástí obchodního procesu **Získání/vývoj součástí IT služeb/řešení (10677)** ).

### <a name="translating-data-model-content"></a>Překlad obsahu datového modelu

Obsah datového modelu (štítky a popisy) lze přeložit do jiných jazyků, které aplikace Dynamics 365 for Operations podporuje. Obsah datového modelu můžete chtít převést z následujících důvodů:

-   V době návrhu – aby byl obsah více srozumitelný pro návrháře formátu mluvící cizím jazykem, kteří využívají data modelu k mapování dat komponentů formátu
-   V době běhu – aby byl obsah příjemnější a více příjemný pro uživatele představením požadavků a asistence parametrů spuštění, stejně jako nakonfigurovaných zpráv ověření (chyby a upozornění) v jazyce, který uživatel aktuálně přihlášený do aplikace Microsoft Dynamics 365 for Operations upřednostňuje

Následující obrázek zobrazuje příklad toho, jak lze obsah datového modelu přeložit z angličtiny do japonštiny. [![Obsah datového modelu v angličtině](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Obsah datového modelu přeložený do japonštiny](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Konfigurace mapování modelu dat

EV poskytuje návrháře mapování modelu, který umožňuje uživatelům mapovat datové modely, které jsou navrženy pro konkrétní zdroje dat aplikace Dynamics 365 for Operations. Následující obrázek popisuje příklad tohoto typu mapování modelu dat (mapování modelu **platebního převodu SEPA** datového modelu platební domény). [![Příklad mapování datového modelu](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) K seznámení se s tímto scénářem podrobněji si přehrajte průvodce úkoly **Elektronické vykazování – definování mapování modelů a výběr zdrojů dat** a **Elektronické vykazování – namapování datového modelu na vybrané zdroje dat** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Uložení navrženého modelu komponent jako konfigurace modelu

EV může ukládat navržený datový model společně s přiřazenými mapováními dat jako konfiguraci modelu aktuální instance aplikace Dynamics 365 for Operations. Následující obrázek znázorňuje příklad tohoto typu konfigurace datového modelu (konfigurace modelu dat pro doménu platby). [![Příklad konfigurace modelu dat ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce záznamem úloh **Elektronické vykazování – návrh datového modelu pro určitou doménu** (součást **součástí obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)** ).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Vytvoření formátu využívajícího datového modelu jako základu

EV podporuje návrháře formátu k vytvoření formátu konkrétního elektronického dokumentu pro vybrané obchodní domény výběrem komponenty modelu jako základu. Stejný návrhář formátu EV nabízí schopnost mapování vytvořeného formátu pro výběr mapování modelu dat vybrané domény jako zdroje dat. Následující obrázek znázorňuje příklad tohoto typu formátu (konfigurace formátu, která podporuje formát platby **BACS** pro Spojené království). [![Příklad formátu, který má datový model jako základ](./media/pic-format-1024x690.png)](./media/pic-format.png) K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce záznamem úloh **Elektronické vykazování – návrh datového modelu pro určitou doménu** (součástí obchodního procesu **Získání/vývoj součástí IT služeb/řešení (10677)** ).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Vytváření konfigurace pro generování elektronických dokumentů ve formátu listu OPENXML

Návrhář formátu EV slouží k vytvoření konkrétních elektronický dokumentů ve formátu listu OPENXML. Následující obrázek znázorňuje příklad tohoto typu formátu (formát konfigurace generovat OPENXML list s podrobnostmi vybraném deníku plateb):[![Pic-ER-Formát Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) se seznámit s podrobnostmi tohoto scénáře, hrát **ER vytvořit konfiguraci sestav ve formátu OPENXML** úloh průvodce (část **7.5.4.3 získání/vývoje IT řešení nebo služby komponent (10677)** obchodního procesu). Použijte níže uvedený soubor aplikace Excel jako šablonu návrhu formátu EV a dokončete tak krok importu šablony formátu popsaný v tomto průvodci záznamem úloh : [Šablona sestavy platby (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202):

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Uložení navržené komponenty formátu do konfigurace formátu

EV umožňuje ukládat navržený formát společně s konfigurovanými mapováními dat jako konfiguraci formátu aktuální instance aplikace Dynamics 365 for Operations. Na předchozím obrázku je uveden příklad tohoto typu konfigurace formátu (**BACS (UK)**, který je podřízený konfiguraci **Platební model**). K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – návrh formátu pro určitou doménu** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Konfigurace aplikace Dynamics 365 for Operations k použití interně vytvořeného formátu

Aplikaci Dynamics 365 for Operations lze použít ke spuštění za použití vytvořeného formátu pro generování elektronických sestav. Odkaz k vytvořené konfiguraci formátu by měl být definován ve specifických nastaveních určité domény. Například pokud chcete zahájit používání konfigurace formátu EV pro elektronické platby dodavatelů ve formátu BACS, na konfigurace formátu by se mělo odkazovat v určitém způsoby platby tak, jak je znázorněno na následujícím obrázku: 

[![Konfigurace formátu BACS (UK)](media/ger-bacs-uk-format-configuration.png) 

[![Odkazování na formát BACS (UK) v metodě platby](media/ger-bacs-uk-format-method.png) 

K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – použití formátu ke generování elektronického dokumentu pro platby** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

## <a name="handling-er-components"></a>Zpracování komponent EV
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Publikování komponent EV v LCS pro jejich externímu nabízení (lokalizace)

Vlastník vytvořené součásti (modelu nebo formátu) je schopen používat EV pro publikování dokončené verze součásti do LCS. Je požadováno úložiště typu **projekt LCS**pro aktuálního zprostředkovatele konfigurací EV. Při změně stavu dokončené verze součásti z **DOKONČENO** na **SDÍLENO**, je tato verze publikována do LCS. Při publikování komponenty do LCS se vlastník této součásti stane poskytovatelem služby pro podporu této součásti. Například pokud součást formátu slouží ke generování zákonem požadovaných elektronických dokumentů (například podle scénáře lokalizace), předpokládá se, že tento formát splňuje změny právních předpisů, a že poskytovatel vydává nové verze pokaždé, když musí podporovat nové právní požadavky. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Odeslání konfigurace ER do služby Lifecycle Services**(součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Import součásti EV z LCS pro interní použití

EV umožňuje importovat komponenty EV z LCS do aktuální instance Dynamics 365 for Operations. Je požadováno úložiště typu **projekt LCS**. Při importu komponent EV z LCS do aktuální instance aplikace Dynamics AX, vlastník této instance Dynamics 365 for Operations se stane příjemcem služby poskytované vlastníkem importované komponenty (autorem). Například pokud tato komponenta formátu umožňuje generovat konkrétní elektronické dokumenty z aplikace Microsoft Dynamics 365 for Operations v určitém formátu některé země/oblasti (scénář lokalizace), předpokládá se, že uživatel dané služby bude mít možnost získat jakoukoli aktualizaci pro tento formát, a udržován ho v souladu s právními požadavky. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Import konfigurace ER ze služby Lifecycle Services** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Vytvoření formátu výběrem jiného formátu jako základu (přizpůsobení)

EV umožňuje vytváření (odvození) nové komponenty z aktuální verze komponenty (základní), která byla importována z LCS. Například uživatel chce odvodit nový formát a implementovat tak některé zvláštní požadavky na elektronický dokument (například další pole nebo rozsáhlý popis) s cílem podpořit scénář přizpůsobení. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – aktualizace formátu osvojováním jeho nové základní verze** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Upgrade formátu výběrem nové verze základního formátu (přeskládání)

EV podporuje schopnost automaticky přijmout změny poslední verze základní komponenty v aktuální verzi konceptu odvozené komponenty. Pro tento proces je používáno označení *přeskladnění*. Například nové regulační změny zavedené v nejnovější verzi formátu importovaných z LCS mohou být automaticky sloučeny do vlastní přizpůsobené verze tohoto formátu elektronického dokumentu. Všechny změny, které nelze automaticky sloučit, jsou považovány za konflikty. Tyto konflikty jsou uvedeny a připraveny pro ruční vyřešení v nástroji Návrhář příslušné součásti. K seznámení se s tímto scénářem v podrobnostech si přehrajte průvodce úkolem **Elektronické vykazování – aktualizace formátu osvojováním jeho nové základní verze** (součástí obchodního procesu **7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Seznam konfigurací EV, které jsou k dispozici v řešení Dynamics 365 for Operations
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



<a name="see-also"></a>Viz také
--------

[Požadavky na lokalizaci – vytvoření konfigurace elektronického výkaznictví](electronic-reporting-configuration.md)

[Správa životního cyklu konfigurace elektronického vykazování](general-electronic-reporting-manage-configuration-lifecycle.md)





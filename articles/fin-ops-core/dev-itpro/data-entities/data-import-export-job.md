---
title: Přehled úloh importu a exportu dat
description: Použijte pracovní prostor Správa dat k vytvoření a správě úloh importu a exportu dat.
author: Sunil-Garg
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3af49d9355f37e0016f491ed37050f75bbc65d72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684053"
---
# <a name="data-import-and-export-jobs-overview"></a>Přehled úloh importu a exportu dat

[!include [banner](../includes/banner.md)]

Použijte pracovní prostor **Správa dat** k vytvoření a správě úloh importu a exportu dat v aplikaci . Ve výchozím nastavení proces importu a exportu dat vytvoří tabulky fázování pro každou entitu v cílové databázi. Tabulky fázování umožňují ověřit, vyčistit anebo převést dat předtím, než budou přesunuta.

> [!NOTE]
> V tomto tématu se předpokládá, že jste obeznámeni s [datovými entitami](data-entities.md).

## <a name="data-importexport-process"></a>Proces importu a exportu dat
Import a export dat se skládá z následujících kroků.

1. Vytvoření úlohy importu nebo exportu, kde dokončíte následující úkoly:

    - Definujte kategorii projektu.
    - Identifikujte entity, které chcete importovat nebo exportovat.
    - Nastavte formát dat pro úlohu.
    - Seřaďte entity tak, aby se zpracovaly v logických skupin a v pořadí, které dává smysl.
    - Určete, zda použít tabulky fázování.

2. Ověřte, zda jsou zdrojová a cílová data správně namapována.
3. Ověřte zabezpečení pro úlohu import nebo exportu.
4. Spusťte úlohu importu nebo exportu.
5. Ověřte, zda úloha proběhla podle očekávání tím, že zkontrolujete historii úlohy.
6. Vyčistěte tabulky fázování.

Zbývající části tohoto tématu poskytují podrobnější informace o jednotlivých krocích postupu.

> [!NOTE]
> Chcete-li obnovit formulář Import/export dat a zobrazit poslední vývoj, použijte ikonu obnovení formuláře. Obnovení úrovně prohlížeče se nedoporučuje, protože přeruší všechny úlohy importu/exportu, které nejsou spuštěny v dávce.

## <a name="create-an-import-or-export-job"></a>Vytvoření úlohy importu nebo exportu
Úlohu importu nebo exportu dat lze spustit jednou i několikrát.

### <a name="define-the-project-category"></a>Definování kategorie projektu
Doporučujeme, abyste si dali načas s výběrem vhodné kategorie projektu pro svou úlohu importu a exportu. Kategorie projektu mohou pomoct se správou souvisejících úloh.

### <a name="identify-the-entities-to-import-or-export"></a>Identifikace entit, které chcete importovat nebo exportovat
Můžete přidat konkrétní entity do úlohy importu nebo exportu, nebo zvolit použití šablony. Šablony naplní úlohu seznamem entit. Možnost **Použít šablonu** je k dispozici po zadání názvu úlohy a uložení úlohy.

### <a name="set-the-data-format-for-the-job"></a>Nastavení formátu dat pro úlohu
Vyberete-li entitu, je nutné vybrat formát dat, která budou exportována nebo importována. Formáty definujete pomocí dlaždice **Nastavení datových zdrojů**. Formát zdrojových dat je kombinací **typ**, **formát**, **oddělovač řádků** a **oddělovač sloupců**. Existují také další atributy, ale ty jsou klíčové pro porozumění. V následující tabulce jsou uvedeny platné kombinace.

| Formát souboru            | Oddělovač řádků/sloupců                       | Styl XML                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Není k dispozici-                     |
| XML                    | \-Není k dispozici-                                      | XML-Element XML-Attribute |
| Oddělené, Pevná šířka | Čárka, středník, tabulátor, svislá čára, dvojtečka | \-Není k dispozici-                     |

### <a name="sequence-the-entities"></a>Seřazení entit
Entity lze seřadit v šabloně dat nebo v úloze importu a exportu. Při spuštění úlohy, která obsahuje více než jednu entitu dat, se musíte ujistit, že jsou entity správně seřazeny. Entity seřazujete především proto, abyste mohli adresovat všechny funkční závislosti mezi entitami. Pokud nemají entity žádnou funkční závislost, lze je naplánovat pro paralelní import nebo export.

#### <a name="execution-units-levels-and-sequences"></a>Spuštění jednotek, úrovní nebo řad
Jednotka spuštění, úroveň v jednotce spuštění a řazení entity pomáhají kontrolovat pořadí, v jakém jsou data exportována nebo importována.

- Entity v jiných jednotkách spuštění se zpracovávají souběžně.
- U každé jednotky spuštění se entity zpracovávají souběžně, pokud mají stejnou úroveň.
- V každé úrovni se entity zpracování podle jejich pořadového čísla v úrovni.
- po zpracování jedné úrovně se zpracuje další úroveň.

#### <a name="resequencing"></a>Opětovné seřazení
Může být zapotřebí opětovně seřadit vaše entity v následujících situacích:

- Pokud je použita jen jedna datová úlohu pro všechny vaše změny, můžete použít možnosti změny seřazení, abyste optimalizovali dobu provádění celé úlohy. V těchto případech můžete použít jednotku spuštění, aby představovala modul, úroveň, která představuje oblast funkce v modulu, a seřazení představující entitu. Díky tomuto přístupu je možné pracovat ve všech modulech současně, ale i nadále můžete pracovat v pořadí v jednotlivém modulu. K zajištění, aby proběhly paralelní operace úspěšně, je nutné brát ohled na všechny závislosti.
- Při použití vícero datových úloh (například jedna úloha pro každý modul) můžete použít řazení k ovlivnění úrovně a pořadí entit za účelem optimálního provedení úlohy.
- Pokud vůbec neexistují žádné závislosti, můžete seřadit entity na jiných jednotkách spuštění pro maximální optimalizaci.

Nabídka **Opětovné seřazení** je k dispozici při výběru více entit. Můžete opětovně provést řazení na základě jednotky spuštění, úrovně nebo možností seřazení. Můžete nastavit přírůstek pro opětovné seřazení vybraných entit. Jednotka, úroveň anebo pořadové číslo, které bylo vybráno pro každou entitu, je aktualizováno podle zadaného přírůstku.

#### <a name="sorting"></a>Třídění
Použijte možnost **Seřadit podle** k zobrazení seznamu entit v sekvenčním pořadí.

### <a name="truncating"></a>Zkrácení
Pro projekty importu můžete zkrátit záznamy předchozích entit před importem. To je užitečné v případě, že je nutné importovat záznamy do čisté sady tabulek. Toto nastavení je ve výchozím nastavení vypnuté.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Ověření, zda jsou zdrojová a cílová data správně namapována
Mapování je funkce vztahující se jak k úloze importu, tak k úloze exportu.

- V kontextu úlohy importu popisuje mapování to, jaké sloupce ve zdrojovém souboru se stanou sloupci v tabulce fázování. Systém tedy může určit, která data sloupce ze zdrojového souboru musí být zkopírována do příslušného sloupce v tabulce fázování.
- V kontextu úlohy exportu popisuje mapování to, jaké sloupce tabulky fázování (tedy zdroje) se stanou sloupci v cílovém souboru.

Pokud se názvy sloupců v tabulce fázování a v souboru shodují, systém automaticky vytvoří mapování na základě názvů. Avšak pokud se názvy liší, sloupce se automaticky nenamapují. V těchto případech je nutné dokončit mapování výběrem možnosti **Zobrazit mapu** na entitě v datové úloze.

Existují dvě zobrazení mapování: **Vizualizace mapování**, což je výchozí zobrazení, a **Podrobnosti mapování**. Červená hvězdička (\*) identifikuje všechna povinná pole entity. Než začnete pracovat s entitou, musí být tato pole mapována. U dalších polí lze při práci s entitou zrušit mapování podle potřeby. Chcete-li zrušit mapování pole, vyberte pole buď ve sloupci **Entita** nebo sloupec **Zdroj**, a poté vyberte **Odstranit výběr**. Vyberte **Uložit** pro uložení změn a zavřete stránku. Tím se vrátíte do projektu. Stejný postup můžete použít k úpravě mapování pole ze zdroje do fázování po provedení importu.

Mapování na stránce můžete vygenerovat výběrem možnosti **Generovat mapování zdroje**. Vygenerované mapování se chová jako automatické mapování. Proto je nutné ručně namapovat všechna nenamapovaná pole.

![Mapování dat](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Ověření zabezpečení pro úlohu import nebo exportu
Přístup k pracovnímu prostoru **Správa dat** lze omezit, tak, aby uživatelé bez oprávnění správce měli přístup pouze k určitým datovým úlohám. Přístup k úloze dat zahrnuje úplný přístup ke spuštění historie této úlohy a přístup k tabulkám fázování. Proto je třeba se ujistit, že existují příslušný ovládací prvky přístupu při vytváření datové úlohy na místě.

### <a name="secure-a-job-by-roles-and-users"></a>Zabezpečení úlohy podle role uživatelů
Použijte nabídku **Použitelné role** k omezení úlohy na jednu nebo více rolí zabezpečení. Pouze uživatelé v těchto rolích budou mít přístup k úloze.

Úlohu lze omezit také pro konkrétní uživatele. Pokud zabezpečíte úlohu podle uživatelů, nikoliv podle rolí, máte větší kontrolu, pokud je k jedné roli přiřazeno více uživatelů.

### <a name="secure-a-job-by-legal-entity"></a>Zabezpečení úlohy podle právnické osoby
Datové úlohy jsou svým charakterem globální. Je-li tedy datová úloha vytvořena a použita u právnické osoby, bude viditelná i u jiných právnických osob v systému. Toto výchozí chování může být upřednostňované v některých scénářích aplikace. Například organizace, která importuje faktury pomocí datových entit, může nabídnout centralizovaný tým zpracovávající faktury, který je zodpovědný za správu fakturačních chyb pro všechny divize v organizaci. V tomto případě je pro centralizovaný tým zpracovávající faktury užitečné mít přístup k úlohám importu faktur ze všech právnických osob. Výchozí chování tedy splňuje požadavek z hlediska právnické osoby.

Organizace však může potřebovat mít týmy zpracovávající faktury podle právnické osoby. V takovém případě by měl tým v právnické osobě mít přístup pouze k úloze importu faktury v rámci vlastní právnické osoby. Aby byl tento požadavek splněn, lze konfigurovat kontrolu přístupu k datovým úlohám na základě právnické osoby pomocí nabídky **Použitelné právnické osoby** uvnitř datové úlohy. Po dokončení konfigurace mohou uživatelé zobrazit pouze úlohy, které jsou k dispozici v právnické osobě, ke která jsou aktuálně přihlášeni. Pokud chtějí uživatelé zobrazit úlohy z jiné právnické osoby, musí přepnout na tuto právnickou osobu.

Úlohu lze zabezpečit podle rolí, uživatelů a právnické osoby současně.

## <a name="run-the-import-or-export-job"></a>Spuštění úlohy importu nebo exportu
Spustit úlohu můžete jednou výběrem tlačítka **Importovat** nebo **Exportovat** poté, co nadefinujete úlohu. Chcete-li nastavit opakovanou úlohu, zvolte **Vytvořit opakovanou datovou úlohu**.

> [!NOTE]
> Úlohu importu nebo exportu lze spustit výběrem tlačítka **Importovat** nebo **Exportovat**. Tím se naplánuje spuštění dávkové úlohy pouze jednou. Úloha se nemusí provést okamžitě, pokud dávková služba má výpadky kvůli velkému množství požadavků. Úlohy můžete také provádět synchronně výběrem **Importovat nyní** nebo **Exportovat nyní**. Úloha se spustí ihned a je to užitečné, pokud se dávka nespustí z důvodu omezení. Úlohy lze také naplánovat tak, aby se spustila později. Toho lze dosáhnout výběrem možnosti **Spustit v dávce**. Zdroje dávky podléhají omezení, takže dávková úloha nemusí začít okamžitě. Použití dávky je doporučená možnost, protože také pomáhá u velkých objemů dat, která je třeba importovat nebo exportovat. Dávkové úlohy lze naplánovat tak, aby se spouštěly na určité skupině dávek, což umožňuje větší kontrolu z pohledu vyvažování zátěže.

## <a name="validate-that-the-job-ran-as-expected"></a>Ověření, zda byla úloha spuštěna podle očekávání
Historie úloh je dostupná pro řešení potíží a analýzu na úlohách importu i exportu. Historie spuštění úloh je organizována podle časových rozsahů.

![Rozsahy historie úloh](./media/dixf-job-history.md.png)

Spuštění každé úlohy poskytuje následující podrobnosti:

- Podrobnosti o spuštění
- Protokol provádění

Podrobnosti o spuštění zobrazují stav každé datové entity, kterou úloha zpracovala. Díky tomu můžete rychle vyhledat následující informace:

- Jaké entity byly zpracovány.
- Kolik záznamů bylo pro danou entitu zpracováno a kolik se jich nezdařilo.
- Záznamy fázování pro každou entitu.

Můžete stáhnout data fázování do souboru pro úlohy exportu, nebo je můžete stáhnout jako balíček pro úlohy importu a exportu.

Chcete-li znát podrobnosti spuštění, můžete rovněž otevřít protokol provádění.

## <a name="parallel-imports"></a>Souběžné importy
Chcete-li urychlit import dat, lze souběžné zpracování importu povolit, pokud entita podporuje souběžné importy. Chcete-li konfigurovat paralelní import pro entitu, je nutné provést následující kroky.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa dat**.
2. V oddílu **Import/export** vyberte dlaždici **Parametry architektury**, která otevře stránku **Parametry platformy importu a exportu dat**.
3. Na kartě **Nastavení entity** vyberte možnost **Konfigurovat parametry spuštění entity** a otevřete stránku **Parametry spuštění importu entity**.
4. Nastavte následující pole pro konfiguraci paralelního importu pro entitu:

    - V poli **Entita** zvolte entitu.
    - Do pole **Počet záznamů prahové hodnoty pro import** zadejte počet záznamů prahové hodnoty pro import. Určuje počet záznamů, které mají být zpracovány podprocesem. Má-li soubor 10 000 záznamů, bude počet záznamů 2500 s počtem úkolů 4 znamenat, že v každém podprocesu bude zpracováno 2500 záznamů.
    - Do pole **Počet úkolů importu** zadejte počet úkolů importu. Tato hodnota nesmí přesáhnout maximální počet dávkových podprocesů přidělených pro dávkové zpracování v **Správa systému \> Konfigurace serveru**.

## <a name="clean-up-the-staging-tables"></a>Vyčištění tabulek fázování
Od aktualizace platformy 29 se tato funkce již nepoužívá. Je nahrazena novou verzí funkce Vyčištění historie úloh, která je vysvětlena níže.

Můžete vyčistit tabulky fázování pomocí funkce **Vyčištění fázování** v pracovním prostoru **Správa dat**. Chcete-li zvolit, jaké záznamy by měly být odstraněny z konkrétní tabulky fázování, můžete použít následující možnosti:

- **Entita** – Pokud je zadaná pouze entita, všechny záznamy z této tabulky fázování se odstraní. Zvolte tuto možnost, abyste vyčistili všechna data z entity napříč všemi datovými projekty a všemi úlohami.
- **ID úlohy** – Je-li zadáno pouze ID úlohy, všechny záznamy pro všechny entity ve zvolené úloze se odstraní z příslušných tabulek fázování.
- **Datové projekty** – Pokud je vybrán datový projekt, budou odstraněny všechny záznamy pro všechny entity a napříč všemi úlohami pro zvolený datový projekt.

Také můžete kombinovat možnosti pro další omezení sady záznamů, která je odstraněna.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>Vyčištění historie úloh (k dispozici v aktualizaci platformy 29 a novější)

Funkce vyčištění historie úlohy ve správě dat musí být použita k naplánování pravidelného mazání historie provedení. Tato funkce nahrazuje předchozí funkci Vyčištění pracovní tabulky, která je nyní zastaralá. Následující tabulky budou vyčištěny procesem vyčištění.

-   Všechny tabulky fází

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Funkce **Vyčištění historie provádění** musí být povolena ve správě funkcí a lze k ní přistupovat z nabídky **Správa dat \> Vymazání historie úloh**.

### <a name="scheduling-parameters"></a>Parametry plánování

Při plánování procesu čištění je nutné zadat následující parametry definující kritéria pro vyčištění.

-   **Počet dnů pro uchování historie** – toto nastavení slouží k řízení rozsahu historie provádění, která má být zachována. Specifikuje se v počtech dní. Pokud je úloha čištění naplánována jako opakovaná dávková úloha, toto nastavení bude fungovat jako neustálé přesouvání okna, takže vždy zůstala historie zadaného počtu dnů při odstranění zbývající položky. Výchozí hodnota je 7 dní.

-   **Počet hodin pro provedení úlohy** – v závislosti na množství historie, která má být vyčištěna, se může celková doba provádění úlohy čištění pohybovat v rozsahu od několika minut až po několik hodin. Tento parametr musí být nastaven na počet hodin, který bude úloha provádět. Poté, co byla úloha čištění provedena po zadaný počet hodin, úloha se ukončí a bude pokračovat v vyčištění při příštím spuštění na základě plánu opakování.

    Maximální čas provedení lze určit nastavením maximálního počtu hodin, které musí úloha spustit pomocí tohoto nastavení. Logika čištění projde v čase s chronologicky uspořádaným pořadím jedno ID spuštění úlohy a nejstarší je nejprve pro vyčištění související historie spuštění. Ukončí vyzvednutí nového ID provedení vyčištění, když je zbývající doba trvání během posledních 10 % zadané doby trvání. V některých případech se očekává, že úloha vyčištění bude pokračovat i po uplynutí určené maximální doby. To bude převážně záviset na počtu záznamů, které mají být odstraněny pro aktuální ID spuštění, které bylo zahájeno před dosažením prahové hodnoty 10 %. Čištění, které bylo zahájeno, musí být dokončeno, aby byla zajištěna integrita dat, což znamená, že vyčištění bude pokračovat navzdory překročení stanoveného limitu. Po dokončení operace nebudou nová ID spuštění vydána a úloha vyčištění skončí. Zbývající historie spuštění, která nebyla vyčištěna z důvodu nedostatečné doby provádění, bude vybrána při příštím plánování úlohy čištění. Výchozí a minimální hodnota pro toto nastavení je 2 hodiny.

-   **Opakovaná dávka** – úlohu čištění lze spustit jako jednorázové, ruční spuštění nebo je také možné naplánovat její opakované provedení v dávce. Dávku lze naplánovat pomocí nastavení **Spustit na pozadí**, což je standardní nastavení dávky.

> [!NOTE]
> Nejsou-li záznamy v pracovních tabulkách zcela vyčištěny, zkontrolujte, zda je naplánováno spuštění úlohy čištění. Jak bylo vysvětleno výše, při jakékoli čisté realizaci bude úloha čistit pouze tolik ID spuštění, kolik je možné v zadaných maximálních hodinách. Chcete-li pokračovat v čištění všech zbývajících záznamů fázování, je nutné naplánovat pravidelné spouštění úlohy.

## <a name="job-history-clean-up-and-archival-available-for-preview-in-platform-update-39-or-version-10015"></a>Vyčištění a archivace historie úloh (k dispozici jako preview v aktualizaci platformy 39 nebo verzi 10.0.15)
Funkce vyčištění a archivace historie úloh nahradí předchozí verze funkce vyčištění. Tato část vysvětluje tyto nové funkce.

Jednou z hlavních změn ve funkci čištění je použití dávkové úlohy systému k vyčištění historie. Použití dávkové úlohy systému umožňuje aplikacím Finance and Operations mít automaticky naplánovanou a spouštěnou dávkovou úlohu vyčištění, jakmile je systém připraven. Dávkové úlohy již není nutné ručně plánovat. V tomto výchozím režimu provádění bude dávková úloha spuštěna každou hodinu počínaje půlnocí a zachová si historii provádění za posledních 7 dní. Vymazaná historie je archivována pro budoucí načtení.

> [!NOTE]
> Protože je tato funkce zatím v preview, dávková úloha systému neodstraní žádnou historii provádění, dokud nebude povolena prostřednictvím testovací verze úlohy DMFEnableExecutionHistoryCleanupSystemJob. Až bude funkce obecně k dispozici v budoucím vydání, nebude testo testovací verze vyžadována a dávková úloha systému začne čistit a archivovat na základě definovaného plánu, až bude systém připraven, jak je vysvětleno výše. 

> [!NOTE]
> V budoucím vydání budou předchozí verze funkce vyčištění odebrány z aplikací Finance and Operations.

Druhou změnou v procesu čištění je archivace vymazané historie provádění. Úloha vyčištění archivuje odstraněné záznamy do úložiště objektů blob, které DIXF používá pro běžné integrace. Archivovaný soubor bude ve formátu balíčku DIXF a bude k dispozici po dobu 7 dnů v objektu blob, během kterého bude možné jej stáhnout. Výchozí životnost archivovaného souboru 7 dní lze v parametrech změnit na maximálně 90 dní.

### <a name="changing-the-default-settings"></a>Změna výchozího nastavení
Tato funkce je aktuálně v náhledu a musí být explicitně zapnuta povolením testovací verze úlohy DMFEnableExecutionHistoryCleanupSystemJob. Ve správě funkcí musí být také zapnuta funkce vyčištění fázování.

Chcete-li změnit výchozí nastavení životnosti archivovaného souboru, přejděte do pracovního prostoru správy dat a vyberte možnost **Vyčištění historie úlohy**. Nastavte **Počet dnů uchování balíčku v objektu blob** na hodnotu mezi 7 a 90 (včetně). Změna se projeví u archivů, které jsou vytvořeny po provedení této změny.

### <a name="downloading-the-archived-package"></a>Stahování archivovaného balíčku
Tato funkce je aktuálně v náhledu a musí být explicitně zapnuta povolením testovací verze úlohy DMFEnableExecutionHistoryCleanupSystemJob. Ve správě funkcí musí být také zapnuta funkce vyčištění fázování.

Chcete-li stáhnout archivovanou historii spuštění, přejděte do pracovního prostoru správy dat a vyberte možnost **Vyčištění historie úlohy**. Výběrem položky **Historie zálohování balíčku** otevřete formulář historie. Tento formulář zobrazuje seznam všech archivovaných balíčků. Archiv lze vybrat a stáhnout výběrem možnosti **Stáhnout balíček**. Stažený balíček bude ve formátu balíčku DIXF a bude obsahovat následující soubory:

-   Soubor tabulky fázování entit
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG


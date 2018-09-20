---
title: "Úlohy importu a exportu dat"
description: "Použijte pracovní prostor Správa dat k vytvoření a správě úloh importu a exportu dat."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 68cafc167c178e2feeb0a5af764a491ea6b3c60b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="data-import-and-export-jobs"></a>Úlohy importu a exportu dat

[!include [banner](../includes/banner.md)]

K vytvoření a správě úloh importu a exportu dat v aplikaci Microsoft Dynamics 365 for Finance and Operations používáte pracovní prostor **Správa dat**. Ve výchozím nastavení proces importu a exportu dat vytvoří tabulky fázování pro každou entitu v cílové databázi. Tabulky fázování umožňují ověřit, vyčistit anebo převést dat předtím, než budou přesunuta.

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

## <a name="validate-that-the-job-ran-as-expected"></a>Ověření, zda byla úloha spuštěna podle očekávání
Historie úloh je dostupná pro řešení potíží a analýzu na úlohách importu i exportu. Historie spuštění úloh je organizována podle časových rozsahů.

![Rozsahy historie úloh](./media/dixf-job-history.md.png)

Spuštění každé úlohy poskytuje následující podrobnosti:

- Podrobnosti o spuštění
- Protokol provádění

Podrobnosti o spuštění zobrazují stav každé datové entity, kterou úloha zpracovala. Díky tomu můžete rychle vyhledat následující informace:

- Jaké entity byly zpracovány
- Kolik záznamů bylo pro danou entitu zpracováno a kolik se jich nezdařilo
- Záznamy fázování pro každou entitu

Můžete stáhnout data fázování do souboru pro úlohy exportu, nebo je můžete stáhnout jako balíček pro úlohy importu a exportu.

Chcete-li znát podrobnosti spuštění, můžete rovněž otevřít protokol provádění.

## <a name="clean-up-the-staging-tables"></a>Vyčištění tabulek fázování
Můžete vyčistit tabulky fázování pomocí funkce **Vyčištění fázování** v pracovním prostoru **Správa dat**. Chcete-li zvolit, jaké záznamy by měly být odstraněny z konkrétní tabulky fázování, můžete použít následující možnosti:

- **Entita** – Pokud je zadaná pouze entita, všechny záznamy z této tabulky fázování se odstraní. Zvolte tuto možnost, abyste vyčistili všechna data z entity napříč všemi datovými projekty a všemi úlohami.
- **ID úlohy** – Je-li zadáno pouze ID úlohy, všechny záznamy pro všechny entity ve zvolené úloze se odstraní z příslušných tabulek fázování.
- **Datové projekty** – Pokud je vybrán datový projekt, budou odstraněny všechny záznamy pro všechny entity a napříč všemi úlohami pro zvolený datový projekt.

Také můžete kombinovat možnosti pro další omezení sady záznamů, která je odstraněna.


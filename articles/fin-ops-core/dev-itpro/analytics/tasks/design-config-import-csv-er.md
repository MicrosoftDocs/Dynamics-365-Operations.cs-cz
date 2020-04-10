---
title: Návrh konfigurací elektronického výkaznictví pro import dat z externích CSV souborů
description: Tento postup uvádí informace o tom, jak navrhnout konfigurace elektronického vykazování pro import dat do aplikace Finance and Operations z externího souboru ve formátu CSV.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8511b83a5d327f6a1d5c9ace091eae9e546307b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142222"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>Návrh konfigurací elektronického výkaznictví pro import dat z externích CSV souborů

[!include [banner](../../includes/banner.md)]

Tento postup uvádí informace o tom, jak navrhnout konfigurace elektronického vykazování pro import dat do aplikace z externího souboru ve formátu CSV. V tomto postupu vytvoříte požadované ER konfigurace pro vzorovou společnost Litware, Inc. K dokončení těchto kroků musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního". 

Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady USMF. 

Je nutné také stáhnout a uložit místně následující soubory: (https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Můžete nakonfigurovat proces importu externích souborů ve formátu XML, TXT nebo CSV do tabulek aplikace. Nejprve je nutné vytvořit abstraktní datový model představující importu dat z obchodního hlediska – vytvoření – pro tento účel je vytvořena konfigurace datového modelu ER. Dále definujte strukturu importovaného souboru, který se mapuje na určený datový model jako způsob přemostění dat ze souboru do abstraktního datového modelu – pro to je vytvořena konfigurace formátu ER. Pak je nutné rozšířit konfiguraci datového modelu ER o nové mapování modelu, které popisuje, jakým způsobem budou data z importovaného souboru a trvalá data z abstraktního datového modelu použita k aktualizaci tabulek aplikace nebo datových entit.  
    * Následující kroky popisují, jak jsou importovány externě sledované transakce dodavatelů z externího souboru CSV pro pozdější použití ve vypořádání dodavatele pro formuláře 1099.   
    * Ověřte, zda poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.  
2. Klikněte na Konfigurace výkaznictví.
3. Použijte filtr model platby 1099. Pokud jste už dokončili postup "ER Vytvoření požadovaných konfigurací importu dat z externího souboru pro elektronické vykazování" a v konfiguračním stromu je k dispozici konfigurace 'Model plateb 1099', přeskočte všechny kroky v dalším dílčím úkolu.   

## <a name="add-a-new-er-model-configuration"></a>Přidání nové konfigurace ER modelu
1. Místo vytváření nového modelu k podpoře importu dat načtěte soubor 1099model.xml, který jste předtím stáhli. Tento soubor obsahuje vlastní datový model transakcí dodavatele. Tento datový model je již namapován na nezbytné datové komponenty.  
2. Klikněte na Směna.
3. Klikněte na Načíst ze souboru XML.
4. Klikněte na tlačítko Procházet a vyhledejte soubor 1099model.xml, který jste předtím stáhli.  
5. Klikněte na tlačítko OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Přidání nové konfigurace ER modelu, která podporuje import dat
1. Ve stromové struktuře zvolte '1099 Model platby'.
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Nový zadejte 'Formát založený na datovém modelu 1099 Model platby'.
4. Vyberte možnost Ano v poli Podporuje import dat.
5. Stisknutím klávesy ESC zavřete tuto stránku.
    * Místo vytváření nového formátu ER k podpoře importu dat načtěte soubor 1099formatcsv.xml, který jste předtím stáhli. Tento soubor obsahuje požadovaný formát ER, který definuje strukturu příchozího souboru CSV, který chcete importovat, a mapování této struktury na vlastní datový model transakcí dodavatelů.   
6. Klikněte na Směna.
7. Klikněte na Načíst ze souboru XML.
    * Klikněte na tlačítko Procházet a vyhledejte soubor 1099formatcsv.xml, který jste předtím stáhli.  
8. Klikněte na tlačítko OK.
9. Ve stromové struktuře rozbalte '1099 Platební model'.
10. Ve stromové struktuře vyberte  '1099 Payments model\For importing vendors' transactions (CSV)'.

## <a name="review-format-settings"></a>Revize nastavení formátu
1. Klikněte na možnost Návrhář.
2. Klikněte na Rozbalit/sbalit.
3. Přepnutím aktivujte 'Zobrazit podrobnosti'.
    * Navržený formát představuje očekávanou strukturu externího souboru ve formátu CSV.  
4. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence'.
    * pro kořenový element typu SEQUENCE, byla v poli 'Speciální znaky' vybrána možnost ‘Nový řádek - Windows (CR LF)’. Na základě tohoto nastavení musí být každý řádek souboru analýzy považován za samostatný záznam.   
5. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* '.
    * Pro element Root\Line typu SEQUENCE, byla v poli ‘Multiplicity’ vybrána možnost 'Jeden k mnoha'. Na základě tohoto nastavení bude v souboru analýzy přítomen alespoň jeden řádek.   
6. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case'.
    * Byl přidán element Root\Line\Types typu CASE jako vnořený element sekvence Root\Line. Vzhledem k tomu, že tento element CASE obsahuje 3 vnořené elementy sekvence, předpokládá toto nastavení, že v souboru analýzy budou tři typy řádků.   
7. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1 '.
    * Element Root\Line\Types\Header typu SEQUENCE obsahuje vnořený element STRING, jehož hodnota je definovaná jako pevná hodnota řetězce. Tato sekvence provede analýzu řádku záhlaví souboru analýzy.   
8. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)'.
    * Element Root\Line\Types\Record typu SEQUENCE je nakonfigurovaný tak, aby analyzoval řádky transakce. Všimněte si, že možnost 'vlastního oddělovače' byla nakonfigurovaná jako čárka. To znamená, že se čárka bude používat jako oddělovač polí u tohoto typu řádku v souboru analýzy.   
    * Všimněte si, že pro element Root\Line\Types\Record bylo přidáno několik vnořených elementů různých datových typů k analýze řádků transakce jako samostatných polí. Všimněte si, že možnost 'Nabídka aplikace' byla nakonfigurována jako 'Žádný'. To znamená, že v souboru analýzy budou všechna pole tohoto typu považována za pole bez uzavřených znaků.   
9. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime'.
    * Element Root\Line\Types\Record\TransactionDate byl například nakonfigurován na získání hodnoty data a času transakce ze souboru analýzy ve formátu ‘M/d/rrrr’.   
10. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1 '.
    * Všimněte si, že element Root\Line\Types\Record\CountryCode typu STRING je nakonfigurovaný na možnost ‘Nula jedna’ v poli ‘Multiplicity’. Toto nastavení považuje hodnotu pole CountryCode na řádku souboru analýzy za volitelnou.   
11. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)'.
    * Všimněte si, že element Root\Line\Types\Record\Remark typu SEQUENCE je nakonfigurovaný jako element s možností ‘Vše’ v poli ‘Aplikace nabídky’ a znak dvojité uvozovky v poli 'Nabídka'. Znamená to, že všechna pole tohoto typu řádků v souboru analýzy (popsaném vnořenými elementy: Text typu STRING) budou považovány za znaky ve dvojitých uvozovkách.  
12. Ve stromovém zobrazení vyberte 'Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1 '.
    * Element Root\Line\Types\Unparsed typu SEQUENCE byl nakonfigurován na analýzu řádek transakce pro strukturu, která neodpovídá struktuře popsané výše v nadřazeném elementu CASE.   

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Kontrola nastavení mapování formátu na datový model
1. Klikněte na Mapovat formát na model.
    * Formát mapování modelu Mapování na model z formátu CSV popisuje tok dat převodu dat z příchozího souboru CSV na datový model.   
2. Klikněte na možnost Návrhář.
3. Ve stromové struktuře rozbalte Formát.
    * Všimněte si, že navržený formát je zde prezentován jako komponenta zdroje dat.  
4. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)'.
5. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)'.
6. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)'.
7. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)'.
8. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)'.
9. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data'.
10. Ve stromovém zobrazení rozbalte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)'.
11. Ve stromovém zobrazení vyberte 'format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)'.
    * Všimněte si, že povinné a volitelné elementy formátu, jako je TransactionDate a CountryCode, vypadají jinak v předdefinované komponentě zdroje dat 'formát'.   
12. Ve stromovém zobrazení rozbalte 'Transactions = '$both''.
    * Všimněte si, že prvky formátu, který určuje strukturu importovaného souboru, jsou vázány na prvky datového modelu. Na základě těchto vazeb bude obsah importovaného souboru CSV uložen za běhu v existujícím datovém modelu. Věnujte pozornost vazbě elementu CountryRegion. Pro jakýkoliv element transakce v příchozím souboru, který nemá zadanou hodnotu kódu země, se v datovém modelu načte výchozí kód země 'USA'.   
13. Přepnutím aktivujte 'Zobrazit podrobnosti'.
14. Klikněte na kartu Ověření.
15. Klikněte na Hledat.
16. Do pole Najít zadejte 'vend'.
17. Klikněte na Najít další.
    * Toto mapování formátu může obsahovat uživatelem definovanou logiku k ověření přesnosti importovaných dat z obchodního hlediska. Například na základě nastavení bude pro jakýkoli řádek v importujícím souboru, jehož struktura neodpovídá struktuře řádku záhlaví ani řádku transakce, generována zpráva s upozorněním v informačním protokolu, která o tomto případu informuje uživatele a vyznačuje číslo pořadí transakce v souboru.   
18. Zavřete stránku.

## <a name="run-the-format-mapping"></a>Spuštění mapování formátu
Pro účely testování proveďte mapování formátu pomocí souboru 1099entriescsv.csv souboru, který jste stáhli. Generovaný výstup bude prezentovat data, která budou importována z vybraného souboru CSV a načtena do vlastního datového modelu při reálném importu.   
1. Klikněte na položku Spustit.
    * Klikněte na tlačítko Procházet a vyhledejte soubor 1099entriescsv.csv, který jste předtím stáhli.  
2. Klikněte na tlačítko OK.
    * Všimněte si varovných zpráv o řádcích, které nebyly přijaty. Řádek 4 obsahuje hodnotu příjmu, která je uvedena v nepřijatelném formátu, zatímco řádek 7 neobsahuje text poznámky k transakci v uvozovkách.   
    * Zkontrolujte výstup ve formátu XML, který představuje data importovaná z vybraného souboru a přenesená do datového modelu. Všimněte si, že byly zpracovány všechny řádky 7 importovaného souboru CSV. Řádek 1 nadpisů obsahujících polí byl vynechán, 4 transakce byly správně analyzovány a 2 transakce byly rozpoznány jako neplatné.   
3. Zavřete stránku.
4. Zavřete stránku.


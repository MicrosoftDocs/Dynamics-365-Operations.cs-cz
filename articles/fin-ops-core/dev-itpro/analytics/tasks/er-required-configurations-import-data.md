---
title: Elektronické vykazování – Vytvoření požadovaných konfigurací pro import dat z externího souboru
description: Následující kroky vysvětlují, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhnout konfiguraci elektronického výkaznictví pro import dat v aplikaci Microsoft Dynamics 365 Finance z externího souboru.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48a327fc5033a7478d2ae5e401ffdce6e4546ad0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042866"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>Elektronické vykazování – Vytvoření požadovaných konfigurací pro import dat z externího souboru

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující kroky vysvětlují, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhnout konfiguraci elektronického výkaznictví pro import dat v aplikaci z externího souboru. V tomto příkladu vytvoříte požadované ER konfigurace pro vzorovou společnost Litware, Inc. K dokončení těchto krokůmusíte nejprve dokončit postup z průvodce záznamem úloh ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního. Tyto kroky lze dokončit za použití datové sady USMF. Je nutné stáhnout a uložit lokálně následující soubory pomocí odkazů z tématu Přehled elektronického vykazování (https://go.microsoft.com/fwlink/?linkid=852550): 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

ER umožňuje podnikovým uživatelům konfigurovat proces importu souborů externích dat do tabulek v ve formátech .XML nebo .TXT. Nejprve je třeba navrhnout konfiguraci abstraktního datového modelu a ER datového modelu, které budou představovat importovaná data. Dále je třeba definovat strukturu souboru, který chcete importovat, a metodu, kterou použijete k importu dat ze souboru do abstraktního datového modelu. Pro tento abstraktní datový model msuí být vytvořena konfigurace formátu ER, která se mapuje na navržený datový model. Poté musí být konfigurace datového modelu rozšířena mapováním, které popisuje, jak jsou importovaná data zachována jako data abstraktního datového modelu a jak se použijí k aktualizaci tabulek.  Konfigurace ER datového modelu musí být připojena k novému mapování modelu popisujícímu vazbu datového modelu k umístění aplikací.  

Následující scénář ukazuje možnosti importu ER dat. To zahrnuje transakce dodavatele, které jsou sledovány externě a následně importovány, aby byly uvedeny ve vyrovnání dodavatele pro sestavy 1099.   

## <a name="add-a-new-er-model-configuration"></a>Přidání nové konfigurace ER modelu
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.

    Ověřte, že poskytovatel konfigurace pro vzorovou společnost Litware, Inc. je k dispozici a označen jako aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.    

2. Klikněte na Konfigurace výkaznictví.

    Místo vytváření nového modelu k podpoře importu dat načtěte soubor 1099model.xml, který jste předtím stáhli. Tento soubor obsahuje vlastní datový model transakcí dodavatele. Tento datový model je mapován na komponenty dat, které jsou v datové entitě AOT.   

3. Klikněte na Směna.
4. Klikněte na Načíst ze souboru XML.

    Klikněte na tlačítko Procházet a vyhledejte soubor 1099model.xml, který jste předtím stáhli.  

5. Klikněte na tlačítko OK.
6. Ve stromové struktuře zvolte '1099 Model platby'.

## <a name="review-data-model-settings"></a>Revize nastavení datového modelu
1. Klikněte na možnost Návrhář.

    Tento model je určen k představení transakcí dodavatelů z obchodního hlediska a ty jsou nezávislé na implementaci.   

2. Ve stromové struktuře rozbalte '1099-MISC'.
3. Ve stromové struktuře zvolte '1099-MISC\Transakce'.
4. Ve stromové struktuře rozbalte '1099-MISC\Transakce'.

    Prvek Transakce tohoto modelu představuje jednotlivé transakce. Podřízené prvky slouží k zadání požadovaných podrobností, jako je například účet dodavatele a datum transakce, pro každou transakci.   

5. Zavřete stránku.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Přidání nové konfigurace ER modelu, která podporuje import dat
Kroky v této dílčí úloze ukazují, jak lze vytvořit novou konfiguraci formátu pro správu importu dat z externích souborů.   
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte 'Formát založený na datovém modelu 1099 Model platby'.
3. Vyberte možnost Ano v poli Podporuje import dat.
4. Stisknutím klávesy ESC zavřete tuto stránku.

    Místo vytváření nového formátu k podpoře importu dat načtěte soubor 1099format.xml, který jste předtím stáhli. Tento soubor obsahuje definovanou strukturu souboru, který chcete importovat, a mapování struktury na vlastní datový model transakcí dodavatelů.   
5. Klikněte na Směna.
6. Klikněte na Načíst ze souboru XML.
    Klikněte na tlačítko Procházet a vyhledejte soubor 1099format.xml, který jste předtím stáhli.  
7. Klikněte na tlačítko OK.
8. Ve stromové struktuře rozbalte '1099 Platební model'.
9. Ve stromové struktuře vyberte '1099 Platební model\Formát pro import transakcí dodavatele'.

## <a name="review-format-settings"></a>Revize nastavení formátu
1. Klikněte na možnost Návrhář.
2. Přepnutím aktivujte 'Zobrazit podrobnosti'.
3. Klikněte na Rozbalit/sbalit.
4. Klikněte na Rozbalit/sbalit.

    Navržený formát představuje očekávanou strukturu externího souboru. Tento soubor musí být ve formátu XML a musí mít kořenový prvek vyrovnání. Transakce každého dodavatele je představována prvkem transakce, který je definován tak, že má násobnost zero-to-many. To znamená, že příchozí soubor může obsahovat žádnou až několik transakcí. Vnořené prvky prvku 'transakce' představují atributy jediné transakce. Všimněte si, že všechny atributy, s výjimkou země, jsou označeny jako povinné, což znamená, že je nutné je mít v importujícím souboru.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Revize nastavení mapování formátu na datový model
1. Klikněte na Mapovat formát na model.

    Mapování 'pro import transakcí dodavatele' obsahuje pravidla převodu dat ze vstupního souboru XML do vybrané části vlastního datového modelu, který je definován výběrem definice 1099-MISC.  

2. Klikněte na možnost Návrhář.
3. Přepnutím aktivujte 'Zobrazit podrobnosti'.
4. Ve stromové struktuře rozbalte 'formát: Záznam'.
5. Ve stromové struktuře vyberte 'formát: Záznam'.

    Všimněte si, že navržený formát je zde prezentován jako komponenta zdroje dat.  

6. Ve stromové struktuře rozbalte 'format: Record\*settlement: XML Element 1..1 (settlement): Record.
7. Ve stromové struktuře rozbalte format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list.
8. Ve stromové struktuře rozbalte format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record.
9. Ve stromové struktuře rozbalte format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record.
10. Ve stromové struktuře zvolte format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record.

    Všimněte si, že prezentace povinných a nepovinných prvků formátu se v předdefinované komponentě zdroje dat ‘formát’ liší.  
11. Ve stromové struktuře rozbalte 'Transakce: Seznam záznamů= formát.vyrovnání.'$výčtové''.

    Všimněte si, že prvky formátu, který určuje strukturu importovaného souboru, jsou vázány na prvky vlastního datového modelu. Na základě těchto vazeb bude obsah importovaného souboru XML uložen za běhu v existujícím datovém modelu. Věnujte pozornost vazbě prvku země. Pro jakýkoliv prvek transakce v příchozím souboru, který takový prvek nemá, se v datovém modelu načte výchozí kód země 'USA'.  

12. Klikněte na kartu Ověření.

    Toto mapování formátu může obsahovat uživatelem definovanou logiku k ověření přesnosti importovaných dat z obchodního hlediska. Například na základě nastavení se pro jakoukoliv transakci v importujícím souboru bez definovaného kódu země vygeneruje zpráva s upozorněním v informačním protokolu, která informuje uživatele o tomto případu a označuje pořadové číslo transakce.  

13. Zavřete stránku.

## <a name="run-the-format-mapping-to-the-data-model"></a>Spuštění mapování formátu na datový model
Proveďte toto mapování formátu pro účely testování. Použijte 1099entries.xml soubor, který jste předtím stáhli. Tento soubor můžete exportovat z pracovního sešitu 1099entries.xlsx, který slouží k řízení transakcí dodavatelů. Generovaný výstup se naimportuje z vybraného souboru XML a načte vlastní datový model při reálném importu.  

1. Klikněte na položku Spustit.

    Klikněte na tlačítko Procházet a vyhledejte soubor 1099entries.xml, který jste předtím stáhli.  

2. Klikněte na tlačítko OK.

    Všimněte si upozornění o chybějícím kódu země pro transakci v importovaném souboru.  
    
    Zkontrolujte výstup ve formátu XML, který představuje data importovaná z vybraného souboru a přenesená do datového modelu.   

3. Zavřete stránku.
4. Zavřete stránku.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Revize nastavení pro mapování modelu na cíle
1. Ve stromové struktuře zvolte '1099 Model platby'.
2. Klikněte na možnost Návrhář.
3. Klikněte na možnost Mapovat model na datový zdroj.

    Mapování Pro 1099 manuální import transakcí bylo definováno typem směru Do cílového umístění. To znamená, že bylo zadáno pro podporu importu dat a obsahuje nastavení pravidel, která definují, jakým způsobem se použije importovaný externí soubor uložený jako data abstraktního datového modelu k aktualizaci tabulek v aplikaci.  

4. Klikněte na možnost Návrhář.
5. Ve stromové struktuře rozbalte 'model: Datový model 1099 Platební model'.
6. Ve stromové struktuře rozbalte 'model: Datový model 1099 Platební model\Transakce: Seznam záznamů'.

    Všimněte si, že navržený model je zde prezentován jako prvek zdroje dat. Za běhu bude obsahovat data, která se importují z externího souboru. Bylo přidáno několik tabulek jako prvky zdroje dat, aby se zajistilo, že importovaná data budou ve shodě s daty aktuální aplikace, včetně dostupnosti účtu dodavatele importující transakce v systému, existence importujících kódů země a státu atd.  

7. Ve stromové struktuře zvolte model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.
8. Klikněte na položku Upravit.
9. Klikněte na možnost Upravit vzorec.

    Nepodaří-li se alespoň jedno ověření pro jedinou importovanou transakci, tato transakce se označí jako nezdařená pomocí atributu zdroje dat ‘$failed’.  

10. Zavřete stránku.
11. Klikněte na možnost Zrušit.
12. Ve stromové struktuře zvolte 'tax1099trans: Záznamy tabulky 'VendSettlementTax1099'= model.Ověřeno'.
13. Klikněte na možnost Upravit cíl.

    Tento cíl ER byl přidán k určení způsobu, jakým importovaná data aktualizují tabulky aplikace. V takovém případě byla zvolena tabulka dat VendSettlementTax1099. Vzhledem k tomu, že byla vybrána akce záznamu Vložit, budou importované transakce vloženy do tabulky VendSettlementTax1099. Pamatujte, že jediné mapování modelu může obsahovat několik cílů. To znamená, že importovaná data lze použít k aktualizaci několika tabulek aplikace současně. Tabulky, zobrazení a datové entity lze použít jako ER cíle.   

    Pokud bude mapování voláno z bodu v aplikaci (např. tlačítko nebo položka nabídky), který byl speciálně pro tuto akci určen, cíl ER je nutné označit jako bod integrace. V tomto příkladu se jedná o bod ERTableDestination VendSettlementTax1099.  

14. Klikněte na možnost Zrušit.
15. Klikněte na možnost Zobrazit vše.
16. Klikněte na možnost Zobrazit pouze mapované.
17. Ve stromové struktuře rozbalte 'tax1099trans: Záznamy tabulky 'VendSettlementTax1099'= model.Ověřeno'.

    Všimněte se, že prvek zdroje dat obsahující pouze ověřené transakce, je navázán na vytvořený cíl. Importované transakce můžete filtrovat, abyste vynechali ty, které nejsou kompatibilní s daty aplikace.  

18. Ve stromové struktuře zvolte 'failed: Záznamy tabulky 'VendSettlementTax1099Entity'= model.selhal'.
19. Klikněte na kartu Ověření.

    Toto mapování modelu může obsahovat uživatelem definovanou logiku k ověření správnosti importovaných dat z existujících dat aplikace. Například na základě aktuálního nastavení se pro jakoukoliv transakci v importovaném souboru s účtem dodavatele, který není v systému, vygeneruje zpráva s upozorněním, která informuje uživatele a označuje nesprávný kód účtu dodavatele.  

    Všimněte si, že možnost Akce po schválení lze použít pro každé ověření, abyste specifikovali, zda postup importu má pokračovat nebo má být zastaven, stejně jako zda již provedená vložení/aktualizace mají být zachovány nebo vráceny.  

20. Klikněte na možnost Zobrazit pouze mapované.
21. Klikněte na možnost Zobrazit vše.
22. Zavřete stránku.

    Spusťte toto mapování modelu k vyzkoušení navrženého formátu a mapování modelu. Použijte soubor 1099entries.xml. Do systému se naimportují data z vybraného souboru.  

23. Klikněte na položku Spustit.

    Všimněte si, že dialogové okno neobsahuje žádné další otázky o mapování formátu, které musí být použity k analýze importovaného souboru a následnému přenosu dat do datového modelu. Je to proto, že existuje aktuálně pouze jeden formát, který používá tento model, označený jako navržený k podpoře importu dat.  
    
    Definujte ID dokladu k odlišení importovaných transakcí od ostatních transakcí, které již možná byly zadány ručně nebo byly naimportovány.  

24. V poli Zadat ID dokladu zadejte 'IMPORT-001'.

    Vyhledejte soubor '1099entries.xml'.  

25. Klikněte na tlačítko OK.

    Seznam vygenerovaných upozornění obsahuje informace o nesprávných účtech dodavatelů, o nesprávném kódu pole ve formuláři 1099, chybějících kódech země atd. Porovnejte seznam upozornění s obsahem, který je zahrnut ve spouštěcím XML souboru.  

26. Zavřete stránku.
27. Zavřete stránku.
28. Zavřete stránku.
29. Zavřete stránku.
30. Přejděte na Závazky > Pravidelné úlohy > Daň 1099 > Vyrovnání dodavatele pro sestavy 1099.

    Tento formulář zobrazuje kumulativní transakce v tabulce Tax1099Summary, které byla vytvořena na základě importovaných transakcí.  

31. V poli Datum od nastavte datum a čas na „2000-01-01“ .
32. Klikněte na možnost Ruční transakce 1099.

    Tento formulář obsahuje seznam transakcí, které byly přidány ručně a ty, které jsme právě naimportovali.  

33. Otevřete filtrování sloupce Doklad.
34. Zadejte hodnotu filtru „IMPORT-001“ v poli „Doklad“ za použití operátoru filtru „začíná na“.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Zobrazit vztah mezi mapováním modelu a formátu
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
4. Klikněte na Konfigurace výkaznictví.
5. Ve stromové struktuře zvolte '1099 Model platby'.

    Předpokládejme, že chcete podporovat import stejných dat, ale z formátu souboru .TXT.   

6. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno. 
7. V poli Nový zadejte 'Formát založený na datovém modelu 1099 Model platby'.
8. Do pole Název zadejte 'Importovat data ze souboru .TXT'.
9. Vyberte možnost Ano v poli Podporuje import dat.
10. Klepněte na možnost Vytvořit konfiguraci.
11. Klikněte na možnost Návrhář.
12. Klikněte na Mapovat formát na model.
13. Klikněte na položku Nová.
14. V poli Definice zadejte nebo vyberte hodnotu.

    Vyberte možnost '1099-MISC'.  

15. Do pole Název zadejte 'Importovat data ze souboru .TXT'.
16. Do pole Popis zadejte 'Importovat data ze souboru .TXT'.
17. Klikněte na položku Uložit.
18. Zavřete stránku.
19. Zavřete stránku.
20. Klikněte na položku Upravit.

    Pokud jste nainstalovali opravy hotfix „KB 4012871 Podpora mapování německého modelu v oddělených konfiguracích se schopností určení různých druhů předpokladů pro jejich nasazení v různých verzích aplikace Dynamics 365 Finance” (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871), proveďte další krok „Zapnout příznak ‘Výchozí nastavení pro mapování modelu’” pro zadanou konfiguraci formátu. Jinak přejděte na následující krok.  

21. Vyberte možnost Ano v položce Výchozí pro pole mapování modelu.
22. Ve stromové struktuře zvolte '1099 Model platby'.
23. Klikněte na možnost Návrhář.
24. Klikněte na možnost Mapovat model na datový zdroj.
25. Klikněte na položku Spustit.

    Pokud jste nainstalovali opravy hotfix „KB 4012871 Podpora mapování německého modelu v oddělených konfiguracích se schopností určení různých druhů předpokladů pro jejich nasazení v různých verzích(https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), ve vyhledávacím poli vyberte upřednostňované mapování modelu. Pokud jste ještě nenainstalovali opravy hotfix, přejděte na další krok, protože mapování již bylo vybráno definicí výchozí konfigurace formátu.  
    
    Pokud jste ještě nenainstalovali opravy hotfix KB 4012871, pamatujte, že dialogové okno obsahuje další dotaz na mapování modelu, který se používá k analýze importovaného souboru. Data jsou pak přenesena z dialogového okna do data modelu. Nyní můžete zvolit, jaké mapování formátu musí být použito v závislosti na typu souboru, který chcete importovat.  
    
    Pokud chcete zavolat toto mapování modelu z bodu v aplikaci, který je speciálně navržen pro tuto akci, cíl ER a mapování formátu musí být označeno jako součást integrace.  

26. Klikněte na možnost Zrušit.
27. Zavřete stránku.
28. Zavřete stránku.


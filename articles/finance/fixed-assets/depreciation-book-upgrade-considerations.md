---
title: Přehled upgradu knihy odpisů
description: Tento článek popisuje aktuální funkce knihy v dlouhodobém majetku. Tato funkce je založena na dřívější funkcí oceňovacího modelu, která byla k dispozici ve starších verzích, ale obsahuje také všechny funkce, které byly dříve k dispozici jen v knihách odpisů.
author: moaamer
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 784ec32ae886ef7ea9342b085f893eeeec761961
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855484"
---
# <a name="depreciation-book-upgrade-overview"></a>Přehled upgradu knihy odpisů

[!include [banner](../includes/banner.md)]

Tento článek popisuje aktuální funkce knihy v dlouhodobém majetku. Tato funkce je založena na dřívější funkcí oceňovacího modelu, která byla k dispozici ve starších verzích, ale obsahuje také všechny funkce, které byly dříve k dispozici jen v knihách odpisů. Funkce modelu hodnoty a knihy odpisů byly sloučeny do jednoho konceptu, který je označován jako kniha. Funkce knihy vám umožňuje používat jedinou sadu stránek, dotazů a sestav pro všechny procesy dlouhodobého majetku vaší organizace. Tento článek obsahuje některé věci, které byste měli zvážit před upgradem. 

Proces upgradu přesune vaše existující nastavení a všechny existující transakce na novou účetní strukturu. Oceňovací modely zůstanou, jaké momentálně jsou, tedy jako knihy, které se účtují do hlavní knihy. Knihy odpisů budou přesunuty do knihy, která má možnost Zaúčtovat do hlavní knihy nastavenu na Ne. Názvy deníku knihy odpisů budou přesunuty do názvu deníku hlavní knihy s účtovací vrstvou nastavenou na Žádná. Transakce knihy odpisů budou přesunuty na transakce dlouhodobého majetku.

Před spuštěním upgradu dat byste se měli seznámit se dvěma možnostmi dostupnými pro upgradování řádku deníků knihy odpisů na transakční doklady a s číselnou řadou, která se bude používat pro řadu dokladů.

Možnost 1:  **číselné řady definované systémem** – výchozí možnost pro optimalizaci výkonu upgradu. Upgrade nebude používat systém číselných řad, ale namísto toho bude přidělovat doklady podle sad. Po upgradu bude vytvořena nová číselná řada s **další sadou čísel** odpovídajícím způsobem na základě upgradovaných transakcí. Použitá číselná řada bude ve výchozím nastavení ve formátu FADBUpgr\#\#\#\#\#\#\#\#\#. Při použití tohoto přístupu je k dispozici několik parametrů pro úpravu formátu:

-   **Kód číselné řady** – kód pro identifikaci číselné řady. Tento kód číselné řady nemůže existovat, protože bude vytvořen v upgradu.
    -   Název konstanty: **NumberSequenceDefaultCode**
    -   Výchozí hodnota: "FADBUpgr"
-   **Předpona** – hodnota řetězce konstanty, která bude použita jako předpony čísla dokladů.
    -   Název konstanty: **NumberSequenceDefaultParameterPrefix**
    -   Výchozí hodnota: "FADBUpgr"
-   **Délka alfanumerické řady** – délka alfanumerického segmentu číselné řady.
    -   Název konstanty: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Výchozí hodnota: 9
-   **Počáteční číslo** – první číslo pro použití v číselné řadě.
    -   Název konstanty: **NumberSequenceDefaultParameterStartNumber**
    -   Výchozí hodnota: 1

Možnost 2: **Existující uživatelem definovaná číselná řada** – tato možnost vám umožní definovat číselnou řadu, která má být použita pro upgrade. Zvažte použití této možnosti, pokud potřebujete pokročilou konfiguraci číselné řady. Pokud chcete použít číselnou řadu, je nutné změnit třídu pro upgrade ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans pomocí následujících informací

-   **Kód číselné řady** – kód číselné řady.
    -   Název konstanty: **NumberSequenceExistingCode**
    -   Výchozí hodnota: žádná výchozí hodnota, musíte aktualizovat na kód číselné řady.
-   **Sdílená číselná řada** – logická hodnota k identifikaci v rámci číselné řady. Pro sdílené číselné řady ve všech společnostech použijte hodnotu true a pro rozsah specifický pro společnost hodnotu false. Použijete-li false, číselná řada se zadaným názvem musí existovat v každé společnosti, která obsahuje transakce knihy odpisů. Sdílené číselné řady existují v každém oddílu obsahujícím transakce knihy odpisů.
    -   Název konstanty: **NumberSequenceExistingIsShared**
    -   Výchozí hodnota: true

Parametry jsou umístěny na začátku třídy ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

*//Určete preferovanou metodu přidělení dokladů* 
 *// true, pokud chcete použít existující kód číselné řady* 
 *// false, chcete-li použití číselnou řadu (výchozí) definovanou systémem* boolean const NumberSequenceUseExistingCode = false;  

*// Pokud použijete způsob definované systémem číselné řady, zadejte parametry pro číselnou řadu.*
 *// Vytvoří se nová číselná řada s těmito parametry.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Používáte-li přístup existující číselné řady, zadejte existující kód číselné řady..* 
 *// Přidělení dokladu půjde po řádcích existující číselné řady.* const str NumberSequenceExistingCode = ''; *// Zadejte identifikační kód pro číselnou řadu.* 
 *// true, pokud je sdílená určená číselné řada* 
 *// false, pokud je určená číselná řada podle společnosti* 
 *// Výchozí číselná řada definovaná systémem se použije, pokud nebude nalezen kód číselné řady se zadaným rozsahem.* const boolean NumberSequenceExistingIsShared = true; 

Znovu vytvořte projekt obsahující třídu po změně konstant. 

Používáte-li přístup generování číselné řady (možnost 1), bude při upgradu použito zpracování založené na sadě k přidělení čísel dokladů, jak je uvedeno v parametrech skriptu pro upgrade. Dále bude vytvořena nová číselná řadu se zadanými parametry po přidělení. 

Používáte-li přístup vytvoření vlastní existující číselné řady (možnost 2), upgrade dat zkontroluje, zda existuje číselná řada s se zadaným rozsahem v databázi pro každý oddíl a společnost s transakcemi knihy odpisů. Pokud existuje, bude při upgradu použito zpracování po řádcích k přidělení čísel dokladů podle číselné řady pomocí rámce číselné řady. Pokud číselná řada neexistuje se zadaným oborem, upgrade bude používat výchozí systémem definovaný přístup číselné řady pro přidělení čísel dokladů a vytvoří novou číselnou řadu se zadanými výchozími parametry po přidělení.

S každým přístupem bude skript pro upgrade dat používat také číselnou řadu pro pole **Řada dokladů** v nových názvech deníku hlavní knihy vytvořených pro dřívější názvy deníku knihy odpisů.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

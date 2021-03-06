---
title: Přehled upgradu knihy odpisů
description: V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek, oceňovací modely a knihy odpisů.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d42936a94e0f4d50ae227d760d5bee6e1e3a12e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826971"
---
# <a name="depreciation-book-upgrade-overview"></a>Přehled upgradu knihy odpisů

[!include [banner](../includes/banner.md)]

V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek - oceňovací modely a knihy odpisů. V aplikaci Microsoft Dynamics 365 for Operations (1611) byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho koncept, který je označován jako kniha. Toto téma obsahuje informace, které je třeba zvážit pro upgrade. 

Proces upgradu přesune vaše existující nastavení a všechny existující transakce na novou účetní strukturu. Oceňovací modely zůstanou, jaké momentálně jsou, tedy jako knihy, které se účtují do hlavní knihy. Knihy odpisů budou přesunuty do knihy, která má možnost **Zaúčtovat do hlavní knihy** nastavenu na **Ne**. Názvy deníku knihy odpisů budou přesunuty do názvu deníku hlavní knihy s účtovací vrstvou nastavenou na **Žádná**. Transakce knihy odpisů budou přesunuty na transakce dlouhodobého majetku. 

Před spuštěním upgradu dat byste se měli seznámit se dvěma možnostmi dostupnými pro upgradování řádku deníků knihy odpisů na transakční doklady a s číselnou řadou, která se bude používat pro řadu dokladů. 

Možnost 1:  **číselné řady definované systémem** – výchozí možnost pro optimalizaci výkonu upgradu. Upgrade nebude používat systém číselných řad, ale namísto toho bude přidělovat doklady podle sad. Po upgradu bude vytvořena nová číselná řada s **další sadou čísel** odpovídajícím způsobem na základě upgradovaných transakcí. Použitá číselná řada bude ve výchozím nastavení ve formátu FADBUpgr\#\#\#\#\#\#\#\#\#. Při použití tohoto přístupu je k dispozici několik parametrů pro úpravu formátu:

-   **Kód číselné řady** – kód pro identifikaci číselné řady. Tento kód číselné řady nemůže existovat, protože bude vytvořen v upgradu.
    -   Název konstanty: **NumberSequenceDefaultCode**
    -   Výchozí hodnota: "FADBUpgr"
-   **Předpona** – hodnota řetězce konstanty, která bude použita jako předpony čísla dokladů.
    -   Název konstanty: **NumberSequenceDefaultParameterPrefix**
    -   Výchozí hodnota: "FADBUpgr"
-   **Délka alfanumerické řady** – délka alfanumerického segmentu číselné řady.
    -   Název konstanty: **NumberSequenceDefaultParameterAlpanumericLength **
    -   Výchozí hodnota: 9
-   **Počáteční číslo** – první číslo pro použití v číselné řadě.
    -   Název konstanty: **NumberSequenceDefaultParameterStartNumber  **
    -   Výchozí hodnota: 1

Možnost 2: **Existující uživatelem definovaná číselná řada** – tato možnost vám umožní definovat číselnou řadu, která má být použita pro upgrade. Zvažte použití této možnosti, pokud potřebujete pokročilou konfiguraci číselné řady. Pokud chcete použít číselnou řadu, je nutné změnit třídu pro upgrade ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans pomocí následujících informací

-   **Kód číselné řady** – kód číselné řady.
    -   Název konstanty: **NumberSequenceExistingCode **
    -   Výchozí hodnota: žádná výchozí hodnota, musíte aktualizovat na kód číselné řady.
-   **Sdílená číselná řada** – logická hodnota k identifikaci v rámci číselné řady. Pro sdílené číselné řady ve všech společnostech použijte hodnotu true a pro rozsah specifický pro společnost hodnotu false. Použijete-li false, číselná řada se zadaným názvem musí existovat v každé společnosti, která obsahuje transakce knihy odpisů. Sdílené číselné řady existují v každém oddílu obsahujícím transakce knihy odpisů.
    -   Název konstanty: **NumberSequenceExistingIsShared **
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
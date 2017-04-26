---
title: "Inovace – Přehled knihy odpisů"
description: "V předchozích verzích byly dvě koncepce oceňování dlouhodobého majetku - oceňovací modely a knihy odpisů. V aplikaci Microsoft Dynamics 365 for Operations verze 1611 byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho koncept, který je označován jako kniha. Toto téma obsahuje informace, které je třeba zvážit pro upgrade."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Inovace – Přehled knihy odpisů

[!include[banner](../includes/banner.md)]


V předchozích verzích byly dvě koncepce oceňování dlouhodobého majetku - oceňovací modely a knihy odpisů. V aplikaci Microsoft Dynamics 365 for Operations verze 1611 byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho koncept, který je označován jako kniha. Toto téma obsahuje informace, které je třeba zvážit pro upgrade. 

Proces upgradu přesune vaše existující nastavení a všechny existující transakce na novou účetní strukturu. Oceňovací modely zůstanou, jaké momentálně jsou, tedy jako knihy, které se účtují do hlavní knihy. Knihy odpisů budou přesunuty do knihy, která má možnost **Zaúčtovat do hlavní knihy** nastavenu na **Ne**. Názvů deníku knihy odpisů budou přesunuty do názvu deníku hlavní knihy s účtovací vrstvou nastavena na **žádný**. Transakce knihy odpisů bude přesunut do transakce dlouhodobého majetku. 

Před spuštěním upgradu dat byste se měli seznámit se dvěma možnostmi dostupnými pro upgradování řádku deníků knihy odpisů na transakční doklady a s číselnou řadou, která se bude používat pro řadu dokladů. 

Možnost 1:  **číselné řady definované systémem** – výchozí možnost pro optimalizaci výkonu upgradu. Upgrade nebude používat systém číselných řad, ale namísto toho bude přidělovat doklady podle sad. Po upgradu, bude vytvořena nová Číselná řada s **další číslo nastavené** odpovídajícím způsobem na základě inovované transakcí. Ve výchozím nastavení, bude číselná řada používaná v FADBUpgr\#\#\#\#\#\#\#\#\# formátu. Jsou k dispozici při použití tohoto přístupu, nastavit formát několik parametrů:

-   **Kód číselné řady** – kód k identifikaci číselné řady. Tento kód číselné řady nemůže existovat, protože bude vytvořen po upgradu.
    -   Název konstanty: **NumberSequenceDefaultCode**
    -   Výchozí hodnota: "FADBUpgr"
-   **Předpona** – hodnota řetězce konstanty, která bude použita jako předpony čísla dokladů.
    -   Název konstanty: **NumberSequenceDefaultParameterPrefix**
    -   Výchozí hodnota: "FADBUpgr"
-   **Délka alfanumerické řady** – délka alfanumerického segmentu číselné řady.
    -   Název konstanty: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Výchozí hodnota: 9
-   **Počáteční číslo** – první číslo pro použití v číselné řadě.
    -   Název konstanty: ** NumberSequenceDefaultParameterStartNumber **
    -   Výchozí hodnota: 1

Možnost 2: **existující, uživatelem definované číselné řady** -tato volba vám umožní definovat číselné řady, který má být použit k inovaci. Zvažte tuto možnost, pokud potřebujete Upřesnit konfiguraci číselné řady. Chcete-li použít číselnou řadu, je třeba upravit upgrade třídy ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans s následujícími informacemi:

-   **Kód číselné řady** – kód číselné řady.
    -   Název konstanty: ** NumberSequenceExistingCode **
    -   Výchozí hodnota: žádná výchozí hodnota, musíte aktualizovat na kód číselné řady.
-   **Sdílená číselná řada** – logická hodnota k identifikaci v rámci číselné řady. Pro sdílené číselné řady ve všech společnostech použijte hodnotu true a pro rozsah specifický pro společnost hodnotu false. Při použití "false", číselná řada se zadaným názvem, musí existovat v každé firmě, která obsahuje transakce knihy odpisů. Sdílené číselné řady existují v každém oddílu, který obsahuje transakce knihy odpisů.
    -   Název konstanty: ** NumberSequenceExistingIsShared **
    -   Výchozí hodnota: true

Parametry jsou umístěny na začátku ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans třídy. 

*Zadat vhodnější přístup přidělení doklady*<ph id="t1">
</ph>*/ / true, pokud chcete použít existující kód číselné řady*<ph id="t2">
</ph>*/ / false, pokud máte v úmyslu použít číselnou řadu (výchozí) definované systémem* boolean const NumberSequenceUseExistingCode = false;  

*Pokud používáte přístup systémem definované číselné posloupnosti, zadejte příslušné parametry pro číselnou řadu. *<ph id="t3">
</ph>*/ / S těmito parametry budou vytvořeny nové číselné řady.* Const str NumberSequenceDefaultCode = "FADBUpgr"; Const str NumberSequenceDefaultParameterPrefix = "FADBUpgr"; Const int NumberSequenceDefaultParameterAlpanumericLength = 9; Const int NumberSequenceDefaultParameterStartNumber = 1;   

*Používáte-li existující číselné řady přístup, zadejte existující kód číselné řady. *<ph id="t4">
</ph>*/ / Doklad přidělení přejde po řádcích pro existující číselné řady.* Const str NumberSequenceExistingCode = "; */ / Zadejte obor existujícího kódu číselné řady*<ph id="t5">
</ph>*/ / true Pokud je sdílené určené číselné řady*<ph id="t6">
</ph>*/ / NEPRAVDA, je-li určené číselné řady pro společnost*<ph id="t7">
</ph>*/ / číselné řady definované systémem výchozí bude použit, pokud není nalezen kód číselné řady s zadaný obor.* const boolean NumberSequenceExistingIsShared = true; 

Znovu vytvořte projekt obsahující třídu po změně konstant. 

Při použití systémem generované číslo sekvenční přístup (možnost 1), použije inovace zpracování na sadu pro přidělení čísla dokladu tak, jak je uvedeno v parametrech skriptu upgradu. Také vytvoří novou číselnou řadu se zadanými parametry po přidělení. 

Používáte-li přístup vytvoření vlastní existující číselné řady (možnost 2), upgrade dat zkontroluje, zda existuje číselná řada s se zadaným rozsahem v databázi pro každý oddíl a společnost s transakcemi knihy odpisů. Pokud neexistuje, použije inovace pro přidělení čísla dokladu podle číselné řady pomocí číselné posloupnosti framework zpracování řádku na řádek. Pokud číselná řada neexistuje zadaný obor, inovace budou používat výchozí systémem definované číselné posloupnosti přístup pro přidělení čísla dokladu a vytvoří novou číselnou řadu s parametry zadané výchozí po přidělení.

S každým přístupem bude skript pro upgrade dat používat také číselnou řadu pro pole **Řada dokladů** v nových názvech deníku hlavní knihy vytvořených pro dřívější názvy deníku knihy odpisů.





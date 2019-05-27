---
title: Import konfigurací pro generování dokumentů s daty aplikace
description: K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1637ba59525f5f8bd9fe41a00c34eca90f7a2751
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544580"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Import konfigurací pro generování dokumentů s daty aplikace

[!include [task guide banner](../../includes/task-guide-banner.md)]

K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".

Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu. V tomto postupu naimportujete požadované konfigurace ER, které byly vytvořeny pro vzorovou společnost Litware, Inc., a poté je použijete k vygenerování elektronických dokumentů. Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF. Než začnete, stáhněte a uložte si soubory uvedené v tématu nápovědy „Generování elektronických dokumentů a aktualizace dat aplikací pomocí nástroje elektronického výkaznictví“ (generate-electronic-documents-update-application-data/). Soubory jsou Intrastat (model).xml, Intrastat (mapping).xml a Intrastat (format).xml.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.  
    * Tento postup ukazuje postup použití možností ER k dokončení aktualizace dat aplikace a vygenerování sestavy Intrastat. Podrobnosti o procesu vykazování jsou archivovány v tabulkách aplikace. V současné době se při aktivaci procesu vykazování Intrastat z formuláře Intrastat archivace provádí podle logiky naprogramované v existujícím zdrojovém kódu. V tomto postupu budete provádět konfiguraci podobné, avšak zjednodušené logiky aplikačních dat pomocí pouze systému ER. Ve zdrojovém kódu nebudou provedeny žádné změny.   

## <a name="import-er-configurations"></a>Import konfigurací ER
1. Klikněte na Konfigurace výkaznictví.
2. Klikněte na Směna.
3. Klikněte na Načíst ze souboru XML.
    * Importujte konfiguraci modelu ER, která obsahuje datový model, který je určen jako zdroj dat pro generování sestavy Intrastat. Později rozšíříte tuto definici datového modelu pro použití pro aktualizaci dat aplikace k archivování podrobných informací o procesu vykazování Intrastat.   
    * Klepněte na tlačítko Procházet a vyberte soubor Intrastat (model).xml.  
4. Klikněte na tlačítko OK.
5. Ve stromovém zobrazení vyberte Intrastat (modul).
6. Klikněte na možnost Návrhář.
7. Ve stromovém zobrazení rozbalte Pro odchozí dokument.
8. Ve stromovém zobrazení rozbalte For outgoing document\Transaction.
    * Zkontrolujte strukturu importovaného modelu dat. Všimněte si, že kořenová položka Pro odchozí dokument je definována tak, aby určila datový tok pro získání dat z aplikace a použila je jako zdroj dat pro vygenerování sestavy Intrastat. „Transakce (seznam záznamů)“ se používá jako reprezentace seznamu transakcí Intrastat, které je třeba uvést v sestavě. Vzhledem k tomu, že archivujete vykázané kódy komodity, jedinečný identifikátor jednoho kódu komodity „ID záznamu komodity (Int64)“ je zapotřebí pro tento datový tok.   
9. Zavřete stránku.
10. Klikněte na Směna.
11. Klikněte na Načíst ze souboru XML.
    * Importujte konfiguraci mapování ER určující tok dat pro získávání dat z aplikace a použijte ji pro vygenerování sestavy Intrastat. Později rozšíříte tuto definici mapování modelu pro získání dat ze sestavy Intrastat a jejich použití pro aktualizaci dat aplikace k archivování podrobných informací o procesu vykazování Intrastat.   
    * Klepněte na tlačítko Procházet a vyberte soubor Intrastat (mapping).xml.  
12. Klikněte na tlačítko OK.
13. Ve stromovém zobrazení rozbalte Intrastat (model).
14. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (mapping).
15. Klikněte na možnost Návrhář.
    * Všimněte si, že aktuální mapování modelu obsahuje v poli Směr hodnotu K modelu. To znamená, že toto mapování modelu bylo vytvořeno pro získávání dat z aplikace a jejich ukládání v datovém modelu.  
16. Klikněte na možnost Návrhář.
17. Ve stromu rozbalte Seznam.
18. Ve stromovém zobrazení rozbalte možnost Transakce = Seznam.
    * Zkontrolujte strukturu mapování modelu, které používá datový model filtrovaný na základě kořenové položky For outgoing document. Všimněte si, že přidaný datový zdroj List poskytuje přístup k požadovaným datům aplikace, což je seznam záznamů v tabulce Intrastat.  
19. Zavřete stránku.
20. Zavřete stránku.
21. Klikněte na Směna.
22. Klikněte na Načíst ze souboru XML.
    * Importujte konfiguraci formátu ER, která určuje rozložení sestavy Intrastat, a proces vyplnění dat do sestavy. Později rozšíříte tuto definici formátu pro vložení dat ze sestavy Intrastat do datového modelu a jejich použití pro aktualizaci dat aplikace k archivování podrobných informací o procesu vykazování Intrastat.   
    * Klepněte na tlačítko Procházet a vyberte soubor Intrastat (format).xml.  
23. Klikněte na tlačítko OK.
24. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).
25. Klikněte na možnost Návrhář.
26. Klikněte na Rozbalit/sbalit.
27. Ve stromovém zobrazení vyberte File\Declaration.
28. Klikněte na kartu Mapování.
29. Ve stromu vyberte Soubor.
    * Prohlédněte si strukturu formátu použitého k vygenerování sestavy Intrastat. Všimněte si, že je navržena k vygenerování souboru formátu XML vyplněním dat z datového modelu, které je založen na kořenové položce Pro odchozí dokument. Ověřte, že název vytvořeného souboru je definován ve formuláři dialogového okna uživatele (k tomu slouží zdroj dat fn).   
30. Zavřete stránku.


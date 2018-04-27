--- 
title: "Generování dokumentů s daty aplikace"
description: "K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 4 - úprava formátu)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5001adbc1c7fae96e94e7b31a64a5a04ba886dc8
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="generate-documents-with-application-data"></a>Generování dokumentů s daty aplikace

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 4: úprava formátu).



Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace. V rámci tohoto postupu můžete provést konfiguraci formátu ER a vygenerovat tak sestavu Intrastat a aktualizovat data aplikace pro archivaci podrobností o procesu vykazování.



Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF. Před zahájením se ujistěte, že kontext země pro společnost DEMF je BEL (Belgie).


## <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
2. Klikněte na kartu Číselné řady.
    * Při archivování podrobných informací o procesu vykazování Intrastat je nutné určit záznamy každého vytvořeného archivu. Tato akce vyžaduje konfiguraci zvláštní číselné řady.  
3. Vyberte referenci ID archivu Intrastat.
4. Zadejte hodnotu do pole Kód číselné řady.
    * V poli Kód číselné řady zadejte nebo vyberte hodnotu Fore_2’.  
5. Vyřešte změny v číselné řadě Číslo.
6. Klikněte na položku Uložit.
7. Zavřete stránku.

## <a name="run-modified-er-format"></a>Spuštění upraveného formátu ER
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Intrastat (model).
3. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).
4. Klikněte na položku Spustit.
5. Do pole Zadat název souboru zadejte intrastat2.xml.
    * intrastat2.xml  
6. Klikněte na tlačítko OK.

## <a name="review-er-format-executions-results"></a>Kontrola výsledků spuštění formátu ER
    * Prohlédněte si vygenerovaný soubor XML.  
1. Zavřete stránku.
2. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
    * Otevřete tento formulář s transakcemi Intrastat, které byly zahrnuty ve vygenerovaném elektronickém dokumentu.  
3. Klikněte na Archiv Intrastat.
    * Vzhledem k tomu, že aktivovaný formát ER nově obsahuje nastavení pro aktualizaci dat aplikace, podrobnosti dokončené sestavy Intrastat byly archivovány. Pomocí tohoto formuláře můžete zobrazit záznam záhlaví vytvořeného archivu.  
4. Klepněte na možnost Podrobnosti.
    * Pomocí tohoto formuláře můžete zobrazit podrobnosti k vytvořenému archivu.  
5. Zavřete stránku.
6. Zavřete stránku.
7. Zavřete stránku.



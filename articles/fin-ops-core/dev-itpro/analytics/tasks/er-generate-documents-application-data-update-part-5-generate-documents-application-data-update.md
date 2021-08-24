---
title: Generování dokumentů s daty aplikace
description: K dokončení kroků v tomto postupu musíte nejprve dokončit postup "ER Generování dokumentů s aktualizací dat aplikace (část 4 - úprava formátu)".
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0166e0afb542baea063f2d563e1eaeb0cdbfd6f62d77898fd9916afbeca90e48
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726230"
---
# <a name="generate-documents-that-have-application-data"></a>Generování dokumentů s daty aplikace

[!include [banner](../../includes/banner.md)]

K dokončení kroků v tomto postupu musíte nejprve dokončit postup "ER Generování dokumentů s aktualizací dat aplikace (část 4: úprava formátu)".



Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace. V rámci tohoto postupu můžete provést konfiguraci formátu ER a vygenerovat tak sestavu Intrastat a aktualizovat data aplikace pro archivaci podrobností o procesu vykazování.



Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF. Před zahájením se ujistěte, že kontext země pro společnost DEMF je BEL (Belgie).


## <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
2. Klikněte na kartu Číselné řady.

    Při archivování podrobných informací o procesu vykazování Intrastat je nutné určit záznamy každého vytvořeného archivu. Tato akce vyžaduje konfiguraci zvláštní číselné řady.  

3. Vyberte referenci 'ID archivu Intrastat'.
4. Zadejte hodnotu do pole Kód číselné řady.

    V poli 'Kód číselné řady' zadejte nebo vyberte hodnotu 'Fore_2’.  

5. Vyřešte změny v číselné řadě Číslo.
6. Klepněte na tlačítko Uložit.
7. Zavřete stránku.

## <a name="run-modified-er-format"></a>Spuštění upraveného formátu ER
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Intrastat (model).
3. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).
4. Klikněte na Spustit.
5. Do pole Zadat název souboru zadejte intrastat2.xml.
6. Klepněte na tlačítko OK.

## <a name="review-er-format-executions-results"></a>Kontrola výsledků spuštění formátu ER
Prohlédněte si vygenerovaný soubor XML.  
1. Zavřete stránku.
2. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.

    Otevřete tento formulář s transakcemi Intrastat, které byly zahrnuty ve vygenerovaném elektronickém dokumentu.  

3. Klikněte na Archiv Intrastat.

    Vzhledem k tomu, že aktivovaný formát ER nově obsahuje nastavení pro aktualizaci dat aplikace, podrobnosti dokončené sestavy Intrastat byly archivovány. Pomocí tohoto formuláře můžete zobrazit záznam záhlaví vytvořeného archivu.  

4. Klepněte na možnost Podrobnosti.

    Pomocí tohoto formuláře můžete zobrazit podrobnosti k vytvořenému archivu.  

5. Zavřete stránku.
6. Zavřete stránku.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
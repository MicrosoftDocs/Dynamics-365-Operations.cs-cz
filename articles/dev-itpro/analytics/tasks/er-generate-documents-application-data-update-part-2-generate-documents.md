--- 
title: "Generování dokumentů s aktualizací dat aplikace pro elektronické výkaznictví (ER)"
description: "K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 1 - konfigurace importování)."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c724ce3c39ed7097a5a842b44a095628dcdfa131
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Generování dokumentů s aktualizací dat aplikace pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 1: konfigurace importování).



Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu. V tomto postupu spustíte importovanou konfiguraci formátu ER vytvořenou pro vzorovou společnost Litware, Inc. k vygenerování elektronických dokumentů.



Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF. 



Před zahájením práce změňte kontext země společnosti DEMF z DEU (Německo) na BEL (Belgie). Klepněte na položku Správa organizace > Organizace > Právní entity a aktualizujte kód země na primární adrese právnické osoby DEMF. Restartujte aplikaci.


## <a name="run-imported-er-format"></a>Spuštění importovaného formátu ER
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Intrastat (model).
3. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).
4. Klikněte na položku Spustit.
    * Spusťte pracovní verzi konfigurace formátu ER pro vygenerování sestavy Intrastat.  
5. Do pole Zadat název souboru zadejte intrastat.xml.
    * Zadejte název souboru.  
6. Klikněte na tlačítko OK.
    * Prohlédněte si vygenerovaný soubor XML.  
7. Zavřete stránku.
8. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
    * Otevřením tohoto formuláře zobrazíte transakce Intrastat, které jsou zahrnuty ve vygenerovaném elektronickém dokumentu.  
9. Klikněte na Archiv Intrastat.
    * Vzhledem k tomu, že aktivovaný formát ER neobsahuje žádné nastavení pro aktualizaci dat aplikace, podrobnosti dokončené sestavy Intrastat nebyly archivovány.  
10. Zavřete stránku.
11. Zavřete stránku.


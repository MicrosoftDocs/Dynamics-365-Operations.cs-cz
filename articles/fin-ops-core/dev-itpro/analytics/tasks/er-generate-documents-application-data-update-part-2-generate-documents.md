---
title: Návrh konfigurací pro generování dokumentů s daty aplikace
description: Tento článek popisuje, jak navrhnout konfigurace elektronického výkaznictví (ER) ke generování elektronického dokumentu. (Část 1 - konfigurace importu).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290537"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Návrh konfigurací pro generování dokumentů s daty aplikace

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

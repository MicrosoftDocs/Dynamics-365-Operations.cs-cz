---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)
description: Tento článek popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 5)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
ms.openlocfilehash: 093bf93ef747279ee8213a3e3f16f140c6ba2426
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290897"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve formátu výstupy (část 4: Spustit formát)".

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Úprava formátu k vyplnění příloh do generování zpráv v binárním formátu
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.
3. Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".
4. Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".
5. Klikněte na možnost Návrhář.
    * Naplníte zprávu faktury v generování výstupu jako soubor XML s kódováním UNICODE.  
6. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
7. Ve stromovém zobrazení vyberte „Společné\Soubor“.
8. Do pole Název zadejte „Xml zpráva“.
    * Zpráva Xml  
9. Zadejte hodnotu UTF-8 do pole Kódování.
    * UTF-8  
10. Klikněte na tlačítko OK.
    * Konfigurace generování výstupu jako souboru ZIP.  
11. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
12. Ve stromovém zobrazení vyberte „Společné\Složka“.
13. Do pole Název zadejte „Výstup Zip“.
    * Výstup ZIP  
14. Klikněte na tlačítko OK.
15. Ve stromu vyberte 'Výstup Zip'.
    * Přidejte přílohy ke generujícímu souboru ZIP jako soubory s původními názvy a příponami.  
16. Klepnutím na možnost Přidat otevřete dialogové okno.
17. Ve stromovém zobrazení vyberte „Společné\Soubor“.
18. Do pole Název zadejte Připojený soubor.
    * Připojený soubor  
19. Klikněte na tlačítko OK.
20. Ve stromu vyberte 'Výstup Zip\Připojený soubor'.
21. Klepnutím na možnost Přidat otevřete dialogové okno.
22. Ve stromu vyberte 'Text\Base64'.
23. Klikněte na tlačítko OK.

## <a name="map-new-format-elements-to-data-model"></a>Mapování nových prvků formátu na prvky datového modelu
1. Klikněte na kartu Mapování.
2. Ve stromovém zobrazení rozbalte „model“.
3. Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.
4. Ve stromu vyberte 'Výstup Zip\Připojený soubor\Base64'.
5. Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.
6. Klikněte na možnost Vazba.
7. Ve stromu vyberte 'Výstup Zip\Připojený soubor'.
8. Klikněte na Upravit název souboru.
9. Ve stromovém zobrazení rozbalte „model“.
10. Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.
11. Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.
12. Klikněte na možnost Přidat datový zdroj.
13. Klepněte na tlačítko Uložit.
14. Zavřete stránku.
15. Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.
16. Klikněte na možnost Vazba.
17. Klikněte na položku Uložit.
18. Zavřete stránku.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Spuštění sestavy navržené pro vybranou fakturu
1. Klikněte na položku Spustit.
2. Rozbalte oddíl Záznamy k zahrnutí ().
3. Klepněte na tlačítko Filtr.
4. Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.
5. V poli Kritéria v poli Prodejní objednávka kritérií zadejte "Prodejní objednávka", zadejte číslo objednávky 000148.
    * 000148  
6. Klepněte na tlačítko OK.
7. Klepněte na tlačítko OK.
    * Prohlédněte si generovaný výstup. Všimněte si, že kromě zprávy s fakturou zprávy ve formátu je pro každou přílohu vytvořen jeden soubor. Soubory příloh jsou naplněny komprimovaným výstupem v binárním formátu.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

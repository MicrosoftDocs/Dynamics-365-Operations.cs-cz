---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví na použití souborů správy dokumentů ve výstupu ER. (část 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d437b31b8a55f345ebc3567bc8c6a2c5ecfd2eec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092509"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití souboru pro správu dokumentů ve výstupech formátu (část 3: Vytvoření formátu).

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Přidejte nezbytné přílohy pro prodejní objednávku z jedné faktury.
1. Přejděte na Pohledávky > Faktury > Otevřené faktury odběratele.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Faktura pomocí hodnoty „CIV-000148“.
    * CIV-000148  
3. Klikněte na odkaz pro vybranou fakturu.
    * CIV-000148  
4. Kliknutím přejdete na odkaz v poli Prodejní objednávka.
    * 000148  
5. V poli Řádky nebo záhlaví vyberte možnost Záhlaví.
    * Vyberte Záhlaví k označení, že to bude cíl pro přidání příloh.  
6. Klikněte na možnost Připojit.
    * Přidejte několik souborů jako přílohy k této prodejní objednávce. Použijte soubory typů dokumentů, které jsou podporovány správou dokumentů (s příponami DOCX, DPF, XML, JPG atd.). Vyhledejte a vyberte soubory k připojení a dalšímu zpracování se související fakturou v elektronické zprávě elektronického výkaznictví.  
7. Klikněte na položku Nová.
8. Klepněte na volby Soubor.
9. Klikněte na položku Nová.
10. Klepněte na volby Soubor.
11. Zavřete stránku.
12. Zavřete stránku.
13. Zavřete stránku.
14. Zavřete stránku.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Spuštění sestavy navržené pro vybranou fakturu
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.
3. Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".
4. Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".
5. Klikněte na položku Spustit.
6. Rozbalte oddíl Záznamy k zahrnutí ().
7. Klepněte na tlačítko Filtr.
8. Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.
9. Zadejte hodnotu 000148 do pole Kritéria.
    * V poli kritérií "Prodejní objednávka" zadejte číslo objednávky 000148.  
10. Klepněte na tlačítko OK.
11. Klepněte na tlačítko OK.
    * Prohlédněte si generovaný výstup. Všimněte si, že pro každou přílohu byl vytvořen jeden uzel XML. Obsah přílohy je naplněna do výstupu XML v textovém formátu MIME (base64).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
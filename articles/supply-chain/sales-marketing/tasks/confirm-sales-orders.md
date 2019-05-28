---
title: Potvrzení prodejních objednávek
description: Tento postup ukazuje postup potvrzení prodejních objednávek.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563987"
---
# <a name="confirm-sales-orders"></a>Potvrzení prodejních objednávek

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje postup potvrzení prodejních objednávek. Bude vám předvedeno, jak potvrdit jednu objednávku a více objednávek najednou. Tyto úkoly obvykle provádějí zpracovatelé prodejních objednávek. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Dříve než začnete, ověřte, že pro stejného odběratele existuje několik otevřených prodejních objednávek. V případě, že používáte data USMF, můžete použít odběratele US-027.


## <a name="confirm-a-single-sales-order"></a>Potvrzení jedné prodejní objednávky
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. V seznamu najděte a vyberte objednávku, kterou chcete potvrdit.
3. Kliknutím na odkaz na čísle prodejní objednávky otevřete vybranou objednávku.
4. V podokně akcí klikněte na možnost Prodej.
5. Klikněte na možnost Potvrdit prodejní objednávku.
6. Rozbalte nebo sbalte oddíl Parametry.
    * Ujistěte se, že je pole Zaúčtování – Ano aktivní.  
7. Nastavte možnost Tisk potvrzení na Ano.
    * Pole Zkontrolovat limit úvěru určuje metodu, která se používá k výpočtu zbývajícího úvěru zákazníka. Ve výchozím nastavení se zkopíruje ze stránky Parametry pohledávek. Pokud chcete kontrolu limitu úvěru přeskočit při potvrzení určité prodejní objednávky, nastavte možnost Zkontrolovat limitu úvěru na hodnotu Neomezeno. Je třeba si však uvědomit, že i když je toto pole je nastaveno na hodnotu Neomezeno, kontrola limitu úvěru bude i přesto provedena, pokud je v hlavních datech odběratele vybrána možnost Povinný limit úvěru.  
8. Klikněte na tlačítko OK.
9. Klepněte na tlačítko Ano.
10. Zavřete stránku.
11. V podokně akcí klikněte na Možnosti.
12. Klikněte na tlačítko Změnit zobrazení.
13. Klikněte na možnost Zobrazení záhlaví.
    * Při potvrzení objednávky je nastaven stav dokumentu na hodnotu Potvrzení.  
14. V podokně akcí klikněte na možnost Prodej.
15. Klikněte na možnost Prodejní objednávka – potvrzení.
16. Zavřete stránku.

## <a name="confirm-multiple-sales-orders-at-once"></a>Potvrzení více prodejních objednávek najednou
1. Přejděte do nabídky Prodej a marketing > Prodejní objednávky > Potvrzení objednávky > Potvrdit prodejní objednávku.
2. Klepněte na tlačítko Vybrat.
3. V seznamu na kartě Rozsah vyhledejte a vyberte záznam, který odkazuje na pole Účet odběratele.
4. V poli Kritéria kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V seznamu najděte a vyberte účet odběratele, který má více objednávek, které chcete hromadně potvrdit.
    * Pokud používáte data USMF, můžete vybrat účet US-027.  
6. Klikněte na tlačítko OK.
    * Karta Přehled zobrazuje seznam objednávek, které splňují kritéria dotazu. Tyto položky budou zahrnuty do potvrzení.  
    * Pole Souhrnná aktualizace pro určuje parametr, pomocí kterého se více objednávek shrne do jednoho potvrzovacího dokumentu. Ve výchozím nastavení je tato možnost zkopírována z nastavení Výchozí hodnoty souhrnné aktualizace na stránce Parametry pohledávek.  
7. V poli Souhrnná aktualizace pro vyberte možnost Objednávka.
    * Minimální parametry požadované k vytvoření souhrnných aktualizací jsou Účet faktury a Měna. To znamená, že souhrnné aktualizace, které mají jiné účty faktur a jiné měny, nejsou povoleny. Na stránce Parametry souhrnné aktualizace, která je přístupná prostřednictvím stránky Parametry pohledávek, lze nastavit další parametry.  
8. V poli Prodejní objednávka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. V seznamu vyberte číslo prodejní objednávky, která má být souhrnnou objednávkou.
10. Klikněte na možnost Uspořádat.
11. Klikněte na tlačítko OK.
12. Klikněte na tlačítko OK.


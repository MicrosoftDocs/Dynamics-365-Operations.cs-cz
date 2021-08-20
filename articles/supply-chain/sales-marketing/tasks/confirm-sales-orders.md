---
title: Potvrzení prodejních objednávek
description: Tento postup ukazuje postup potvrzení prodejních objednávek.
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac5217ecd74e3a8d4dd6a82112788a7aaba4698857cd5854eed1f8c91aa97e73
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779151"
---
# <a name="confirm-sales-orders"></a>Potvrzení prodejních objednávek

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje postup potvrzení prodejních objednávek. Bude vám předvedeno, jak potvrdit jednu objednávku a více objednávek najednou. Tyto úkoly obvykle provádějí zpracovatelé prodejních objednávek. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Dříve než začnete, ověřte, že pro stejného odběratele existuje několik otevřených prodejních objednávek. V případě, že používáte data USMF, můžete použít odběratele US-027.


## <a name="confirm-a-single-sales-order"></a>Potvrzení jedné prodejní objednávky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. V seznamu najděte a vyberte objednávku, kterou chcete potvrdit.
3. Kliknutím na odkaz na čísle prodejní objednávky otevřete vybranou objednávku.
4. V **podokně akcí** klikněte na možnost **Prodej**.
5. Klikněte na možnost **Potvrdit prodejní objednávku**.
6. Rozbalte sekci **Parametry**. Ujistěte se, zda je možnost **Zaúčtování** nastavena na hodnotu Ano.  
7. Nastavte možnost **Tisk potvrzení** na Ano. Pole **Zkontrolovat limit úvěru** určuje metodu, která se používá k výpočtu zbývajícího úvěru zákazníka. Ve výchozím nastavení se zkopíruje ze stránky Parametry pohledávek. Pokud chcete kontrolu limitu úvěru přeskočit při potvrzení určité prodejní objednávky, nastavte možnost **Zkontrolovat limitu úvěru** na hodnotu Neomezeno. Je třeba si však uvědomit, že i když je toto pole je nastaveno na hodnotu Neomezeno, kontrola limitu úvěru bude i přesto provedena, pokud je v hlavních datech odběratele vybrána možnost **Povinný limit úvěru**. 
8. Klikněte na tlačítko **OK**.
9. Klepněte na tlačítko **Ano**.
10. Zavřete stránku.
11. V **podokně akcí** klikněte na **Možnosti**.
12. Klikněte na tlačítko **Změnit zobrazení**.
13. Klikněte na možnost **Zobrazení záhlaví**. Při potvrzení objednávky je nastaven **Stav dokumentu** na hodnotu Potvrzení. 
14. V **podokně akcí** klikněte na možnost **Prodej**.
15. Klikněte na možnost **Prodejní objednávka – potvrzení**.
16. Zavřete stránku.

## <a name="confirm-multiple-sales-orders-at-once"></a>Potvrzení více prodejních objednávek najednou
1. Přejděte do nabídky **Prodej a marketing > Prodejní objednávky > Potvrzení objednávky > Potvrdit prodejní objednávku**.
2. Klepněte na tlačítko **Vybrat**.
3. V seznamu na kartě **Rozsah** vyhledejte a vyberte záznam, který odkazuje na pole **Účet odběratele**.
4. V poli **Kritéria** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V seznamu najděte a vyberte účet odběratele, který má více objednávek, které chcete hromadně potvrdit. Pokud používáte data USMF, můžete vybrat účet US-027.  
6. Klikněte na tlačítko **OK**.
    - Karta **Přehled** zobrazuje seznam objednávek, které splňují kritéria dotazu. Tyto položky budou zahrnuty do potvrzení.  
    - Pole **Souhrnná aktualizace pro** v sekci **Parametry** určuje parametr, pomocí kterého se více objednávek shrne do jednoho potvrzovacího dokumentu. Ve výchozím nastavení je tato možnost zkopírována z nastavení **Výchozí hodnoty souhrnné aktualizace** na stránce **Parametry pohledávek**.  
7. V poli **Souhrnná aktualizace pro** pro vyberte možnost Objednávka. Minimální parametry požadované k vytvoření souhrnných aktualizací jsou **Účet faktury** a **Měna**. To znamená, že souhrnné aktualizace, které mají jiné účty faktur a jiné měny, nejsou povoleny. Na stránce **Parametry souhrnné aktualizace**, která je přístupná prostřednictvím stránky **Parametry pohledávek**, lze nastavit další parametry. 
8. V poli **Prodejní objednávka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. V seznamu vyberte číslo prodejní objednávky, která má být souhrnnou objednávkou.
10. Klikněte na možnost **Uspořádat**.
11. Klikněte na tlačítko **OK**.
12. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
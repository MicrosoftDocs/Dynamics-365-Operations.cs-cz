---
title: Výpočet odpisů dlouhodobého majetku mezi právnickými osobami
description: Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769e271ec9bb202ca695e5430c79e66f7320838fdfd232bab7c72ce5816a7b05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744323"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Výpočet odpisů dlouhodobého majetku mezi právnickými osobami

[!include [banner](../../includes/banner.md)]

Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku. Tento postup ukazuje, jak nastavit a spustit proces pro více právnických osob. Využívá účetní role a ukázková data pro právnické osoby USMF.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Nastavení deníků spuštění odpisování napříč společností
1. Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.
2. Rozbalte část Návrhy dlouhodobého majetku.
3. Klepněte na možnost Přidat.
4. V poli Účtovací vrstva zadejte nebo vyberte hodnotu.
5. V poli Název deníku zadejte nebo vyberte hodnotu.
    * Opakujte nastavení deníku na stránce Parametry dlouhodobého majetku u každé právnické osoby.  

## <a name="depreciation-run"></a>Spuštění odpisu
1. Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.
2. V poli Účtovací vrstva zadejte nebo vyberte hodnotu.
    * Název deníku bude odvozen z parametrů dlouhodobého majetku. Lze změnit na tomto místě pro aktuální právnickou osobu.  
3. Do pole Do data zadejte datum.
    * Vyberte právnické osoby, které mají být zahrnuty do spuštění odpisů.  
    * V seznamu se zobrazí pouze právnické osoby s deníky nastavenými pro návrhy dlouhodobého majetku na stránce Parametry dlouhodobého majetku.  
4. Vyberte možnost Ano v poli Zaúčtovat deníky.
    * Filtrovací pole zahrnují dlouhodobý majetek, skupiny a knihy pro právnické osoby, které jsou vybrány pro toto spuštění odpisu.  
    * Ve výchozím nastavení je povolena možnost Dávkové zpracování. Pokud je tato možnost povolena, vytvoření a zaúčtování deníku odpisů se spustí na pozadí.  
5. Klikněte na Vytvoří deník.
6. Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
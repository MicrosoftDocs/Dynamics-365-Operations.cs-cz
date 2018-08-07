--- 
title: "Výpočet odpisů dlouhodobého majetku mezi právnickými osobami"
description: "Tento postup ukazuje, jak nastavit a spustit proces odpisování pro více právnických osob."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Výpočet odpisů dlouhodobého majetku mezi právnickými osobami

[!include [task guide banner](../../includes/task-guide-banner.md)]

Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku. Tento postup ukazuje, jak nastavit a spustit proces pro více právnických osob. Používá roli účetního.  

Tento záznam používá ukázkovou společnost USMF.


Kroky (16) Dílčí úlohy: Nastavte deníky spuštění odpisování napříč společností. 

1. Nejprve musíte nastavit deníky pro použití při spuštění odepisování napříč společností v každé právnické osoby. Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku. 
2. Rozbalte část Návrhy dlouhodobého majetku. 
3. Vytvořte záznam s názvem deníku, který má být použit pro každou účtovací vrstvu v právnické osobě. Pokud knihy neúčtují do hlavní knihy, pak s přidruženým deníkem zvolte možnost Žádná pro účtovací vrstvu. Klepněte na možnost Přidat. 
4. V poli Účtovací vrstva zadejte nebo vyberte hodnotu. 
5. V poli Název deníku zadejte nebo vyberte hodnotu. 
6. Opakujte nastavení deníku na stránce Parametry dlouhodobého majetku u každé právnické osoby. 

Dílčí úkol: Výpočet odpisu

1. Použijte stránku Vytvořit návrh odpisu ke spuštění odepisování mezi právnickými osobami. Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu. 
2. V poli Účtovací vrstva zadejte nebo vyberte hodnotu. 
3. Název deníku bude odvozen z parametrů dlouhodobého majetku. Lze změnit na tomto místě pro aktuální právnickou osobu. 
4. Do pole Do data zadejte datum. 
5. Vyberte právnické osoby, které mají být zahrnuty do spuštění odpisů. V seznamu se zobrazí pouze právnické osoby s deníky nastavenými pro návrhy dlouhodobého majetku na stránce Parametry dlouhodobého majetku. 
6. Když je povolena, možnost Zaúčtovat deníky automaticky zaúčtuje deníky odpisů, když jsou vytvořeny. Pokud není tato možnost zvolena, deníky se vytvoří, ale nebudou zaúčtovány, a proto je možné zkontrolovat podrobnosti před zaúčtováním. Vyberte možnost Ano v poli Zaúčtovat deníky. 
7. Filtrovací pole zahrnují dlouhodobý majetek, skupiny a knihy pro právnické osoby, které jsou vybrány pro toto spuštění odpisu. 
8. Ve výchozím nastavení je povolena možnost Dávkové zpracování. Pokud je tato možnost povolena, vytvoření a zaúčtování deníku odpisů se spustí na pozadí. 
9. Klikněte na Vytvoří deník. 
10. Musíte zobrazit deníky odpisů vytvořené v odpovídajících právnických osobách. Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.


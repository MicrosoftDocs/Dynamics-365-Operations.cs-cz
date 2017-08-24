--- 
title: " Vytváření skupin oprávnění POS"
description: "Tato procedura vysvětlí, jak vytvořit skupiny oprávnění POS."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b0c930e3722d1d0b1fff8efad7a785a153436b6d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-pos-permission-groups"></a> Vytváření skupin oprávnění POS

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vysvětlí, jak vytvořit skupiny oprávnění POS. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT. Tento úkol je určen pro roli Manažer maloobchodních operací.

1. Přejděte na Skupiny oprávnění.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID skupiny oprávnění POS.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte možnost Ano v poli Zobrazit časové záznamy.
    * Nyní můžete povolit nebo zakázat různá oprávnění pro skupinu oprávnění POS. U některých oprávnění můžete nastavit hodnotu, která se použije k vyhodnocení, zda může uživatel POS provést akci.  Tento průvodce úkolem povolí několik oprávnění, která můžete udělit pokladníkovi.  
6. Vyberte možnost Ano v poli Povolit vytvoření objednávky.
7. Vyberte možnost Ano v poli Povolit úpravu objednávky.
8. Vyberte možnost Ano v poli Povolit načtení objednávky.
9. Vyberte možnost Ano v poli Povolit změnu hesla.
10. Vyberte možnost Ano v poli Povolit uzavření bez zadání částky.
11. Klikněte na položku Uložit.
    * Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti.  
12. Zavřete stránku.
13. Přejděte na položku Úlohy.
    * Dále přiřadíme skupinu oprávnění POS úloze.  
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. Klikněte na možnost Upravit.
17. Rozbalte část Klasifikace úlohy.
18. V poli Skupina oprávnění POS zadejte nebo vyberte hodnotu.
    * Pozice všech pracovníků pro tuto úlohu budou používat toto nastavení skupiny oprávnění POS, pokud oprávnění POS pracovníků nebylo přepsáno na úrovni jejich pozice.  
19. Klikněte na položku Uložit.
    * Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti.  



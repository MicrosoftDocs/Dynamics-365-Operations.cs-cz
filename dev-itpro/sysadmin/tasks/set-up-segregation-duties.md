--- 
title: "Nastavení dělení zodpovědnosti"
description: "Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 2ab30f4326b627406f9a39d6c3203b181b67d68f
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-segregation-of-duties"></a>Nastavení dělení zodpovědnosti

[!include[task guide banner](../../includes/task-guide-banner.md)]

Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli. Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti. Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol. Chcete-li vytvořit pravidlo, proveďte následující postup. K dokončení postupu musíte být správce systému. K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT. 

1. Přejděte do nabídky Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
    * Zadejte název pravidla.  
4. V poli První funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte první zodpovědnost, která se řídí pravidlem.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Druhé funkční oprávnění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte druhou zodpovědnost, která se řídí pravidlem.  
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Vyberte možnost v poli Závažnost.
    * Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.  
11. Zadejte hodnotu do pole Riziko zabezpečení.
    * Zadejte popis rizika zabezpečení.  
12. Zadejte hodnotu do pole Snížení rizika zabezpečení.
    * Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení. Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.  
13. Klikněte na položku Uložit.



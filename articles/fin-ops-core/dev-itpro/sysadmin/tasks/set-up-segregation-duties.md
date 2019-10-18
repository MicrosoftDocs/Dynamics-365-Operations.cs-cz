---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40b40b77877680e28671b7a15ea8c8b58ce94417
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180868"
---
# <a name="set-up-segregation-of-duties"></a>Nastavení dělení zodpovědnosti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli. Tento koncept se nazývá dělení zodpovědnosti. Nemusí být vhodné například, aby stejná osoba prováděla potvrzení příjmu zboží a zpracování platby dodavateli. Dělení zodpovědnosti pomáhá snížit riziko podvodu a rovněž pomáhá zjistit chyby a nesrovnalosti. Můžete také dělení zodpovědnosti použít k vynucení zásad interních kontrol. Chcete-li vytvořit pravidlo, proveďte následující postup. K dokončení postupu musíte být správce systému. K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT. 

1. Přejděte do nabídky **Podokno navigace > Správa systému > Zabezpečení > Dělení zodpovědnosti > Pravidla dělení zodpovědnosti.**
2. Klepněte na možnost **Nový**.
3. Do pole **Název** zadejte hodnotu pravidla.
4. V poli **První funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte první zodpovědnost, která se řídí pravidlem.
6. V poli **Druhé funkční oprávnění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. 
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte druhou zodpovědnost, která se řídí pravidlem.
10. Vyberte možnost v poli **Závažnost**. Vyberte závažnost rizika, ke kterému dochází, když stejný uživatel nebo role provádí obě zodpovědnosti.  
11. Zadejte hodnotu do pole **Riziko zabezpečení**. Zadejte popis rizika zabezpečení.  
12. Zadejte hodnotu do pole **Snížení rizika zabezpečení**. Zadejte popis akcí, které budete provádět pro snížení rizika zabezpečení. Můžete například snížit riziko provedením podrobnějších kontrol procesu, prováděním měsíčních manažerských kontrol nebo sdílením prostředků se jinými odděleními.     
13. Klikněte na možnost **Uložit**.


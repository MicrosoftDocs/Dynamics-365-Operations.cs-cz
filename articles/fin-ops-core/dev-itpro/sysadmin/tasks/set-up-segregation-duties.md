---
title: Nastavení dělení zodpovědnosti
description: Můžete nastavit pravidla k oddělení úkolů, které musí být prováděny různými uživateli.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688166"
---
# <a name="set-up-segregation-of-duties"></a>Nastavení dělení zodpovědnosti

[!include [banner](../../includes/banner.md)]

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


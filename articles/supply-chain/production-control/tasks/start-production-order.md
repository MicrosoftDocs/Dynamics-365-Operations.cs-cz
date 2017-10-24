--- 
title: "Spuštění výrobní zakázky"
description: "Tento postup ukazuje, jak začít výrobní zakázku v dílenském řízení."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33558053d33d9fe4a2ecb3576da569b2c441db80
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="start-a-production-order"></a>Spuštění výrobní zakázky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak začít výrobní zakázku v dílenském řízení. V tomto procesu je uveden čas a spotřeba materiálu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o pátou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.


## <a name="start-a-production-order"></a>Spuštění výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
    * Vyberte výrobní zakázku, která má stav Vydáno.  
2. V podokně akcí klikněte na položku Výrobní zakázka.
3. Klikněte na položku Spustit.
    * Na této stránce můžete potvrdit zahájení výrobní zakázky.  
4. Klikněte na záložku Obecné.
5. Zadejte číslo „10“ do pole Č. pole zadejte 10.
6. V poli Automatická spotřeba postupu vyberte hodnotu „Vždy“.
7. Zaškrtněte pole Zaúčtovat kartu postupu karty postupu.
8. V poli Automatická spotřeba kusovníku vyberte hodnotu „Vždy“.
9. Klepněte na zaškrtávací pole Zaúčtovat výdejku.
10. Klepněte na zaškrtávací pole Tisk výdejky.
11. Klikněte na tlačítko OK.
    * Toto je vytištěná výdejku zobrazující materiály použité pro výrobní zakázku.  
12. Zavřete stránku.

## <a name="validate-the-picking-list"></a>Ověření výdejky
1. V podokně akcí klikněte na možnost Zobrazit.
2. Klepněte na Výdejka.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Klikněte na položku Upravit.
6. Zadejte číslo do pole Spotřeba.
7. Klikněte na položku Zaúčtovat.
8. Klikněte na tlačítko OK.
    * V deníku výdejek jsou zaúčtovány materiály spotřebovány výrobní zakázkou. Před zaúčtováním deníku můžete provádět úpravy, pokud existuje rozdíl mezi odhadovaným množstvím a skutečným spotřebovaným množstvím.  
9. Klepněte na kartu panel mřížky.
10. Zavřete stránku.

## <a name="verify-the-route-card-journal"></a>Ověření deníku karet postupů
1. V podokně akcí klikněte na možnost Zobrazit.
2. Klepněte na Karta postupu.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Klikněte na položku Upravit.
6. Do pole Hodiny zadejte číslo.
7. Klikněte na položku Zaúčtovat.
8. Klikněte na tlačítko OK.
    * V deníku karet postupu je zaznamenáván čas strávený na jednotlivých operacích. Může být rovněž uvedeno dobré a chybné množství.  



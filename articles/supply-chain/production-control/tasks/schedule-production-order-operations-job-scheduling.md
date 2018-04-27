--- 
title: "Naplánování výrobní zakázky s naplánováním operací a úloh"
description: "Tento postup je zaměřen na plánování výrobní zakázky pomocí plánování operací a úloh."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Naplánování výrobní zakázky s naplánováním operací a úloh

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup je zaměřen na plánování výrobní zakázky pomocí plánování operací a úloh. Žádné úlohy se při plánování operací nevytváří, zatímco při plánování úloh se úlohy vytváří. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento postup je určen pro vedoucí výroby, výrobní plánovače nebo dílenského vedoucího pracujícího v samostatném výrobním prostředí.


## <a name="create-a-production-order"></a>Vytvoření výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
2. Klikněte na možnost Nová výrobní zakázka.
3. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Vyberte číslo položky D0001.  
4. Klikněte na položku Vytvořit.

## <a name="schedule-operations-for-the-production-order"></a>Naplánování operací pro výrobní zakázku
1. Označte v seznamu vybraný řádek.
    * Vyberte výrobní zakázku, kterou jste právě vytvořili. Měla by být v horní části seznamu.      
2. V podokně akcí klikněte na možnost Plán.
3. Klikněte na Plánovat operace.
4. V poli Způsob plánování vyberte „Dopředu od data plánování“.
5. Do pole Datum plánování zadejte datum.
    * Vyberte budoucí datum (například dnešní datum plus jeden týden). Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.  
6. Klikněte na tlačítko OK.
7. Označte v seznamu vybraný řádek.
    * Všimněte si, že se stav změní na Plánováno.  
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klikněte na Všechny úlohy.
    * Všimněte si, že se nevytvoří žádné úlohy při plánování operací.  
10. Zavřete stránku.

## <a name="schedule-jobs-for-the-production-order"></a>Naplánování úloh pro výrobní zakázku
1. V podokně akcí klikněte na možnost Plán.
2. Klikněte na Plánovat úlohy.
3. V poli Způsob plánování vyberte „Dopředu od data plánování“.
4. Do pole Datum plánování zadejte datum.
    * Vyberte budoucí datum (například dnešní datum plus jeden týden). Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.  
5. Klikněte na tlačítko OK.
6. V podokně akcí klikněte na položku Výrobní zakázka.
7. Klikněte na Všechny úlohy.
    * Všimněte si, že na základě aktivní trasy je vytvořeno 5 úloh s plánováním úlohy.  



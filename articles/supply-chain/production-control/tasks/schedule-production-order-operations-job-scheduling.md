---
title: Naplánování výrobní zakázky s naplánováním operací a úloh
description: Toto téma je zaměřeno na plánování výrobní zakázky pomocí plánování operací a úloh.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c27611d7b0c8e4e180ff14d1bd1ca8e36bc82d79d3849494e4de44202bd642b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774023"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Naplánování výrobní zakázky s naplánováním operací a úloh

[!include [banner](../../includes/banner.md)]

Toto téma je zaměřeno na plánování výrobní zakázky pomocí plánování operací a úloh. Žádné úlohy se při plánování operací nevytváří, zatímco při plánování úloh se úlohy vytváří. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento postup je určen pro vedoucí výroby, výrobní plánovače nebo dílenského vedoucího pracujícího v samostatném výrobním prostředí.


## <a name="create-a-production-order"></a>Vytvoření výrobní zakázky
1. V navigačním podokně přejděte na **Moduly > Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky**.
2. Vyberte **Nová výrobní zakázka**.
3. V poli **Číslo položky** zadejte nebo vyberte hodnotu. Vyberte číslo položky **D0001**.  
4. Vyberte **Vytvořit**.

## <a name="schedule-operations-for-the-production-order"></a>Naplánování operací pro výrobní zakázku
1. Označte nově vytvořený řádek.      
2. V podokně akcí vyberte možnost **Plánovat**.
3. Vyberte **Plánovat operace**.
4. V poli **Způsob plánování** vyberte **Dopředu od data plánování**.
5. Do pole **Datum plánování** zadejte datum. Vyberte budoucí datum (například dnešní datum plus jeden týden). Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.  
6. Vyberte **OK**.
7. Označte na seznamu vybraný řádek. Všimněte si, že se stav změní na **Plánováno**. 
8. Vyberte **Všechny úlohy**. Všimněte si, že se nevytvoří žádné úlohy při plánování operací.  
9. Zavřete stránku.

## <a name="schedule-jobs-for-the-production-order"></a>Naplánování úloh pro výrobní zakázku
1. V podokně akcí vyberte možnost **Plánovat**.
2. Vyberte **Plánovat úlohy**.
3. V poli **Způsob plánování** vyberte **Dopředu od data plánování**.
4. Do pole **Datum plánování** zadejte datum. Vyberte budoucí datum (například dnešní datum plus jeden týden). Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.  
5. Vyberte **OK**.
6. V podokně akcí vyberte možnost **Výrobní zakázka**.
7. Vyberte **Všechny úlohy**. Všimněte si, že na základě aktivní trasy je vytvořeno 5 úloh s plánováním úlohy.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
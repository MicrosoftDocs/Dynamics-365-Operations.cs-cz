---
title: Nastavení číselných řad pomocí průvodce
description: Toto téma popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca8174444d5a84f7efb402d6efc787e693801e82
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694732"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Nastavení číselných řad pomocí průvodce

[!include [banner](../../includes/banner.md)]

Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují. Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz. Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem. Toto téma popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte na **Navigace > Moduly > Správa organizace > Číselné řady > Číselné řady**.
2. Vyberte **Generovat**.
3. Zvolte **Další**.

   - Na této stránce můžete upravit identifikační kód, nejnižší hodnotu a nejvyšší hodnotu. Kromě toho můžete určit, zda musí být číselné řady souvislé.   
   - Nevybírejte možnost **Souvislá**, pokud musíte předem přidělit čísla pro číselnou řadu. Chcete-li přidat rozsah segmentu do formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost **Zahrnout obor do formátu**. Chcete-li odebrat rozsah segmentu z formátu číselné řady, vyberte formát v seznamu a potom vyberte možnost **Odebrat obor z formátu**. Chcete-li vyloučit číselnou řadu z automatického generování, vyberte číselnou řadu v seznamu a potom vyberte **Odstranit**.  

4. Zvolte **Další**.
5. Vyberte **Dokončit**.


---
title: Nastavení číselných řad pomocí průvodce
description: Tento článek popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.
author: SunilGarg
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cae739aad1166eee1abebe3c0adc7939bca55bc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847056"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Nastavení číselných řad pomocí průvodce

[!include [banner](../../includes/banner.md)]

Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují. Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz. Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem. Tento článek popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte na **Navigace > Moduly > Správa organizace > Číselné řady > Číselné řady**.
2. Vyberte **Generovat**.
3. Zvolte **Další**.

   - Na této stránce můžete upravit identifikační kód, nejnižší hodnotu a nejvyšší hodnotu. Kromě toho můžete určit, zda musí být číselné řady souvislé.   
   - Nevybírejte možnost **Souvislá**, pokud musíte předem přidělit čísla pro číselnou řadu. Chcete-li přidat rozsah segmentu do formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost **Zahrnout obor do formátu**. Chcete-li odebrat rozsah segmentu z formátu číselné řady, vyberte formát v seznamu a potom vyberte možnost **Odebrat obor z formátu**. Chcete-li vyloučit číselnou řadu z automatického generování, vyberte číselnou řadu v seznamu a potom vyberte **Odstranit**.  

4. Zvolte **Další**.
5. Vyberte **Dokončit**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

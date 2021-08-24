---
title: Reset zablokovaných dávkových úloh
description: Toto téma vysvětluje, jak vyřešit problémy s dávkovými úlohami, které se zasekly.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: c8b80406991bab6ba87fc8e38b9e49391921d98df5dbf223561848157f8f419d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738336"
---
# <a name="reset-stuck-batch-jobs"></a>Reset zablokovaných dávkových úloh

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Výdej

V aplikaci Microsoft Dynamics 365 Human Resources může dojít k problémům s dávkovými úlohami, které se zasekly v jednom ze stavů **Provádění** nebo **Ruší se** a nedokončí se.

## <a name="resolution"></a>Řešení

Když je dávková úloha zaseknutá ve stavu **Provádění** nebo **Ruší se**, můžete stav resetovat vynuceným zrušením úlohy. Po zrušení můžete dávkovou úlohu resetovat nastavením na do stavu **Čekání**. Poté bude znovu vyzvednuta k provedení v příštím plánovaném běhu dávek.

1. V pracovním prostoru **Správa systému** vyberte stránku **Odkazy** a v ní vyberte **Dávkové úlohy**.

2. Na stránce se seznamem **Dávkové úlohy** vyberte úlohu, kterou je třeba resetovat.

3. Na pásu karet akcí vyberte **Vynutit zrušení** a akci potvrďte.

   > [!NOTE]
   > Akce **Vynutit zrušení** je k dispozici pouze pokud má vybraná dávková úloha stav buď **Provádění** nebo **Ruší se** a pro úlohu nejsou spuštěny žádné dávkové procesy spuštění nebo zrušení.

4. Na pásu karet akcí vyberte možnost **Změnit stav**.

5. Na stránce **Vyberte nový stav** vyberte **Čekání** a potom vyberte **OK**.

   ![Vyberte nový stav dávkové úlohy.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Viz také

[Optimalizace výkonu naplánováním dávkových úloh po hodinách](hr-admin-troubleshooting-batch-jobs.md)<br>
[Optimalizace výkonu pomocí úloh automatického vyčištění](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

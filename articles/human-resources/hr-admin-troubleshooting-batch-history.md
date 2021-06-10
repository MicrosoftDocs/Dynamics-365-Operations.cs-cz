---
title: Optimalizace výkonu pomocí úloh automatického vyčištění
description: V tomto článku je vysvětleno, jak vyřešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources vyčištěním historie dávkových úloh.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053484"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalizace výkonu pomocí úkolů automatického čištění

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Vydání**

Microsoft Dynamics 365 Human Resources může zaznamenat problémy s výkonem, pokud se historie dávkových úloh příliš zvětší.

**Příčina**

Dávkové úlohy, které běží často, mohou vést k neudržitelnému nárůstu historie dávkových úloh. To může způsobit problémy s výkonem. 

**Rozlišení**

Naplánování automatického úkolu vyčištění historie dávkových úloh Doporučujeme nastavit úlohu tak, aby se spouštěla týdně, ale v závislosti na daném prostředí může být nutné spustit vyčištění častěji nebo méně často. Následující postup obsahuje naše doporučená nastavení, ale lze je podle potřeby změnit.

1. V modulu Human Resources vyberte **Správa systému**.

2. Na panelu **Hledat** zadejte **Vyčištění historie dávkových úloh**.

   ![Vyhledejte vymazání historie dávkové úlohy](media/talent-batch-history-cleanup-search-bar.png)

3. V části **Limit historie (dny)** zadejte **30**.

   ![Nastavení limitu historie na 30](media/talent-batch-history-cleanup-history-limit.png)

4. Vyberte možnost **Spustit na pozadí** a vyberte **Opakování**.

   ![Nastavení opakování](media/talent-batch-history-cleanup-recurrence.png)

5. Ve skupinovém rámečku **definovat opakování** nastavte **Počáteční datum** a **Počáteční čas** mimo pracovní dobu nebo víkend a vyberte možnost **žáDNé DATUM UKONčENí**. 

   ![Definování počátečního data a času opakování](media/talent-batch-history-cleanup-define-recurrence.png)

6. Ve skupinovém rámečku **VZOREC OPAKOVáNí** vyberte **Dny** a nastavte **OPAKOVAT PO ZADANéM INTERVALU** na **7**.

   ![Nastavení čištění na týdenní opakování](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Vyberte **OK**.

8. V případě potřeby změňte všechny ostatní parametry v podnabídce **Spustit na pozadí** a pak vyberte **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
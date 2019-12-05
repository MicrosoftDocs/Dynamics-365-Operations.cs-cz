---
title: Optimalizace výkonu pomocí úkolů automatického čištění
description: V tomto tématu je vysvětleno, jak vyřešit některé problémy s aplikací Microsoft Dynamics 365 Talent vyčištěním historie dávkových úloh.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832575"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalizace výkonu pomocí úkolů automatického čištění

[!include [banner](includes/banner.md)]

**Vydání**

Microsoft Dynamics 365 Talent může zaznamenat problémy s výkonem, pokud se historie dávkových úloh příliš zvětší.

**Příčina**

Dávkové úlohy, které běží často, mohou vést k neudržitelnému nárůstu historie dávkových úloh. To může způsobit problémy s výkonem. 

**Rozlišení**

Naplánování automatického úkolu vyčištění historie dávkových úloh Doporučujeme nastavit úlohu tak, aby se spouštěla týdně, ale v závislosti na daném prostředí může být nutné spustit vyčištění častěji nebo méně často. Následující postup obsahuje naše doporučená nastavení, ale lze je podle potřeby změnit.

1. V aplikaci Talent vyberte možnost **Správa systému**.

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


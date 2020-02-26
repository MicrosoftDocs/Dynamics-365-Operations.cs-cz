---
title: Optimalizace výkonu pomocí úloh automatického vyčištění
description: V tomto článku je vysvětleno, jak vyřešit některé problémy s aplikací Microsoft Dynamics 365 Human Resources vyčištěním historie dávkových úloh.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008315"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalizace výkonu pomocí úkolů automatického čištění

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


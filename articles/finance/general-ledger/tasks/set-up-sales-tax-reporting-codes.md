---
title: Nastavit kódy vykazování DPH
description: Kódy vykazování DPH odkazují na číslo pole uvedené v sestavě DPH.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646174"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Nastavit kódy vykazování DPH

[!include [banner](../../includes/banner.md)]

Kódy vykazování DPH odkazují na číslo pole uvedené v sestavě DPH. Používají se na rozložení sestavy specifickém pro zemi. Používají se také v sestavě platby DPH podle kódu. Tato sestava zobrazuje částky daně z obratu za období vypořádání shrnuté pro každý kód vykazování. Jakmile vytvoříte kódy vykazování DPH, můžete na ně odkazovat na pevných záložkách Nastavení sestavy, k nimž přejdete ze stránky **Kódy DPH**. 

Tento záznam používá ukázkovou společnost DEMF.

1. V **Navigačním podokně** přejděte na **Daň > Nepřímé daně > DPH > Kódy vykazování DPH**.
2. Klepněte na možnost **Nový**.
3. Vyberte rozvržení sestavy, do které patří kód vykazování. Toto rozvržení slouží k filtrování dostupných kódů vykazování pro kód DPH. Každý kód DPH patří do období vyrovnání, které patří finančnímu úřadu používajícímu rozvržení sestavy.  
4. Zadejte číslo do pole **Kód vykazování-**.
5. V poli **Text sestavy** zadejte popis, který se zobrazí v sestavách.
6. V poli **Stručný popis** zadejte popis pro interní účely.
7. Klikněte na možnost **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
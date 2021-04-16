---
title: Nastavit kódy vykazování DPH
description: Kódy vykazování DPH odkazují na číslo pole uvedené v sestavě DPH.
author: twheeloc
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e040bac6ef9e950e8d7f97e3c136636acf1fe43
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813524"
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
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222136"
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
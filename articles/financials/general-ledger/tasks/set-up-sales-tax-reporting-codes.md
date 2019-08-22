---
title: Nastavit kódy vykazování DPH
description: Kódy vykazování DPH odkazují na číslo pole v sestavě DPH.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 830a3465944b32cc17feee60e3cbc5ad0a4dc9d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834766"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Nastavit kódy vykazování DPH

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kódy vykazování DPH odkazují na číslo pole v sestavě DPH. Používají se na rozvržení sestav specifických podle země a platby DPH podle kódu sestavy pro tisk částek DPH za období vyrovnání sečtené podle kódu vykazování. Jakmile vytvoříte kódy vykazování DPH, můžete na ně odkázat kódy na pevné záložce Nastavení sestavy na stránce Kódy DPH. 

Tento záznam používá ukázkovou společnost DEMF.



1. Přejděte na Daň > Nastavení > DPH > Kódy vykazování DPH.
2. Klikněte na položku Nová.
3. Vyberte rozvržení sestavy, do které patří kód vykazování.
    * Toto rozvržení slouží k filtrování dostupných kódů vykazování pro kód DPH. Každý kód DPH patří do období vyrovnání, které patří finančnímu úřadu používajícímu rozvržení sestavy.  
4. Zadejte číslo, které odkazuje na pole v sestavě DPH.
5. V poli Text sestavy zadejte popis, který se zobrazí v sestavách.
6. V poli Stručný popis zadejte popis pro interní účely.
7. Klikněte na položku Uložit.


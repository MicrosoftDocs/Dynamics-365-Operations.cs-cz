---
title: Nastavení daňových úřadů
description: Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb0b30be91e33cb50af0ae5c2e4dcd75bd12599b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175329"
---
# <a name="set-up-sales-tax-authorities"></a>Nastavení daňových úřadů

[!include [task guide banner](../../includes/task-guide-banner.md)]

Finanční úřady jsou entity, pro které je třeba vykazovat a platit shromážděné DPH. Můžete finančnímu úřadu platit DPH přímo nebo prostřednictvím účtu dodavatele, který pro daný finanční úřad vytvoříte. Pokud to provedete, může společnost použít své obvyklé platební postupy, aby DPH odvedla finančnímu úřadu včas. Jestliže nenastavíte finanční úřad jako dodavatele, musí někdo připravit ruční platbu finančnímu úřadu k příslušnému datu splatnosti. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte na Daň > Nepřímé daně > DPH > Finanční úřady.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Úřad.
4. Zadejte hodnotu do pole Název.
5. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Vyberte rozvržení sestavy pro svou zemi či oblast (pokud je k dispozici). Jestliže rozvržení sestav neodpovídá požadavkům finančního úřadu, použijte výchozí rozvržení.
9. Zadejte hodnoty do formuláře a polí Zaokrouhlení a určete tak způsob zaokrouhlení celkové částky k úhradě. Rozdíly zaokrouhlení budou zaúčtovány v části Účty pro automatické transakce nastavené v hlavní knize.
10. V poli Zaokrouhlení zadejte číslo.
11. Klikněte na položku Uložit.

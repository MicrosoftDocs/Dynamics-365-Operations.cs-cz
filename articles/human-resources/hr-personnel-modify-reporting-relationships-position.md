---
title: Úprava vztahů podřízenosti pro určitou pozici
description: Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad7220661677ce72168d20903486230411ec00f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688517"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Úprava vztahů podřízenosti pro určitou pozici


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance. Vztah sestav lze použít pro směrování dokumentů prostřednictvím workflowu. Procedura také ukazuje postup přiřazení zaměstnance k dalším hierarchiím. Například zaměstnanec může být součástí projektového týmu s neformálním vykazováním vztahů k vedoucímu projektu. Další vztahy vykazování lze definovat na pozici pro různé scénáře projektu nebo matice. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte k nabídce **Lidské zdroje** \> **Pozice** \> **Pozice**.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat na hodnotě **000091** pro pole **Pozice**.
3. Vyberte odkaz na vybraném řádku v seznamu.
4. Rozbalte sekci **Sestavy pro umístění**.
5. Výběrem možnosti **Nové** otevřete rozevírací dialogové okno.
6. V poli **Nadřízená pozice** zadejte nebo vyberte hodnotu.
7. Vyberte **Vytvořit**.
8. Rozbalte oddíl **Vztahy**.
9. Vyberte **přidat**.
10. Zaškrtněte políčko po levé straně mřížky.
11. V poli **Název hierarchie** zadejte nebo vyberte hodnotu (např. **Projekt**).
12. V poli **Nadřízená pozice** zadejte nebo vyberte hodnotu. (Příklad: **000437**).
13. Zvolte možnost **Uložit**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

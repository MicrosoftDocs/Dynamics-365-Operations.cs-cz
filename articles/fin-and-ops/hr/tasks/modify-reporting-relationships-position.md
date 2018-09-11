--- 
title: "Úprava vztahů podřízenosti pro určitou pozici"
description: "Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance."
author: ShielaSogge
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4d8c82998e6b19adbd67b6b5ea3d68d2fbd08d8b
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a>Úprava vztahů podřízenosti pro určitou pozici

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance. Vztah sestav lze použít pro směrování dokumentů prostřednictvím workflowu. Procedura také ukazuje postup přiřazení zaměstnance k dalším hierarchiím. Například zaměstnanec může být součástí projektového týmu s neformálním vykazováním vztahů k vedoucímu projektu. Další vztahy vykazování lze definovat na pozici pro různé scénáře projektu nebo matice. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte k nabídce Lidské zdroje > Pozice > Pozice.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Pozice pomocí hodnoty „000091“.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Rozbalte pole Sestavy pro umístění oddílu.
5. Kliknutím na možnost Nový otevřete dialogové okno.
6. V poli Nadřízená pozice zadejte nebo vyberte hodnotu.
7. Klikněte na položku Vytvořit.
8. Rozbalte nebo sbalte oddíl Vztahy.
9. Klepněte na možnost Přidat.
10. Zaškrtněte políčko po levé straně mřížky.
11. V poli Název hierarchie zadejte nebo vyberte hodnotu.
    * Příklad: Projekt  
12. V poli Nadřízená pozice zadejte nebo vyberte hodnotu.  Příklad: 000437
13. Klikněte na položku Uložit.



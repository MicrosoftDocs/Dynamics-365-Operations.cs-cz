---
title: Úprava vztahů podřízenosti pro určitou pozici
description: Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae8ca5b20f331709e9fc1d9ae3b5f350e5c19ab
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430133"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Úprava vztahů podřízenosti pro určitou pozici



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


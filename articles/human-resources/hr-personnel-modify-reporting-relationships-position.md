---
title: Úprava vztahů podřízenosti pro určitou pozici
description: Tento postup popisuje, jak změnit vykazování vztahu pro určitého zaměstnance.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465383"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Úprava vztahů podřízenosti pro určitou pozici

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: "Stránka seznamu transakcí dodavatele"
description: "Toto téma obsahuje informace o stránce se seznamem transakcí dodavatele pro aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: cs-cz
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Stránka seznamu transakcí dodavatele

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Zobrazit vyrovnání

Karta **Zobrazit vyrovnání** v podokně akcí poskytuje rychlý přístup k historii vyrovnání a další informace o celé transakci vyrovnání. Můžete také zobrazit další transakce, které souvisejí s vybranou transakcí, ať už proto, že byly součástí stejného vyrovnání, nebo protože jsou to platby, které byly vytvořeny ve stejném deníku plateb.

1. Zvolte **Závazky \> Všichni dodavatelé**.
2. Vyberte dodavatele, který má transakce, a poté vyberte **Dodavatel \> Transakce**.
3. Vyberte transakci k prozkoumání.
4. Zvolte kartu **Zobrazit vyrovnání** v podokně akcí.

    Otevře se dialogové okno **Zobrazit vyrovnání** a zobrazí vybrané transakce a všechny doklady, proti kterým probíhá vyrovnání. Toto dialogové okno připomíná zobrazení historie vyrovnání, ale obsahuje všechny související dokumenty.

5. Z tohoto dialogového okna můžete provádět různé úkoly. Vyberte jeden nebo více dokladů a pak vyberte některou z následujících nabídek:

   - **Zobrazit účetnictví** – Zobrazí se všechny doklady, které souvisí se zvolenými dokumenty. Zvolte **Zavřít** a zavřete dialogové okno.
   - **Exportovat** – Exportujte vybrané doklady do aplikace Microsoft Excel.
   - **Zobrazit související platby** -Zobrazí se všechny transakce deníku plateb, které byly vytvořeny v deníku plateb souvisejícím se zvoleným dokumentem. Kromě toho se zobrazí všechna vyrovnání, která souvisejí s těmito platbami. Popisek této nabídky se změní také na **Zobrazit vyrovnání**. Vyberte **Zobrazit vyrovnání**, chcete-li zobrazit pouze transakce, které byly zobrazeny při prvním otevření dialogového okna **Zobrazit vyrovnání**.
    - **Vyrovnat transakce** – Tato nabídka se zobrazí v případě, že původní dokument, který byl vybrán, nebyl plně vyrovnán. Pokud ho zvolíte, zobrazí se dialogové okno **Vyrovnat transakce**, kde lze vybrat transakce pro vyrovnání.
    - **Zrušit vyrovnání** – Tato nabídka se zobrazí v případě, že původní dokument, který byl vybrán, byl plně vyrovnán. Pokud ho zvolíte, zobrazí se dialogové okno **Zrušit vyrovnání**, kde je možné zrušit vyrovnání, která byla vytvořena pro tento dokument.


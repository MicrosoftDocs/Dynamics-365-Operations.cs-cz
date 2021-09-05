---
title: Uložení průvodců záznamem úloh do LCS a jejich opětovné přehrání
description: Toto téma vysvětluje, jak uložit průvodce záznamem úloh do Microsoft Dynamics Lifecycle Services (LCS) a poté je opětovně přehrát.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fad014590abebf159b71227a44eb8df60bf05e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416874"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Uložení průvodců záznamem úloh do LCS a jejich opětovné přehrání

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Podrobnosti o prostředí** 

Microsoft Dynamics 365 Human Resources, která byla nasazena pomocí služby Microsoft Dynamics Lifecycle Services (LCS)

**Výdej**

Zákazník chce uložit nové záznamy úlohy do projektu LCS a poté uložené průvodce záznamem úloh přehrát.

**Rozlišení**

Chcete-li uložit záznam úloh do LCS, postupujte takto:

1. Přihlaste se do LCS a vyberte projekt.
2. Zvolte dlaždici **Modelování podnikových procesů**.
3. Zobrazte tuto stránku v aktualizované zkušenosti BPM.
4. Vyberte knihovnu a pak vyberte **Kopírovat**.
5. Zadejte název modelu Modelování podnikových procesů.
6. Přihlaste se k modulu Lidské zdroje z LCS.
7. Do pole **Vyhledat** zadejte **Nápověda**. Otevře se nápověda služeb Lifecycle Services
8. Zvolte tlačítko **Aktualizovat** pro konfiguraci nápovědy ke službě Lifecycle Services.

    Měla by se zobrazit nová knihovna BPM a měla by být aktivní.

9. Zavřete stránku.
10. Vytvořit záznam úkolů.
11. Po dokončení zvolte **Uložit ve službách Lifecycle Services**.

    ![Uložit ve službách Lifecycle Services.](media/task-guides.png)

12. Vyberte BPM knihovnu a uzel, do kterého chcete uložit záznam úloh.

Postupujte podle těchto kroků k opětovnému přehrání průvodce záznamem úloh z LCS.

1. Spusťte záznamník úloh.
2. Zvolte **Otevřít z LCS**.
3. Vyberte knihovnu a BPM uzel, který má uloženého průvodce záznamem úloh.
4. Otevřete průvodce záznamem úloh.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: "Uložení průvodců záznamem úloh do LCS a jejich opakované přehrání"
description: "Toto téma vysvětluje, jak uložit průvodce záznamem úloh do Microsoft Dynamics Lifecycle Services (LCS) a poté je opětovně přehrát."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>Uložení průvodců záznamem úloh do LCS a jejich opakované přehrání

[!include [banner](includes/banner.md)]

**Podrobnosti o prostředí** 

Aplikace Microsoft Dynamics 365 for Talent, která byla nasazena pomocí Microsoft Dynamics Lifecycle Services (LCS)

**Problém**

Zákazník chce uložit nové záznamy úlohy do projektu LCS a poté uložené průvodce záznamem úloh přehrát.

**Řešení**

Chcete-li uložit záznam úloh do LCS, postupujte takto:

1. Přihlaste se do LCS a vyberte projekt.
2. Zvolte dlaždici **Modelování podnikových procesů**.
3. Zobrazte tuto stránku v aktualizované zkušenosti BPM.
4. Vyberte knihovnu a pak vyberte **Kopírovat**.
5. Zadejte název modelu Modelování podnikových procesů.
6. Přihlaste se do aplikace Talent z LCS.
7. Do pole **Vyhledat** zadejte **Nápověda**. Otevře se nápověda služeb Lifecycle Services
8. Zvolte tlačítko **Aktualizovat** pro konfiguraci nápovědy ke službě Lifecycle Services.

    Měla by se zobrazit nová knihovna BPM a měla by být aktivní.

9. Zavřete stránku.
10. Vytvořit záznam úkolů.
11. Po dokončení zvolte **Uložit ve službách Lifecycle Services**.

    ![Uložit ve službách Lifecycle Services](media/task-guides.png)

12. Vyberte BPM knihovnu a uzel, do kterého chcete uložit záznam úloh.

Postupujte podle těchto kroků k opětovnému přehrání průvodce záznamem úloh z LCS.

1. Spusťte záznamník úloh.
2. Zvolte **Otevřít z LCS**.
3. Vyberte knihovnu a BPM uzel, který má uloženého průvodce záznamem úloh.
4. Otevřete průvodce záznamem úloh.


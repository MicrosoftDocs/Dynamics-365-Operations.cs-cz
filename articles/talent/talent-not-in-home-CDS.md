---
title: Talent se nezobrazuje mezi aplikacemi Microsoft Dynamics 365 (CDS1.0).
description: "Toto téma vysvětluje, jak postupovat v případech, kdy zákazník nevidí aplikaci Microsoft Dynamics 365 for Talent mezi aplikacemi Microsoft Dynamics 365."
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
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent se nezobrazuje mezi aplikacemi Microsoft Dynamics 365 (CDS1.0).

[!include [banner](includes/banner.md)]

**Problém**

Zákazník nevidí aplikaci Microsoft Dynamics 365 for Talent mezi aplikacemi Microsoft Dynamics 365.

**Řešení**

Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft PowerApps.

1. Uživatel s rolí správce, který má licenci plánu 2 pro PowerApps musí otevřít [Portál správy PowerApps](https://preview.admin.powerapps.com/).
2. Vyberte **Prostředí**a zvolte správné prostředí pro Talent.
3. Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.

    ![Karta Role prostředí](media/environment-roles.png)

4. Na kartě **Uživatelé** přidejte uživatele nebo organizaci.

    ![Karta Uživatelé](media/environment-maker.png)

5. Zvolte **Uložit**.
6. Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.

    ![Tlačítko Synchronizovat](media/get-more.png)

    Po dokončení synchronizace se Talent se objeví na domovské stránce.


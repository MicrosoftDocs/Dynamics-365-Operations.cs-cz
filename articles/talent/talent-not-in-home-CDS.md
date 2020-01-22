---
title: Talent se neobjevuje mezi aplikacemi Microsoft Dynamics 365 (Common Data Service 1.0)
description: Toto téma vysvětluje, jak postupovat v případech, kdy zákazník nevidí aplikaci Dynamics 365 Talent for Talent mezi aplikacemi Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897020"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent se neobjevuje mezi aplikacemi Microsoft Dynamics 365 (Common Data Service 1.0)

**Vydání**

Zákazník nevidí aplikaci Microsoft Dynamics 365 Talent mezi aplikacemi Microsoft Dynamics 365.

**Rozlišení**

Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft Power Apps.

1. Uživatel s rolí správce, který má licenci plánu 2 pro Power Apps, musí otevřít [portál pro správu Power Apps](https://preview.admin.powerapps.com/).
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

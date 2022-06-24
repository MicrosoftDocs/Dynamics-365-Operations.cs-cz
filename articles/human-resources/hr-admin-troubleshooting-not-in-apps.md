---
title: Human Resources se nezobrazují v aplikacích Microsoft Dynamics 365
description: Tento článek vysvětluje, co dělat, pokud Microsoft Dynamics 365 Human Resources není uveden v seznamu aplikací Microsoft Dynamics 365.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872232"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Aplikace Human Resources se nezobrazuje v aplikacích Microsoft Dynamics 365


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problém**

Zákazník nevidí Dynamics 365 Human Resources mezi aplikacemi Microsoft Dynamics 365.

**Rozlišení**

Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft Power Apps.

1. Uživatel s rolí správce, který má licenci plánu 2 pro Power Apps, musí otevřít [portál pro správu Power Apps](https://preview.admin.powerapps.com/).

2. Vyberte **Prostředí** a zvolte správné prostředí pro Human Resources.

3. Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.

    ![Karta Role prostředí.](media/environment-roles.png)

4. Na kartě **Uživatelé** přidejte uživatele nebo organizaci.

    ![Karta Uživatelé.](media/environment-maker.png)

5. Zvolte možnost **Uložit**.

6. Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.

    ![Tlačítko Synchronizovat.](media/get-more.png)

    Po dokončení synchronizace se Human Resources se objeví na domovské stránce.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

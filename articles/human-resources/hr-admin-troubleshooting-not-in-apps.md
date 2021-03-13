---
title: Human Resources se nezobrazují v aplikacích Microsoft Dynamics 365
description: Tento článek vysvětluje, jak postupovat v případech, kdy zákazník nevidí aplikaci Microsoft Dynamics 365 Human Resources for Talent mezi aplikacemi Microsoft Dynamics 365.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111825"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources se nezobrazují v aplikacích Microsoft Dynamics 365

**Vydání**

Zákazník nevidí Dynamics 365 Human Resources mezi aplikacemi Microsoft Dynamics 365.

**Rozlišení**

Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft Power Apps.

1. Uživatel s rolí správce, který má licenci plánu 2 pro Power Apps, musí otevřít [portál pro správu Power Apps](https://preview.admin.powerapps.com/).

2. Vyberte **Prostředí** a zvolte správné prostředí pro Human Resources.

3. Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.

    ![Karta Role prostředí](media/environment-roles.png)

4. Na kartě **Uživatelé** přidejte uživatele nebo organizaci.

    ![Karta Uživatelé](media/environment-maker.png)

5. Zvolte **Uložit**.

6. Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.

    ![Tlačítko Synchronizovat](media/get-more.png)

    Po dokončení synchronizace se Human Resources se objeví na domovské stránce.

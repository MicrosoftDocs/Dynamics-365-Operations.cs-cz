---
title: Human Resources se nezobrazují v aplikacích Microsoft Dynamics 365
description: Tento článek vysvětluje, jak postupovat v případech, kdy zákazník nevidí aplikaci Microsoft Dynamics 365 Human Resources for Talent mezi aplikacemi Microsoft Dynamics 365.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803962"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="52c7d-103">Human Resources se nezobrazují v aplikacích Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="52c7d-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="52c7d-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="52c7d-104">**Issue**</span></span>

<span data-ttu-id="52c7d-105">Zákazník nevidí Dynamics 365 Human Resources mezi aplikacemi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="52c7d-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="52c7d-106">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="52c7d-106">**Resolution**</span></span>

<span data-ttu-id="52c7d-107">Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="52c7d-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="52c7d-108">Uživatel s rolí správce, který má licenci plánu 2 pro Power Apps, musí otevřít [portál pro správu Power Apps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="52c7d-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="52c7d-109">Vyberte **Prostředí** a zvolte správné prostředí pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52c7d-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="52c7d-110">Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="52c7d-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Karta Role prostředí](media/environment-roles.png)

4. <span data-ttu-id="52c7d-112">Na kartě **Uživatelé** přidejte uživatele nebo organizaci.</span><span class="sxs-lookup"><span data-stu-id="52c7d-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Karta Uživatelé](media/environment-maker.png)

5. <span data-ttu-id="52c7d-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="52c7d-114">Select **Save**.</span></span>

6. <span data-ttu-id="52c7d-115">Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="52c7d-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="52c7d-116">Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.</span><span class="sxs-lookup"><span data-stu-id="52c7d-116">Select **Sync** to update the user apps.</span></span>

    ![Tlačítko Synchronizovat](media/get-more.png)

    <span data-ttu-id="52c7d-118">Po dokončení synchronizace se Human Resources se objeví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="52c7d-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
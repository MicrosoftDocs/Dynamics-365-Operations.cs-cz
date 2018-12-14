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

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="e9237-103">Talent se nezobrazuje mezi aplikacemi Microsoft Dynamics 365 (CDS1.0).</span><span class="sxs-lookup"><span data-stu-id="e9237-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9237-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="e9237-104">**Issue**</span></span>

<span data-ttu-id="e9237-105">Zákazník nevidí aplikaci Microsoft Dynamics 365 for Talent mezi aplikacemi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e9237-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="e9237-106">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="e9237-106">**Resolution**</span></span>

<span data-ttu-id="e9237-107">Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e9237-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="e9237-108">Uživatel s rolí správce, který má licenci plánu 2 pro PowerApps musí otevřít [Portál správy PowerApps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="e9237-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="e9237-109">Vyberte **Prostředí**a zvolte správné prostředí pro Talent.</span><span class="sxs-lookup"><span data-stu-id="e9237-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="e9237-110">Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e9237-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Karta Role prostředí](media/environment-roles.png)

4. <span data-ttu-id="e9237-112">Na kartě **Uživatelé** přidejte uživatele nebo organizaci.</span><span class="sxs-lookup"><span data-stu-id="e9237-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Karta Uživatelé](media/environment-maker.png)

5. <span data-ttu-id="e9237-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e9237-114">Select **Save**.</span></span>
6. <span data-ttu-id="e9237-115">Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="e9237-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="e9237-116">Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.</span><span class="sxs-lookup"><span data-stu-id="e9237-116">Select **Sync** to update the user apps.</span></span>

    ![Tlačítko Synchronizovat](media/get-more.png)

    <span data-ttu-id="e9237-118">Po dokončení synchronizace se Talent se objeví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="e9237-118">After synchronization is completed, Talent will appear on the home page.</span></span>


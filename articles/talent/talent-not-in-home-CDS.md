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
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="c4779-103">Talent se neobjevuje mezi aplikacemi Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="c4779-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

<span data-ttu-id="c4779-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="c4779-104">**Issue**</span></span>

<span data-ttu-id="c4779-105">Zákazník nevidí aplikaci Microsoft Dynamics 365 Talent mezi aplikacemi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c4779-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="c4779-106">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="c4779-106">**Resolution**</span></span>

<span data-ttu-id="c4779-107">Uživatel musí být přidán do role tvůrce prostředí pro prostředí v Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c4779-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="c4779-108">Uživatel s rolí správce, který má licenci plánu 2 pro Power Apps, musí otevřít [portál pro správu Power Apps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="c4779-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="c4779-109">Vyberte **Prostředí**a zvolte správné prostředí pro Talent.</span><span class="sxs-lookup"><span data-stu-id="c4779-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="c4779-110">Na kartě **Zabezpečení** na kartě **Role prostředí** zvolte **Tvůrce prostředí**.</span><span class="sxs-lookup"><span data-stu-id="c4779-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Karta Role prostředí](media/environment-roles.png)

4. <span data-ttu-id="c4779-112">Na kartě **Uživatelé** přidejte uživatele nebo organizaci.</span><span class="sxs-lookup"><span data-stu-id="c4779-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Karta Uživatelé](media/environment-maker.png)

5. <span data-ttu-id="c4779-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c4779-114">Select **Save**.</span></span>
6. <span data-ttu-id="c4779-115">Uživatel se musí nyní přihlásit do [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="c4779-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="c4779-116">Vyberte **Synchronizovat** pro aktualizaci uživatelských aplikací.</span><span class="sxs-lookup"><span data-stu-id="c4779-116">Select **Sync** to update the user apps.</span></span>

    ![Tlačítko Synchronizovat](media/get-more.png)

    <span data-ttu-id="c4779-118">Po dokončení synchronizace se Talent se objeví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="c4779-118">After synchronization is completed, Talent will appear on the home page.</span></span>

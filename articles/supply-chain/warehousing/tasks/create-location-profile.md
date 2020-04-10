---
title: Vytvoření profilu skladového místa
description: Toto téma vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 764d1dc1d7fb54e0fa14a681d6d3cdb1d829aa57
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146116"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="a125a-103">Vytvoření profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="a125a-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a125a-104">Toto téma vysvětluje, jak vytvořit profil skladového místa v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a125a-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a125a-105">Každé umístění ve skladu musí mít přidružený profil umístění, který popisuje vlastnosti umístění, například zda umístění povoluje smíšené zboží.</span><span class="sxs-lookup"><span data-stu-id="a125a-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="a125a-106">V této proceduře vytvoříte profil pro umístění, které nevyžaduje kontrolu registrační značky.</span><span class="sxs-lookup"><span data-stu-id="a125a-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="a125a-107">Povolíme stav Smíšené zboží a Smíšené zásoby a také periodickou inventuru.</span><span class="sxs-lookup"><span data-stu-id="a125a-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="a125a-108">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a125a-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="a125a-109">V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Sklad > Profily skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="a125a-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="a125a-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a125a-110">Select **New**.</span></span>
3. <span data-ttu-id="a125a-111">Zadejte hodnotu do pole **ID profilu skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="a125a-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="a125a-112">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="a125a-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a125a-113">V poli **Formát skladového místa** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a125a-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="a125a-114">V poli **Typ skladového místa** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a125a-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="a125a-115">V poli **ID profilu správy dokování** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a125a-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="a125a-116">Vyberte možnost **Ano** v poli **Povolit smíšené položky**.</span><span class="sxs-lookup"><span data-stu-id="a125a-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="a125a-117">Vyberte možnost **Ano** v poli **Povolit smíšené stavy zásob**.</span><span class="sxs-lookup"><span data-stu-id="a125a-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="a125a-118">Vyberte možnost **Ano** v poli **Povolit cyklickou inventuru**.</span><span class="sxs-lookup"><span data-stu-id="a125a-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="a125a-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a125a-119">Select **Save**.</span></span>


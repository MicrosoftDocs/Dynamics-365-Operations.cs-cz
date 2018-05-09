---
title: "Konfigurace možnosti Zobrazení starších dávek v rámci skladu na mobilním zařízení"
description: "Toto téma popisuje, jak nastavit mobilní zařízení k zobrazení seznamu skladových míst s dávkami, které jsou starší než aktuální umístění řádku práce."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 27fbf57ba7114ca773f2a80de51b36b4e63c6dd6
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="70904-103">Konfigurace možnosti Zobrazení starších dávek v rámci skladu na mobilním zařízení</span><span class="sxs-lookup"><span data-stu-id="70904-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70904-104">Konfigurace **Zobrazení starších dávek v rámci skladu** umožňuje zobrazit seznam skladových míst s dávkami, které jsou starší než aktuální umístění řádku práce.</span><span class="sxs-lookup"><span data-stu-id="70904-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="70904-105">Seznam skladových míst, která se zobrazují, obsahuje informace o starších dávkách ve skladovém místě s datem vypršení platnosti a fyzickými zásobami pro každou dávku.</span><span class="sxs-lookup"><span data-stu-id="70904-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="70904-106">Můžete se rozhodnout pro vyskladnění z nového skladového místa nebo můžete pokračovat ve vyskladnění z aktuálního skladového místa.</span><span class="sxs-lookup"><span data-stu-id="70904-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="70904-107">Vyskladnění z nového umístění – pokud vyberete nové místo k vyskladnění, aktuální řádek práce bude aktualizován na nové skladové místo použití a práce bude v novém místě pokračovat obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="70904-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="70904-108">Aby bylo nové skladové místo platné, musí mít dostatek disponibilního množství pro celý řádek práce.</span><span class="sxs-lookup"><span data-stu-id="70904-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="70904-109">Pokud není požadované množství k dispozici, nebude řádek práce aktualizován a zobrazí se seznam.</span><span class="sxs-lookup"><span data-stu-id="70904-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="70904-110">Pokračovat ve vyskladnění z aktuálního místa – pokud budete pokračovat v aktuálním umístění řádku práce, bude množství pro řádek práce dále vyskladňováno z původního umístění.</span><span class="sxs-lookup"><span data-stu-id="70904-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="70904-111">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="70904-111">Where it applies</span></span>
<span data-ttu-id="70904-112">Možnost Zobrazit starší dávky ve skladu je nakonfigurována pro položky nabídky mobilního zařízení a má vliv na vyskladnění dávky pod položkami.</span><span class="sxs-lookup"><span data-stu-id="70904-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="70904-113">Nastavení zobrazení starších dávek v rámci skladu</span><span class="sxs-lookup"><span data-stu-id="70904-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="70904-114">Konfigurace **Zobrazení starších dávke v rámci skladu** je k dispozici v položkách nabídky mobilního zařízení, pokud je možnost **Vyskladnit nejstarší dávku** nastavena na **Upozornit**.</span><span class="sxs-lookup"><span data-stu-id="70904-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="70904-115">V části **Správa skladu** > **Nastavení** > **Mobilní zařízení** > **Položky nabídky mobilního zařízení** nastavte možnost **Použít existující práci** na **Ano** u položek nabídky a vyberte možnost **Upozornit** v poli **Vyskladnění nejstarší dávky**.</span><span class="sxs-lookup"><span data-stu-id="70904-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



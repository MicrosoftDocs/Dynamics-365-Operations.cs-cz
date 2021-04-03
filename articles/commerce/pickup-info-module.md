---
title: Modul informací o vyzvednutí
description: Tohle téma se zabývá modulem informací o vyzvednutí a popisuje, jak jej přidat na stránky pokladny v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263173"
---
# <a name="pickup-information-module"></a><span data-ttu-id="6a265-103">Modul informací o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="6a265-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a265-104">Tohle téma se zabývá modulem informací o vyzvednutí a popisuje, jak jej přidat na stránky pokladny v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a265-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6a265-105">Modul informací o vyzvednutí lze použít v modulu pokladny k zobrazení informací o vyzvednutí objednávky.</span><span class="sxs-lookup"><span data-stu-id="6a265-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="6a265-106">Zákazníci si mohou prohlédnout dostupná data vyzvednutí a časové úseky a poté vybrat vhodný čas pro vyzvednutí objednávky.</span><span class="sxs-lookup"><span data-stu-id="6a265-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="6a265-107">Například si zákazník může vybrat vyzvednutí objednávky v 15:00 dne 21. března v obchodě v San Francisku.</span><span class="sxs-lookup"><span data-stu-id="6a265-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="6a265-108">Časové úseky vyzvednutí pro příslušné obchody musí být nakonfigurovány v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a265-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="6a265-109">Další informace viz [Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="6a265-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="6a265-110">Pokud je na stránce pokladny vytvořen modul s informacemi o vyzvednutí, ale pro obchod, který je vybrán pro vyzvednutí, nejsou definovány žádné časové úseky, modul zobrazí informace, ale uživatel nebude moci vybrat žádné časové úseky.</span><span class="sxs-lookup"><span data-stu-id="6a265-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="6a265-111">Časové úseky jsou volitelné a nejsou nutné k zadání objednávky.</span><span class="sxs-lookup"><span data-stu-id="6a265-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="6a265-112">Pokud je pro vyzvednutí vybráno více položek ve více obchodech, modul s informacemi o vyzvednutí umožní uživateli vybrat časový úsek pro každý obchod za předpokladu, že jsou pro něj dostupné.</span><span class="sxs-lookup"><span data-stu-id="6a265-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="6a265-113">Podpora časových úseků a modul informací o vyzvednutí v pokladně je k dispozici v Dynamics 365 Commerce verze 10.0.15 a novější.</span><span class="sxs-lookup"><span data-stu-id="6a265-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="6a265-114">Následující obrázek ukazuje příklad výběru časového úseku prostřednictvím modulu s informacemi o vyzvednutí na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="6a265-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Příklad modulu s informacemi o vyzvednutí na stránce pokladny](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="6a265-116">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="6a265-116">Module properties</span></span>

- <span data-ttu-id="6a265-117">**Nadpis** – Zadejte nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="6a265-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="6a265-118">Zobrazení informací o časovém úseku po zadání objednávky</span><span class="sxs-lookup"><span data-stu-id="6a265-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="6a265-119">Po zadání objednávky lze informace o vybraném časovém úseku zobrazit v [modulu potvrzení objednávky](order-confirmation-module.md) a [modul podrobností objednávky](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="6a265-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="6a265-120">Oba tyto moduly mají vlastnost **Zobrazit informace o časovém úseku**.</span><span class="sxs-lookup"><span data-stu-id="6a265-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="6a265-121">Aby mohly během procesu objednávky zobrazit vybraný časový úsek, musí být tato vlastnost nastavena na **Pravda**.</span><span class="sxs-lookup"><span data-stu-id="6a265-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="6a265-122">Přidání modulu s informacemi o vyzvednutí na pokladně na stránce</span><span class="sxs-lookup"><span data-stu-id="6a265-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="6a265-123">Pokyny k přidání modulu s informacemi o vyzvednutí na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="6a265-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="6a265-124">Následující ilustrace ukazuje příklad stránky pokladny elektronického obchodu, která obsahuje časové úseky pro vyzvednutí řádkových položek.</span><span class="sxs-lookup"><span data-stu-id="6a265-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Příklad stránky pokladny elektronického obchodu, která obsahuje časové úseky pro vyzvednutí řádkových položek](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="6a265-126">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6a265-126">Additional resources</span></span>

[<span data-ttu-id="6a265-127">Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem</span><span class="sxs-lookup"><span data-stu-id="6a265-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="6a265-128">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="6a265-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6a265-129">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="6a265-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6a265-130">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="6a265-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
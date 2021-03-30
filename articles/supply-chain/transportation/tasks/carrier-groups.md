---
title: Skupiny dopravců
description: Toto téma popisuje, jak nastavit data pro skupiny dopravců.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 95517153dda06cecf8e57b1f9b080aa07966c111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247255"
---
# <a name="carrier-groups"></a><span data-ttu-id="d05ac-103">Skupiny dopravců</span><span class="sxs-lookup"><span data-stu-id="d05ac-103">Carrier groups</span></span>

<span data-ttu-id="d05ac-104">Skupina přepravců je soubor přepravců a služeb dopravců.</span><span class="sxs-lookup"><span data-stu-id="d05ac-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="d05ac-105">Každá skupina dopravců určuje preferovanou sekvenci pro přepravce a služby dopravců, které k ní patří.</span><span class="sxs-lookup"><span data-stu-id="d05ac-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="d05ac-106">Pokud pro stejný segment trasy existuje více přepravců a služeb dopravce, můžete v plánu trasy nebo v průvodci trasami namísto konkrétního přepravce a služby dopravce určit skupinu dopravců.</span><span class="sxs-lookup"><span data-stu-id="d05ac-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="d05ac-107">Vytvoření skupiny dopravců</span><span class="sxs-lookup"><span data-stu-id="d05ac-107">Create a carrier group</span></span>

1. <span data-ttu-id="d05ac-108">Přejděte do nabídky **Správa přepravy &gt; Nastavení &gt; Dopravci &gt; Skupina dopravců**.</span><span class="sxs-lookup"><span data-stu-id="d05ac-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="d05ac-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d05ac-109">Select **New**.</span></span>
1. <span data-ttu-id="d05ac-110">Do pole **Skupina dopravců** zadejte jedinečný identifikátor skupiny.</span><span class="sxs-lookup"><span data-stu-id="d05ac-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="d05ac-111">V poli **Název** zadejte popisný název skupiny.</span><span class="sxs-lookup"><span data-stu-id="d05ac-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="d05ac-112">Na pevné záložce **Detaily** přidejte řádek a vyberte dopravce a službu dopravce.</span><span class="sxs-lookup"><span data-stu-id="d05ac-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="d05ac-113">Tento krok opakujte, dokud nepřidáte tolik dopravců, kolik pro skupinu potřebujete.</span><span class="sxs-lookup"><span data-stu-id="d05ac-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="d05ac-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d05ac-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
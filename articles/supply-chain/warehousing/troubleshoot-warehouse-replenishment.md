---
title: Odstraňování problémů s doplňováním skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s doplňováním skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644866"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="6b47d-103">Odstraňování problémů s doplňováním skladu</span><span class="sxs-lookup"><span data-stu-id="6b47d-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b47d-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s doplňováním skladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6b47d-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="6b47d-105">Zobrazuje se mi následující chybová zpráva: „Pác %1 nelze odblokovat, protože má nedokončené doplňování.“</span><span class="sxs-lookup"><span data-stu-id="6b47d-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6b47d-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="6b47d-106">Issue description</span></span>

<span data-ttu-id="6b47d-107">Výběr práce je blokován z důvodu práce se závislým doplňováním.</span><span class="sxs-lookup"><span data-stu-id="6b47d-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6b47d-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="6b47d-108">Issue resolution</span></span>

<span data-ttu-id="6b47d-109">Při použití doplňování požadavků vlny, pokud je nutné místo pro výdej doplnit, aby byla splněna zdrojový požadavek na objednávku, vytvoří systém práci s doplňováním i výdejem.</span><span class="sxs-lookup"><span data-stu-id="6b47d-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="6b47d-110">Blokuje však výdej práci, dokud není dokončena doplňovací práce.</span><span class="sxs-lookup"><span data-stu-id="6b47d-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="6b47d-111">Toto chování je záměrné, protože místo výdeje nebude mít dostatek zásob, dokud nebude dokončeno doplňování.</span><span class="sxs-lookup"><span data-stu-id="6b47d-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="6b47d-112">Dokončete doplňovací práci a poté zpracujte výdej.</span><span class="sxs-lookup"><span data-stu-id="6b47d-112">Complete the replenishment work, and then process the picking work.</span></span>

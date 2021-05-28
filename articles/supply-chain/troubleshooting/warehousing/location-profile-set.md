---
title: Profil polohy vylučuje negativní zásoby, ale negativní zásoby k dispozici jsou povoleny
description: Možnost Povolit negativní zásoby pro profil umístění je nastavena na Ne, ale systém stále umožňuje negativní zásoby k dispozici.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026335"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="3111a-103">Profil polohy vylučuje negativní zásoby, ale negativní zásoby k dispozici jsou povoleny</span><span class="sxs-lookup"><span data-stu-id="3111a-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="3111a-104">Číslo článku znalostní báze: 4613622</span><span class="sxs-lookup"><span data-stu-id="3111a-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="3111a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3111a-105">Symptoms</span></span>

<span data-ttu-id="3111a-106">Možnost **Povolit negativní zásoby** pro profil umístění je nastavena na *Ne*, ale systém stále umožňuje negativní zásoby k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3111a-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3111a-107">Příklad</span><span class="sxs-lookup"><span data-stu-id="3111a-107">Example scenario</span></span>

<span data-ttu-id="3111a-108">U vládou regulovaných transakcí musí být systém schopen zaznamenávat negativní zásoby, aby zaúčtoval ztráty.</span><span class="sxs-lookup"><span data-stu-id="3111a-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="3111a-109">Chcete, aby položka mohla zobrazit negativní zásoby, ale pouze na určených místech, jako jsou nádrže.</span><span class="sxs-lookup"><span data-stu-id="3111a-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="3111a-110">Pokud však skupina modelů položek umožňuje negativní zásoby, zjistíte, že nezáleží na tom, zda je umístění nastaveno tak, aby umožňovalo negativní zásoby.</span><span class="sxs-lookup"><span data-stu-id="3111a-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="3111a-111">Pokud je položka nastavena tak, že nejsou povoleny negativní zásoby, nezáleží na tom, jak je nastaven profil polohy.</span><span class="sxs-lookup"><span data-stu-id="3111a-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="3111a-112">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3111a-112">Resolution</span></span>

<span data-ttu-id="3111a-113">Nastavení **Povolit negativní zásoby** z profilu umístění platí pouze pro procesy ve skladu, jako je vychystávání.</span><span class="sxs-lookup"><span data-stu-id="3111a-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="3111a-114">Skupiny modelů položek, které jsou nastaveny tak, aby umožňovaly negativní zásoby, však ovlivňují všechny procesy z modulů správy zásob a správy skladu a profil umístění toto nastavení nepřepíše.</span><span class="sxs-lookup"><span data-stu-id="3111a-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="3111a-115">Můžete určit, zda je ve skladu povoleno provádět negativní zásoby.</span><span class="sxs-lookup"><span data-stu-id="3111a-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="3111a-116">Nastavte skupiny modelů položek tak, aby nepovolovaly negativní fyzické zásoby, a nastavte pouze příslušný sklad, aby byly povoleny negativní zásoby.</span><span class="sxs-lookup"><span data-stu-id="3111a-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>

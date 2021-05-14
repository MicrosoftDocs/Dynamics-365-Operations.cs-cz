---
title: Vzorkování položek řízení kvality
description: Toto téma popisuje, jak nastavit vzorkování položek.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956572"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="d650f-103">Vzorkování položek řízení kvality</span><span class="sxs-lookup"><span data-stu-id="d650f-103">Quality management item sampling</span></span>

<span data-ttu-id="d650f-104">Vzorkování položek se používá jako součást přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="d650f-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="d650f-105">Definuje množství aktuální fyzické zásoby, která musí být zkontrolována.</span><span class="sxs-lookup"><span data-stu-id="d650f-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="d650f-106">Vzorkování může být založeno na pevném množství, procentuální hodnotě nebo celé licenční značky.</span><span class="sxs-lookup"><span data-stu-id="d650f-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="d650f-107">Nastavení vzorkování zboží</span><span class="sxs-lookup"><span data-stu-id="d650f-107">Set up item sampling</span></span>

<span data-ttu-id="d650f-108">Pro nastavení vzorkování položek postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d650f-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="d650f-109">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Vzorkování položek**.</span><span class="sxs-lookup"><span data-stu-id="d650f-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="d650f-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d650f-110">Select **New**.</span></span>
1. <span data-ttu-id="d650f-111">Zadejte hodnotu do pole **Vzorkování položky**.</span><span class="sxs-lookup"><span data-stu-id="d650f-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="d650f-112">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d650f-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="d650f-113">Zadejte číslo do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="d650f-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="d650f-114">Tato hodnota se vztahuje k určení množství, které je vybráno v přilehlém poli.</span><span class="sxs-lookup"><span data-stu-id="d650f-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="d650f-115">V oddílu **Zpracování** vyberte zaškrtávací políčko **Úplné blokování**, pokud má být zablokováno celé množství šarže nebo množství objednávky, pokud test selže.</span><span class="sxs-lookup"><span data-stu-id="d650f-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="d650f-116">Pokud toto políčko není zaškrtnuto, budou v případě neúspěchu testu blokovány pouze položky v objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="d650f-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="d650f-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d650f-117">Select **Save**.</span></span>
1. <span data-ttu-id="d650f-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d650f-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="d650f-119">Funkce *Správa kvality pro procesy skladu* poskytuje dodatečné možnosti vzorkování zboží.</span><span class="sxs-lookup"><span data-stu-id="d650f-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="d650f-120">Přidá koncepci *rozsahu vzorkování položek* a možnost definovat plnou registrační značku jako specifikaci množství.</span><span class="sxs-lookup"><span data-stu-id="d650f-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="d650f-121">Pokud jste tuto funkci povolili, další informace naleznete v tématu [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="d650f-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

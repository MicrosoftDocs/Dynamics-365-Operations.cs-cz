---
title: "Vrácení stavu výrobní zakázky"
description: "Toto téma popisuje způsob stornování stavu výrobní zakázky."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 10ce698ef07e9f290547b0eedd7c357f54852e76
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="ac60d-103">Vrácení stavu výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="ac60d-103">Reverse the production order status</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ac60d-104">Toto téma popisuje způsob stornování stavu výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="ac60d-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="ac60d-105">Při stornování stavu výrobní zakázky se vrátí zakázku včetně všech operací připojených k postupům do předchozího kroku výrobního cyklu.</span><span class="sxs-lookup"><span data-stu-id="ac60d-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="ac60d-106">Například výrobní zakázka má stav **Plánováno**, a vy změníte stav zpět na **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="ac60d-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="ac60d-107">V tomto případě musí systém nejprve stav změnit na **Odhad**, což je stav, který okamžitě předchází stavu **Plánováno**.</span><span class="sxs-lookup"><span data-stu-id="ac60d-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="ac60d-108">Stav pak můžete změnit na stav, který chcete, **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="ac60d-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="ac60d-109">**Poznámka:** Pokud vaše zakázka dosáhla stavu **Hlášeno jako dokončené**, můžete ji stále vrátit do dřívějšího stavu.</span><span class="sxs-lookup"><span data-stu-id="ac60d-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="ac60d-110">Je třeba znovu spustit odhad a plánování operací, plánování úlohy, nebo oba typy plánování a aktualizovat informace na zakázce.</span><span class="sxs-lookup"><span data-stu-id="ac60d-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="ac60d-111">Důvodem nutnosti tohoto kroku je, že veškeré rezervace spotřeby zbývajících položek a spotřeby provozních prostředků musí být rovněž vynulovány.</span><span class="sxs-lookup"><span data-stu-id="ac60d-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="ac60d-112">Zbývající část tohoto článku vysvětluje, co se děje po stornování stavu výrobní zakázky následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="ac60d-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="ac60d-113">Ze stavu **Odhadnuto** do stavu **Vytvořeno**</span><span class="sxs-lookup"><span data-stu-id="ac60d-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="ac60d-114">Ze stavu **Plánováno** do stavu **Odhadnuto**</span><span class="sxs-lookup"><span data-stu-id="ac60d-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="ac60d-115">Ze stavu **Uvolněno** do stavu **Plánováno**</span><span class="sxs-lookup"><span data-stu-id="ac60d-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="ac60d-116">Ze stavu **Zahájeno** do stavu **Uvolněno**</span><span class="sxs-lookup"><span data-stu-id="ac60d-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="ac60d-117">Ze stavu Odhadnuto do stavu Vytvořeno</span><span class="sxs-lookup"><span data-stu-id="ac60d-117">From Estimated to Created</span></span>
<span data-ttu-id="ac60d-118">Když vrátíte stav výrobní zakázky ze stavu **Odhadnuto** na **Vytvořeno**, spotřeba položky, která byla vypočtena pro položky v kusovnících, je odstraněna.</span><span class="sxs-lookup"><span data-stu-id="ac60d-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="ac60d-119">Skladové transakce v řádku výroby jsou odstraněny a pole **Následný stav** na řádcích kusovníku výrobní zakázky je nastaven zpět na **Ukončeno**.</span><span class="sxs-lookup"><span data-stu-id="ac60d-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="ac60d-120">Pokud vyberete možnost **Odvozené nákupy** a **Odvozené výroby**, veškeré podřízené nákupní objednávky nebo výrobní zakázky budou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="ac60d-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="ac60d-121">Pokud jste odhadovali náklady výrobní zakázky, nebo ručně rezervovali položky, takže je lze použít ve výrobě, tyto transakce budou odebrány.</span><span class="sxs-lookup"><span data-stu-id="ac60d-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="ac60d-122">Ze stavu Plánováno do stavu Odhadnuto</span><span class="sxs-lookup"><span data-stu-id="ac60d-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="ac60d-123">Když stav vrátíte výrobní zakázky ze stavu **Plánováno** na **odhadnuto**, budou odstraněny plánovaná počáteční a koncová data a časy.</span><span class="sxs-lookup"><span data-stu-id="ac60d-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="ac60d-124">Odstraní se rezervace kapacity provedené během plánování a úlohy, jež byly vytvořeny během plánování úlohy.</span><span class="sxs-lookup"><span data-stu-id="ac60d-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="ac60d-125">Všechny informace, které jsou zaznamenány o plánování operací a plánování práce na stránce **Podrobnosti výrobní zakázky** budou obnoveny.</span><span class="sxs-lookup"><span data-stu-id="ac60d-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="ac60d-126">Ze stavu Uvolněno do stavu Plánováno</span><span class="sxs-lookup"><span data-stu-id="ac60d-126">From Released to Scheduled</span></span>
<span data-ttu-id="ac60d-127">Když vrátíte stav výrobní zakázky ze stavu **Uvolněno** do stavu **Plánováno**, jedinou změnou bude změna hodnoty ve stavovém poli.</span><span class="sxs-lookup"><span data-stu-id="ac60d-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="ac60d-128">Ze stavu Zahájeno do stavu Uvolněno</span><span class="sxs-lookup"><span data-stu-id="ac60d-128">From Started to Released</span></span>
<span data-ttu-id="ac60d-129">Když vrátíte stav výrobní zakázky ze stavu **Zahájeno** zpět do stavu **Uvolněno**, budou všechny položky hlášené jako dokončené vráceny zpět.</span><span class="sxs-lookup"><span data-stu-id="ac60d-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="ac60d-130">Jestliže došlo k vydání materiálu nebo k provedení vstupních a výstupních dodávek do výroby, budou tato nastavení stornována.</span><span class="sxs-lookup"><span data-stu-id="ac60d-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="ac60d-131">Pole **Následný stav** na řádcích kusovníku výrobní zakázky se změní z **Ukončeno** na **Spotřeba materiálu**.</span><span class="sxs-lookup"><span data-stu-id="ac60d-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="ac60d-132">Pokud nebyl zaregistrován čas, nebo množství bylo hlášeno jako dokončené u operací ve výrobním postupu, budou tato nastavení stornována.</span><span class="sxs-lookup"><span data-stu-id="ac60d-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="ac60d-133">Pole **Následný stav** se změní z **Ukončeno** na **Spotřeba postupu** ve výrobním postupu.</span><span class="sxs-lookup"><span data-stu-id="ac60d-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="ac60d-134">Nastavení pro všechny položky, které jsou zaúčtovány jako procesu nebo nedokončená výroba, budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="ac60d-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="ac60d-135">Na stránce **Podrobnosti výrobní zakázky** se vynulují pole, která zobrazí množství, které bylo zahájeno nebo ohlášeno jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="ac60d-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="ac60d-136">Data pro tyto transakce jsou rovněž vynulovány.</span><span class="sxs-lookup"><span data-stu-id="ac60d-136">The dates for those transactions are also reset.</span></span>





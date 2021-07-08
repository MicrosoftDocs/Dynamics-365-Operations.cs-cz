---
title: Při spuštění integrovaného hlavního plánovacího modulu se zobrazí chyba
description: Při spuštění zastaralého integrovaného hlavního plánovacího modulu se zobrazí chyba
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294030"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="18073-103">Při spuštění integrovaného hlavního plánovacího modulu se zobrazí chyba</span><span class="sxs-lookup"><span data-stu-id="18073-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="18073-104">Kód chyby: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="18073-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="18073-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="18073-105">Symptoms</span></span>

<span data-ttu-id="18073-106">Při spuštění hlavního plánování pomocí zastaralého integrovaného hlavního plánovacího modulu, zobrazí se následující chyba:</span><span class="sxs-lookup"><span data-stu-id="18073-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="18073-107">Tato chybová zpráva se zobrazí, protože předdefinovaný hlavní plánovací modul byl použit pro scénáře podporované optimalizací plánování.</span><span class="sxs-lookup"><span data-stu-id="18073-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="18073-108">Měli byste migrovat na optimalizaci plánování hned teď, protože aktuální vestavěné hlavní plánování bude zastaralé.</span><span class="sxs-lookup"><span data-stu-id="18073-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="18073-109">Všimněte si, že toto spuštění hlavního plánování bylo úspěšně dokončeno.</span><span class="sxs-lookup"><span data-stu-id="18073-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="18073-110">V případě, že vaše migrace má silné závislosti na čekajících funkcích, lze požádat o výjimku z dalšího používání integrovaného hlavního plánovacího modulu.</span><span class="sxs-lookup"><span data-stu-id="18073-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="18073-111">Chcete-li začít, vyplňte prosím následující dotazník a případně požádejte o výjimku z migrace na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="18073-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="18073-112">Dotazník pro optimalizaci plánování migrace a výjimky</span><span class="sxs-lookup"><span data-stu-id="18073-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="18073-113">Příčina</span><span class="sxs-lookup"><span data-stu-id="18073-113">Cause</span></span>

<span data-ttu-id="18073-114">Pokud spustíte plánování a nepoužíváte funkce řízení výroby, měli byste zvážit migraci na Optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="18073-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="18073-115">Podpora integrovaného hlavního plánování je ukončena.</span><span class="sxs-lookup"><span data-stu-id="18073-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="18073-116">Proto, pokud jej chcete i nadále používat bez přijetí chybové zprávy, musíte požádat o výjimku od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="18073-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="18073-117">Řešení</span><span class="sxs-lookup"><span data-stu-id="18073-117">Resolution</span></span>

<span data-ttu-id="18073-118">Další informace o tom, jak migrovat na Optimalizaci plnánování, nebo jak požádat o výjimku, abyste místo toho mohli nadále používat zastaralý integrovaný plánovací modul, najdete v tématu [Migrace na optimalizaci plánování pro hlavní plánování](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="18073-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>

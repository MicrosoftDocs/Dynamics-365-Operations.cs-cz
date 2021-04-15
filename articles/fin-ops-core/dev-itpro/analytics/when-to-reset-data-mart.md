---
title: Kdy resetovat datové tržiště
description: V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754137"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="e4b1e-103">Kdy resetovat datové tržiště</span><span class="sxs-lookup"><span data-stu-id="e4b1e-103">When to reset a data mart</span></span>

<span data-ttu-id="e4b1e-104">Resetování datového tržiště může být časově náročné.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="e4b1e-105">V závislosti na okolnostech nemusí být tato akce řešením, které je potřeba.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="e4b1e-106">V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="e4b1e-107">Kdy potřebujete provést reset datového tržiště?</span><span class="sxs-lookup"><span data-stu-id="e4b1e-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="e4b1e-108">Před resetováním datového tržiště zvažte následující otázky.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="e4b1e-109">Odpověď ano na jednu nebo více otázek může znamenat, že vaše organizace může mít prospěch z resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="e4b1e-110">Databáze aplikace byla obnovena, ale nebyla obnovena databáze datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="e4b1e-111">Zobrazují se nesprávné údaje za účetní období, které není výsledkem problému s návrhem sestavy.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="e4b1e-112">Zobrazují se nesprávné údaje za účetní období a záznamy jsou uvedeny v části Pokusy o integraci na stránce **Stav integrace** v Návrháři sestav (spusťte Návrháře sestav a vyberte **Nástroje> Stav integrace**).</span><span class="sxs-lookup"><span data-stu-id="e4b1e-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="e4b1e-113">Otevřeli jste incident podpory a technik podpory vám nařídil resetovat datové tržiště jako součást kroku odstraňování problémů.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="e4b1e-114">Když není vhodné resetovat datové tržiště?</span><span class="sxs-lookup"><span data-stu-id="e4b1e-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="e4b1e-115">Existují okolnosti, kdy nedoporučujeme resetovat datové tržiště.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="e4b1e-116">Mezi ně patří následující.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-116">These include the following.</span></span> 

- <span data-ttu-id="e4b1e-117">Kdykoli důvod není uveden v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="e4b1e-118">Máte problémy s výkonem spojené se synchronizací dat. Za těchto okolností pravděpodobně obnovení datového tržiště nepomůže.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="e4b1e-119">Pokud máte opakující se vzor pro resetování z některého z následujících důvodů:</span><span class="sxs-lookup"><span data-stu-id="e4b1e-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="e4b1e-120">**Chybějící data** - Nejprve odstraňte problémy s návrhem sestavy a problémy s časováním synchronizace dat, například zjistíte, že mapa faktů se nespustila, protože byla zveřejněna chybějící data.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="e4b1e-121">**Zaseknutý stav integrace** - Pokud je integrace pomalá nebo se zdá být zaseknutá, je nepravděpodobné, že resetování datového tržiště problém vyřeší.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="e4b1e-122">**Pokusy o resetování byly neúspěšné** - Pokud bylo provedeno několik pokusů o dokončení resetu a byly neúspěšné z důvodu chybějících dat, doporučujeme zahájit incident podpory a spolupracovat s technikem podpory na analýze vaší situace před dalším pokusem o resetování datového trhu.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="e4b1e-123">**Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="e4b1e-124">Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="e4b1e-125">Co resetování datového tržiště nedělá</span><span class="sxs-lookup"><span data-stu-id="e4b1e-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="e4b1e-126">Reset se spustí až po dokončení stávajících úkolů.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="e4b1e-127">Tím je zajištěno, že nebudou vložena stará data.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="e4b1e-128">V tomto okamžiku se může zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat kvůli aktivní úloze.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="e4b1e-129">Prosím zkuste to znovu později."</span><span class="sxs-lookup"><span data-stu-id="e4b1e-129">Please try again later.”</span></span>
- <span data-ttu-id="e4b1e-130">Reset deaktivuje integrační úlohy a vymaže všechna data datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="e4b1e-131">Integrace je znovu povolena.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="e4b1e-132">Následující body specifikují dvě věci, které resetování datového tržiště *nebude* dělat.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="e4b1e-133">Resetování nevymaže návrhy sestav.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="e4b1e-134">Resetování nevymaže firemní ani uživatelská data, pokud není vybráno.</span><span class="sxs-lookup"><span data-stu-id="e4b1e-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
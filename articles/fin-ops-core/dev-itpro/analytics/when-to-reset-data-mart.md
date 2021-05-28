---
title: Kdy resetovat datové tržiště
description: V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988985"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="ba1d9-103">Kdy resetovat datové tržiště</span><span class="sxs-lookup"><span data-stu-id="ba1d9-103">When to reset a data mart</span></span>

<span data-ttu-id="ba1d9-104">Resetování datového tržiště může být časově náročné.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="ba1d9-105">V závislosti na okolnostech nemusí být tato akce řešením, které je potřeba.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="ba1d9-106">V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="ba1d9-107">Kdy je třeba provést reset datového tržiště?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="ba1d9-108">Před resetováním datového tržiště zvažte následující otázky.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="ba1d9-109">Odpověď ano na jednu nebo více otázek může znamenat, že vaše organizace může mít prospěch z resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="ba1d9-110">Byla obnovena databáze aplikací?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-110">Was the application database restored?</span></span>
- <span data-ttu-id="ba1d9-111">Otevřeli jste incident podpory a technik podpory vám dal pokyn resetovat datové tržiště jako součást kroku odstraňování problémů?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="ba1d9-112">Kdy není vhodné resetovat datové tržiště?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="ba1d9-113">Existují okolnosti, kdy nedoporučujeme resetovat datové tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="ba1d9-114">Mezi ně patří následující.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-114">These include the following.</span></span> 

- <span data-ttu-id="ba1d9-115">Máte problémy s výkonem spojené se synchronizací dat.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="ba1d9-116">Pokud máte opakující se vzor pro resetování z některého z následujících důvodů:</span><span class="sxs-lookup"><span data-stu-id="ba1d9-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="ba1d9-117">**Chybějící data**</span><span class="sxs-lookup"><span data-stu-id="ba1d9-117">**Missing data**</span></span> 
  - <span data-ttu-id="ba1d9-118">**Zaseknutý stav integrace**</span><span class="sxs-lookup"><span data-stu-id="ba1d9-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="ba1d9-119">**Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="ba1d9-120">Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="ba1d9-121">Co je resetování datového tržiště?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-121">What is a data mart reset?</span></span>
- <span data-ttu-id="ba1d9-122">Reset se spustí až po dokončení stávajících úkolů.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="ba1d9-123">Tím je zajištěno, že nebudou vložena stará data.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="ba1d9-124">V tomto okamžiku se může zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat kvůli aktivní úloze.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="ba1d9-125">Prosím zkuste to znovu později."</span><span class="sxs-lookup"><span data-stu-id="ba1d9-125">Please try again later.”</span></span>
- <span data-ttu-id="ba1d9-126">Reset deaktivuje integrační úlohy a vymaže všechna data datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="ba1d9-127">Integrace je znovu povolena.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="ba1d9-128">Pokud resetuji datové tržiště, přijdu o sestavy, které jsem již vytvořil?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="ba1d9-129">Ne, vaše sestavy jsou uloženy v tabulkách SQL, které nejsou ovlivněny resetem datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="ba1d9-130">Pokud se obáváte ztráty jakýchkoli sestav, které jste navrhli, můžete zálohovat návrhy, které nechcete ztratit.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="ba1d9-131">Chcete-li je zálohovat, otevřete návrhář sestav a přejděte na **Společnost > Společnosti > Stavební bloky > Export**.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="ba1d9-132">Je nutné, aby všichni uživatelé opustili systém a resetovali datové tržiště?</span><span class="sxs-lookup"><span data-stu-id="ba1d9-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="ba1d9-133">Ne, uživatelé mohou pokračovat v práci v systému během resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="ba1d9-134">Nebudou však mít přístup k žádným sestavám, které byly vytvořeny pomocí nástroje Financial Reporter, dokud nedojde k dokončení resetu.</span><span class="sxs-lookup"><span data-stu-id="ba1d9-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

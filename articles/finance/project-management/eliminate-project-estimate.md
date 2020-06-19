---
title: Eliminace odhadu projektu
description: Toto téma poskytuje informace o odstranění odhadu projektu po jeho dokončení.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410198"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="a0829-103">Eliminace odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="a0829-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0829-104">Odhady projektu poskytují finanční pohled na práci, která je odhadována a naplánována na projekt.</span><span class="sxs-lookup"><span data-stu-id="a0829-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="a0829-105">Chcete-li pracovat s odhady pro určitý projekt, je třeba tento projekt přiřadit k projektu odhadu.</span><span class="sxs-lookup"><span data-stu-id="a0829-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="a0829-106">Projekt odhadu je vždy založen na stávajícím projektu, ale jednotlivé projekty mohou odkazovat na jeden projekt odhadu.</span><span class="sxs-lookup"><span data-stu-id="a0829-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="a0829-107">K odhadu projektů lze připojit pouze investiční projekty s pevnou cenou a investiční projekty, které musí patřit do stejné skupiny projektů jako odhadovaný projekt.</span><span class="sxs-lookup"><span data-stu-id="a0829-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="a0829-108">Aby bylo možné projekt odhadu vyloučit, musí být kompletní.</span><span class="sxs-lookup"><span data-stu-id="a0829-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="a0829-109">Následující kroky vysvětlují, jak eliminovat odhad.</span><span class="sxs-lookup"><span data-stu-id="a0829-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="a0829-110">Přejděte na **Řízení projektu a účetnictví** > **Všechny projekty** a otevřete projekt.</span><span class="sxs-lookup"><span data-stu-id="a0829-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="a0829-111">Na kartě **Spravovat** vyberte **Odhady** a na stránce **Odhad** vyberte **Eliminovat**.</span><span class="sxs-lookup"><span data-stu-id="a0829-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="a0829-112">Na stránce **Eliminujte odhad** na kartě **Všeobecné** nastavte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="a0829-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="a0829-113">**Kód období**: Chcete-li vybrat vhodné projekty odhadu, vyberte kód období.</span><span class="sxs-lookup"><span data-stu-id="a0829-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="a0829-114">**Datum odhadu**: Vyberte příslušné datum odhadu pro eliminaci.</span><span class="sxs-lookup"><span data-stu-id="a0829-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="a0829-115">**Eliminovat s varováními WIP** : Povolte tuto možnost, chcete-li poskytovat upozornění, pokud bude eliminován odhad, který je spojen s nedokončenou prací (WIP).</span><span class="sxs-lookup"><span data-stu-id="a0829-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="a0829-116">Pokud tato možnost není povolena, eliminace nemůže pokračovat, pokud existují neočekávané transakce.</span><span class="sxs-lookup"><span data-stu-id="a0829-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="a0829-117">Tato možnost je k dispozici, pouze pokud je eliminace použita na odhadovaný projekt.</span><span class="sxs-lookup"><span data-stu-id="a0829-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="a0829-118">Není k dispozici, pokud používáte pravidelné účtování.</span><span class="sxs-lookup"><span data-stu-id="a0829-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="a0829-119">Toto nastavení pracuje s nastavením na kartě **Odhad** na stránce **Parametry projektu** ve skupině polí **Umožněte odstranění, pokud existují transakce bez odhadu**.</span><span class="sxs-lookup"><span data-stu-id="a0829-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="a0829-120">**Nastavte fázi na Dokončené**: Povolením této možnosti nastavíte fázi odhadu projektu na **Dokončeno** po spuštění eliminace.</span><span class="sxs-lookup"><span data-stu-id="a0829-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="a0829-121">**Tisk seznamu odhadu**: Vyberte informace, které mají být zahrnuty při tisku odhadu projektů.</span><span class="sxs-lookup"><span data-stu-id="a0829-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="a0829-122">**Zobrazit Infolog**: Povolením této možnosti zobrazíte Infolog.</span><span class="sxs-lookup"><span data-stu-id="a0829-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="a0829-123">**Datum zaúčtování**: Vyberte datum zaúčtování odhadu do účetní knihy.</span><span class="sxs-lookup"><span data-stu-id="a0829-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="a0829-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0829-124">Select **OK**.</span></span>
5. <span data-ttu-id="a0829-125">Po dokončení procesu eliminace se zobrazí projekt eliminovaného odhadu se zápornou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="a0829-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="a0829-126">Pokud jste nezamýšleli eliminovat odhad, můžete vybrat eliminovaný odhad a vybrat **Storno eliminace**.</span><span class="sxs-lookup"><span data-stu-id="a0829-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   

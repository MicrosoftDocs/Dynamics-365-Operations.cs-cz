---
title: Kontrola stavu experimentu
description: Toto téma vysvětluje, jaký stav má experiment v životním cyklu experimentování v Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930153"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="ee2dd-103">Kontrola stavu experimentu</span><span class="sxs-lookup"><span data-stu-id="ee2dd-103">Review the status of an experiment</span></span>
<span data-ttu-id="ee2dd-104">Nastavení a spuštění experimentu v Dynamics 365 Commerce zahrnuje mnoho kroků.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ee2dd-105">Informace o životním cyklu experimentování najdete v tématu [Experimentování v Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee2dd-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="ee2dd-106">Pokud se chcete dozvědět, kde v životním cyklu se experiment nachází, přejděte na kartu **Experimenty** v konfigurátoru webů.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="ee2dd-107">Zobrazí se seznam experimentů se stavem každého experimentu v Commerce i ve službě třetí strany, která se používá k povolení vytváření experimentů, přiřazování variant a analýze dat.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="ee2dd-108">Ve sloupci **Stav Commerce** se mohou zobrazit následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="ee2dd-109">**Koncept** – Experiment je připojen ke stránce nebo fragmentu v Commerce a je upravován.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="ee2dd-110">**Publikováno** – Varianty experimentu jsou připraveny k zobrazení na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="ee2dd-111">Pokud je experiment spuštěn ve službě třetí strany, uvidí uživatelé webu variantu stránky nebo fragmentu vybranou službou třetí strany.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="ee2dd-112">**Nepublikováno** – Experiment už na vašem webu není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="ee2dd-113">Pokud je experiment spuštěn ve službě třetí strany, uvidí uživatelé webu jen výchozí verzi stránky nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="ee2dd-114">**Dokončeno** – Experiment proběhl a varianta byla povýšena na živě publikovanou pro všechny uživatele webu.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="ee2dd-115">Podobně ve sloupci **Stav třetí strany** mohou být zobrazeny následující hodnoty, které označují, v jakém stavu se nachází experimenty ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="ee2dd-116">**Koncept** – Experiment je nastaven ve službě třetí strany, ale nebyl spuštěn.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="ee2dd-117">**Spuštěno** – Experiment byl spuštěn ve službě třetí strany a shromažďuje data.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="ee2dd-118">**Pozastaveno** – Experiment je pozastaven a neshromažďuje data.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="ee2dd-119">Pokud má experiment znovu shromažďovat data, musíte ho znovu spustit.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="ee2dd-120">**Archivováno** – Experiment proběhl a byl zařazen do katalogu ve službě třetí strany pro budoucí referenci.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="ee2dd-121">Schéma níže znázorňuje obě sady stavů a jejich vzájemný vztah.</span><span class="sxs-lookup"><span data-stu-id="ee2dd-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="ee2dd-122">[ ![Stavy experimentování](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ee2dd-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>

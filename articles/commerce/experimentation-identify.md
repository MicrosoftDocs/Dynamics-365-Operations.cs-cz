---
title: Identifikace hypotézy a určení metriky experimentu
description: Toto téma popisuje, jak identifikovat hypotézu a metriku úspěšnosti experimentu, který spouštíte na webu elektronického obchodu v Dynamics 365 Commerce.
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
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930154"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="c18d8-103">Identifikace hypotézy a určení metriky úspěšnosti experimentu</span><span class="sxs-lookup"><span data-stu-id="c18d8-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="c18d8-104">První fáze životního cyklu experimentování zahrnuje identifikování hypotézy experimentu a určení metriky, kterou budete sledovat k vyhodnocení úspěšnosti.</span><span class="sxs-lookup"><span data-stu-id="c18d8-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="c18d8-105">Následující schéma znázorňuje všechny kroky, které zahrnuje [nastavení a spuštění experimentu](experimentation-overview.md) na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c18d8-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c18d8-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="c18d8-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="c18d8-107">[ ![Cesta uživatele experimentováním – identifikace](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c18d8-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="c18d8-108">Hypotéza je tvrzení, ve kterém predikujete výsledek experimentu.</span><span class="sxs-lookup"><span data-stu-id="c18d8-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="c18d8-109">Do definování hypotézy vstupuje mnoho faktorů, například výzkum chování uživatelů a data webu, která jste shromáždili.</span><span class="sxs-lookup"><span data-stu-id="c18d8-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="c18d8-110">Pomocí hypotézy definujete předpoklad nebo teorii, které chcete ověřit experimentem.</span><span class="sxs-lookup"><span data-stu-id="c18d8-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="c18d8-111">Příkladem hypotézy pro váš experiment může být tvrzení, že „ *obrázek bílého trička na mé domovské stránce bude mít v letních měsících více kliknutí než tmavomodrý svetr, protože lidé chtějí v létě nosit něco lehkého a světlého.* ”</span><span class="sxs-lookup"><span data-stu-id="c18d8-111">An example of a hypothesis for your experiment may be " *a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.* "</span></span> <span data-ttu-id="c18d8-112">V takovém případě vytvoříte varianty, které budou zahrnovat bílé tričko a tmavomodrý svetr, a publikujete obě najednou.</span><span class="sxs-lookup"><span data-stu-id="c18d8-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="c18d8-113">K ověření hypotézy by měl být úspěch nebo neúspěch experimentu přímo svázán s akcemi uživatelů – například jestli uživatel webu klikne na určitý odkaz nebo tlačítko.</span><span class="sxs-lookup"><span data-stu-id="c18d8-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="c18d8-114">Tyto akce musí odpovídat událostem, které budou hlášeny službě třetí strany, která experiment sleduje.</span><span class="sxs-lookup"><span data-stu-id="c18d8-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="c18d8-115">V průběhu času se bude procento uživatelů, kteří provedou danou akci, načítat jako metrika, kterou můžete použít ke generování sestav a provádění analýz.</span><span class="sxs-lookup"><span data-stu-id="c18d8-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="c18d8-116">V článku [Události komponent Commerce pro diagnostiku a řešení potíží](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) se můžete podívat na všechny dostupné události a atributy.</span><span class="sxs-lookup"><span data-stu-id="c18d8-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c18d8-117">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="c18d8-117">Previous step</span></span>
[<span data-ttu-id="c18d8-118">Experimentování v Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c18d8-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="c18d8-119">Další krok</span><span class="sxs-lookup"><span data-stu-id="c18d8-119">Next step</span></span>
[<span data-ttu-id="c18d8-120">Nastavení experimentu</span><span class="sxs-lookup"><span data-stu-id="c18d8-120">Set up an experiment</span></span>](experimentation-setup.md)

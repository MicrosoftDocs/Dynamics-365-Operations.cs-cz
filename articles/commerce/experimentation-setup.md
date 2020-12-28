---
title: Nastavení experimentu
description: Toto téma popisuje, jak nastavit experiment ve službě třetí strany.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2020
ms.locfileid: "4410925"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="0e914-103">Nastavení experimentu</span><span class="sxs-lookup"><span data-stu-id="0e914-103">Set up an experiment</span></span>

<span data-ttu-id="0e914-104">Jakmile [definujete hypotézu a určíte, jakou metriku úspěšnosti chcete používat](experimentation-identify.md), budete svůj experiment muset nastavit ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="0e914-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="0e914-105">Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e914-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0e914-106">Další kroky jsou popsány v samostatných tématech.</span><span class="sxs-lookup"><span data-stu-id="0e914-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0e914-107">[ ![Cesta uživatele experimentováním – nastavení](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0e914-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="0e914-108">Nastavení experimentu ve službě třetí strany</span><span class="sxs-lookup"><span data-stu-id="0e914-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="0e914-109">Nyní už byste měli mít vybranou službu třetí strany, abyste mohli spustit a monitorovat svůj experiment a nastavit konektor experimentování.</span><span class="sxs-lookup"><span data-stu-id="0e914-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="0e914-110">Tyto předpoklady jsou uvedeny v tématu [Experimentování v Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0e914-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="0e914-111">Postupujte podle pokynů vyžadovaných k vytvoření experimentu ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="0e914-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="0e914-112">Pokud je konektor správně nakonfigurován, objeví se kompletní seznam experimentů, které nastavíte ve službě třetí strany, v konfigurátoru webů Commerce asi do 5 minut.</span><span class="sxs-lookup"><span data-stu-id="0e914-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="0e914-113">Nastavení metriky úspěšnosti</span><span class="sxs-lookup"><span data-stu-id="0e914-113">Set up your success metrics</span></span>
<span data-ttu-id="0e914-114">Každý experiment potřebuje metriku k měření dopadu variant a k ověření hypotézy.</span><span class="sxs-lookup"><span data-stu-id="0e914-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="0e914-115">Postupem podle pokynů níže povolte výpočet metriky ve službě třetí strany pomocí událostí živé telemetrie z Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e914-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0e914-116">Chcete-li nastavit metriku úspěšnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="0e914-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="0e914-117">V konfigurátoru webů Commerce vyberte kartu **Stránky** v levém navigačním podokně a pak vyberte stránku, pro kterou chcete metriku shromažďovat.</span><span class="sxs-lookup"><span data-stu-id="0e914-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="0e914-118">Přejděte do části **Sledovaná ID událostí** v pravém podokně vlastností stránky nebo modulu, který chcete sledovat.</span><span class="sxs-lookup"><span data-stu-id="0e914-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="0e914-119">Vyberte **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="0e914-119">Select **View**.</span></span> <span data-ttu-id="0e914-120">Zobrazí se seznam všech ID událostí.</span><span class="sxs-lookup"><span data-stu-id="0e914-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="0e914-121">Zkopírujte událost, kterou chcete sledovat, a vložte klíč této události do určeného umístění ve službě třetí strany.</span><span class="sxs-lookup"><span data-stu-id="0e914-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="0e914-122">Pokud potřebujete více událostí, zkopírujte klíče postupně po jednom.</span><span class="sxs-lookup"><span data-stu-id="0e914-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="0e914-123">Informace o tom, jak zobrazit všechny dostupné události a atributy včetně počtu zobrazení stránky a sledování tržeb, najdete v tématu [Události komponent Commerce pro diagnostiku a řešení potíží](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="0e914-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="0e914-124">Proveďte všechny další kroky pro sledování metriky vyžadované službou třetí strany.</span><span class="sxs-lookup"><span data-stu-id="0e914-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0e914-125">Předchozí krok</span><span class="sxs-lookup"><span data-stu-id="0e914-125">Previous step</span></span>
[<span data-ttu-id="0e914-126">Identifikace hypotézy a určení metriky experimentu</span><span class="sxs-lookup"><span data-stu-id="0e914-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="0e914-127">Další krok</span><span class="sxs-lookup"><span data-stu-id="0e914-127">Next step</span></span>
[<span data-ttu-id="0e914-128">Připojení a úpravy experimentu</span><span class="sxs-lookup"><span data-stu-id="0e914-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

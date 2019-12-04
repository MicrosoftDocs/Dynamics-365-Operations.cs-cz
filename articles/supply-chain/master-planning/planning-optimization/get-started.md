---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773915"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="daad8-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="daad8-104">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="daad8-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="daad8-105">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="daad8-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="daad8-106">Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="daad8-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="daad8-107">Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.</span><span class="sxs-lookup"><span data-stu-id="daad8-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="daad8-108">Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="daad8-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="daad8-109">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="daad8-110">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="daad8-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="daad8-111">Licencování</span><span class="sxs-lookup"><span data-stu-id="daad8-111">Licensing</span></span>

<span data-ttu-id="daad8-112">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="daad8-113">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="daad8-113">Install the add-in</span></span>

<span data-ttu-id="daad8-114">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="daad8-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="daad8-115">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="daad8-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="daad8-116">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="daad8-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="daad8-117">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="daad8-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="daad8-118">Vyberte **Správa** nebo přejděte na pevnou záložku **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="daad8-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="daad8-119">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="daad8-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="daad8-120">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="daad8-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="daad8-121">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="daad8-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="daad8-122">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="daad8-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="daad8-123">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-123">Planning Optimization integration</span></span>

<span data-ttu-id="daad8-124">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Integrace optimalizace plánování** \> **Parametry integrace**.</span><span class="sxs-lookup"><span data-stu-id="daad8-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="daad8-125">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="daad8-125">Connection status</span></span>

<span data-ttu-id="daad8-126">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="daad8-127">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="daad8-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="daad8-128">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="daad8-128">Connection status</span></span> | <span data-ttu-id="daad8-129">Popis</span><span class="sxs-lookup"><span data-stu-id="daad8-129">Description</span></span> | <span data-ttu-id="daad8-130">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="daad8-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="daad8-131">Připojeno</span><span class="sxs-lookup"><span data-stu-id="daad8-131">Connected</span></span> | <span data-ttu-id="daad8-132">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="daad8-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="daad8-133">Ano</span><span class="sxs-lookup"><span data-stu-id="daad8-133">Yes</span></span> |
| <span data-ttu-id="daad8-134">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="daad8-134">Enabling connection</span></span> | <span data-ttu-id="daad8-135">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="daad8-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="daad8-136">Ne</span><span class="sxs-lookup"><span data-stu-id="daad8-136">No</span></span> |
| <span data-ttu-id="daad8-137">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="daad8-137">Disconnected</span></span> | <span data-ttu-id="daad8-138">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="daad8-139">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="daad8-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="daad8-140">Ne</span><span class="sxs-lookup"><span data-stu-id="daad8-140">No</span></span> |
| <span data-ttu-id="daad8-141">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="daad8-141">Disabling connection</span></span> | <span data-ttu-id="daad8-142">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="daad8-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="daad8-143">Ne</span><span class="sxs-lookup"><span data-stu-id="daad8-143">No</span></span> |
| <span data-ttu-id="daad8-144">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="daad8-144">Getting status</span></span> | <span data-ttu-id="daad8-145">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="daad8-146">Ne</span><span class="sxs-lookup"><span data-stu-id="daad8-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="daad8-147">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="daad8-148">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="daad8-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="daad8-149">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="daad8-150">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="daad8-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="daad8-151">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="daad8-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="daad8-152">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="daad8-152">Integration with the setup</span></span>

<span data-ttu-id="daad8-153">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="daad8-154">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="daad8-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="daad8-155">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="daad8-155">Related resources</span></span>

[<span data-ttu-id="daad8-156">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="daad8-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="daad8-157">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="daad8-158">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="daad8-159">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="daad8-160">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="daad8-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="daad8-161">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="daad8-161">Cancel a planning job</span></span>](cancel-planning-job.md)

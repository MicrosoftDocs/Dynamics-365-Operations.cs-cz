---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339871"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="0b5ab-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b5ab-104">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b5ab-105">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="0b5ab-106">Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0b5ab-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="0b5ab-107">Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="0b5ab-108">Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="0b5ab-109">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="0b5ab-110">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="0b5ab-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="0b5ab-111">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="0b5ab-111">Availability</span></span>
<span data-ttu-id="0b5ab-112">Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Velká Británie a Austrálie.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="0b5ab-113">Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="0b5ab-114">Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="0b5ab-115">Licence</span><span class="sxs-lookup"><span data-stu-id="0b5ab-115">Licensing</span></span>

<span data-ttu-id="0b5ab-116">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="0b5ab-117">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="0b5ab-117">Install the add-in</span></span>

<span data-ttu-id="0b5ab-118">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b5ab-119">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="0b5ab-120">Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="0b5ab-121">Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="0b5ab-122">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="0b5ab-123">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="0b5ab-124">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="0b5ab-125">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="0b5ab-126">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="0b5ab-127">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="0b5ab-128">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-128">Select **Install**.</span></span>
1. <span data-ttu-id="0b5ab-129">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="0b5ab-130">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="0b5ab-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="0b5ab-131">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="0b5ab-132">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-132">Planning Optimization integration</span></span>

<span data-ttu-id="0b5ab-133">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="0b5ab-134">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="0b5ab-134">Connection status</span></span>

<span data-ttu-id="0b5ab-135">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="0b5ab-136">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="0b5ab-137">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="0b5ab-137">Connection status</span></span> | <span data-ttu-id="0b5ab-138">Popis</span><span class="sxs-lookup"><span data-stu-id="0b5ab-138">Description</span></span> | <span data-ttu-id="0b5ab-139">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="0b5ab-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="0b5ab-140">Připojeno</span><span class="sxs-lookup"><span data-stu-id="0b5ab-140">Connected</span></span> | <span data-ttu-id="0b5ab-141">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="0b5ab-142">Ano</span><span class="sxs-lookup"><span data-stu-id="0b5ab-142">Yes</span></span> |
| <span data-ttu-id="0b5ab-143">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="0b5ab-143">Enabling connection</span></span> | <span data-ttu-id="0b5ab-144">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0b5ab-145">Ne</span><span class="sxs-lookup"><span data-stu-id="0b5ab-145">No</span></span> |
| <span data-ttu-id="0b5ab-146">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="0b5ab-146">Disconnected</span></span> | <span data-ttu-id="0b5ab-147">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="0b5ab-148">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="0b5ab-149">Ne</span><span class="sxs-lookup"><span data-stu-id="0b5ab-149">No</span></span> |
| <span data-ttu-id="0b5ab-150">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="0b5ab-150">Disabling connection</span></span> | <span data-ttu-id="0b5ab-151">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0b5ab-152">Ne</span><span class="sxs-lookup"><span data-stu-id="0b5ab-152">No</span></span> |
| <span data-ttu-id="0b5ab-153">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="0b5ab-153">Getting status</span></span> | <span data-ttu-id="0b5ab-154">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="0b5ab-155">Ne</span><span class="sxs-lookup"><span data-stu-id="0b5ab-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="0b5ab-156">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="0b5ab-157">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="0b5ab-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="0b5ab-158">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="0b5ab-159">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0b5ab-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="0b5ab-160">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="0b5ab-161">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="0b5ab-161">Integration with the setup</span></span>

<span data-ttu-id="0b5ab-162">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="0b5ab-163">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="0b5ab-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b5ab-164">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0b5ab-164">Additional resources</span></span>

[<span data-ttu-id="0b5ab-165">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="0b5ab-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="0b5ab-166">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0b5ab-167">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0b5ab-168">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0b5ab-169">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="0b5ab-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="0b5ab-170">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="0b5ab-170">Cancel a planning job</span></span>](cancel-planning-job.md)

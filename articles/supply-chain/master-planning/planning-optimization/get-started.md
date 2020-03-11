---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
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
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076125"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="85166-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="85166-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85166-104">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85166-105">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="85166-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="85166-106">Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="85166-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="85166-107">Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.</span><span class="sxs-lookup"><span data-stu-id="85166-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="85166-108">Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="85166-109">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="85166-110">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="85166-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="85166-111">Licencování</span><span class="sxs-lookup"><span data-stu-id="85166-111">Licensing</span></span>

<span data-ttu-id="85166-112">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="85166-113">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="85166-113">Install the add-in</span></span>

<span data-ttu-id="85166-114">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85166-115">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="85166-116">Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností (ne OneBox prostředí) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="85166-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="85166-117">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="85166-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="85166-118">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="85166-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="85166-119">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="85166-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="85166-120">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="85166-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="85166-121">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="85166-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="85166-122">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="85166-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="85166-123">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="85166-123">Select **Install**.</span></span>
1. <span data-ttu-id="85166-124">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="85166-125">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="85166-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="85166-126">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="85166-127">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="85166-127">Planning Optimization integration</span></span>

<span data-ttu-id="85166-128">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="85166-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="85166-129">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="85166-129">Connection status</span></span>

<span data-ttu-id="85166-130">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="85166-131">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="85166-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="85166-132">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="85166-132">Connection status</span></span> | <span data-ttu-id="85166-133">Popis</span><span class="sxs-lookup"><span data-stu-id="85166-133">Description</span></span> | <span data-ttu-id="85166-134">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="85166-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="85166-135">Připojeno</span><span class="sxs-lookup"><span data-stu-id="85166-135">Connected</span></span> | <span data-ttu-id="85166-136">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85166-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="85166-137">Ano</span><span class="sxs-lookup"><span data-stu-id="85166-137">Yes</span></span> |
| <span data-ttu-id="85166-138">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="85166-138">Enabling connection</span></span> | <span data-ttu-id="85166-139">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="85166-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="85166-140">Ne</span><span class="sxs-lookup"><span data-stu-id="85166-140">No</span></span> |
| <span data-ttu-id="85166-141">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="85166-141">Disconnected</span></span> | <span data-ttu-id="85166-142">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="85166-143">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="85166-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="85166-144">Ne</span><span class="sxs-lookup"><span data-stu-id="85166-144">No</span></span> |
| <span data-ttu-id="85166-145">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="85166-145">Disabling connection</span></span> | <span data-ttu-id="85166-146">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="85166-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="85166-147">Ne</span><span class="sxs-lookup"><span data-stu-id="85166-147">No</span></span> |
| <span data-ttu-id="85166-148">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="85166-148">Getting status</span></span> | <span data-ttu-id="85166-149">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="85166-150">Ne</span><span class="sxs-lookup"><span data-stu-id="85166-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="85166-151">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="85166-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="85166-152">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="85166-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="85166-153">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="85166-154">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="85166-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="85166-155">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="85166-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="85166-156">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="85166-156">Integration with the setup</span></span>

<span data-ttu-id="85166-157">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="85166-158">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="85166-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="85166-159">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="85166-159">Related resources</span></span>

[<span data-ttu-id="85166-160">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="85166-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="85166-161">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="85166-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="85166-162">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="85166-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="85166-163">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="85166-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="85166-164">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="85166-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="85166-165">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="85166-165">Cancel a planning job</span></span>](cancel-planning-job.md)

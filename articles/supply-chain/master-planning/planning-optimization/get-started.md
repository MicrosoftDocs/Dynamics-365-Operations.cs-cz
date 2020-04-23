---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213508"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="5d312-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d312-104">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5d312-105">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="5d312-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="5d312-106">Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5d312-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="5d312-107">Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.</span><span class="sxs-lookup"><span data-stu-id="5d312-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="5d312-108">Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="5d312-109">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="5d312-110">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="5d312-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="5d312-111">Licencování</span><span class="sxs-lookup"><span data-stu-id="5d312-111">Licensing</span></span>

<span data-ttu-id="5d312-112">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="5d312-113">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="5d312-113">Install the add-in</span></span>

<span data-ttu-id="5d312-114">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5d312-115">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="5d312-116">Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností (ne OneBox prostředí) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="5d312-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="5d312-117">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="5d312-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="5d312-118">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="5d312-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="5d312-119">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="5d312-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="5d312-120">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="5d312-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="5d312-121">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="5d312-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="5d312-122">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="5d312-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="5d312-123">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="5d312-123">Select **Install**.</span></span>
1. <span data-ttu-id="5d312-124">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="5d312-125">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="5d312-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="5d312-126">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="5d312-127">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-127">Planning Optimization integration</span></span>

<span data-ttu-id="5d312-128">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="5d312-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="5d312-129">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="5d312-129">Connection status</span></span>

<span data-ttu-id="5d312-130">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="5d312-131">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5d312-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="5d312-132">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="5d312-132">Connection status</span></span> | <span data-ttu-id="5d312-133">Popis</span><span class="sxs-lookup"><span data-stu-id="5d312-133">Description</span></span> | <span data-ttu-id="5d312-134">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="5d312-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="5d312-135">Připojeno</span><span class="sxs-lookup"><span data-stu-id="5d312-135">Connected</span></span> | <span data-ttu-id="5d312-136">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d312-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="5d312-137">Ano</span><span class="sxs-lookup"><span data-stu-id="5d312-137">Yes</span></span> |
| <span data-ttu-id="5d312-138">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="5d312-138">Enabling connection</span></span> | <span data-ttu-id="5d312-139">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="5d312-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5d312-140">Ne</span><span class="sxs-lookup"><span data-stu-id="5d312-140">No</span></span> |
| <span data-ttu-id="5d312-141">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="5d312-141">Disconnected</span></span> | <span data-ttu-id="5d312-142">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="5d312-143">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5d312-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="5d312-144">Ne</span><span class="sxs-lookup"><span data-stu-id="5d312-144">No</span></span> |
| <span data-ttu-id="5d312-145">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="5d312-145">Disabling connection</span></span> | <span data-ttu-id="5d312-146">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="5d312-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5d312-147">Ne</span><span class="sxs-lookup"><span data-stu-id="5d312-147">No</span></span> |
| <span data-ttu-id="5d312-148">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="5d312-148">Getting status</span></span> | <span data-ttu-id="5d312-149">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="5d312-150">Ne</span><span class="sxs-lookup"><span data-stu-id="5d312-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="5d312-151">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="5d312-152">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="5d312-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="5d312-153">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="5d312-154">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d312-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="5d312-155">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="5d312-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="5d312-156">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="5d312-156">Integration with the setup</span></span>

<span data-ttu-id="5d312-157">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="5d312-158">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="5d312-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5d312-159">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="5d312-159">Related resources</span></span>

[<span data-ttu-id="5d312-160">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="5d312-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="5d312-161">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5d312-162">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5d312-163">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5d312-164">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="5d312-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5d312-165">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="5d312-165">Cancel a planning job</span></span>](cancel-planning-job.md)

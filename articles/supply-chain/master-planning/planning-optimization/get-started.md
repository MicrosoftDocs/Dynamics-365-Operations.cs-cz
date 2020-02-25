---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971457"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="c9a23-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="c9a23-104">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c9a23-105">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="c9a23-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="c9a23-106">Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c9a23-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="c9a23-107">Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.</span><span class="sxs-lookup"><span data-stu-id="c9a23-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="c9a23-108">Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="c9a23-109">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="c9a23-110">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="c9a23-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="c9a23-111">Licencování</span><span class="sxs-lookup"><span data-stu-id="c9a23-111">Licensing</span></span>

<span data-ttu-id="c9a23-112">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="c9a23-113">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="c9a23-113">Install the add-in</span></span>

<span data-ttu-id="c9a23-114">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c9a23-115">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="c9a23-116">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="c9a23-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="c9a23-117">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="c9a23-118">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="c9a23-119">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="c9a23-120">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="c9a23-121">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="c9a23-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="c9a23-122">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-122">Select **Install**.</span></span>
1. <span data-ttu-id="c9a23-123">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="c9a23-124">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="c9a23-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="c9a23-125">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="c9a23-126">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-126">Planning Optimization integration</span></span>

<span data-ttu-id="c9a23-127">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="c9a23-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="c9a23-128">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="c9a23-128">Connection status</span></span>

<span data-ttu-id="c9a23-129">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="c9a23-130">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="c9a23-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="c9a23-131">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="c9a23-131">Connection status</span></span> | <span data-ttu-id="c9a23-132">Popis</span><span class="sxs-lookup"><span data-stu-id="c9a23-132">Description</span></span> | <span data-ttu-id="c9a23-133">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="c9a23-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="c9a23-134">Připojeno</span><span class="sxs-lookup"><span data-stu-id="c9a23-134">Connected</span></span> | <span data-ttu-id="c9a23-135">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c9a23-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="c9a23-136">Ano</span><span class="sxs-lookup"><span data-stu-id="c9a23-136">Yes</span></span> |
| <span data-ttu-id="c9a23-137">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="c9a23-137">Enabling connection</span></span> | <span data-ttu-id="c9a23-138">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="c9a23-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="c9a23-139">Ne</span><span class="sxs-lookup"><span data-stu-id="c9a23-139">No</span></span> |
| <span data-ttu-id="c9a23-140">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="c9a23-140">Disconnected</span></span> | <span data-ttu-id="c9a23-141">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="c9a23-142">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="c9a23-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="c9a23-143">Ne</span><span class="sxs-lookup"><span data-stu-id="c9a23-143">No</span></span> |
| <span data-ttu-id="c9a23-144">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="c9a23-144">Disabling connection</span></span> | <span data-ttu-id="c9a23-145">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="c9a23-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="c9a23-146">Ne</span><span class="sxs-lookup"><span data-stu-id="c9a23-146">No</span></span> |
| <span data-ttu-id="c9a23-147">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="c9a23-147">Getting status</span></span> | <span data-ttu-id="c9a23-148">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="c9a23-149">Ne</span><span class="sxs-lookup"><span data-stu-id="c9a23-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="c9a23-150">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="c9a23-151">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="c9a23-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="c9a23-152">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="c9a23-153">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c9a23-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="c9a23-154">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="c9a23-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="c9a23-155">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="c9a23-155">Integration with the setup</span></span>

<span data-ttu-id="c9a23-156">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="c9a23-157">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="c9a23-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c9a23-158">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="c9a23-158">Related resources</span></span>

[<span data-ttu-id="c9a23-159">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="c9a23-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="c9a23-160">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c9a23-161">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c9a23-162">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c9a23-163">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="c9a23-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="c9a23-164">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="c9a23-164">Cancel a planning job</span></span>](cancel-planning-job.md)

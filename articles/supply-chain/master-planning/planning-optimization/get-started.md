---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973469"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="18c03-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18c03-104">Tak jak bylo [dříve oznámeno](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), optimalizace plánování nahradí stávající integrovaný hlavní plánovací modul.</span><span class="sxs-lookup"><span data-stu-id="18c03-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="18c03-105">Pokud aktuálně používáte integrovaný hlavní plánovací modul, měli byste nyní začít plánovat migraci na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="18c03-106">Je důležité zahájit proces migrace co nejdříve, protože při vynucení ukončení podpory může dojít k ovlivnění vašich operací.</span><span class="sxs-lookup"><span data-stu-id="18c03-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="18c03-107">Abyste se vyhnuli problémům na poslední chvíli při vynuceném ukončení podpory, důrazně doporučujeme dokončit migraci před 1. prosincem 2020.</span><span class="sxs-lookup"><span data-stu-id="18c03-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="18c03-108">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="18c03-109">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="18c03-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="18c03-110">Funkce Optimalizace plánování není ve výchozím nastavení ve službě Dynamics Lifecycle Services (LCS) zapnutá, takže si ji můžete před zapnutím vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="18c03-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="18c03-111">Pokud váš hlavní plánovací proces nezahrnuje produkci (hlavní plánování generovalo plánované výrobní zakázky) a vyžadujete vestavěný hlavní plánovací stroj verze vyšší než 10.0.15, musíte požádat o výjimku z migrace na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="18c03-112">Počínaje verzí 10.0.16 se v prostředích zobrazí chyba při spuštění integrovaného hlavního plánování bez generování plánovaných výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="18c03-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="18c03-113">Optimalizace plánování by se měla použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="18c03-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="18c03-114">Vlastníci stávajících prostředí, na nichž běží vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky.</span><span class="sxs-lookup"><span data-stu-id="18c03-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="18c03-115">Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.</span><span class="sxs-lookup"><span data-stu-id="18c03-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="18c03-116">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="18c03-117">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="18c03-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="18c03-118">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="18c03-118">Availability</span></span>
<span data-ttu-id="18c03-119">Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Velká Británie a Austrálie.</span><span class="sxs-lookup"><span data-stu-id="18c03-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="18c03-120">Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována.</span><span class="sxs-lookup"><span data-stu-id="18c03-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="18c03-121">Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="18c03-122">Licence</span><span class="sxs-lookup"><span data-stu-id="18c03-122">Licensing</span></span>

<span data-ttu-id="18c03-123">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="18c03-124">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="18c03-124">Install the add-in</span></span>

<span data-ttu-id="18c03-125">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="18c03-126">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="18c03-127">Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="18c03-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="18c03-128">Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.</span><span class="sxs-lookup"><span data-stu-id="18c03-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="18c03-129">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="18c03-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="18c03-130">Přejděte na **Úplné podrobnosti** .</span><span class="sxs-lookup"><span data-stu-id="18c03-130">Go to **Full details** .</span></span>
1. <span data-ttu-id="18c03-131">Přejděte na záložku s náhledem **Doplňky prostředí** .</span><span class="sxs-lookup"><span data-stu-id="18c03-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="18c03-132">Vyberte možnost **Nainstalovat nový doplněk** .</span><span class="sxs-lookup"><span data-stu-id="18c03-132">Select **Install a new add-in** .</span></span>
1. <span data-ttu-id="18c03-133">Vyberte **Optimalizace plánování** .</span><span class="sxs-lookup"><span data-stu-id="18c03-133">Select **Planning Optimization** .</span></span>
1. <span data-ttu-id="18c03-134">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="18c03-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="18c03-135">Vyberte **Instalovat** .</span><span class="sxs-lookup"><span data-stu-id="18c03-135">Select **Install** .</span></span>
1. <span data-ttu-id="18c03-136">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="18c03-137">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="18c03-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="18c03-138">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="18c03-139">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-139">Planning Optimization integration</span></span>

<span data-ttu-id="18c03-140">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování** .</span><span class="sxs-lookup"><span data-stu-id="18c03-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters** .</span></span>

#### <a name="connection-status"></a><span data-ttu-id="18c03-141">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="18c03-141">Connection status</span></span>

<span data-ttu-id="18c03-142">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="18c03-143">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="18c03-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="18c03-144">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="18c03-144">Connection status</span></span> | <span data-ttu-id="18c03-145">Popis</span><span class="sxs-lookup"><span data-stu-id="18c03-145">Description</span></span> | <span data-ttu-id="18c03-146">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="18c03-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="18c03-147">Připojeno</span><span class="sxs-lookup"><span data-stu-id="18c03-147">Connected</span></span> | <span data-ttu-id="18c03-148">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18c03-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="18c03-149">Ano</span><span class="sxs-lookup"><span data-stu-id="18c03-149">Yes</span></span> |
| <span data-ttu-id="18c03-150">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="18c03-150">Enabling connection</span></span> | <span data-ttu-id="18c03-151">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="18c03-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="18c03-152">Ne</span><span class="sxs-lookup"><span data-stu-id="18c03-152">No</span></span> |
| <span data-ttu-id="18c03-153">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="18c03-153">Disconnected</span></span> | <span data-ttu-id="18c03-154">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="18c03-155">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="18c03-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="18c03-156">Ne</span><span class="sxs-lookup"><span data-stu-id="18c03-156">No</span></span> |
| <span data-ttu-id="18c03-157">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="18c03-157">Disabling connection</span></span> | <span data-ttu-id="18c03-158">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="18c03-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="18c03-159">Ne</span><span class="sxs-lookup"><span data-stu-id="18c03-159">No</span></span> |
| <span data-ttu-id="18c03-160">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="18c03-160">Getting status</span></span> | <span data-ttu-id="18c03-161">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="18c03-162">Ne</span><span class="sxs-lookup"><span data-stu-id="18c03-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="18c03-163">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="18c03-164">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="18c03-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="18c03-165">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="18c03-166">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="18c03-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="18c03-167">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano** , tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="18c03-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes** , those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="18c03-168">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="18c03-168">Integration with the setup</span></span>

<span data-ttu-id="18c03-169">Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="18c03-170">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="18c03-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18c03-171">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="18c03-171">Additional resources</span></span>

[<span data-ttu-id="18c03-172">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="18c03-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="18c03-173">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="18c03-174">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="18c03-175">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="18c03-176">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="18c03-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="18c03-177">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="18c03-177">Cancel a planning job</span></span>](cancel-planning-job.md)

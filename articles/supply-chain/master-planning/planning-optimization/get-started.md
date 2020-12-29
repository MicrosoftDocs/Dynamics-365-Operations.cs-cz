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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424259"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="f60e6-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f60e6-104">Tak jak bylo [dříve oznámeno](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), optimalizace plánování nahradí stávající integrovaný hlavní plánovací modul.</span><span class="sxs-lookup"><span data-stu-id="f60e6-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="f60e6-105">Pokud aktuálně používáte integrovaný hlavní plánovací modul, měli byste nyní začít plánovat migraci na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="f60e6-106">Je důležité zahájit proces migrace co nejdříve, protože při vynucení ukončení podpory může dojít k ovlivnění vašich operací.</span><span class="sxs-lookup"><span data-stu-id="f60e6-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="f60e6-107">Abyste se vyhnuli problémům na poslední chvíli při vynuceném ukončení podpory, důrazně doporučujeme dokončit migraci před 1. prosincem 2020.</span><span class="sxs-lookup"><span data-stu-id="f60e6-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="f60e6-108">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="f60e6-109">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="f60e6-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="f60e6-110">Funkce Optimalizace plánování není ve výchozím nastavení ve službě Dynamics Lifecycle Services (LCS) zapnutá, takže si ji můžete před zapnutím vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="f60e6-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="f60e6-111">Pokud váš hlavní plánovací proces nezahrnuje produkci (hlavní plánování generovalo plánované výrobní zakázky) a vyžadujete vestavěný hlavní plánovací stroj verze vyšší než 10.0.15, musíte požádat o výjimku z migrace na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="f60e6-112">Počínaje verzí 10.0.16 se v prostředích zobrazí chyba při spuštění integrovaného hlavního plánování bez generování plánovaných výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="f60e6-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="f60e6-113">Optimalizace plánování by se měla použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="f60e6-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="f60e6-114">Vlastníci stávajících prostředí, na nichž běží vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky.</span><span class="sxs-lookup"><span data-stu-id="f60e6-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="f60e6-115">Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.</span><span class="sxs-lookup"><span data-stu-id="f60e6-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="f60e6-116">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="f60e6-117">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="f60e6-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="f60e6-118">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="f60e6-118">Availability</span></span>
<span data-ttu-id="f60e6-119">Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Velká Británie a Austrálie.</span><span class="sxs-lookup"><span data-stu-id="f60e6-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="f60e6-120">Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována.</span><span class="sxs-lookup"><span data-stu-id="f60e6-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="f60e6-121">Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="f60e6-122">Licence</span><span class="sxs-lookup"><span data-stu-id="f60e6-122">Licensing</span></span>

<span data-ttu-id="f60e6-123">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="f60e6-124">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="f60e6-124">Install the add-in</span></span>

<span data-ttu-id="f60e6-125">Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f60e6-126">Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="f60e6-127">Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="f60e6-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="f60e6-128">Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.</span><span class="sxs-lookup"><span data-stu-id="f60e6-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="f60e6-129">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="f60e6-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="f60e6-130">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="f60e6-131">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="f60e6-132">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="f60e6-133">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="f60e6-134">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="f60e6-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="f60e6-135">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-135">Select **Install**.</span></span>
1. <span data-ttu-id="f60e6-136">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="f60e6-137">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="f60e6-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="f60e6-138">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f60e6-139">Hlavním účelem instalace doplňku Optimalizace plánování je propojení služby a prostředí.</span><span class="sxs-lookup"><span data-stu-id="f60e6-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="f60e6-140">Proto musíte doplněk nainstalovat samostatně do každého prostředí, kde budete používat optimalizaci plánování, bez ohledu na jakýkoli kód přesunutý mezi prostředími.</span><span class="sxs-lookup"><span data-stu-id="f60e6-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="f60e6-141">Integrace optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-141">Planning Optimization integration</span></span>

<span data-ttu-id="f60e6-142">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="f60e6-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="f60e6-143">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="f60e6-143">Connection status</span></span>

<span data-ttu-id="f60e6-144">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="f60e6-145">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f60e6-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="f60e6-146">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="f60e6-146">Connection status</span></span> | <span data-ttu-id="f60e6-147">Popis</span><span class="sxs-lookup"><span data-stu-id="f60e6-147">Description</span></span> | <span data-ttu-id="f60e6-148">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="f60e6-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="f60e6-149">Připojeno</span><span class="sxs-lookup"><span data-stu-id="f60e6-149">Connected</span></span> | <span data-ttu-id="f60e6-150">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f60e6-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="f60e6-151">Ano</span><span class="sxs-lookup"><span data-stu-id="f60e6-151">Yes</span></span> |
| <span data-ttu-id="f60e6-152">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="f60e6-152">Enabling connection</span></span> | <span data-ttu-id="f60e6-153">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="f60e6-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f60e6-154">Ne</span><span class="sxs-lookup"><span data-stu-id="f60e6-154">No</span></span> |
| <span data-ttu-id="f60e6-155">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="f60e6-155">Disconnected</span></span> | <span data-ttu-id="f60e6-156">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="f60e6-157">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f60e6-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="f60e6-158">Ne</span><span class="sxs-lookup"><span data-stu-id="f60e6-158">No</span></span> |
| <span data-ttu-id="f60e6-159">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="f60e6-159">Disabling connection</span></span> | <span data-ttu-id="f60e6-160">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="f60e6-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f60e6-161">Ne</span><span class="sxs-lookup"><span data-stu-id="f60e6-161">No</span></span> |
| <span data-ttu-id="f60e6-162">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="f60e6-162">Getting status</span></span> | <span data-ttu-id="f60e6-163">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="f60e6-164">Ne</span><span class="sxs-lookup"><span data-stu-id="f60e6-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="f60e6-165">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="f60e6-166">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="f60e6-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="f60e6-167">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="f60e6-168">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f60e6-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="f60e6-169">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="f60e6-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="f60e6-170">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="f60e6-170">Integration with the setup</span></span>

<span data-ttu-id="f60e6-171">Je-li zapnuta optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="f60e6-172">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="f60e6-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f60e6-173">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f60e6-173">Additional resources</span></span>

[<span data-ttu-id="f60e6-174">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="f60e6-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="f60e6-175">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f60e6-176">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f60e6-177">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f60e6-178">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="f60e6-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="f60e6-179">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="f60e6-179">Cancel a planning job</span></span>](cancel-planning-job.md)

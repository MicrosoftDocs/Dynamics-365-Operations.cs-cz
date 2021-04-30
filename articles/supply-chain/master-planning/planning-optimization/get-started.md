---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d346251e82737624edfce88dc7b2ee10280f6877
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907660"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="f9e6b-103">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9e6b-104">Tak jak bylo [dříve oznámeno](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), optimalizace plánování nahradí stávající integrovaný hlavní plánovací modul.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="f9e6b-105">Pokud aktuálně používáte integrovaný hlavní plánovací modul, měli byste nyní začít plánovat migraci na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="f9e6b-106">Je důležité zahájit proces migrace co nejdříve, protože při vynucení ukončení podpory může dojít k ovlivnění vašich operací.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="f9e6b-107">Abyste se vyhnuli problémům na poslední chvíli při vynuceném ukončení podpory, důrazně doporučujeme dokončit migraci před 1. prosincem 2020.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="f9e6b-108">Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="f9e6b-109">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="f9e6b-110">Funkce Optimalizace plánování není ve výchozím nastavení ve službě Dynamics Lifecycle Services (LCS) zapnutá, takže si ji můžete před zapnutím vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e6b-111">Pokud váš hlavní plánovací proces nezahrnuje produkci (hlavní plánování generovalo plánované výrobní zakázky) a vyžadujete vestavěný hlavní plánovací stroj verze vyšší než 10.0.15, musíte požádat o výjimku z migrace na optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="f9e6b-112">Počínaje verzí 10.0.16 se v prostředích zobrazí chyba při spuštění integrovaného hlavního plánování bez generování plánovaných výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="f9e6b-113">Optimalizace plánování by se měla použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="f9e6b-114">Vlastníci stávajících prostředí, na nichž běží vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="f9e6b-115">Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="f9e6b-116">Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="f9e6b-117">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="f9e6b-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="f9e6b-118">Dostupnost</span><span class="sxs-lookup"><span data-stu-id="f9e6b-118">Availability</span></span>

<span data-ttu-id="f9e6b-119">Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Velká Británie, Austrálie a Asie a Tichomoří.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="f9e6b-120">Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="f9e6b-121">Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="f9e6b-122">Licence</span><span class="sxs-lookup"><span data-stu-id="f9e6b-122">Licensing</span></span>

<span data-ttu-id="f9e6b-123">Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="f9e6b-124">Instalace a povolení optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="f9e6b-125">Chcete-li použít optimalizaci plánování, musí mít systém zavedené všechny předpoklady a poté povolit svůj licenční klíč a nainstalovat doplněk Optimalizace plánování pro Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f9e6b-126">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f9e6b-126">Prerequisites</span></span>

<span data-ttu-id="f9e6b-127">Před instalací doplňku Optimalizace plánování musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="f9e6b-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="f9e6b-128">Musíte používat Supply Chain Management v LCS aktivovaném prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="f9e6b-129">Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="f9e6b-130">Váš systém musí být nastaven na integraci Power Platform.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="f9e6b-131">Další informace viz [Předpoklady pro nastavení doplňků](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) a [Nastavení doplňků](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span><span class="sxs-lookup"><span data-stu-id="f9e6b-131">For more information, see [Prerequisites for setting up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) and [Set up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="f9e6b-132">Povolení licence Optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="f9e6b-133">Chcete-li použít optimalizaci plánování, musíte povolit její konfigurační klíč.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="f9e6b-134">Postup je následující:</span><span class="sxs-lookup"><span data-stu-id="f9e6b-134">To do so:</span></span>

1. <span data-ttu-id="f9e6b-135">Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6b-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="f9e6b-136">Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="f9e6b-137">Na kartě **Konfigurační klíče** zaškrtněte políčko **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="f9e6b-138">Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6b-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="f9e6b-139">Instalace doplňku optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="f9e6b-140">Musíte instalovat doplněk z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="f9e6b-141">Instalace doplňku optimalizace plánování:</span><span class="sxs-lookup"><span data-stu-id="f9e6b-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="f9e6b-142">Přihlaste se k LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="f9e6b-143">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="f9e6b-144">Přejděte na záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="f9e6b-145">Vyberte možnost **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="f9e6b-146">Vyberte **Optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="f9e6b-147">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="f9e6b-148">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-148">Select **Install**.</span></span>
1. <span data-ttu-id="f9e6b-149">Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="f9e6b-150">Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku).</span><span class="sxs-lookup"><span data-stu-id="f9e6b-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="f9e6b-151">Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f9e6b-152">Hlavním účelem instalace doplňku Optimalizace plánování je propojení služby a prostředí.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="f9e6b-153">Proto musíte doplněk nainstalovat samostatně do každého prostředí, kde budete používat optimalizaci plánování, bez ohledu na jakýkoli kód přesunutý mezi prostředími.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="f9e6b-154">Integrace optimalizace plánování do systému</span><span class="sxs-lookup"><span data-stu-id="f9e6b-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="f9e6b-155">Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="f9e6b-156">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="f9e6b-156">Connection status</span></span>

<span data-ttu-id="f9e6b-157">Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="f9e6b-158">Následující tabulka zobrazuje možné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="f9e6b-159">Stav připojení</span><span class="sxs-lookup"><span data-stu-id="f9e6b-159">Connection status</span></span> | <span data-ttu-id="f9e6b-160">Popis</span><span class="sxs-lookup"><span data-stu-id="f9e6b-160">Description</span></span> | <span data-ttu-id="f9e6b-161">Lze používat optimalizaci plánování?</span><span class="sxs-lookup"><span data-stu-id="f9e6b-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="f9e6b-162">Připojeno</span><span class="sxs-lookup"><span data-stu-id="f9e6b-162">Connected</span></span> | <span data-ttu-id="f9e6b-163">Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="f9e6b-164">Ano</span><span class="sxs-lookup"><span data-stu-id="f9e6b-164">Yes</span></span> |
| <span data-ttu-id="f9e6b-165">Povolení připojení</span><span class="sxs-lookup"><span data-stu-id="f9e6b-165">Enabling connection</span></span> | <span data-ttu-id="f9e6b-166">Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f9e6b-167">Ne</span><span class="sxs-lookup"><span data-stu-id="f9e6b-167">No</span></span> |
| <span data-ttu-id="f9e6b-168">Odpojeno</span><span class="sxs-lookup"><span data-stu-id="f9e6b-168">Disconnected</span></span> | <span data-ttu-id="f9e6b-169">Neexistuje připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="f9e6b-170">Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="f9e6b-171">Ne</span><span class="sxs-lookup"><span data-stu-id="f9e6b-171">No</span></span> |
| <span data-ttu-id="f9e6b-172">Zakazování připojení</span><span class="sxs-lookup"><span data-stu-id="f9e6b-172">Disabling connection</span></span> | <span data-ttu-id="f9e6b-173">Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="f9e6b-174">Ne</span><span class="sxs-lookup"><span data-stu-id="f9e6b-174">No</span></span> |
| <span data-ttu-id="f9e6b-175">Načítání stavu</span><span class="sxs-lookup"><span data-stu-id="f9e6b-175">Getting status</span></span> | <span data-ttu-id="f9e6b-176">Systém čeká na informace o stavu ze služby optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="f9e6b-177">Ne</span><span class="sxs-lookup"><span data-stu-id="f9e6b-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="f9e6b-178">Možnost použití optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="f9e6b-179">Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:</span><span class="sxs-lookup"><span data-stu-id="f9e6b-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="f9e6b-180">**Ano** – optimalizace plánování se používá pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="f9e6b-181">**Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f9e6b-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e6b-182">Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="f9e6b-183">Integrace s nastavením</span><span class="sxs-lookup"><span data-stu-id="f9e6b-183">Integration with the setup</span></span>

<span data-ttu-id="f9e6b-184">Je-li zapnuta optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="f9e6b-185">V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="f9e6b-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9e6b-186">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f9e6b-186">Additional resources</span></span>

[<span data-ttu-id="f9e6b-187">Podmínky a ustanovení pro náhled</span><span class="sxs-lookup"><span data-stu-id="f9e6b-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="f9e6b-188">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f9e6b-189">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f9e6b-190">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f9e6b-191">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="f9e6b-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="f9e6b-192">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="f9e6b-192">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Expedice malých balíků
description: Toto téma obsahuje informace o funkci expedice malých balíků (SPS). Tato funkce umožňuje produktu Microsoft Dynamics 365 Supply Chain Management odeslat přepravci podrobnosti o zabaleném kontejneru a poté od něj obdržet přepravní štítek, sazbu za dopravu a sledovací číslo.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910202"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="eaa02-104">Expedice malých balíků</span><span class="sxs-lookup"><span data-stu-id="eaa02-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eaa02-105">Funkce přepravy malých balíčků (SPS) umožňuje produktu Microsoft Dynamics 365 Supply Chain Management přímo komunikovat s přepravci poskytnutím rámce pro komunikaci prostřednictvím API dopravce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="eaa02-106">Tato funkce je užitečná, když odesíláte jednotlivé prodejní objednávky prostřednictvím komerčních přepravců místo použití kontejnerové přepravy nebo přepravy méně než nákladní vůz (LTL).</span><span class="sxs-lookup"><span data-stu-id="eaa02-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="eaa02-107">Funkce SPS interaguje s vaším dopravcem prostřednictvím vyhrazeného *výpočtu přepravních sazeb*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="eaa02-108">Vaše organizace musí tento výpočet přepravních sazeb vyvinout ve spolupráci s vaším dopravcem nebo službou dopravního centra.</span><span class="sxs-lookup"><span data-stu-id="eaa02-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="eaa02-109">Výpočet přepravních sazeb umožňuje produktu Supply Chain Management odeslat přepravci podrobnosti o zabaleném kontejneru a poté od něj obdržet přepravní štítek, sazbu za dopravu a sledovací číslo.</span><span class="sxs-lookup"><span data-stu-id="eaa02-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="eaa02-110">Vrácená sazba za přepravu se přidá k související prodejní objednávce jako různé poplatky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="eaa02-111">Vrácený přepravní štítek lze poté automaticky vytisknout pomocí tiskárny ZPL (Zebra Programming Language) a použít na zásilku.</span><span class="sxs-lookup"><span data-stu-id="eaa02-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="eaa02-112">Přepravce tento přepravní štítek naskenuje, když vyzvedne balíčky ve skladu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="eaa02-113">Příprava systému na podporu SPS</span><span class="sxs-lookup"><span data-stu-id="eaa02-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="eaa02-114">Než budete moci začít používat funkce SPS, musíte zapnout funkci SPS ve Správě funkcí, přidat modul rychlosti a nastavit moduly **Řízení dopravy** a **Vedení skladu** na jeho podporu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="eaa02-115">Zapnutí funkce SPS</span><span class="sxs-lookup"><span data-stu-id="eaa02-115">Turn on the SPS feature</span></span>

<span data-ttu-id="eaa02-116">Než můžete použít funkci SPS, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="eaa02-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="eaa02-117">Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="eaa02-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eaa02-118">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="eaa02-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eaa02-119">**Modul:** *Správa přepravy*</span><span class="sxs-lookup"><span data-stu-id="eaa02-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="eaa02-120">**Název funkce:** *Expedice malých balíků*</span><span class="sxs-lookup"><span data-stu-id="eaa02-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="eaa02-121">Nasazení a nastavení výpočtu přepravních sazeb</span><span class="sxs-lookup"><span data-stu-id="eaa02-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="eaa02-122">Supply Chain Management nezahrnuje žádné výpočty přepravních sazeb.</span><span class="sxs-lookup"><span data-stu-id="eaa02-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="eaa02-123">Musíte získat nebo vytvořit jakékoli výpočty přepravních sazeb, které požadujete, a poté je přidat do svého systému.</span><span class="sxs-lookup"><span data-stu-id="eaa02-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="eaa02-124">Společnost Microsoft však poskytuje ukázkový výpočet přepravních sazeb, který můžete použít k testování.</span><span class="sxs-lookup"><span data-stu-id="eaa02-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="eaa02-125">Stažení a nasazení ukázkového výpočtu přepravních sazeb</span><span class="sxs-lookup"><span data-stu-id="eaa02-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="eaa02-126">Chcete-li získat ukázkový výpočet přepravních sazeb, postupujte podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="eaa02-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="eaa02-127">Na GitHubu si stáhněte [knihovnu DLL pro ukázkový výpočet přepravních sazeb](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="eaa02-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="eaa02-128">Na serveru Supply Chain Management uložte knihovnu DLL do složky **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\zásobník**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="eaa02-129">Vytvoření a nasazení funkčních výpočtů přepravních sazeb</span><span class="sxs-lookup"><span data-stu-id="eaa02-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="eaa02-130">Informace o tom, jak vytvořit a nasadit funkční výpočty přepravních sazeb, aby je bylo možné použít v produkčním nebo testovacím prostředí, najdete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="eaa02-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="eaa02-131">Vytvoření nového modulu správy přepravy</span><span class="sxs-lookup"><span data-stu-id="eaa02-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="eaa02-132">Nastavení modulů správy přepravy</span><span class="sxs-lookup"><span data-stu-id="eaa02-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="eaa02-133">Další informace o tom, jak vytvořit výpočet přepravních sazeb SPS, najdete v následujícím příspěvku na blogu: [Expedice malých balíků: Jak využít funkce expedice malých balíků v Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="eaa02-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="eaa02-134">Nastavení výpočtu přepravních sazeb v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="eaa02-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="eaa02-135">Poté, co jste vytvořili a nasadili výpočet přepravních sazeb pro SPS, nastavte jej podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="eaa02-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="eaa02-136">Přejděte do nabídky **Správa přepravy \> Nastavení \> Moduly \> Výpočet přepravních sazeb**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="eaa02-137">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="eaa02-138">Na novém řádku nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="eaa02-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="eaa02-139">**Výpočet přepravních sazeb** - Zadejte jedinečný název pro výpočet přepravních sazeb.</span><span class="sxs-lookup"><span data-stu-id="eaa02-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="eaa02-140">Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *ukázkový výpočet přepravních sazeb*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="eaa02-141">**Název** - Zadejte stručný popis výpočtu přepravních sazeb.</span><span class="sxs-lookup"><span data-stu-id="eaa02-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="eaa02-142">Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *ukázkový výpočet přepravních sazeb*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="eaa02-143">**ID metadat hodnocení** - Vyberte základ, který by se měl použít k výpočtu vaší sazby.</span><span class="sxs-lookup"><span data-stu-id="eaa02-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="eaa02-144">Například vaše sazba může být vypočítána na základě vzdálenosti.</span><span class="sxs-lookup"><span data-stu-id="eaa02-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="eaa02-145">Pokud používáte ukázkový výpočet přepravních sazeb, můžete toto pole nechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="eaa02-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="eaa02-146">**Sestava modulu** - Zadejte název souboru balíčku DLL, který jste nasadili.</span><span class="sxs-lookup"><span data-stu-id="eaa02-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="eaa02-147">Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="eaa02-148">**Třída modulu** - Zadejte název třídy, který byl stanoven pro váš výpočet přepravních sazeb.</span><span class="sxs-lookup"><span data-stu-id="eaa02-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="eaa02-149">Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="eaa02-150">Příklad</span><span class="sxs-lookup"><span data-stu-id="eaa02-150">Example scenario</span></span>

<span data-ttu-id="eaa02-151">Tento příklad scénáře ukazuje, jak nastavit a používat SPS poté, co jste připravili systém, jak je popsáno výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="eaa02-152">Tento scénář používá dříve zmíněný ukázkový výpočet přepravních sazeb.</span><span class="sxs-lookup"><span data-stu-id="eaa02-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="eaa02-153">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="eaa02-153">Make demo data available</span></span>

<span data-ttu-id="eaa02-154">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="eaa02-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="eaa02-155">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="eaa02-156">Nastavení scénáře</span><span class="sxs-lookup"><span data-stu-id="eaa02-156">Set up the scenario</span></span>

<span data-ttu-id="eaa02-157">V tomto příkladu scénáře musíte mít ukázkového přepravce, skupinu přepravců, zásady balení a profil balení.</span><span class="sxs-lookup"><span data-stu-id="eaa02-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="eaa02-158">Následující podsekce vysvětlují, jak připravit záznamy, které jsou pro scénář vyžadovány.</span><span class="sxs-lookup"><span data-stu-id="eaa02-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="eaa02-159">V produkčním scénáři se proces instalace obvykle podobá procesu, který je zde popsán.</span><span class="sxs-lookup"><span data-stu-id="eaa02-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="eaa02-160">Nastavíte však jiné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="eaa02-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="eaa02-161">Nastavení dopravců</span><span class="sxs-lookup"><span data-stu-id="eaa02-161">Set up carriers</span></span>

<span data-ttu-id="eaa02-162">Chcete-li nastavit dopravce, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="eaa02-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="eaa02-163">Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="eaa02-164">V podokně Akce vyberte možnost **Nový** a přidejte dopravce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="eaa02-165">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="eaa02-166">**Dopravce dodávky:** *Demo Carrier*</span><span class="sxs-lookup"><span data-stu-id="eaa02-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="eaa02-167">**Jméno:** *Demo Carrier*</span><span class="sxs-lookup"><span data-stu-id="eaa02-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="eaa02-168">**Režim:** *Pozemní*</span><span class="sxs-lookup"><span data-stu-id="eaa02-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="eaa02-169">Na pevné záložce **Přehled** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eaa02-170">**Aktivace rozhraní dopravců:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="eaa02-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="eaa02-171">**Aktivace hodnocení dopravce:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="eaa02-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="eaa02-172">Na záložce s náhledem **Služby** přidejte službu do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="eaa02-173">Nastavte následující hodnoty pro novou službu:</span><span class="sxs-lookup"><span data-stu-id="eaa02-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="eaa02-174">**Služba přepravce:** *Demo carrier service*</span><span class="sxs-lookup"><span data-stu-id="eaa02-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="eaa02-175">**Jméno:** *Demo Carrier service*</span><span class="sxs-lookup"><span data-stu-id="eaa02-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="eaa02-176">**Způsob přepravy:** *pozemní*</span><span class="sxs-lookup"><span data-stu-id="eaa02-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="eaa02-177">Podle potřeby zadejte hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="eaa02-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="eaa02-178">(Když uložíte nový záznam přepravce, vytvoří se nový způsob doručení a pole **Způsob dodání** bude nastaveno automaticky.)</span><span class="sxs-lookup"><span data-stu-id="eaa02-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="eaa02-179">Na záložce s náhledem **Profily sazeb** vyberte **Nový** a vytvořte profil sazeb pro mřížku.</span><span class="sxs-lookup"><span data-stu-id="eaa02-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="eaa02-180">Nastavte následující hodnoty pro nový profil:</span><span class="sxs-lookup"><span data-stu-id="eaa02-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="eaa02-181">**Profil hodnocení:** *Ukázková služba dopravce*</span><span class="sxs-lookup"><span data-stu-id="eaa02-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="eaa02-182">**Jméno:** *Demo Carrier service*</span><span class="sxs-lookup"><span data-stu-id="eaa02-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="eaa02-183">**Výpočet přepravních sazeb:** *Ukázkový výpočet přepravních sazeb*</span><span class="sxs-lookup"><span data-stu-id="eaa02-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="eaa02-184">Podle potřeby zadejte hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="eaa02-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="eaa02-185">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="eaa02-186">Další informace o postupu při nastavení dopravců získáte v tématu [Nastavení dopravců](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="eaa02-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="eaa02-187">Nastavení účtů služeb dopravce</span><span class="sxs-lookup"><span data-stu-id="eaa02-187">Set up carrier service accounts</span></span>

<span data-ttu-id="eaa02-188">Pokud chcete nastavit účet služby dopravce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="eaa02-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="eaa02-189">Přejděte do nabídky **Správa přepravy \> Nastavení \> Hodnocení \> Náklady na účet služeb dopravce**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="eaa02-190">V podokně akcí vyberte možnost **Nový** pro přidání účtu služby dopravce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="eaa02-191">Nastavte následující hodnoty pro nový účet:</span><span class="sxs-lookup"><span data-stu-id="eaa02-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="eaa02-192">**Dopravce:** *Ukázkový dopravce*</span><span class="sxs-lookup"><span data-stu-id="eaa02-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="eaa02-193">**Služba přepravce:** *Demo carrier service*</span><span class="sxs-lookup"><span data-stu-id="eaa02-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="eaa02-194">**Číslo účtu dopravce:** Číslo účtu zákazníka dopravce, které se používá k ověření a potvrzení připojení k dopravci.</span><span class="sxs-lookup"><span data-stu-id="eaa02-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="eaa02-195">Tuto hodnotu poskytne váš dopravce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-195">Your carrier will provide this value.</span></span> <span data-ttu-id="eaa02-196">Pokud používáte ukázkovou službu, můžete zadat libovolnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="eaa02-197">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="eaa02-197">**Site:** *6*</span></span>
    - <span data-ttu-id="eaa02-198">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="eaa02-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="eaa02-199">Často je hodnota **Číslo zákaznického účtu dopravce** jediná hodnota, která je vyžadována k ověření připojení.</span><span class="sxs-lookup"><span data-stu-id="eaa02-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="eaa02-200">Pokud však váš operátor vyžaduje další parametry ověřování, měla by vaše organizace přizpůsobit tuto stránku a podle potřeby přidat další pole.</span><span class="sxs-lookup"><span data-stu-id="eaa02-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="eaa02-201">Nastavení zásad balení kontejneru</span><span class="sxs-lookup"><span data-stu-id="eaa02-201">Set up a container packing policy</span></span>

<span data-ttu-id="eaa02-202">Pokud chcete nastavit zásady balení kontejneru, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="eaa02-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="eaa02-203">Pokud jste ještě nenastavili definici tiskárny ZPL, použijte ji k nastavení aplikace Document Routing Agent.</span><span class="sxs-lookup"><span data-stu-id="eaa02-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="eaa02-204">Další informace viz [Přehled tisku dokumentů](../../fin-ops-core/dev-itpro/analytics/print-documents.md) a související témata.</span><span class="sxs-lookup"><span data-stu-id="eaa02-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="eaa02-205">Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="eaa02-206">V podokně akcí vyberte možnost **Nový** pro přidání zásad balení kontejneru.</span><span class="sxs-lookup"><span data-stu-id="eaa02-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="eaa02-207">V záhlaví nové zásady nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="eaa02-208">**Zásady balení kontejnerů:** *Ukázka zásad balení*</span><span class="sxs-lookup"><span data-stu-id="eaa02-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="eaa02-209">**Popis:** Popis zásad</span><span class="sxs-lookup"><span data-stu-id="eaa02-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="eaa02-210">Na pevné záložce **Přehled** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eaa02-211">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="eaa02-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eaa02-212">**Výchozí umístění pro konečnou zásilku:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="eaa02-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="eaa02-213">**Jednotka hmotnosti:** *KG*</span><span class="sxs-lookup"><span data-stu-id="eaa02-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="eaa02-214">**Zásady uzavírání kontejnerů:** *Automatické vydání*</span><span class="sxs-lookup"><span data-stu-id="eaa02-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="eaa02-215">**Zásady pro uvolňování kontejnerů:** *Zpřístupnit na konečném místě dodání*</span><span class="sxs-lookup"><span data-stu-id="eaa02-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="eaa02-216">Na záložce s náhledem **Obecné** můžete nastavit následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eaa02-217">**Automatický manifest při zavření kontejneru:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="eaa02-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="eaa02-218">**Požadavky manifestu pro kontejner:** *Správa dopravy*</span><span class="sxs-lookup"><span data-stu-id="eaa02-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="eaa02-219">**Obsah tiskového kontejneru:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="eaa02-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="eaa02-220">Na záložce s náhledem **Tisk štítku dopravce** můžete nastavit následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eaa02-221">**Vytisknout přepravní štítek kontejneru:** *Vždy*</span><span class="sxs-lookup"><span data-stu-id="eaa02-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="eaa02-222">**Název tiskárny:** Název tiskárny ZPL, která by měla tisknout přepravní štítky</span><span class="sxs-lookup"><span data-stu-id="eaa02-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="eaa02-223">Nastavení profilu balení</span><span class="sxs-lookup"><span data-stu-id="eaa02-223">Set up a packing profile</span></span>

<span data-ttu-id="eaa02-224">Chcete-li nastavit profil balení, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="eaa02-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="eaa02-225">Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="eaa02-226">V podokně Akce vyberte možnost **Nový**. Tím se přidá profil balení do mřížky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="eaa02-227">Nastavte následující hodnoty pro nový profil:</span><span class="sxs-lookup"><span data-stu-id="eaa02-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="eaa02-228">**ID profilu balení:** *Ukázka profilu balení*</span><span class="sxs-lookup"><span data-stu-id="eaa02-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="eaa02-229">**Popis:** Popis profilu</span><span class="sxs-lookup"><span data-stu-id="eaa02-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="eaa02-230">**Zásady balení kontejnerů:** *Ukázka zásad balení*</span><span class="sxs-lookup"><span data-stu-id="eaa02-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="eaa02-231">**Režim ID kontejneru:** *Automatický*</span><span class="sxs-lookup"><span data-stu-id="eaa02-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="eaa02-232">**Typ kontejneru:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="eaa02-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="eaa02-233">Nastavení zákazníka, aby používal dopravce SPS</span><span class="sxs-lookup"><span data-stu-id="eaa02-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="eaa02-234">Pomocí těchto kroků nastavíte zákazníka tak, aby mohl používat vámi vytvořeného operátora.</span><span class="sxs-lookup"><span data-stu-id="eaa02-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="eaa02-235">Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="eaa02-236">V mřížce vyhledejte a vyberte odběratele *US-027*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="eaa02-237">V podokně akcí na kartě **Obecné** ve skupině **Nastavení** zvolte **Účty odběratele dopravce**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="eaa02-238">Na stránce **Účty zákazníků dopravce**, v podokně akcí vyberte **Nový** pro přidání účtu do mřížky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="eaa02-239">Nastavte následující hodnoty pro nový účet:</span><span class="sxs-lookup"><span data-stu-id="eaa02-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="eaa02-240">**Dopravce dodávky:** *Demo Carrier*</span><span class="sxs-lookup"><span data-stu-id="eaa02-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="eaa02-241">**Číslo účtu přepravce:** *12345* (Hodnota není pro tento scénář důležitá, ale bude na ni odkazováno v další části.)</span><span class="sxs-lookup"><span data-stu-id="eaa02-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="eaa02-242">Projděte si ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="eaa02-242">Go through the example scenario</span></span>

<span data-ttu-id="eaa02-243">Poté, co nastavíte všechna ukázková data, jak je popsáno v předchozí části, jste připraveni projít ukázkovým scénářem.</span><span class="sxs-lookup"><span data-stu-id="eaa02-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="eaa02-244">Vytvoření prodejní objednávky a zpracování práce</span><span class="sxs-lookup"><span data-stu-id="eaa02-244">Create a sales order and process the work</span></span>

<span data-ttu-id="eaa02-245">Chcete-li vytvořit prodejní objednávku, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="eaa02-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="eaa02-246">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eaa02-247">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eaa02-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="eaa02-248">V dialogovém okně **Vytvořit prodejní objednávku** nastavte v poli **Účet odběratele** hodnotu *US-027*.</span><span class="sxs-lookup"><span data-stu-id="eaa02-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="eaa02-249">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="eaa02-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="eaa02-250">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="eaa02-250">The new sales order is opened.</span></span> <span data-ttu-id="eaa02-251">Na kartě s náhledem **Záhlaví prodejní objednávky** nastavte hodnotu v poli **Číslo účtu odběratele dopravce** na hodnotu, kterou jste pro tohoto odběratele vybrali předtím (*12345*).</span><span class="sxs-lookup"><span data-stu-id="eaa02-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="eaa02-252">V části **Řádky prodejní objednávky** přidejte řádek prodeje a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="eaa02-253">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="eaa02-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="eaa02-254">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="eaa02-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eaa02-255">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="eaa02-255">**Site:** *6*</span></span>
    - <span data-ttu-id="eaa02-256">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="eaa02-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="eaa02-257">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eaa02-258">Na záložce s náhledem **Doručení** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eaa02-259">**Dopravce dodávky:** *Demo Carrier*</span><span class="sxs-lookup"><span data-stu-id="eaa02-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="eaa02-260">**Služba přepravce:** *Demo carrier service*</span><span class="sxs-lookup"><span data-stu-id="eaa02-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="eaa02-261">Přepněte znovu do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="eaa02-262">Pokud se zobrazí výzva k aktualizaci způsobu doručení prodejních linek, vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="eaa02-263">V části **Řádky prodejní objednávky** vyberte řádek objednávky, který jste nastavili dříve, a poté vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="eaa02-264">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="eaa02-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="eaa02-265">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eaa02-266">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="eaa02-267">Je vytvořeno dílo pro přesun položek z místa vychystávání do balicí stanice.</span><span class="sxs-lookup"><span data-stu-id="eaa02-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="eaa02-268">V části **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti o dodávce**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="eaa02-269">Na stránce **Podrobnosti o zásilce** si poznamenejte ID dodávky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="eaa02-270">Budete ho potřebovat, až zabalíte dodávku na balicí stanici.</span><span class="sxs-lookup"><span data-stu-id="eaa02-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="eaa02-271">Zavřete stránku **Podrobnosti o dodávce** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="eaa02-272">Poznamenejte si číslo prodejní objednávky a přejděte na **Řízení skladu \> Práce \> Všechny práce**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="eaa02-273">Pomocí čísla prodejní objednávky vyhledejte a vyberte práci, která byla pro objednávku vytvořena.</span><span class="sxs-lookup"><span data-stu-id="eaa02-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="eaa02-274">V podokně akcí na kartě **Práce** zvolte **Dokončit práci**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="eaa02-275">Na stránce **Dokončení práce** v poli **ID uživatele** vyberte ID uživatele.</span><span class="sxs-lookup"><span data-stu-id="eaa02-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="eaa02-276">Pak v podokně akcí vyberte možnost **Ověřit práci**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="eaa02-277">Pokud práce projede ověřením, vyberte **Dokončit práci** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="eaa02-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="eaa02-278">Práce je označena jako dokončená pro simulaci pohybu věcí do balírny.</span><span class="sxs-lookup"><span data-stu-id="eaa02-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="eaa02-279">Zabalení dodávky</span><span class="sxs-lookup"><span data-stu-id="eaa02-279">Pack the shipment</span></span>

<span data-ttu-id="eaa02-280">Chcete-li zpracovat dodávku, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="eaa02-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="eaa02-281">Jděte na **Řízení skladu \> Nastavení \> Pracovník** a ujistěte se, že je váš uživatelský účet přidružen k pracovnímu účtu pro správu skladu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="eaa02-282">Přejděte na **Řízení skladu \> Vyzvednutí a kontejnerizace \> Balení**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="eaa02-283">V dialogovém okně **Vybrat balicí stanici** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eaa02-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eaa02-284">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="eaa02-284">**Site:** *6*</span></span>
    - <span data-ttu-id="eaa02-285">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="eaa02-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eaa02-286">**Místo:** *balení*</span><span class="sxs-lookup"><span data-stu-id="eaa02-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="eaa02-287">**ID profilu balení:** *Ukázka profilu balení*</span><span class="sxs-lookup"><span data-stu-id="eaa02-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="eaa02-288">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-288">Select **OK**.</span></span>
1. <span data-ttu-id="eaa02-289">Zobrazí se stránka **Balení**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-289">The **Pack** page appears.</span></span> <span data-ttu-id="eaa02-290">V produkčním scénáři pracovník naskenuje registrační značku nebo ID zásilky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="eaa02-291">U tohoto scénáře však otevřete stránku **Všechny zásilky** a vyhledejte číslo zásilky, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="eaa02-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="eaa02-292">Poté zadejte tuto hodnotu do pole **Registrační značka nebo zásilka** na straně **Balíček**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="eaa02-293">Případně zadejte ID zásilky, které jste si dříve poznamenali.</span><span class="sxs-lookup"><span data-stu-id="eaa02-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="eaa02-294">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eaa02-295">Zobrazí se dialogové okno, které zobrazuje podrobnosti o novém kontejneru.</span><span class="sxs-lookup"><span data-stu-id="eaa02-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="eaa02-296">Nechejte výchozí hodnoty a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="eaa02-297">Na stránce **Balení** na kartě s náhledem **Balení zboží** v poli **Identifikátor** vyberte *A0002* pro zabalení této položky.</span><span class="sxs-lookup"><span data-stu-id="eaa02-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="eaa02-298">Položka je přidána do kontejneru.</span><span class="sxs-lookup"><span data-stu-id="eaa02-298">The item is added to the container.</span></span>
1. <span data-ttu-id="eaa02-299">V podokně akcí klikněte na možnost **Kontejnery pro dodávku**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="eaa02-300">Stránka **Kontejnery pro dodávku**, která se zobrazí, má řádek pro kontejner, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="eaa02-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="eaa02-301">Pole **ID manifestu kontejneru** v tomto řádku je však aktuálně prázdné, protože jste od dopravce dosud neobdrželi přepravní štítek a sledovací číslo.</span><span class="sxs-lookup"><span data-stu-id="eaa02-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="eaa02-302">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eaa02-303">V dialogovém okně **Zavřít kontejner** nastavte pole **Hrubá hmotnost** na *1 kg* a potom vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaa02-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="eaa02-304">Přepravní štítek by nyní měl být vytištěn na tiskárně ZPL, kterou jste vybrali dříve.</span><span class="sxs-lookup"><span data-stu-id="eaa02-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="eaa02-305">Výsledek by měl vypadat podobně jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="eaa02-305">It should resemble the following example.</span></span>

    <span data-ttu-id="eaa02-306">![Příklad expedičního štítku](media/sps-label-example.png "Příklad expedičního štítku")</span><span class="sxs-lookup"><span data-stu-id="eaa02-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="eaa02-307">Všimněte si, že hodnoty **ID manifestu kontejneru** a **Celkem dopravné** byly přidány jako přijaté od dopravce.</span><span class="sxs-lookup"><span data-stu-id="eaa02-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
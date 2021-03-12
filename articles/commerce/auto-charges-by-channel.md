---
title: Povolení a konfigurace automatických nákladů podle kanálu
description: V tomto tématu je vysvětleno, jak povolit a konfigurovat automatické náklady podle kanálu v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d37b2b785dd29850dcd02d0905e5872445384990
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993721"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="5c110-103">Povolení a konfigurace automatických nákladů podle kanálu</span><span class="sxs-lookup"><span data-stu-id="5c110-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="5c110-104">V tomto tématu je vysvětleno, jak povolit a konfigurovat automatické náklady (auto náklady) podle kanálu v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5c110-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c110-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="5c110-105">Overview</span></span>

<span data-ttu-id="5c110-106">Je možné, že používáte scénáře, ve kterých je nutné použít náklady za recyklaci nebo jiné náklady pro skupinu produktů prodávaných ve všech nebo v některých prodejnách v určitém stavu (například Kalifornie).</span><span class="sxs-lookup"><span data-stu-id="5c110-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="5c110-107">Funkce **Povolit automatické náklady filtru podle kanálů** v modulu Commerce vám umožní určit automatické náklady podle kanálu (například konkrétní kanál kamenného obchodu).</span><span class="sxs-lookup"><span data-stu-id="5c110-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="5c110-108">Tato funkce je k dispozici v Dynamics 365 Commerce verze 10.0.10 a novější.</span><span class="sxs-lookup"><span data-stu-id="5c110-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="5c110-109">Chcete-li povolit a konfigurovat automatické náklady podle kanálu, je nutné provést následující úkony:</span><span class="sxs-lookup"><span data-stu-id="5c110-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="5c110-110">Zapněte funkci **Povolit automatické náklady filtru podle kanálu**.</span><span class="sxs-lookup"><span data-stu-id="5c110-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="5c110-111">Konfigurujte účel organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="5c110-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="5c110-112">Definovat automatické náklady podle kanálu.</span><span class="sxs-lookup"><span data-stu-id="5c110-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="5c110-113">Funkce **Povolit automatické náklady filtru podle kanálů** funguje pouze v případě, že je zapnuta také funkce Rozšířené automatické náklady.</span><span class="sxs-lookup"><span data-stu-id="5c110-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="5c110-114">Informace o tom, jak zapnout funkci rozšířené náklady, naleznete v tématu [Omnikanál – pokročilé automatické náklady](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="5c110-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="5c110-115">Zapněte funkci Povolit automatické náklady filtru podle kanálu</span><span class="sxs-lookup"><span data-stu-id="5c110-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="5c110-116">Chcete-li povolit automatické náklady podle kanálu v Commerce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5c110-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5c110-117">Přejděte do nabídky **Správce systému \> Pracovní prostory \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="5c110-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="5c110-118">Na kartě **Nepovoleno** v seznamu **Název funkce** najděte a vyberte možnost **Povolit filtrování automatických poplatků podle kanálu.**</span><span class="sxs-lookup"><span data-stu-id="5c110-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="5c110-119">V pravém dolním rohu vyberte možnost **Povolit nyní.**</span><span class="sxs-lookup"><span data-stu-id="5c110-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="5c110-120">Jakmile je funkce zapnuta, zobrazí se v seznamu na kartě **Vše**.</span><span class="sxs-lookup"><span data-stu-id="5c110-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="5c110-121">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="5c110-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c110-122">V levém podokně vyhledejte a vyberte úlohu **1110** (**globální konfigurace**).</span><span class="sxs-lookup"><span data-stu-id="5c110-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="5c110-123">V podokně akcí vyberte možnost **Spustit nyní** a rozšiřte změny konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5c110-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="5c110-124">Pokud vypnete funkci **Automatické náklady filtru po kanálech** po jejím použití, pole **Vztah maloobchodní sítě** v části **Automatické náklady** se již nezobrazí a všechny existující konfigurace budou ztraceny.</span><span class="sxs-lookup"><span data-stu-id="5c110-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="5c110-125">Pokud odebrání konfigurací **Vztah maloobchodní sítě** způsobí, že budou pravidla pro automatické náklady duplikována, pokus o vypnutí této funkce se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="5c110-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="5c110-126">Před vypnutím funkce zkontrolujte všechna pravidla automatických poplatků a proveďte požadované změny.</span><span class="sxs-lookup"><span data-stu-id="5c110-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="5c110-127">Konfigurujte účel organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="5c110-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="5c110-128">Byl vytvořen nový účel hierarchie organizace, který se nazývá **Maloobchodní auto poplatek** za účelem správy hierarchie pro automatické náklady podle kanálu.</span><span class="sxs-lookup"><span data-stu-id="5c110-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="5c110-129">Chcete-li přiřadit výchozí hierarchii k účelu organizační hierarchie v Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5c110-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="5c110-130">Přejděte do nabídky **Správa organizace \> Organizace \> Účely organizační hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="5c110-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="5c110-131">V levém podokně vyberte možnost **Automatické náklady maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="5c110-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="5c110-132">V části **Přiřazené hierarchie** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5c110-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="5c110-133">V dialogovém okně **Organizační hierarchie** vyberte organizační hierarchii (naříklad **Maloobchody podle regionu**) a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c110-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="5c110-134">V části **Přiřazené hierarchie** vyberte **Nastavit jako výchozí**.</span><span class="sxs-lookup"><span data-stu-id="5c110-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="5c110-135">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="5c110-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c110-136">V levém podokně vyhledejte a vyberte úlohu **1040** (**Produkty**).</span><span class="sxs-lookup"><span data-stu-id="5c110-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5c110-137">V podokně akcí zvolte **Spustit nyní**.</span><span class="sxs-lookup"><span data-stu-id="5c110-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5c110-138">Zopakováním předchozích dvou kroků spusťte úlohy **1070** (**Konfigurace kanálů**) a **1110** (**globální konfigurace**).</span><span class="sxs-lookup"><span data-stu-id="5c110-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Konfigurace maloobchodního automatického poplatku účel organizační hierarchie](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="5c110-140">Definovat automatické náklady podle kanálu</span><span class="sxs-lookup"><span data-stu-id="5c110-140">Define auto charges by channel</span></span>

<span data-ttu-id="5c110-141">Po zapnutí funkce **Povolit automatické náklady filtru podle kanálů** a nakonfigurování organizační hierarchie **Maloobchodní automatický poplatek** lze automatické náklady podle kanálu definovat buď na úrovni záhlaví objednávky nebo na úrovni řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="5c110-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="5c110-142">Chcete-li definovat automatické náklady podle kanálu v Commerce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5c110-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5c110-143">Přejděte na **Pohledávky \> Nastavení nákladů \> Automatické náklady**.</span><span class="sxs-lookup"><span data-stu-id="5c110-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="5c110-144">V levém podokně v poli **Úroveň** vyberte možnost **Záhlaví** nebo **Řádek** podle požadavků na obchod.</span><span class="sxs-lookup"><span data-stu-id="5c110-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="5c110-145">V poli **Kód maloobchodní sítě** vyberte příslušný kód kanálu (například **tabulka** nebo **skupina**).</span><span class="sxs-lookup"><span data-stu-id="5c110-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="5c110-146">Je-li použita výchozí hodnota **Vše**, použijí se pravidla poplatků pro všechny kanály.</span><span class="sxs-lookup"><span data-stu-id="5c110-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="5c110-147">Pokud vyberete **Skupina**, ujistěte se, že je vytvořena skupina poplatků maloobchodních kanálů v **Retail and Commerce \> Nastavení kanáků \> Náklady \> Skupiny nákladů maloobchodních kanálů**.</span><span class="sxs-lookup"><span data-stu-id="5c110-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="5c110-148">Pokud vyberete možnost **Tabulka**, můžete vybrat určitý kanál (například **San Francisco**) v poli **Vztah maloobchodních kanálů**.</span><span class="sxs-lookup"><span data-stu-id="5c110-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="5c110-149">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="5c110-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c110-150">V levém podokně vyhledejte a vyberte úlohu **1040** (**Produkty**).</span><span class="sxs-lookup"><span data-stu-id="5c110-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5c110-151">V podokně akcí zvolte **Spustit nyní**.</span><span class="sxs-lookup"><span data-stu-id="5c110-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5c110-152">Zopakováním předchozích dvou kroků spusťte úlohy **1070** (**Konfigurace kanálů**) a **1110** (**globální konfigurace**).</span><span class="sxs-lookup"><span data-stu-id="5c110-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatické náklady definované podle kanálu](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="5c110-154">Příklad</span><span class="sxs-lookup"><span data-stu-id="5c110-154">Example scenario</span></span>

<span data-ttu-id="5c110-155">Následující příklad popisuje kroky, které jsou nutné ke konfiguraci produktu tak, aby byly náklady za recyklaci účtovány při prodeji produktu prostřednictvím kamenného obchodu v San Franciscu.</span><span class="sxs-lookup"><span data-stu-id="5c110-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="5c110-156">V příkladu se také zobrazuje způsob zobrazení automatických nákladů v aplikaci pokladní místo (POS) Commerce.</span><span class="sxs-lookup"><span data-stu-id="5c110-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="5c110-157">Organizace definuje kód nákladů, který se nazývá **RECYKLACE**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="5c110-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Kód nákladů RECYKLACE](media/Auto-charges-charge-code.png)

<span data-ttu-id="5c110-159">Vytvoří se automatické náklady na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="5c110-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="5c110-160">Má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="5c110-160">It has the following configuration:</span></span>

- <span data-ttu-id="5c110-161">Pole **Kód účtu** je nastaveno na **Vše**.</span><span class="sxs-lookup"><span data-stu-id="5c110-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="5c110-162">Pole **Kód položky** je nastaveno na **Tabulka**.</span><span class="sxs-lookup"><span data-stu-id="5c110-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="5c110-163">Pole **Vztah položky** je nastaveno na ID produktu **91001**.</span><span class="sxs-lookup"><span data-stu-id="5c110-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="5c110-164">Pole **Kód způsobu dodání** je nastaveno na **Vše**.</span><span class="sxs-lookup"><span data-stu-id="5c110-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="5c110-165">Pole **Kód maloobchodní sítě** je nastaveno na **Tabulka**.</span><span class="sxs-lookup"><span data-stu-id="5c110-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="5c110-166">Pole **Vztah maloobchodních kanálů** je nastaveno na obchod **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="5c110-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="5c110-167">Je vytvořen řádek automatických nákladů.</span><span class="sxs-lookup"><span data-stu-id="5c110-167">An auto charges line is created.</span></span> <span data-ttu-id="5c110-168">Má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="5c110-168">It has the following configuration:</span></span>

- <span data-ttu-id="5c110-169">Pole **Měna** je nastaveno na hodnotu **USD**.</span><span class="sxs-lookup"><span data-stu-id="5c110-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="5c110-170">Pole **Kód nákladů** je nastaveno na **RECYKLACE**.</span><span class="sxs-lookup"><span data-stu-id="5c110-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="5c110-171">Pole **Kategorie** je nastaveno na hodnotu **Pevná**.</span><span class="sxs-lookup"><span data-stu-id="5c110-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="5c110-172">Pole **Náklady** je nastaveno na **$ 6,25**.</span><span class="sxs-lookup"><span data-stu-id="5c110-172">The **Charges** field is set to **$6.25**.</span></span>

![Konfigurace automatického nákladu na úrovni řádku a řádku automatických nákladů](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="5c110-174">V aplikaci POS se vytvoří prodejní objednávka v kanálu obchodu **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="5c110-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="5c110-175">Řádek **Náklady** zobrazuje poplatek za recyklaci **$6,25.**</span><span class="sxs-lookup"><span data-stu-id="5c110-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="5c110-176">Výběrem **Možnosti transakce \> Náklady \> Správa nákladů** v aplikaci POS můžete zobrazit kód nákladů a popis poplatku za recyklaci.</span><span class="sxs-lookup"><span data-stu-id="5c110-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Poplatek za recyklaci v aplikaci POS](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="5c110-178">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5c110-178">Additional resources</span></span>

[<span data-ttu-id="5c110-179">Omnikanálové rozšířené automatické náklady</span><span class="sxs-lookup"><span data-stu-id="5c110-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="5c110-180">Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje</span><span class="sxs-lookup"><span data-stu-id="5c110-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)

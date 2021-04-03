---
title: Přiznání ke srážkové dani pro Egypt
description: Toto téma vysvětluje, jak nakonfigurovat a vygenerovat přiznání ke srážkové dani pro Egypt.
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574316"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="b0596-103">Přiznání ke srážkové dani pro Egypt (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="b0596-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="b0596-104">Přehled</span><span class="sxs-lookup"><span data-stu-id="b0596-104">Overview</span></span>
<span data-ttu-id="b0596-105">Toto téma vysvětluje, jak nastavit a generovat prohlášení o srážkové dani a formuláře 41 a 11 přiznání ke srážkové dani pro právnické osoby v Egyptě</span><span class="sxs-lookup"><span data-stu-id="b0596-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="b0596-106">Všechny egyptské subjekty musí připravit formulář 41, který shrnuje všechny daně zadržené od místních dodavatelů a poskytovatelů služeb.</span><span class="sxs-lookup"><span data-stu-id="b0596-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="b0596-107">Kromě formuláře 41 musí být generován formulář 11, který podrobně popisuje všechny zadržené daně od zahraničních poskytovatelů.</span><span class="sxs-lookup"><span data-stu-id="b0596-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="b0596-108">Sestava **Přiznání ke srážkové dani** v Dynamics 365 Finance zahrnuje následující sestavy:</span><span class="sxs-lookup"><span data-stu-id="b0596-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="b0596-109">Formulář přiznání č.</span><span class="sxs-lookup"><span data-stu-id="b0596-109">Declaration form No.</span></span> <span data-ttu-id="b0596-110">41</span><span class="sxs-lookup"><span data-stu-id="b0596-110">41</span></span>
- <span data-ttu-id="b0596-111">Formulář přiznání č.</span><span class="sxs-lookup"><span data-stu-id="b0596-111">Declaration form No.</span></span> <span data-ttu-id="b0596-112">11</span><span class="sxs-lookup"><span data-stu-id="b0596-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="b0596-113">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="b0596-113">Prerequisites</span></span>
<span data-ttu-id="b0596-114">Primární adresa právnické osoby musí být v Egyptě.</span><span class="sxs-lookup"><span data-stu-id="b0596-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="b0596-115">V pracovním prostoru **Správa funkcí** musí být zapnutá následující funkce:</span><span class="sxs-lookup"><span data-stu-id="b0596-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="b0596-116">**Globální srážková daň**</span><span class="sxs-lookup"><span data-stu-id="b0596-116">**Global withholding tax**</span></span>

<span data-ttu-id="b0596-117">Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="b0596-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="b0596-118">Přejděte na **Daň** > **Nastavení** > **Parametry** > **Parametry hlavní knihy** a poté na kartě **Srážková daň** nastavte možnost **Povolit globální srážkovou** daň na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b0596-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="b0596-119">V pracovním prostoru **Elektronické přiznání** importujte z úložiště následující formáty elektronického hlášení:</span><span class="sxs-lookup"><span data-stu-id="b0596-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="b0596-120">Přiznání k WHT Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="b0596-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0596-121">Výše uvedený formát je založen na **Modelu daňového přiznání** a používá **Mapování modelu daňového přiznání**.</span><span class="sxs-lookup"><span data-stu-id="b0596-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="b0596-122">Tato další konfigurace bude automaticky importována.</span><span class="sxs-lookup"><span data-stu-id="b0596-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="b0596-123">Další informace o tom, jak importovat konfigurace elektronických sestav, najdete v části [Stažení konfigurací elektronických sestav ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="b0596-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="b0596-124">Stažení konfigurací elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b0596-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="b0596-125">Implementace formulářů přiznání k WHT pro Egypt je založena na konfiguracích elektronických přiznání (ER).</span><span class="sxs-lookup"><span data-stu-id="b0596-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="b0596-126">Další informace o možnostech a konceptech konfigurovatelných sestav najdete v tématu [Elektronické přiznání](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b0596-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="b0596-127">Prostředí produkčního a uživatelského akceptačního testování (UAT) najdete v pokynech v tématu [Stáhnout konfiguraci elektronických zpráv ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="b0596-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="b0596-128">Chcete-li vygenerovat přiznání ke srážkové dani v egyptské právnické osobě, musíte nahrát následující konfigurace:</span><span class="sxs-lookup"><span data-stu-id="b0596-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="b0596-129">Daňové přiznání model.version.82.xml nebo novější verze</span><span class="sxs-lookup"><span data-stu-id="b0596-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="b0596-130">Daňové přiznání model mapping.version.82.133.xml nebo novější verze</span><span class="sxs-lookup"><span data-stu-id="b0596-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="b0596-131">Přiznání k WHT Excel (EG).version.82.21 nebo novější verze</span><span class="sxs-lookup"><span data-stu-id="b0596-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="b0596-132">Po stažení konfigurací ER ze služby Lifecycle Services (LCS) nebo z globálního úložiště proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="b0596-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="b0596-133">Přejděte do pracovního prostoru **Elektronické výkaznictví** a vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="b0596-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="b0596-134">Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange > Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="b0596-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="b0596-135">Nahrajte všechny soubory v pořadí, v jakém jsou uvedeny v předchozích odrážkách.</span><span class="sxs-lookup"><span data-stu-id="b0596-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="b0596-136">Po načtení všech konfigurací bude v aplikaci Finance uveden konfigurační strom.</span><span class="sxs-lookup"><span data-stu-id="b0596-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="b0596-137">Nastavení parametrů pro konkrétní aplikaci</span><span class="sxs-lookup"><span data-stu-id="b0596-137">Set up application-specific parameters</span></span>

<span data-ttu-id="b0596-138">Možnost parametrů specifických pro aplikaci umožňuje uživatelům stanovit kritéria, jak budou daňové transakce klasifikovány a počítány v každém řádku generovaného přehledu v závislosti na konfiguraci **skupina položek srážkové daně** nebo jiných kritériích stanovená v definici vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0596-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="b0596-139">Formulář 41 prohlášení o srážkové dani obsahuje zvláštní sloupec, kde musí být transakce srážkové daně klasifikována v souladu s pojmenovanou klasifikací daňového úřadu **Typ slevového kódu**.</span><span class="sxs-lookup"><span data-stu-id="b0596-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="b0596-140">Namísto zahrnutí těchto nových klasifikací jako nových vstupních údajů při zaúčtování transakcí bude klasifikace určena na základě různých vyhledávání zavedených v nabídce **Konfigurace** > **Nastavit parametry specifické pro aplikaci** > **Nastavit** za účelem splnění požadavků přiznání ke srážkové dani pro Egypt.</span><span class="sxs-lookup"><span data-stu-id="b0596-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="b0596-141">Následující konfigurace se používá ke klasifikaci transakcí v sestavě formuláře přiznání ke srážkové dani 41:</span><span class="sxs-lookup"><span data-stu-id="b0596-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="b0596-142">**DiscountTaxTypeLookup** -> Sloupec č. 18</span><span class="sxs-lookup"><span data-stu-id="b0596-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="b0596-143">Pomocí následujících kroků můžete nastavit různá vyhledávání použitá ke generování přiznání k WHT a souvisejících účetních výkazů.</span><span class="sxs-lookup"><span data-stu-id="b0596-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="b0596-144">V pracovním prostoru **Elektronické přiznání** vyberte **Konfigurace** > **Nastavení** k nastavení pravidel klasifikace transakcí v sestavě přiznání k WHT.</span><span class="sxs-lookup"><span data-stu-id="b0596-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="b0596-145">Vyberte aktuální verzi a na kartě s náhledem **Vyhledávání** vyberte název vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0596-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="b0596-146">Například **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="b0596-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="b0596-147">Toto vyhledávání identifikuje seznam typů slev požadovaných daňovým úřadem.</span><span class="sxs-lookup"><span data-stu-id="b0596-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="b0596-148">Na záložce s náhledem **Podmínky** vyberte **Přidat** a v novém řádku ve sloupci **Výsledek vyhledávání** vyberte související řádek, který představuje klasifikaci ve **sloupci 18**.</span><span class="sxs-lookup"><span data-stu-id="b0596-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="b0596-149">Ve sloupci **Skupina položek srážkové daně** vyberte související kód, který se používá k identifikaci klasifikace.</span><span class="sxs-lookup"><span data-stu-id="b0596-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="b0596-150">Například **Povolená sleva**.</span><span class="sxs-lookup"><span data-stu-id="b0596-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="b0596-151">Opakujte kroky 3 a 4 pro všechna dostupná vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0596-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="b0596-152">Opět vyberte **Přidat** k zahrnutí závěrečného řádku záznamu a ve sloupci **Výsledek vyhledávání** vyberte **Nelze použít**.</span><span class="sxs-lookup"><span data-stu-id="b0596-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="b0596-153">Ve zbývajících sloupcích vyberte **Není prázdné**.</span><span class="sxs-lookup"><span data-stu-id="b0596-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="b0596-154">Nastavení parametrů hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b0596-154">Set up General ledger parameters</span></span>

<span data-ttu-id="b0596-155">Chcete-li vygenerovat hlášení formuláře přiznání k WHT v Microsoft Excel, definujte formát ER na stránce **Obecné parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="b0596-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="b0596-156">Přejděte na **Daň** > **Nastavení** > **Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="b0596-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="b0596-157">Na kartě **Srážková daň** v poli **Mapování formát přiznání k WHT** vyberte **Přiznání k WHT Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="b0596-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="b0596-158">Pokud toto pole necháte prázdné, vygeneruje se standardní hlášení o DPH ve formátu SSRS.</span><span class="sxs-lookup"><span data-stu-id="b0596-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Formulář přiznání](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="b0596-160">Vygenerování formulářů přiznání ke srážkové dani</span><span class="sxs-lookup"><span data-stu-id="b0596-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="b0596-161">Proces přípravy a odeslání formuláře přiznání ke srážkové dani pro konkrétní období je založen na transakcích srážkové daně zaúčtovaných během úlohy vypořádání a platby daně.</span><span class="sxs-lookup"><span data-stu-id="b0596-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="b0596-162">Další informace o globální srážkové dani viz [Globální srážková daň](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b0596-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="b0596-163">Chcete-li vygenerovat zprávu o daňovém přiznání, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="b0596-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="b0596-164">Přejděte do nabídky **Daň** > **Přiznání** > **Srážková daň** > \**Platba srážkové daně*.</span><span class="sxs-lookup"><span data-stu-id="b0596-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="b0596-165">Vyberte zúčtovací období a poté vyberte datum od pro zprávu.</span><span class="sxs-lookup"><span data-stu-id="b0596-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="b0596-166">Zadejte datum transakce a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0596-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="b0596-167">V dialogovém okně, které se otevře, vyberte jeden nebo více typů formulářů **Formulář č. 41**, **Formulář č. 11** nebo **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="b0596-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="b0596-168">Pokud vyberete **Žádný**, je generována standardní sestava.</span><span class="sxs-lookup"><span data-stu-id="b0596-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="b0596-169">Vyberte jazyk.</span><span class="sxs-lookup"><span data-stu-id="b0596-169">Select the language.</span></span> <span data-ttu-id="b0596-170">Všechny sestavy jsou přeloženy do **en-us** a **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="b0596-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="b0596-171">Zadejte pobočku a název banky, kde bude zaplacena daň.</span><span class="sxs-lookup"><span data-stu-id="b0596-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="b0596-172">Vyberte typ firmy a poté zadejte čísla šeků a dokladů.</span><span class="sxs-lookup"><span data-stu-id="b0596-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="b0596-173">Zadejte typ entity.</span><span class="sxs-lookup"><span data-stu-id="b0596-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="b0596-174">Zadejte jméno registrované osoby pro přiřazení formuláře a vyberte **OK** pro potvrzení generování sestavy.</span><span class="sxs-lookup"><span data-stu-id="b0596-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]

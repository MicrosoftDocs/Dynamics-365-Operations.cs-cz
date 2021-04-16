---
title: Nastavení parametrů formátu ER podle právnické osoby
description: V tomto tématu je vysvětleno, jak nastavit parametry formátu elektronického výkaznictví (ER) podle právnické osoby.
author: NickSelin
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 4003208a1f02db134bbec1ecf90c1cdd2973e67f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751147"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="8c23e-103">Nastavení parametrů formátu ER podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="8c23e-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="8c23e-104">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="8c23e-104">Prerequisites</span></span>

<span data-ttu-id="8c23e-105">Chcete-li provést tento postup, musíte nejprve dokončit kroky v [Nastavení formátů ER, které budou používat parametry specifikované podle právnické osoby](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="8c23e-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="8c23e-106">K dokončení příkladů v tomto tématu musíte mít přístup k aplikaci Microsoft Dynamics 365 Finance (Finance) pro některou z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="8c23e-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="8c23e-107">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8c23e-107">Electronic reporting developer</span></span>
- <span data-ttu-id="8c23e-108">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8c23e-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="8c23e-109">Správce systému</span><span class="sxs-lookup"><span data-stu-id="8c23e-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="8c23e-110">Import konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="8c23e-110">Import ER configurations</span></span>

1.  <span data-ttu-id="8c23e-111">Přihlaste se k prostředí.</span><span class="sxs-lookup"><span data-stu-id="8c23e-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="8c23e-112">Na výchozím řídicím panelu vyberte **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="8c23e-113">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="8c23e-114">Importujte do aktuální instance aplikace Finance konfigurace, které jste exportovali ze služby Regulatory Configuration Services (RCS) při dokončování kroků v tématu [Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="8c23e-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="8c23e-115">Tyto kroky proveďte pro každou konfiguraci elektronického výkaznictví (ER) v následujícím pořadí: datový model, mapování modelu a formáty.</span><span class="sxs-lookup"><span data-stu-id="8c23e-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="8c23e-116">Vyberte **Exchange \> Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="8c23e-117">Zvolte **Procházet** a vyberte soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="8c23e-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="8c23e-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-118">Select **OK**.</span></span>
    
    <span data-ttu-id="8c23e-119">Následující ilustrace znázorňuje konfigurace, které je nutné mít po dokončení.</span><span class="sxs-lookup"><span data-stu-id="8c23e-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Stránka konfigurací elektronického výkaznictví](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="8c23e-121">Nastavení parametrů pro společnost DEMF</span><span class="sxs-lookup"><span data-stu-id="8c23e-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="8c23e-122">Pomocí systému ER můžete nastavit specifické parametry aplikace pro formát ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="8c23e-123">Vyberte právnickou osobu **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="8c23e-124">Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="8c23e-125">V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="8c23e-127">Na stránce **Parametry specifické pro aplikaci** můžete konfigurovat pravidla pro zdroj dat **Selektor** formátu **Formát pro učení se, jak vyhledávat data ER**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="8c23e-128">Pokud základní formát ER bude obsahovat několik zdrojů dat typu **vyhledávání**, musíte vybrat požadovaný zdroj dat na pevné záložce **Vyhledávání** před zahájením konfigurace sady pravidel pro zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="8c23e-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="8c23e-129">Pro každý zdroj dat lze nakonfigurovat samostatná pravidla pro každou verzi vybraného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="8c23e-130">Celá sada pravidel pro všechny vyhledávací zdroje dat, které jsou k dispozici ve vybrané verzi základního formátu ER, tvoří parametry specifické pro aplikaci ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="8c23e-131">Vyberte verzi **1.1.1** formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="8c23e-132">Na pevné záložce **Podmínky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="8c23e-133">V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c23e-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="8c23e-134">Vyhledávání představuje seznam kódů daní pro výběr.</span><span class="sxs-lookup"><span data-stu-id="8c23e-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="8c23e-135">Tento seznam je vrácen zdrojem dat **Model.Data.Tax**, který byl nakonfigurován v základním formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="8c23e-136">Vzhledem k tomu, že tento zdroj dat obsahuje pole **Název**, zobrazí se názvy jednotlivých kódů daní ve vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c23e-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="8c23e-138">Vyberte kód daně **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="8c23e-139">V poli **Výsledek vyhledávání** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c23e-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="8c23e-140">Vyhledávání představuje seznam hodnot pro formát výčtu TaxationLevel pro výběr.</span><span class="sxs-lookup"><span data-stu-id="8c23e-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="8c23e-141">Všimněte si, že pokud je jako preferovaný jazyk uživatele, jako který jste přihlášeni, vybrána němčina, budou popisky hodnot ve vyhledávání v němčině, pokud byly přeloženy do formátu Base ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="8c23e-142">Kromě toho, pokud byl přeložen popisek vyhledávacího zdroje dat, bude tento popisek zobrazen na kartě **vyhledávání** v preferovaném jazyce uživatele.</span><span class="sxs-lookup"><span data-stu-id="8c23e-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="8c23e-144">Vyberte hodnotu **Běžné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="8c23e-145">Přidáte-li tento záznam, definujete následující pravidlo: vždy, když je požadován zdroj dat vyhledávání **Selektor**, je požadován datový zdroj výběru, a kód DPH **VAT19** je předán jako argument, bude vrácena hodnota **Běžné zdanění** jako požadovaná úroveň zdanění.</span><span class="sxs-lookup"><span data-stu-id="8c23e-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="8c23e-146">Vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-147">V poli **Kód** vyberte kód daně **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="8c23e-148">V poli **výsledek vyhledávání** vyberte hodnotu **normální zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="8c23e-149">Znovu vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-150">V poli **Kód** vyberte kód daně **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="8c23e-151">V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="8c23e-152">Znovu vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-153">V poli **Kód** vyberte kód daně **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="8c23e-154">V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="8c23e-155">Znovu vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-156">V poli **Kód** vyberte kód daně **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="8c23e-157">V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="8c23e-158">Znovu vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-159">V poli **Kód** vyberte kód daně **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="8c23e-160">V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="8c23e-161">Znovu vyberte **přidat** a postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c23e-162">V poli **kód** vyberte možnost **\*Notblank\***.</span><span class="sxs-lookup"><span data-stu-id="8c23e-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="8c23e-163">V poli **výsledek vyhledávání** vyberte hodnotu **Jiné**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="8c23e-164">Přidáte-li tento poslední záznam, definujete následující pravidlo: vždy, když kód daně předaný jako argument nesplňuje žádné z předchozích pravidel, vrátí zdroj dat vyhledávání jako požadovanou úroveň zdanění **Jiné**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="8c23e-166">V poli **Stav** vyberte možnost **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="8c23e-167">Po spuštění verze formátu ER, která má stav **Dokončeno** nebo **Sdíleno**, musí mít tato sada pravidel stav **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="8c23e-168">V opačném případě bude provedení základního formátu ER přerušeno při pokusu o načtení dat z této sady pravidel v době, kdy je spuštěn zdroj dat vyhledávání **Selektor**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="8c23e-169">Při spuštění verze formátu ER, která má stav **koncept**, může základní formát ER přistupovat k této sadě pravidel bez ohledu na její stav.</span><span class="sxs-lookup"><span data-stu-id="8c23e-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="8c23e-170">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-170">Select **Save**.</span></span>
18. <span data-ttu-id="8c23e-171">zavřete stránku **Parametry specifické podle aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="8c23e-172">Spuštění formátu ER ve společnosti DEMF</span><span class="sxs-lookup"><span data-stu-id="8c23e-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="8c23e-173">Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="8c23e-174">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="8c23e-175">V zobrazeném dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="8c23e-176">Stáhněte výpis, který je vygenerován, a uložte ho místně.</span><span class="sxs-lookup"><span data-stu-id="8c23e-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="8c23e-177">V generovaném výpisu si všimněte, že souhrn kódu daně **InVAT7** byl vložen na **Redukované** úrovni a souhrny **VAT19** d **InVA19** byly umístěny na **běžnou** úroveň.</span><span class="sxs-lookup"><span data-stu-id="8c23e-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="8c23e-178">Toto chování je určeno konfigurací pro sadu pravidel závislých na právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="8c23e-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="8c23e-179">Přejděte na **Daň \> Nepřímé daně \> DPH \> Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="8c23e-180">Vyberte kód daně **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="8c23e-181">V podokně akcí na kartě **Kód DPH** ve skupině **Dotazy** vyberte **Zaúčtovaná DPH** k zobrazení informací o hodnotě daně a použité daňové sazbě podle kódu daně.</span><span class="sxs-lookup"><span data-stu-id="8c23e-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Zaúčtovaná stránka DPH](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="8c23e-183">Zavřete stránku Zaúčtovaná DPH.</span><span class="sxs-lookup"><span data-stu-id="8c23e-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="8c23e-184">Nastavení parametrů pro společnost USMF</span><span class="sxs-lookup"><span data-stu-id="8c23e-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="8c23e-185">Vyberte právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="8c23e-186">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="8c23e-187">Ve stromu konfigurací rozbalte položku **Model k učení parametrizovaných volání**, rozbalte položku **Formát k učení se parametrizovaných volání** a vyberte **Formát k učení se, jak vyhledávat data LE**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="8c23e-188">V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="8c23e-189">Vyberte verzi **1.1.1** vybraného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="8c23e-190">Na pevné záložce **Podmínky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="8c23e-191">V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c23e-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="8c23e-192">Vyhledávání nyní představuje seznam kódů daní pro daň **USMF** společnosti pro výběr.</span><span class="sxs-lookup"><span data-stu-id="8c23e-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="8c23e-194">Vyberte kód daně **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="8c23e-195">V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **žádné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="8c23e-196">Znovu vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-196">Select **Add** again.</span></span>
11. <span data-ttu-id="8c23e-197">V poli **kód** nového záznamu vyberte možnost **\*Notblank\***.</span><span class="sxs-lookup"><span data-stu-id="8c23e-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="8c23e-198">V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **běžné zdanění**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="8c23e-199">V poli **Stav** vyberte možnost **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="8c23e-200">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-200">Select **Save**.</span></span>

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="8c23e-202">zavřete stránku **Parametry specifické podle aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="8c23e-203">Spuštění formátu ER ve společnosti USMF</span><span class="sxs-lookup"><span data-stu-id="8c23e-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="8c23e-204">Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="8c23e-205">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="8c23e-206">V zobrazeném dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="8c23e-207">Stáhněte výpis, který je vygenerován, a uložte ho místně.</span><span class="sxs-lookup"><span data-stu-id="8c23e-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="8c23e-208">V generovaném příkazu si všimněte, že jste nyní opakovaně použili stejný formát ER pro jinou právnickou osobu, ale bez provedení úprav formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="8c23e-209">Znovu použít parametry závislé na právnické osobě</span><span class="sxs-lookup"><span data-stu-id="8c23e-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="8c23e-210">Parametry exportu</span><span class="sxs-lookup"><span data-stu-id="8c23e-210">Export parameters</span></span>

1.  <span data-ttu-id="8c23e-211">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="8c23e-212">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="8c23e-213">Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="8c23e-214">V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="8c23e-215">Vyberte verzi **1.1.1** formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="8c23e-216">V podokně akcí klikněte na možnost **Export**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="8c23e-217">Stáhněte soubor, který je vygenerován, a uložte ho místně.</span><span class="sxs-lookup"><span data-stu-id="8c23e-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="8c23e-218">Konfigurovaná sada parametrů specifických pro aplikaci byla nyní exportována jako soubor XML.</span><span class="sxs-lookup"><span data-stu-id="8c23e-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="8c23e-219">Parametry importu</span><span class="sxs-lookup"><span data-stu-id="8c23e-219">Import parameters</span></span>

1.  <span data-ttu-id="8c23e-220">Vyberte verzi **1.1.2** formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="8c23e-221">V podokně akcí klikněte na možnost **Import**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="8c23e-222">Výběrem možnosti **Ano** potvrďte, že chcete přepsat existující parametry specifické pro aplikaci pro tuto verzi formátu.</span><span class="sxs-lookup"><span data-stu-id="8c23e-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="8c23e-223">Vyberte **Procházet**, pokud chcete vyhledat soubor obsahující exportované parametry specifické pro aplikaci verze **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="8c23e-224">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-224">Select **OK**.</span></span>

    <span data-ttu-id="8c23e-225">Verze **1.1.2** ve formátu ER má nyní stejné parametry specifické pro danou aplikaci, které jste původně nakonfigurovali pro verzi **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="8c23e-226">Všimněte si, že parametry formátu ER specifické pro aplikaci jsou závislé na právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="8c23e-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="8c23e-227">Chcete-li znovu použít specifické parametry aplikace, které byly nakonfigurovány pro jednu právnickou osobu v jiné právnické osobě, je nutné je exportovat v době, kdy jste se přihlásili k první právnické osobě, a poté je importovat po přihlášení k jiné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="8c23e-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="8c23e-228">Tento přístup lze také použít k převodu formátu ER, které jsou specifické pro konkrétní aplikace, které byly původně nakonfigurovány v jedné instanci finančního oddělení na jinou instanci modulu finance.</span><span class="sxs-lookup"><span data-stu-id="8c23e-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="8c23e-229">Uvědomte si, že pokud konfigurujete parametry specifické pro určitou aplikaci pro jednu verzi formátu ER a importujete vyšší verzi stejného formátu do aktuální instance finance, nebudou pro importovanou verzi použity existující parametry specifické pro danou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="8c23e-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="8c23e-230">Je také nutné mít na paměti, že při výběru souboru pro import bude porovnána struktura parametrů specifických pro aplikaci v tomto souboru se strukturou odpovídajícího zdroje dat typu **vyhledávání** ve formátu ER, který je vybrán pro import.</span><span class="sxs-lookup"><span data-stu-id="8c23e-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="8c23e-231">Import je proveden v případě, že struktura jednotlivých parametrů specifických pro aplikaci odpovídá struktuře odpovídajícího zdroje dat ve formátu ER vybraném pro import.</span><span class="sxs-lookup"><span data-stu-id="8c23e-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="8c23e-232">Pokud se struktury neshodují, zobrazí se varovná zpráva oznamující, že import nelze provést.</span><span class="sxs-lookup"><span data-stu-id="8c23e-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="8c23e-233">Pokud vynutíte provedení importu, budou vymazány stávající parametry specifické pro vybraný formát ER a bude nutné je nastavit až od začátku.</span><span class="sxs-lookup"><span data-stu-id="8c23e-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="8c23e-234">Vztah mezi parametry specifickými pro aplikaci a formátem ER</span><span class="sxs-lookup"><span data-stu-id="8c23e-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="8c23e-235">Vztah mezi formátem ER a jeho parametry specifickými pro danou aplikaci je vytvořen jedinečným identifikačním kódem nezávislým na instanci formátu ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="8c23e-236">Pokud tedy z modulu Finance odeberete formát ER, budou parametry specifické pro aplikaci, které jsou nakonfigurovány pro formát ER, uloženy v aktuální instanci modulu finance.</span><span class="sxs-lookup"><span data-stu-id="8c23e-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="8c23e-237">Lze k nim přistupovat při každém zpětném importu základního formátu ER do této instance modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="8c23e-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="8c23e-238">Přístup k parametrům specifickým pro aplikaci pomocí architektury ER</span><span class="sxs-lookup"><span data-stu-id="8c23e-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="8c23e-239">V předchozím příkladu jste získali přístup k parametrům formátu ER, které jsou specifické pro jednotlivé aplikace, pomocí architektury ER.</span><span class="sxs-lookup"><span data-stu-id="8c23e-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="8c23e-240">Tento přístup neumožňuje omezit přístup k parametrům specifického formátu ER, které jsou specifické pro jednotlivé aplikace.</span><span class="sxs-lookup"><span data-stu-id="8c23e-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="8c23e-241">Pokud je nutné tato omezení použít, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8c23e-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="8c23e-242">Znovu použijte existující položku nabídky **ERSolutionAppSpecificParametersDesigner** nebo implementujte vlastní položku nabídky **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Stránka Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="8c23e-244">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8c23e-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="8c23e-245">Vytvořte tlačítko položky nové nabídky a propojte ho s příslušným záznamem z tabulky **ERSolutionTable** nastavením jeho vlastnosti **Data Source** na **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="8c23e-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Stránka Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="8c23e-247">Vytvořte jednoduché tlačítko a přepište metodu **Kliknuto**, jak je znázorněno v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="8c23e-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="8c23e-248">Použijete-li tento přístup, můžete zadat jedinečné ID řešení (definované pomocí hodnoty **GUID**), které umožní přístup k parametrům specifickým pouze pro specifický formát ER a kopií, které byly od něj odvozeny.</span><span class="sxs-lookup"><span data-stu-id="8c23e-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="8c23e-249">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8c23e-249">Additional resources</span></span>

[<span data-ttu-id="8c23e-250">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8c23e-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="8c23e-251">Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="8c23e-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
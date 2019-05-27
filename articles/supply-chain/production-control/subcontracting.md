---
title: Subdodávka
description: Toto téma vás provede subdodávkami ve výrobě v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568376"
---
# <a name="subcontracting"></a><span data-ttu-id="37349-103">Subdodávka</span><span class="sxs-lookup"><span data-stu-id="37349-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37349-104">Toto téma vás provede subdodávkami ve výrobě v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="37349-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="37349-105">První část tohoto tématu popisuje nastavení dat.</span><span class="sxs-lookup"><span data-stu-id="37349-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="37349-106">Druhá část vás provede kroky v této ukázce.</span><span class="sxs-lookup"><span data-stu-id="37349-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="37349-107">Cílová skupina</span><span class="sxs-lookup"><span data-stu-id="37349-107">Target audience</span></span>

<span data-ttu-id="37349-108">V tomto tématu se naučíte, jak nastavit subdodávky ve výrobě.</span><span class="sxs-lookup"><span data-stu-id="37349-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="37349-109">Budete používat existující data v právnické osobě HQUS k provedení základního nastavení toku aktivity subdodávky.</span><span class="sxs-lookup"><span data-stu-id="37349-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="37349-110">Ukázková data v právnické osobě HQUS obsahují nastavení parametrů, které byly přednastaveny k podpoře kroků v ukázce.</span><span class="sxs-lookup"><span data-stu-id="37349-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="37349-111">Přestože ukázka adresuje klíčové problémy a výzvy pro různé role, může ji dokončit správce systému.</span><span class="sxs-lookup"><span data-stu-id="37349-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="37349-112">Scénář ukázky</span><span class="sxs-lookup"><span data-stu-id="37349-112">Demo scenario</span></span>

<span data-ttu-id="37349-113">V právnické osobě HQUS jsou vyráběny špičkové reproduktory.</span><span class="sxs-lookup"><span data-stu-id="37349-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="37349-114">Během výrobního procesu procházejí reproduktory třemi následujícími operacemi.</span><span class="sxs-lookup"><span data-stu-id="37349-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="37349-115">**Předběžné sestavení** – Skříň reproduktoru je sestavena.</span><span class="sxs-lookup"><span data-stu-id="37349-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="37349-116">Materiál pro skříň je vydán ve skladu materiálu před zahájením operace.</span><span class="sxs-lookup"><span data-stu-id="37349-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="37349-117">**Lakování** – Po sestavení skříně reproduktoru je třeba ji nalakovat.</span><span class="sxs-lookup"><span data-stu-id="37349-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="37349-118">Tuto operaci provádí dodavatel (subdodavatel).</span><span class="sxs-lookup"><span data-stu-id="37349-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="37349-119">Předběžně sestavená skříň reproduktoru je expedována subdodavateli k nátěru spolu s dvěma materiály.</span><span class="sxs-lookup"><span data-stu-id="37349-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="37349-120">**Konečná úprava** – Poté, co je předběžně sestavená skříň reproduktoru nalakována subdodavatelem, vrátí se do právnické osoby HQUS, aby bylo dokončeno finální sestavení.</span><span class="sxs-lookup"><span data-stu-id="37349-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="37349-121">Následující obrázek znázorňuje tři operace a materiály, které tyto operace spotřebovávají.</span><span class="sxs-lookup"><span data-stu-id="37349-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Předběžné sestavení lakování a operace dokončení, spolu se spotřebovávanými materiály.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="37349-123">Nastavení</span><span class="sxs-lookup"><span data-stu-id="37349-123">Setup</span></span>

<span data-ttu-id="37349-124">Dříve než začnete s ukázkou, musíte nastavit data.</span><span class="sxs-lookup"><span data-stu-id="37349-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="37349-125">Nastavení dokončeného produktu</span><span class="sxs-lookup"><span data-stu-id="37349-125">Set up the finished product</span></span>

<span data-ttu-id="37349-126">Tento postup vás provede nastavením uvolněného produktu D8100, „Nalakovaná skříň.“</span><span class="sxs-lookup"><span data-stu-id="37349-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="37349-127">Vyberte **Řízení informací o produktech \> Produkty \> Uvolněné produkty** pro otevření stránky **Podrobnosti uvolněného produktu**.</span><span class="sxs-lookup"><span data-stu-id="37349-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="37349-128">V poli rychlého filtru zadejte **D8100** pro vyhledání existujícího uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="37349-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Filtrování uvolněného produktu D8100 na stránce Podrobnosti uvolněného produktu](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="37349-130">V podokně akcí na kartě **Analýza** zvolte **Postup** k otevření stránky **Postup**.</span><span class="sxs-lookup"><span data-stu-id="37349-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="37349-131">Stránka **Postup** zobrazuje osm verzí postupu pro uvolněný produkt D8100.</span><span class="sxs-lookup"><span data-stu-id="37349-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="37349-132">Osm verzí postupu je rozděleno mezi čtyři postupy na pracovišti 1 a pracovišti 5.</span><span class="sxs-lookup"><span data-stu-id="37349-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="37349-133">Postup 000400 se používá pro výpočet nákladů, postup 00041 se používá, když je lakování interní operací a postup 00042 se používá tehdy, když je lakování externí operací.</span><span class="sxs-lookup"><span data-stu-id="37349-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Osm verzí postupu na stránce Postup](./media/subcontract03_route-page.png)

4. <span data-ttu-id="37349-135">V horním podokně v mřížce **Verze** zvolte verzi postupu **00042** pro pracoviště **5**.</span><span class="sxs-lookup"><span data-stu-id="37349-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="37349-136">V dolním podokně na **Přehled** zvolte operaci **20** (**Cbnt CtSc**) v mřížce.</span><span class="sxs-lookup"><span data-stu-id="37349-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Je zvolena operace 20 pro verzi postupu 00042 pro pracoviště 5](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="37349-138">Zvolte kartu **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="37349-138">Select the **General** tab.</span></span>

    <span data-ttu-id="37349-139">Všimněte si, že pole **Typ postupu** je nastaveno na **Dodavatel**.</span><span class="sxs-lookup"><span data-stu-id="37349-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="37349-140">Tato hodnota označuje, že operace 20 (Cbnt CtSc) je subdodavatelskou operací.</span><span class="sxs-lookup"><span data-stu-id="37349-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Pole typ postupu nastavené na Dodavatel na kartě Obecné](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="37349-142">Zvolte kartu**Požadavky na zdroj**.</span><span class="sxs-lookup"><span data-stu-id="37349-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="37349-143">Možnosti budou použity pro vyhledání použitelného zdroje během plánování výroby.</span><span class="sxs-lookup"><span data-stu-id="37349-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="37349-144">U operace 20 (Cbnt CtSc) 20 si všimněte, že je nutný zdroj s dvěma možnostmi **Lakování** a **Lakované skříňky**.</span><span class="sxs-lookup"><span data-stu-id="37349-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Možnosti Lakování a Lakované skříňky na kartě požadavků na zdroj](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="37349-146">Zvolte **Použitelné prostředky** a otevřete dialogové okno **Použitelné prostředky**.</span><span class="sxs-lookup"><span data-stu-id="37349-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="37349-147">Byly nalezeny tři zdroje, které splňují požadavky na zdroje pro operaci.</span><span class="sxs-lookup"><span data-stu-id="37349-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="37349-148">Všimněte si, že zdroje 8851 a 8852 jsou typem **Dodavatel**.</span><span class="sxs-lookup"><span data-stu-id="37349-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Tři vhodné zdroje v dialogovém okně Použitelné prostředky](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="37349-150">Vyberte **OK**, zavřete dialogové okno **Použitelné prostředky** a vraťte se na stránku **Postup**.</span><span class="sxs-lookup"><span data-stu-id="37349-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="37349-151">Zavřete stránku **Postup** a vraťte se na stránku **Podrobnosti uvolněného produktu**.</span><span class="sxs-lookup"><span data-stu-id="37349-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Stránka podrobností o uvolněném produktu](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="37349-153">V podokně akcí na kartě **Analýza** zvolte **Verze kusovníku** k otevření stránky **Verze kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="37349-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="37349-154">Stránka **Verze kusovníku** zobrazuje čtyři verze kusovníku pro uvolněný produkt D8100.</span><span class="sxs-lookup"><span data-stu-id="37349-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="37349-155">Kusovník 000040 se používá pro výpočet nákladů a plánování, kusovník 000041 se používá, pokud je operace lakování prováděna interně a kusovníky 000042 a 000043 se používají v případě, že je operace lakování .subdodavatelskou aktivitou.</span><span class="sxs-lookup"><span data-stu-id="37349-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="37349-156">Všimněte si, že položka S8050 je produktem typu položky **Služba**.</span><span class="sxs-lookup"><span data-stu-id="37349-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="37349-157">Tato položka reprezentuje práci subdodavatele.</span><span class="sxs-lookup"><span data-stu-id="37349-157">This item represents the subcontracted work.</span></span>

    ![Čtyři verze kusovníku na stránce verzí kusovníku](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="37349-159">Na pevné záložce **Řádky kusovníku** zvolte **Upravit** a otevřete dialogové okno **Upravit řádek kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="37349-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="37349-160">Po vytvoření a ocenění výrobní zakázky pro uvolněný produkt D8100 bude automaticky vygenerována nákupní objednávka pro položku S8050.</span><span class="sxs-lookup"><span data-stu-id="37349-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="37349-161">Tato nákupní objednávka bude propojena na výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="37349-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="37349-162">Aby mohly být automaticky vygenerovány nákupní objednávky, je třeba nastavit **Typ řádku** na **Dodavatel** a musí být vybrán účet dodavatele pro subdodavatele.</span><span class="sxs-lookup"><span data-stu-id="37349-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="37349-163">V tomto případě je účet dodavatele US-801.</span><span class="sxs-lookup"><span data-stu-id="37349-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="37349-164">Všimněte si, že řádek kusovníku je připojen k operaci lakování prostřednictvím čísla operace (v tomto případě 20).</span><span class="sxs-lookup"><span data-stu-id="37349-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Úprava dialogové okna řádku kusovníku](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="37349-166">Vytvoření hesla pro pracovníky skladu</span><span class="sxs-lookup"><span data-stu-id="37349-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="37349-167">Musíte definovat heslo pro pracovníky skladu, kteří používají ruční zařízení.</span><span class="sxs-lookup"><span data-stu-id="37349-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="37349-168">Vyberte **Řízení skladu \> Nastavení \> Pracovník** a otevřete stránku **Uživatelé práce**.</span><span class="sxs-lookup"><span data-stu-id="37349-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="37349-169">Na pevné záložce **Uživatelé** vyberte řádek pro uživatele **51**.</span><span class="sxs-lookup"><span data-stu-id="37349-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Stránka uživatelů práce](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="37349-171">Zvolte **Resetovat heslo**.</span><span class="sxs-lookup"><span data-stu-id="37349-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="37349-172">V polích **Heslo** a **Potvrdit heslo** zadejte **1**.</span><span class="sxs-lookup"><span data-stu-id="37349-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="37349-173">Zvolte **Nastavit heslo**.</span><span class="sxs-lookup"><span data-stu-id="37349-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="37349-174">Ukázka krok za krokem</span><span class="sxs-lookup"><span data-stu-id="37349-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="37349-175">**Scénář a pozadí**</span><span class="sxs-lookup"><span data-stu-id="37349-175">**Scenario and background**</span></span>

<span data-ttu-id="37349-176">Je vytvořena výrobní zakázka na 10 kusů pro produkt D8100, „Nalakovaná skříňka.“</span><span class="sxs-lookup"><span data-stu-id="37349-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="37349-177">Lakování skříněk je subdodavatelská operace, která se provádí u dodavatele USA 801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="37349-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="37349-178">Výrobní zakázka se skládá ze tří operací.</span><span class="sxs-lookup"><span data-stu-id="37349-178">The production order consists of three operations.</span></span> <span data-ttu-id="37349-179">V první operaci je skříňka předběžně sestavena v rámci interní operace.</span><span class="sxs-lookup"><span data-stu-id="37349-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="37349-180">Materiál pro předběžné sestavení je uvolněn k výdeji ve skladu surovin.</span><span class="sxs-lookup"><span data-stu-id="37349-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="37349-181">Po dokončení předběžného sestavení je skříňka odeslána do společnosti Perfect Coating Solutions spolu s dvěma materiály, které jsou zapotřebí pro operaci lakování.</span><span class="sxs-lookup"><span data-stu-id="37349-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="37349-182">Když je nalakovaná skříňka vrácena zpět od dodavatele, projde operací konečného sestavní, než je označena jako dokončená.</span><span class="sxs-lookup"><span data-stu-id="37349-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="37349-183">Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="37349-184">V podokně akcí zvolte **Nová výrobní zakázka** a otevřete dialogové okno **Vytvořit výrobní zakázku**.</span><span class="sxs-lookup"><span data-stu-id="37349-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Vytvoření dialogového okna výrobní zakázky](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="37349-186">V poli **Číslo položky** zvolte **D8100**.</span><span class="sxs-lookup"><span data-stu-id="37349-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="37349-187">Pole dimenzí zásob se zobrazí po výběru čísla položky.</span><span class="sxs-lookup"><span data-stu-id="37349-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="37349-188">V poli **Barva** vyberte **Chromovaná**.</span><span class="sxs-lookup"><span data-stu-id="37349-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="37349-189">Objeví se okno s dotazem, zda se mají vložit aktivní verze kusovníku a postupu.</span><span class="sxs-lookup"><span data-stu-id="37349-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Okno se zprávou](./media/subcontract13_message-box.png)

5. <span data-ttu-id="37349-191">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="37349-191">Select **Yes**.</span></span> 

    <span data-ttu-id="37349-192">V dialogovém okně **Vytvořit výrobní zakázku** jsou automaticky zvoleny aktivní verze kusovníku a postupu pro produkt D8100 v polích **Číslo kusovníku** a **Číslo postupu**.</span><span class="sxs-lookup"><span data-stu-id="37349-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="37349-193">V tomto případě jsou vybrány kusovník **000040** a postup **000040**.</span><span class="sxs-lookup"><span data-stu-id="37349-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="37349-194">Pro kusovník a postup se používá verze 000040 pro výpočet nákladů a plánování.</span><span class="sxs-lookup"><span data-stu-id="37349-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="37349-195">V poli **Pracoviště** zvolte **5**.</span><span class="sxs-lookup"><span data-stu-id="37349-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="37349-196">V poli **Sklad** zvolte **51**.</span><span class="sxs-lookup"><span data-stu-id="37349-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="37349-197">V polích **Číslo kusovníku** a **Číslo postupu** změňte hodnotu, která byla automaticky vybrána, na **000042**.</span><span class="sxs-lookup"><span data-stu-id="37349-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37349-198">Pro kusovník a postup se použije verze 000042 pro postoupení subdodávky lakování skříňky dodavateli US-801.</span><span class="sxs-lookup"><span data-stu-id="37349-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Hodnoty nastavené v dialogovém okně Vytvořit výrobní zakázku](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="37349-200">Vyberte **Vytvořit** pro vytvoření výrobní zakázky a přejdete zpět na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Nová výrobní zakázka na stránce Všechny výrobní zakázky](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="37349-202">V podokně akcí na kartě **Výrobní zakázka** zvolte **Odhad** pro otevření dialogového okna **Odhad**.</span><span class="sxs-lookup"><span data-stu-id="37349-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialogové okno Odhad](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="37349-204">Vyberte **OK** pro potvrzení odhadu a přejdete zpět na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37349-205">Když je výrobní zakázky oceněna, vygeneruje se nákupní objednávka pro servisní položku S8050 pro dodavatele US-801.</span><span class="sxs-lookup"><span data-stu-id="37349-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="37349-206">V podokně akcí na kartě **Výrobní zakázka** zvolte **Kusovník** pro otevření stránky **Kusovník** , kde můžete zobrazit řádky kusovníku pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="37349-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="37349-207">U servisní položky S8050 si všimněte, že existuje odkaz na nákupní objednávku, která byla vygenerována při ocenění výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="37349-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Řádky kusovníku výrobní zakázky na stránce kusovníku](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="37349-209">Zavřete stránku **Kusovník** a vraťte se na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="37349-210">V podokně akcí na kartě **Plán** zvolte **Plánovat úlohy** pro otevření dialogového okna **Plánování úlohy**.</span><span class="sxs-lookup"><span data-stu-id="37349-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="37349-211">Určete následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="37349-211">Specify the following values:</span></span>

    - <span data-ttu-id="37349-212">V poli **Způsob plánování** vyberte **Vpřed od zítřka**.</span><span class="sxs-lookup"><span data-stu-id="37349-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="37349-213">Nastavte možnost **Omezená kapacita** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="37349-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialogové okno plánování úlohy](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="37349-215">Vyberte **OK**, zavřete dialogové okno **Plánování úlohy** a vraťte se na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="37349-216">V podokně akcí na kartě **Plán** zvolte **Ganttův diagram** a otevřete stránku **Ganttův diagram – Zobrazení zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="37349-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="37349-217">Ganttův diagram obsahuje grafické znázornění plánování výrobních úloh na prostředcích.</span><span class="sxs-lookup"><span data-stu-id="37349-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="37349-218">Všimněte si, že externí operace nátěru se skládá ze tří úloh: úloha zpracování, úloha přepravy a úloha času čekání.</span><span class="sxs-lookup"><span data-stu-id="37349-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Ganttův diagram na stránce Ganttův diagram - Zobrazení zdrojů](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="37349-220">Zavřete stránku **Ganttův diagram - Zobrazení zdrojů** a vraťte se na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="37349-221">V podokně akcí na kartě **Výrobní zakázka** zvolte **Uvolnění** pro otevření dialogového okna **Uvolnění**.</span><span class="sxs-lookup"><span data-stu-id="37349-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialogové okno uvolnění](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="37349-223">Zvolte **OK** a zavřete dialogové okno **Uvolnění**.</span><span class="sxs-lookup"><span data-stu-id="37349-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="37349-224">Vyberte **Řízení výroby \> Pravidelné úlohy \> Uvolnění do skladu \> Automaticky uvolnit řádky kusovníku a receptury** a otevřete dialogové okno **Automaticky uvolnit řádky kusovníku a receptury**.</span><span class="sxs-lookup"><span data-stu-id="37349-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialogové okno Automaticky uvolnit řádky kusovníku a receptury](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="37349-226">Vyberte **OK** a spusťte úlohu Automaticky uvolnit řádky kusovníku a receptury.</span><span class="sxs-lookup"><span data-stu-id="37349-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="37349-227">Tato úloha uvolní práci výdeje pro suroviny do skladu.</span><span class="sxs-lookup"><span data-stu-id="37349-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="37349-228">Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="37349-229">Použijte pole rychlého filtru pro volbu výrobní zakázky, na které jste pracovali.</span><span class="sxs-lookup"><span data-stu-id="37349-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="37349-230">V podokně akcí na kartě **Sklad** zvolte **Podrobnosti práce** k otevření stránky **Práce**.</span><span class="sxs-lookup"><span data-stu-id="37349-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="37349-231">Všimněte si, že stránka zobrazuje dvě sady práce pro výdej suroviny.</span><span class="sxs-lookup"><span data-stu-id="37349-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="37349-232">První práce je pro materiály M8100 a M8101.</span><span class="sxs-lookup"><span data-stu-id="37349-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="37349-233">Tyto materiály jsou spotřebovány operací 10.</span><span class="sxs-lookup"><span data-stu-id="37349-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="37349-234">Druhá práce je pro materiály M8202 a M8250.</span><span class="sxs-lookup"><span data-stu-id="37349-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="37349-235">Tyto materiály spotřebovává operace 20, což je operace subdodavatele.</span><span class="sxs-lookup"><span data-stu-id="37349-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Dvě sady práce pro výdej suroviny na stránce Práce](./media/subcontract22_work-page.png)

26. <span data-ttu-id="37349-237">Spusťte aplikaci skladu ke zpracování práce skladu pro operaci 10.</span><span class="sxs-lookup"><span data-stu-id="37349-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="37349-238">Vyberte **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="37349-239">Použijte pole rychlého filtru pro volbu výrobní zakázky, na které jste pracovali.</span><span class="sxs-lookup"><span data-stu-id="37349-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="37349-240">V podokně akcí na kartě **Výrobní zakázka** zvolte **Spustit** pro otevření dialogového okna **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="37349-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="37349-241">Na kartě **Obecné** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="37349-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="37349-242">V poli **Od operace č.**</span><span class="sxs-lookup"><span data-stu-id="37349-242">In the **From Oper. No.**</span></span> <span data-ttu-id="37349-243">zvolte **10**.</span><span class="sxs-lookup"><span data-stu-id="37349-243">field, select **10**.</span></span>
    - <span data-ttu-id="37349-244">V poli **Do operace č.**</span><span class="sxs-lookup"><span data-stu-id="37349-244">In the **To Oper. No.**</span></span> <span data-ttu-id="37349-245">zvolte **10**.</span><span class="sxs-lookup"><span data-stu-id="37349-245">field, select **10**.</span></span>

    ![Hodnoty nastavené na kartě Obecné](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="37349-247">Vyberte **OK**, zavřete dialogové okno **Spustit** a vraťte se na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="37349-248">Všimněte si, že stav výrobní zakázky je nyní **Spuštěno**.</span><span class="sxs-lookup"><span data-stu-id="37349-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="37349-249">Materiály pro operaci 10 se spotřebují automatickým zaúčtováním deníku výdejek.</span><span class="sxs-lookup"><span data-stu-id="37349-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="37349-250">Spotřeba času pro operaci 10 je zaúčtována automatických zaúčtováním deníku karet postupů.</span><span class="sxs-lookup"><span data-stu-id="37349-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="37349-251">Spusťte aplikaci skladu ke zpracování práce skladu pro operaci 20.</span><span class="sxs-lookup"><span data-stu-id="37349-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="37349-252">V podokně akcí na kartě **Výrobní zakázka** zvolte **Spustit** pro otevření dialogového okna **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="37349-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="37349-253">Na kartě **Obecné** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="37349-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="37349-254">V poli **Od operace č.**</span><span class="sxs-lookup"><span data-stu-id="37349-254">In the **From Oper. No.**</span></span> <span data-ttu-id="37349-255">zvolte **20**.</span><span class="sxs-lookup"><span data-stu-id="37349-255">field, select **20**.</span></span>
    - <span data-ttu-id="37349-256">V poli **Do operace č.**</span><span class="sxs-lookup"><span data-stu-id="37349-256">In the **To Oper. No.**</span></span> <span data-ttu-id="37349-257">zvolte **20**.</span><span class="sxs-lookup"><span data-stu-id="37349-257">field, select **20**.</span></span>
    - <span data-ttu-id="37349-258">Do pole **Množství** zadejte **10**.</span><span class="sxs-lookup"><span data-stu-id="37349-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="37349-259">Nastavte možnost **Zaúčtovat výdejku** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="37349-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Hodnoty nastavené na kartě Obecné](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="37349-261">Vyberte **OK**, zavřete dialogové okno **Spustit** a vraťte se na stránku **Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="37349-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="37349-262">Je vytvořena výdejka pro materiály, které jsou použity pro operaci lakování, a pro servisní položku.</span><span class="sxs-lookup"><span data-stu-id="37349-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="37349-263">Servisní položka reprezentuje náklady za subdodavatelskou operaci.</span><span class="sxs-lookup"><span data-stu-id="37349-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="37349-264">V podokně akcí na kartě **Zobrazení** zvolte **Výdejka** a otevřete stránku **Výdejka**.</span><span class="sxs-lookup"><span data-stu-id="37349-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="37349-265">Vyberte výdejku, která není zaúčtována, a poté vyberte číslo deníku pro zobrazení řádků deníku.</span><span class="sxs-lookup"><span data-stu-id="37349-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Řádky deníku na stránce Výdejka](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="37349-267">V podokně akcí zvolte **Tisk** \> **Sestava výdejky** a otevřete dialogové okno **Sestava výdejky**.</span><span class="sxs-lookup"><span data-stu-id="37349-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="37349-268">Nastavte možnost **Použít rozvržení poznámky k dodání** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="37349-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialogové okno sestavy výdejky](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="37349-270">Zvolte **OK** pro vygenerování sestavy **Výdejka**.</span><span class="sxs-lookup"><span data-stu-id="37349-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="37349-271">V takovém případě se vytiskne poznámka k dodání od dodavatele z deníku výrobních výdejek.</span><span class="sxs-lookup"><span data-stu-id="37349-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="37349-272">Poznámka k dodání určuje materiály expedované dodavateli, který provede operaci lakování.</span><span class="sxs-lookup"><span data-stu-id="37349-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Sestava výdejky](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="37349-274">Zavřete sestavu **Výdejka** a vraťte se na stránku **Výdejka**.</span><span class="sxs-lookup"><span data-stu-id="37349-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="37349-275">V podokně akcí zvolte **Zaúčtovat** a otevřete dialogové okno **Zaúčtovat deník**.</span><span class="sxs-lookup"><span data-stu-id="37349-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialogové okno Zaúčtování deník](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="37349-277">Zvolte **OK** a zavřete dialogové okno **Zaúčtování deník**.</span><span class="sxs-lookup"><span data-stu-id="37349-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="37349-278">Otevřené nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="37349-278">Open the purchase order.</span></span>

    ![Stránka nákupní objednávky](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="37349-280">V podokně akcí na kartě **Nákup** zvolte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="37349-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="37349-281">Zvolte **Zaúčtovat** a otevřete dialogové okno **Zaúčtování deník**.</span><span class="sxs-lookup"><span data-stu-id="37349-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="37349-282">Vyberte **OK**, zavřete dialogové okno **Zaúčtovat deník** a vraťte se na stránku **Nákupní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="37349-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="37349-283">Změňte jednotkovou cenu z **33** na **40**.</span><span class="sxs-lookup"><span data-stu-id="37349-283">Change the unit price from **33** to **40**.</span></span>

    ![Změněná jednotková cena na stránce Nákupní objednávka](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="37349-285">Potvrďte znovu nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="37349-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="37349-286">Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="37349-286">Product receipt.</span></span>

    ![Dialogové okno Zaúčtování příjemky produktu](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="37349-288">Nákupní faktura.</span><span class="sxs-lookup"><span data-stu-id="37349-288">Purchase invoice.</span></span>
52. <span data-ttu-id="37349-289">Aktualizujte stav párování.</span><span class="sxs-lookup"><span data-stu-id="37349-289">Update the match status.</span></span>

    ![Stránka faktury dodavatele](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="37349-291">Hlášení jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="37349-291">Report as finished.</span></span>

    ![Dialogové okno Hlášení jako dokončené](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="37349-293">Ukončit.</span><span class="sxs-lookup"><span data-stu-id="37349-293">End.</span></span>

    ![Dialogové okno Ukončit](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="37349-295">Porovnání nákladů.</span><span class="sxs-lookup"><span data-stu-id="37349-295">Cost comparison.</span></span>

    ![Graf porovnání nákladů](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="37349-297">Chybí nastavení v datech.</span><span class="sxs-lookup"><span data-stu-id="37349-297">Missing setup in data.</span></span>

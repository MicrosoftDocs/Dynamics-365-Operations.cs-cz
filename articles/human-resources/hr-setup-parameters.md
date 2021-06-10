---
title: Konfigurace parametrů Human Resources
description: Toto téma vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052402"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="31eb9-103">Konfigurace parametrů Human Resources</span><span class="sxs-lookup"><span data-stu-id="31eb9-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31eb9-104">Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost.</span><span class="sxs-lookup"><span data-stu-id="31eb9-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="31eb9-105">Toto téma vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost.</span><span class="sxs-lookup"><span data-stu-id="31eb9-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="31eb9-106">K nastavení parametrů lidských zdrojů slouží dvě stránky.</span><span class="sxs-lookup"><span data-stu-id="31eb9-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="31eb9-107">Pro parametry, které jsou sdíleny napříč společnostmi, použijte stránku **Sdílené parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="31eb9-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="31eb9-108">Pro parametry, které jsou specifické pro společnost (jinými slovy nastavení se použije pro jednu společnost), můžete použít stránku **Parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="31eb9-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Přechod na parametry lidských zdrojů](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="31eb9-110">Na stránce **Parametry lidských zdrojů** jsou nastavení rozdělena mezi šest karet:</span><span class="sxs-lookup"><span data-stu-id="31eb9-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="31eb9-111">**Obecný**</span><span class="sxs-lookup"><span data-stu-id="31eb9-111">**General**</span></span>
- <span data-ttu-id="31eb9-112">**Nábor** (tato karta není součástí Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="31eb9-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="31eb9-113">**Kompenzace**</span><span class="sxs-lookup"><span data-stu-id="31eb9-113">**Compensation**</span></span>
- <span data-ttu-id="31eb9-114">**Číselné řady**</span><span class="sxs-lookup"><span data-stu-id="31eb9-114">**Number sequences**</span></span>
- <span data-ttu-id="31eb9-115">**Pracovní volno**</span><span class="sxs-lookup"><span data-stu-id="31eb9-115">**FMLA**</span></span>
- <span data-ttu-id="31eb9-116">**Samoobsluha pro zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="31eb9-116">**Employee self service**</span></span>
- <span data-ttu-id="31eb9-117">**Samoobsluha pro manažery**</span><span class="sxs-lookup"><span data-stu-id="31eb9-117">**Manager self service**</span></span>
- <span data-ttu-id="31eb9-118">**Správa zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="31eb9-118">**Benefits management**</span></span>
- <span data-ttu-id="31eb9-119">**Pracovní volno a absence**</span><span class="sxs-lookup"><span data-stu-id="31eb9-119">**Leave and absence**</span></span>
- <span data-ttu-id="31eb9-120">**Způsoby platby**</span><span class="sxs-lookup"><span data-stu-id="31eb9-120">**Payment methods**</span></span>

<span data-ttu-id="31eb9-121">Každá karta obsahuje informace, které se vztahují na jednu společnost.</span><span class="sxs-lookup"><span data-stu-id="31eb9-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="31eb9-122">Obecný</span><span class="sxs-lookup"><span data-stu-id="31eb9-122">General</span></span>

<span data-ttu-id="31eb9-123">Nastavení kartě **Obecné** určuje vzhled informací o absencích, zraněních a onemocněních a nově přijatých zaměstnancích.</span><span class="sxs-lookup"><span data-stu-id="31eb9-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="31eb9-124">Nastavení na této kartě také definují některé výchozí položky, které se zobrazí při práci.</span><span class="sxs-lookup"><span data-stu-id="31eb9-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="31eb9-125">Tato karta konkrétně umožňuje:</span><span class="sxs-lookup"><span data-stu-id="31eb9-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="31eb9-126">Vybrat barvu, kterou chcete použít na otevřené transakce absencí</span><span class="sxs-lookup"><span data-stu-id="31eb9-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="31eb9-127">Určit šablonu stylů, kterou chcete použít pro sestavy</span><span class="sxs-lookup"><span data-stu-id="31eb9-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="31eb9-128">Povolit integraci mezi školeními a registrací absencí</span><span class="sxs-lookup"><span data-stu-id="31eb9-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="31eb9-129">Vybrat kód absence, který se používá k řízení této integrace.</span><span class="sxs-lookup"><span data-stu-id="31eb9-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="31eb9-130">Uvést, jak dlouho chcete zachovat případy zranění a nemoci.</span><span class="sxs-lookup"><span data-stu-id="31eb9-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="31eb9-131">Zadat výchozí identifikační číslo zobrazené při najímání nového pracovníka.</span><span class="sxs-lookup"><span data-stu-id="31eb9-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Karta Obecné](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="31eb9-133">Nábor</span><span class="sxs-lookup"><span data-stu-id="31eb9-133">Recruitment</span></span>

<span data-ttu-id="31eb9-134">Nastavení na kartě **Nábor** definují typy dokumentů používané pro korespondenci automaticky zasílanou uchazečům.</span><span class="sxs-lookup"><span data-stu-id="31eb9-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="31eb9-135">Můžete také uvést náborový projekt používaný pro nevyžádané přihlášky.</span><span class="sxs-lookup"><span data-stu-id="31eb9-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="31eb9-136">Období definované pro náborový projekt časově určuje náborové projekty, které jsou zahrnuty na dlaždici **Časové projekty** v pracovním prostoru **Řízení náboru**.</span><span class="sxs-lookup"><span data-stu-id="31eb9-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="31eb9-137">Období, které je definováno pro upozornění na termín přihlášky, slouží k zobrazení náborových projektů, kterým se blíží jejich konečný termín přihlášky na dlaždici **Blíží se termín přihlášky** v pracovním prostoru **Nábor**.</span><span class="sxs-lookup"><span data-stu-id="31eb9-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="31eb9-138">Další informace o náboru najdete na stránce [Nábor uchazečů o práci](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="31eb9-139">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="31eb9-139">Compensation</span></span>

<span data-ttu-id="31eb9-140">V aplikaci Dynamics 365 Finance definuje nastavení na kartě **Kompenzace**, zda uživatelé musí potvrzovat, že chtějí uložit informace pro plán fixní nebo variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="31eb9-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="31eb9-141">Vyberete-li možnost **Povolit ověření ukládání**, obdrží uživatelé zprávu s dotazem, zda chtějí uložit záznam, kdykoli zavřou stránku související s kompenzacemi, .</span><span class="sxs-lookup"><span data-stu-id="31eb9-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="31eb9-142">Některé stránky ve Správě kompenzací neumožní uživatelům odstranit informace.</span><span class="sxs-lookup"><span data-stu-id="31eb9-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="31eb9-143">Vyzváním uživatelů k ověření, zda chtějí informace ukládat, budete schopni omezit informace, které jsou ukládány, a později nejdou odstranit.</span><span class="sxs-lookup"><span data-stu-id="31eb9-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="31eb9-144">Pokud zrušíte zaškrtnutí možnosti **Povolit ověření ukládání**, záznamy jsou uloženy okamžitě, možná ještě předtím, než je uživatel připraven.</span><span class="sxs-lookup"><span data-stu-id="31eb9-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="31eb9-145">Pokud používáte funkci Řízení výkonnosti, můžete na kartě **Kompenzace** vybrat model hodnocení, který má být použit namísto modelu přiřazeného k plánům kompenzace při hodnocení výkonnosti.</span><span class="sxs-lookup"><span data-stu-id="31eb9-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="31eb9-146">V Human Resources můžete na kartě **Kompenzace** omezit přístup k plánům kompenzace a nastavit výchozí měnu.</span><span class="sxs-lookup"><span data-stu-id="31eb9-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="31eb9-147">Další informace o kompenzacích naleznete v tématu [Přehled plánů kompenzací](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Karta Kompenzace](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="31eb9-149">Číselné řady</span><span class="sxs-lookup"><span data-stu-id="31eb9-149">Number sequences</span></span>

<span data-ttu-id="31eb9-150">Nastavení na kartě **Číselná řada** určuje posloupnosti používané k automatickému přiřazování ID k položkám v Human Resources, například:</span><span class="sxs-lookup"><span data-stu-id="31eb9-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="31eb9-151">Žádosti</span><span class="sxs-lookup"><span data-stu-id="31eb9-151">Applications</span></span>
- <span data-ttu-id="31eb9-152">Registrace absencí</span><span class="sxs-lookup"><span data-stu-id="31eb9-152">Absence registrations</span></span>
- <span data-ttu-id="31eb9-153">Výsledky procesu kompenzace</span><span class="sxs-lookup"><span data-stu-id="31eb9-153">Compensation process results</span></span>
- <span data-ttu-id="31eb9-154">Čísla případů</span><span class="sxs-lookup"><span data-stu-id="31eb9-154">Case numbers</span></span>
- <span data-ttu-id="31eb9-155">Kurzy</span><span class="sxs-lookup"><span data-stu-id="31eb9-155">Courses</span></span>
- <span data-ttu-id="31eb9-156">Agendy kurzů</span><span class="sxs-lookup"><span data-stu-id="31eb9-156">Course agendas</span></span>

<span data-ttu-id="31eb9-157">Spravovat odkazy číselných řad a kódy můžete na stránce se seznamem **Číselné řady** (vyberete **Správa organizace > Číselné řady > Číselné řady**).</span><span class="sxs-lookup"><span data-stu-id="31eb9-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="31eb9-158">Další informace naleznete v tématu [Přehled číselných řad](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="31eb9-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="31eb9-159">Počet hodin, které jsou odpracovány nesmí překročit 1 250 a délka zaměstnání nesmí přesáhnout 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="31eb9-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="31eb9-160">Tyto maximální hodnoty jsou v souladu s federálním právem ve Spojených státech amerických.</span><span class="sxs-lookup"><span data-stu-id="31eb9-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Karta Číselné řady](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="31eb9-162">Pracovní volno</span><span class="sxs-lookup"><span data-stu-id="31eb9-162">FMLA</span></span>

<span data-ttu-id="31eb9-163">Na kartě Pracovní volno nastavíte požadavky na způsobilost a hodiny nároků na pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="31eb9-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="31eb9-164">Další informace naleznete v tématu [Konfigurace parametrů pracovního volna a absence](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![Karta Pracovní volno](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="31eb9-166">Samoobsluha pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="31eb9-166">Employee self service</span></span>

<span data-ttu-id="31eb9-167">Nastavení na kartě **Samoobsluha pro zaměstnance** ovlivňuje, jak se zaměstnancům zobrazuje jejich samoobsluha.</span><span class="sxs-lookup"><span data-stu-id="31eb9-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="31eb9-168">Na této kartě můžete:</span><span class="sxs-lookup"><span data-stu-id="31eb9-168">On this tab, you can:</span></span>

- <span data-ttu-id="31eb9-169">Zapsat název samoobslužného pracovního prostoru zaměstnance</span><span class="sxs-lookup"><span data-stu-id="31eb9-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="31eb9-170">Vybrat, jaké informace může manažer pro zaměstnance zadat</span><span class="sxs-lookup"><span data-stu-id="31eb9-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="31eb9-171">Přidat užitečné odkazy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="31eb9-171">Add useful links for employees</span></span>
- <span data-ttu-id="31eb9-172">U zaměstnanců můžete omezit jejich schopnost přidávat nebo upravovat detaily kontaktních údajů.</span><span class="sxs-lookup"><span data-stu-id="31eb9-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="31eb9-173">Další informace najdete v tématu [Omezení úpravy osobních údajů](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="31eb9-174">Další informace o nastavení samoobsluhy pro zaměstnance najdete v části [Přehled samoobsluhy pro zaměstnance a manažera](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Karta Samoobsluha pro zaměstnance](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="31eb9-176">Samoobsluha pro manažery</span><span class="sxs-lookup"><span data-stu-id="31eb9-176">Manager self service</span></span>

<span data-ttu-id="31eb9-177">Nastavení na kartě **Samoobsluha pro manažery** ovlivní to, co manažeři uvidí ve své samoobsluze.</span><span class="sxs-lookup"><span data-stu-id="31eb9-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="31eb9-178">Na této kartě můžete konfigurovat následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="31eb9-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="31eb9-179">Rozsah pro vypršení platnosti záznamů</span><span class="sxs-lookup"><span data-stu-id="31eb9-179">The range for expiring records</span></span>
- <span data-ttu-id="31eb9-180">Zda mohou manažeři informací prohlížet záznamy, jejichž platnost vyprší</span><span class="sxs-lookup"><span data-stu-id="31eb9-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="31eb9-181">Zda mohou manažeři zobrazit otevřené pozice pro další podřízené</span><span class="sxs-lookup"><span data-stu-id="31eb9-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="31eb9-182">Pohledy na odcházející pracovníky</span><span class="sxs-lookup"><span data-stu-id="31eb9-182">Views of exiting workers</span></span>
- <span data-ttu-id="31eb9-183">Užitečné odkazy pro manažery</span><span class="sxs-lookup"><span data-stu-id="31eb9-183">Useful links for managers</span></span>

<span data-ttu-id="31eb9-184">Další informace o nastavení samoobsluhy pro manažery najdete v části [Přehled samoobsluhy pro zaměstnance a manažera](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Karta Samoobsluha pro manažery](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="31eb9-186">Správa zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="31eb9-186">Benefits management</span></span>

<span data-ttu-id="31eb9-187">Na kartě Správa výhod můžete konfigurovat e-mailové možnosti pro správu výhod.</span><span class="sxs-lookup"><span data-stu-id="31eb9-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="31eb9-188">Další informace o nastavení a použití správy zaměstnaneckých výhod naleznete v tématu [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Karta Správa zaměstnaneckých výhod](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="31eb9-190">Pracovní volno a absence</span><span class="sxs-lookup"><span data-stu-id="31eb9-190">Leave and absence</span></span>

<span data-ttu-id="31eb9-191">Další informace o nastavení a používání pracovního volna a absencí získáte v části [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="31eb9-192">Způsoby platby</span><span class="sxs-lookup"><span data-stu-id="31eb9-192">Payment methods</span></span>

<span data-ttu-id="31eb9-193">Na kartě **Metody platby** můžete vybrat metody platby podporované vaší organizací.</span><span class="sxs-lookup"><span data-stu-id="31eb9-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="31eb9-194">Další informace o konfiguraci kompenzací naleznete v tématu [Přehled plánů kompenzací](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31eb9-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Karta Metody platby](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
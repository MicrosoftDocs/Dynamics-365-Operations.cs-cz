---
title: Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce
description: Toto téma vysvětluje, jak nakonfigurovat integraci mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce pro zpracování výplat.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2019
ms.locfileid: "898437"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="f2086-103">Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2086-104">Integrace mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f2086-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="f2086-105">Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Talent i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f2086-106">Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="f2086-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="f2086-107">Integrace vyžaduje specifická data z aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="f2086-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="f2086-108">Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Talent nakonfigurována tak, aby podporovala integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="f2086-109">Integrace používá následující rozsáhlé kategorie dat:</span><span class="sxs-lookup"><span data-stu-id="f2086-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f2086-110">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="f2086-110">Human resources data</span></span>
- <span data-ttu-id="f2086-111">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="f2086-111">Compensation data</span></span>
- <span data-ttu-id="f2086-112">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f2086-113">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="f2086-113">Worker data</span></span>

<span data-ttu-id="f2086-114">Toto téma popisuje postup, který je třeba provést při povolení integrace.</span><span class="sxs-lookup"><span data-stu-id="f2086-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f2086-115">Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.</span><span class="sxs-lookup"><span data-stu-id="f2086-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f2086-116">Povolení integrace</span><span class="sxs-lookup"><span data-stu-id="f2086-116">Enable the integration</span></span>

<span data-ttu-id="f2086-117">V aplikaci Talent musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f2086-118">Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 for Finance and Operations, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2086-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="f2086-119">Pro zapnutí integrace v aplikaci Talent postupuje podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f2086-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="f2086-120">Na stránce **Správa systému** zvolte **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="f2086-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f2086-121">Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.</span><span class="sxs-lookup"><span data-stu-id="f2086-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f2086-122">Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.</span><span class="sxs-lookup"><span data-stu-id="f2086-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f2086-123">Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f2086-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f2086-124">Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence.</span><span class="sxs-lookup"><span data-stu-id="f2086-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f2086-125">Tuto frekvenci lze změnit v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="f2086-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="f2086-126">Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících tématech Azure:</span><span class="sxs-lookup"><span data-stu-id="f2086-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="f2086-127">O účtech úložiště Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f2086-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f2086-128">Konfigurace řetězců připojení Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f2086-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="f2086-129">Konfigurace vašich dat</span><span class="sxs-lookup"><span data-stu-id="f2086-129">Configure your data</span></span> 

<span data-ttu-id="f2086-130">Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="f2086-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="f2086-131">Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="f2086-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f2086-132">Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f2086-133">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="f2086-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f2086-134">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="f2086-134">Benefits</span></span> 

<span data-ttu-id="f2086-135">Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f2086-136">Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f2086-137">Plány zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f2086-137">Benefit plans</span></span>

- <span data-ttu-id="f2086-138">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-138">Plan (required)</span></span>
- <span data-ttu-id="f2086-139">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-139">Type (required)</span></span>
- <span data-ttu-id="f2086-140">Dopad mzdy (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-140">Payroll impact (required)</span></span>
- <span data-ttu-id="f2086-141">Obnovit nedoplatky</span><span class="sxs-lookup"><span data-stu-id="f2086-141">Recover arrears</span></span>
- <span data-ttu-id="f2086-142">Způsobu provádění odpočtu</span><span class="sxs-lookup"><span data-stu-id="f2086-142">Deduction method</span></span>
- <span data-ttu-id="f2086-143">Priorita odpočtu</span><span class="sxs-lookup"><span data-stu-id="f2086-143">Deduction priority</span></span>
- <span data-ttu-id="f2086-144">Období limitu</span><span class="sxs-lookup"><span data-stu-id="f2086-144">Limit period</span></span>
- <span data-ttu-id="f2086-145">Částka limitu</span><span class="sxs-lookup"><span data-stu-id="f2086-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f2086-146">Zam. výhody</span><span class="sxs-lookup"><span data-stu-id="f2086-146">Benefits</span></span>

- <span data-ttu-id="f2086-147">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-147">Plan (required)</span></span>
- <span data-ttu-id="f2086-148">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-148">Type (required)</span></span>
- <span data-ttu-id="f2086-149">Možnost (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-149">Option (required)</span></span>
- <span data-ttu-id="f2086-150">ID zaměstnanecké výhody (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-150">Benefit ID (required)</span></span>
- <span data-ttu-id="f2086-151">Četnost</span><span class="sxs-lookup"><span data-stu-id="f2086-151">Frequency</span></span>
- <span data-ttu-id="f2086-152">Základ</span><span class="sxs-lookup"><span data-stu-id="f2086-152">Basis</span></span>
- <span data-ttu-id="f2086-153">Částka nebo sazba</span><span class="sxs-lookup"><span data-stu-id="f2086-153">Amount or rate</span></span>
- <span data-ttu-id="f2086-154">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f2086-155">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f2086-155">Supported frequencies</span></span> 

- <span data-ttu-id="f2086-156">Týdně</span><span class="sxs-lookup"><span data-stu-id="f2086-156">Weekly</span></span>
- <span data-ttu-id="f2086-157">Čtrnáctidenně</span><span class="sxs-lookup"><span data-stu-id="f2086-157">Bi-weekly</span></span>
- <span data-ttu-id="f2086-158">Každých 14 dní</span><span class="sxs-lookup"><span data-stu-id="f2086-158">Semi-monthly</span></span>
- <span data-ttu-id="f2086-159">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="f2086-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f2086-160">Podporované základy</span><span class="sxs-lookup"><span data-stu-id="f2086-160">Supported bases</span></span> 

- <span data-ttu-id="f2086-161">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="f2086-161">Fixed amount</span></span>
- <span data-ttu-id="f2086-162">Procento příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-162">Percent of earnings</span></span>
- <span data-ttu-id="f2086-163">Produktivní hodiny</span><span class="sxs-lookup"><span data-stu-id="f2086-163">Productive hours</span></span>

<span data-ttu-id="f2086-164">Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f2086-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f2086-165">Výběr v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-165">Selection in Talent</span></span>        | <span data-ttu-id="f2086-166">Výsledek v aplikaci Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f2086-167">None</span><span class="sxs-lookup"><span data-stu-id="f2086-167">None</span></span>                       | <span data-ttu-id="f2086-168">Nebyla vytvořena žádná srážka.</span><span class="sxs-lookup"><span data-stu-id="f2086-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="f2086-169">Jen odpočet</span><span class="sxs-lookup"><span data-stu-id="f2086-169">Deduction only</span></span>             | <span data-ttu-id="f2086-170">Byla vytvořena srážka zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f2086-171">Jen příspěvek</span><span class="sxs-lookup"><span data-stu-id="f2086-171">Contribution only</span></span>          | <span data-ttu-id="f2086-172">Byla vytvořena srážka zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="f2086-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f2086-173">Odpočet a příspěvek</span><span class="sxs-lookup"><span data-stu-id="f2086-173">Deduction and contribution</span></span> | <span data-ttu-id="f2086-174">Jsou vytvořeny srážky zaměstnance a zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="f2086-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f2086-175">Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f2086-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="f2086-176">Definování programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f2086-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f2086-177">Vytvoření nové zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="f2086-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f2086-178">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="f2086-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f2086-179">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="f2086-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f2086-180">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-180">Compensation</span></span> 

<span data-ttu-id="f2086-181">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="f2086-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f2086-182">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f2086-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f2086-183">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f2086-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f2086-184">Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f2086-185">Plány fixní kompenzace a převody mzdové sazby jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f2086-186">Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f2086-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f2086-187">Další informace o plánech kompenzace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f2086-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="f2086-188">Vytvoření plánů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f2086-189">Vytvoření plánů variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f2086-190">Vývoj struktury platu/kompenzace a plánů</span><span class="sxs-lookup"><span data-stu-id="f2086-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f2086-191">Proces kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f2086-192">Definování procesu kompenzací a výpočet výsledků</span><span class="sxs-lookup"><span data-stu-id="f2086-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f2086-193">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f2086-194">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f2086-195">Práce</span><span class="sxs-lookup"><span data-stu-id="f2086-195">Jobs</span></span> 

<span data-ttu-id="f2086-196">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="f2086-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f2086-197">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f2086-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2086-198">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="f2086-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f2086-199">Definování nových pracovních míst</span><span class="sxs-lookup"><span data-stu-id="f2086-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f2086-200">Pozice</span><span class="sxs-lookup"><span data-stu-id="f2086-200">Positions</span></span>

<span data-ttu-id="f2086-201">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="f2086-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="f2086-202">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="f2086-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f2086-203">Pozice existuje v oddělení.</span><span class="sxs-lookup"><span data-stu-id="f2086-203">A position exists in a department.</span></span> <span data-ttu-id="f2086-204">Ke každé pozic lze přiřadit pouze jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="f2086-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f2086-205">Mějte na paměti následující data a konfiguraci při vytváření pozic:</span><span class="sxs-lookup"><span data-stu-id="f2086-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f2086-206">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-206">Position (required)</span></span>
- <span data-ttu-id="f2086-207">Popis (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-207">Description (required)</span></span>
- <span data-ttu-id="f2086-208">Práce (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-208">Job (required)</span></span>
- <span data-ttu-id="f2086-209">Oddělení (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-209">Department (required)</span></span>
- <span data-ttu-id="f2086-210">Typ pozice (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-210">Position type (required)</span></span>
- <span data-ttu-id="f2086-211">Ekvivalent plného úvazku</span><span class="sxs-lookup"><span data-stu-id="f2086-211">Full-time equivalent</span></span>
- <span data-ttu-id="f2086-212">Roční normální hodiny (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="f2086-213">Placené právnickou osobu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f2086-214">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-214">Pay cycle (required)</span></span>
- <span data-ttu-id="f2086-215">Výchozí finanční dimenze – Nákladové středisko (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f2086-216">Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f2086-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f2086-217">Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f2086-218">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f2086-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2086-219">Uspořádání zaměstnanců podle oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="f2086-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f2086-220">Nastavení pozic</span><span class="sxs-lookup"><span data-stu-id="f2086-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f2086-221">Oddělení</span><span class="sxs-lookup"><span data-stu-id="f2086-221">Departments</span></span>

<span data-ttu-id="f2086-222">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="f2086-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f2086-223">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="f2086-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f2086-224">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="f2086-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f2086-225">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="f2086-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f2086-226">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f2086-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2086-227">Vytvoření oddělení a jeho přidružení k hierarchii oddělení</span><span class="sxs-lookup"><span data-stu-id="f2086-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f2086-228">Definování nových oddělení</span><span class="sxs-lookup"><span data-stu-id="f2086-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f2086-229">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="f2086-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="f2086-230">Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků.</span><span class="sxs-lookup"><span data-stu-id="f2086-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f2086-231">Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="f2086-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f2086-232">Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období.</span><span class="sxs-lookup"><span data-stu-id="f2086-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f2086-233">Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.</span><span class="sxs-lookup"><span data-stu-id="f2086-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f2086-234">Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus.</span><span class="sxs-lookup"><span data-stu-id="f2086-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f2086-235">Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="f2086-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f2086-236">Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.</span><span class="sxs-lookup"><span data-stu-id="f2086-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f2086-237">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f2086-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2086-238">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-238">Pay cycle (required)</span></span>
- <span data-ttu-id="f2086-239">Četnost platebního cyklu (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f2086-240">Počáteční datum období (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f2086-241">Výchozí datum platby (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f2086-242">Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus.</span><span class="sxs-lookup"><span data-stu-id="f2086-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f2086-243">Před integrací musí být vytvořeno nejméně jedno platební období.</span><span class="sxs-lookup"><span data-stu-id="f2086-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f2086-244">Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="f2086-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f2086-245">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-245">Earning codes</span></span>

<span data-ttu-id="f2086-246">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f2086-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2086-247">Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f2086-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f2086-248">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f2086-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2086-249">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-249">Earning Code (required)</span></span>
- <span data-ttu-id="f2086-250">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-250">Description</span></span>
- <span data-ttu-id="f2086-251">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="f2086-251">Unit of measure</span></span>
- <span data-ttu-id="f2086-252">Produktivní</span><span class="sxs-lookup"><span data-stu-id="f2086-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f2086-253">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="f2086-253">Worker data</span></span>

<span data-ttu-id="f2086-254">Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy.</span><span class="sxs-lookup"><span data-stu-id="f2086-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f2086-255">Zadané informace lze použít ke sledování pracovníků a osobních informací.</span><span class="sxs-lookup"><span data-stu-id="f2086-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f2086-256">Pro zaměstnance lze spravovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="f2086-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f2086-257">**Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.</span><span class="sxs-lookup"><span data-stu-id="f2086-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f2086-258">**Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.</span><span class="sxs-lookup"><span data-stu-id="f2086-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f2086-259">**Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.</span><span class="sxs-lookup"><span data-stu-id="f2086-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f2086-260">**Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.</span><span class="sxs-lookup"><span data-stu-id="f2086-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f2086-261">Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f2086-262">Obecné informace</span><span class="sxs-lookup"><span data-stu-id="f2086-262">General information</span></span>

- <span data-ttu-id="f2086-263">Osobní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-263">Personnel number (required)</span></span>
- <span data-ttu-id="f2086-264">Jméno (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-264">First name (required)</span></span>
- <span data-ttu-id="f2086-265">Příjmení (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-265">Last name (required)</span></span>
- <span data-ttu-id="f2086-266">Druhé jméno</span><span class="sxs-lookup"><span data-stu-id="f2086-266">Middle name</span></span>
- <span data-ttu-id="f2086-267">Datum služebního věku</span><span class="sxs-lookup"><span data-stu-id="f2086-267">Seniority date</span></span>
- <span data-ttu-id="f2086-268">Známé jako</span><span class="sxs-lookup"><span data-stu-id="f2086-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f2086-269">Osobní údaje</span><span class="sxs-lookup"><span data-stu-id="f2086-269">Personal information</span></span>

- <span data-ttu-id="f2086-270">Rodinný stav (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-270">Marital status (required)</span></span>
- <span data-ttu-id="f2086-271">Datum narození (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-271">Birth date (required)</span></span>
- <span data-ttu-id="f2086-272">Pohlaví (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-272">Gender (required)</span></span>
- <span data-ttu-id="f2086-273">Osoba s tělesným postižením</span><span class="sxs-lookup"><span data-stu-id="f2086-273">Person with disabilities</span></span>
- <span data-ttu-id="f2086-274">Země nebo oblast národnosti (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2086-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2086-275">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="f2086-275">Address information</span></span>

- <span data-ttu-id="f2086-276">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-276">Primary (required)</span></span>
- <span data-ttu-id="f2086-277">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-277">Country/region (required)</span></span>
- <span data-ttu-id="f2086-278">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-278">Postal code (required)</span></span>
- <span data-ttu-id="f2086-279">Číslo ulice (povinné) (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2086-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f2086-280">Doplňující název budovy (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2086-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f2086-281">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-281">City (required)</span></span>
- <span data-ttu-id="f2086-282">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-282">State (required)</span></span>
- <span data-ttu-id="f2086-283">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f2086-284">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="f2086-284">Contact information</span></span> 

- <span data-ttu-id="f2086-285">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-285">Primary (required)</span></span>
- <span data-ttu-id="f2086-286">Kontaktní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-286">Contact number (required)</span></span>
- <span data-ttu-id="f2086-287">Linka</span><span class="sxs-lookup"><span data-stu-id="f2086-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f2086-288">Informace o mzdě a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-288">Payroll information and earning codes</span></span>

<span data-ttu-id="f2086-289">Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby.</span><span class="sxs-lookup"><span data-stu-id="f2086-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f2086-290">Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.</span><span class="sxs-lookup"><span data-stu-id="f2086-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f2086-291">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-291">Earning codes</span></span>

- <span data-ttu-id="f2086-292">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-292">Position (required)</span></span>
- <span data-ttu-id="f2086-293">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-293">Earning Code (required)</span></span>
- <span data-ttu-id="f2086-294">Frekvence (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-294">Frequency (required)</span></span>
- <span data-ttu-id="f2086-295">Částka (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f2086-296">Mzdové informace</span><span class="sxs-lookup"><span data-stu-id="f2086-296">Payroll information</span></span>

- <span data-ttu-id="f2086-297">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="f2086-297">Payment Method</span></span>
- <span data-ttu-id="f2086-298">Ekonomická oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-298">Economic Region (required)</span></span>
- <span data-ttu-id="f2086-299">ID zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f2086-299">Employee Benefits ID</span></span>
- <span data-ttu-id="f2086-300">Národní číslo ID (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-300">National ID Number (required)</span></span>
- <span data-ttu-id="f2086-301">Číslo vojenské služby</span><span class="sxs-lookup"><span data-stu-id="f2086-301">Military Service Number</span></span>
- <span data-ttu-id="f2086-302">ID směny (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-302">Shift ID (required)</span></span>
- <span data-ttu-id="f2086-303">Daňové číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-303">Tax Number (required)</span></span>
- <span data-ttu-id="f2086-304">ID odborů (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-304">Union ID (required)</span></span>
- <span data-ttu-id="f2086-305">ID pracovního dne (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-305">Work Day ID (required)</span></span>
- <span data-ttu-id="f2086-306">Číslo pracovního povolení</span><span class="sxs-lookup"><span data-stu-id="f2086-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f2086-307">Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**.</span><span class="sxs-lookup"><span data-stu-id="f2086-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f2086-308">Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.</span><span class="sxs-lookup"><span data-stu-id="f2086-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f2086-309">Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-309">Employment details</span></span>

<span data-ttu-id="f2086-310">Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f2086-311">Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f2086-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f2086-312">Počáteční datum zaměstnání (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-312">Employment start date (required)</span></span>
- <span data-ttu-id="f2086-313">Koncové datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-313">Employment end date</span></span>
- <span data-ttu-id="f2086-314">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="f2086-314">Start date</span></span>
- <span data-ttu-id="f2086-315">Upravené počáteční datum</span><span class="sxs-lookup"><span data-stu-id="f2086-315">Adjusted start date</span></span>
- <span data-ttu-id="f2086-316">Datum ukončení zaměstnání (povinné při ukončení)</span><span class="sxs-lookup"><span data-stu-id="f2086-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f2086-317">Důvod ukončení zaměstnání (povinný při ukončení)</span><span class="sxs-lookup"><span data-stu-id="f2086-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f2086-318">Klíčová data zaměstnance se odvozují pomocí následujících informací.</span><span class="sxs-lookup"><span data-stu-id="f2086-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f2086-319">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-319">Talent</span></span>                | <span data-ttu-id="f2086-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2086-321">Datum posledního náboru</span><span class="sxs-lookup"><span data-stu-id="f2086-321">Most recent hire date</span></span> | <span data-ttu-id="f2086-322">Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2086-323">Datum výpovědi</span><span class="sxs-lookup"><span data-stu-id="f2086-323">Termination date</span></span>      | <span data-ttu-id="f2086-324">Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2086-325">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="f2086-325">Start date</span></span>            | <span data-ttu-id="f2086-326">Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f2086-327">Datum původního přijetí</span><span class="sxs-lookup"><span data-stu-id="f2086-327">Original hire date</span></span>    | <span data-ttu-id="f2086-328">Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f2086-329">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-329">Compensation</span></span>

<span data-ttu-id="f2086-330">Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f2086-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f2086-331">Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.</span><span class="sxs-lookup"><span data-stu-id="f2086-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f2086-332">Datum platnosti (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-332">Effective Date (required)</span></span>
- <span data-ttu-id="f2086-333">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="f2086-333">Expiration date</span></span>
- <span data-ttu-id="f2086-334">Mzdová sazba (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-334">Pay Rate (required)</span></span>
- <span data-ttu-id="f2086-335">Převody mzdové sazby (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f2086-336">Roční ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="f2086-337">Hodinový ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="f2086-338">Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f2086-339">U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f2086-340">Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f2086-341">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="f2086-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f2086-342">Identifikátor sociálního pojištění</span><span class="sxs-lookup"><span data-stu-id="f2086-342">Social Security identifier</span></span> 

<span data-ttu-id="f2086-343">Každý zaměstnanec musí mít jeden primární identifikátor.</span><span class="sxs-lookup"><span data-stu-id="f2086-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f2086-344">Tento identifikátor musí být typ identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f2086-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f2086-345">V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.</span><span class="sxs-lookup"><span data-stu-id="f2086-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f2086-346">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-346">Primary (required)</span></span>
- <span data-ttu-id="f2086-347">Typ identifikace = SSN</span><span class="sxs-lookup"><span data-stu-id="f2086-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f2086-348">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="f2086-348">Issued Date</span></span>
- <span data-ttu-id="f2086-349">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="f2086-349">Expiration Date</span></span>

<span data-ttu-id="f2086-350">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f2086-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f2086-351">Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.</span><span class="sxs-lookup"><span data-stu-id="f2086-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f2086-352">Bankovní účty a úhrady</span><span class="sxs-lookup"><span data-stu-id="f2086-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="f2086-353">Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="f2086-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f2086-354">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-354">Talent</span></span>                         | <span data-ttu-id="f2086-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2086-356">Číslo bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f2086-357">Kód SWIFT (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-357">SWIFT code (required)</span></span>          | <span data-ttu-id="f2086-358">Pole **ID banky** použité při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f2086-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f2086-359">Číslo pobočky (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f2086-360">Typ bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-360">Bank account type (required)</span></span>   | <span data-ttu-id="f2086-361">Pole **Typ účtu** použitý při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f2086-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f2086-362">Podporované hodnoty jsou **Běžný** a **Mzdový**.</span><span class="sxs-lookup"><span data-stu-id="f2086-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f2086-363">Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky.</span><span class="sxs-lookup"><span data-stu-id="f2086-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f2086-364">Jiné než zůstatkové účty budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="f2086-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2086-365">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="f2086-365">Address information</span></span>

<span data-ttu-id="f2086-366">Každý zaměstnanec musí mít jedno primární místo.</span><span class="sxs-lookup"><span data-stu-id="f2086-366">Every employee must have one primary location.</span></span> <span data-ttu-id="f2086-367">V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="f2086-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f2086-368">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-368">Primary (required)</span></span>
- <span data-ttu-id="f2086-369">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-369">Country/region (required)</span></span>
- <span data-ttu-id="f2086-370">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="f2086-371">Ulice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-371">Street (required)</span></span>
- <span data-ttu-id="f2086-372">Číslo ulice (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-372">Street Number (required)</span></span>
- <span data-ttu-id="f2086-373">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="f2086-373">Building Complement</span></span>
- <span data-ttu-id="f2086-374">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-374">City (required)</span></span>
- <span data-ttu-id="f2086-375">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-375">State (required)</span></span>
- <span data-ttu-id="f2086-376">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f2086-377">Konfigurace dat pro generování mzdy v USA a Kanadě</span><span class="sxs-lookup"><span data-stu-id="f2086-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f2086-378">Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="f2086-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f2086-379">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="f2086-379">Departments are required on positions.</span></span>
- <span data-ttu-id="f2086-380">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f2086-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2086-381">Aplikaci Talent lze konfigurovat tak, aby od pozic požadovala určení oddělení.</span><span class="sxs-lookup"><span data-stu-id="f2086-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="f2086-382">Chcete-li to provést, přejděte na **Sdílené pozice lidských zdrojů > Pozice > Vyžadovat oddělení na pozicích**.</span><span class="sxs-lookup"><span data-stu-id="f2086-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f2086-383">Doporučujeme, aby toto nastavení bylo vynuceno pro integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2086-384">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="f2086-384">Job types</span></span>

<span data-ttu-id="f2086-385">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="f2086-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2086-386">Typy prací jsou povinné pro zpracování mezd v USA a Kanadě.</span><span class="sxs-lookup"><span data-stu-id="f2086-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f2086-387">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="f2086-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2086-388">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="f2086-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2086-389">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2086-390">Typ práce</span><span class="sxs-lookup"><span data-stu-id="f2086-390">Job type</span></span>   | <span data-ttu-id="f2086-391">Popis</span><span class="sxs-lookup"><span data-stu-id="f2086-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2086-392">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f2086-392">Hourly</span></span>     | <span data-ttu-id="f2086-393">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f2086-393">Hourly</span></span>      |
| <span data-ttu-id="f2086-394">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f2086-394">Salaried</span></span>   | <span data-ttu-id="f2086-395">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f2086-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f2086-396">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="f2086-396">Position types</span></span> 

<span data-ttu-id="f2086-397">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="f2086-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2086-398">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="f2086-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2086-399">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2086-400">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="f2086-400">Position type</span></span>   | <span data-ttu-id="f2086-401">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2086-402">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-402">Full-time</span></span>       | <span data-ttu-id="f2086-403">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-403">Full time employee</span></span> |
| <span data-ttu-id="f2086-404">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-404">Part-time</span></span>       | <span data-ttu-id="f2086-405">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2086-406">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="f2086-406">Reason codes</span></span>

<span data-ttu-id="f2086-407">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2086-408">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2086-409">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2086-410">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f2086-410">Reason code</span></span>    | <span data-ttu-id="f2086-411">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-411">Description</span></span>      | <span data-ttu-id="f2086-412">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="f2086-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f2086-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2086-413">RESIGNATION</span></span>    | <span data-ttu-id="f2086-414">Výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-414">Resignation</span></span>      | <span data-ttu-id="f2086-415">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-415">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2086-416">TERMINATION</span></span>    | <span data-ttu-id="f2086-417">Ukončení</span><span class="sxs-lookup"><span data-stu-id="f2086-417">Termination</span></span>      | <span data-ttu-id="f2086-418">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-418">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2086-419">RETIREMENT</span></span>     | <span data-ttu-id="f2086-420">Důchod</span><span class="sxs-lookup"><span data-stu-id="f2086-420">Retirement</span></span>       | <span data-ttu-id="f2086-421">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-421">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-422">JINÝ</span><span class="sxs-lookup"><span data-stu-id="f2086-422">OTHER</span></span>          | <span data-ttu-id="f2086-423">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="f2086-423">Other Reasons</span></span>    | <span data-ttu-id="f2086-424">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-424">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2086-425">DEATH</span></span>          | <span data-ttu-id="f2086-426">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="f2086-426">Death</span></span>            | <span data-ttu-id="f2086-427">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-427">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2086-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f2086-429">Dovolená</span><span class="sxs-lookup"><span data-stu-id="f2086-429">Leave of Absence</span></span> | <span data-ttu-id="f2086-430">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-430">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2086-431">CONTRACTEND</span></span>    | <span data-ttu-id="f2086-432">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="f2086-432">End of Contract</span></span>  | <span data-ttu-id="f2086-433">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-433">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2086-434">SALARYCHANGE</span></span>   | <span data-ttu-id="f2086-435">Změna platu</span><span class="sxs-lookup"><span data-stu-id="f2086-435">Change of Salary</span></span> | <span data-ttu-id="f2086-436">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f2086-437">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="f2086-437">Marital status</span></span>

<span data-ttu-id="f2086-438">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2086-439">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2086-440">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-440">Talent</span></span>                 | <span data-ttu-id="f2086-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f2086-442">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f2086-442">Married</span></span>                | <span data-ttu-id="f2086-443">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f2086-443">Married</span></span>              |
| <span data-ttu-id="f2086-444">Jedno</span><span class="sxs-lookup"><span data-stu-id="f2086-444">Single</span></span>                 | <span data-ttu-id="f2086-445">Jedno</span><span class="sxs-lookup"><span data-stu-id="f2086-445">Single</span></span>               |
| <span data-ttu-id="f2086-446">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f2086-446">Widowed</span></span>                | <span data-ttu-id="f2086-447">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f2086-447">Widowed</span></span>              |
| <span data-ttu-id="f2086-448">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f2086-448">Divorced</span></span>               | <span data-ttu-id="f2086-449">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f2086-449">Divorced</span></span>             |
| <span data-ttu-id="f2086-450">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="f2086-450">Registered Partnership</span></span> | <span data-ttu-id="f2086-451">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="f2086-451">Domestic Partnership</span></span> |
| <span data-ttu-id="f2086-452">None</span><span class="sxs-lookup"><span data-stu-id="f2086-452">None</span></span>                   | <span data-ttu-id="f2086-453">None</span><span class="sxs-lookup"><span data-stu-id="f2086-453">None</span></span>                 |
| <span data-ttu-id="f2086-454">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f2086-454">Cohabiting</span></span>             | <span data-ttu-id="f2086-455">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f2086-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f2086-456">Rod</span><span class="sxs-lookup"><span data-stu-id="f2086-456">Gender</span></span>

<span data-ttu-id="f2086-457">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2086-458">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2086-459">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-459">Talent</span></span>       | <span data-ttu-id="f2086-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f2086-461">Muž</span><span class="sxs-lookup"><span data-stu-id="f2086-461">Male</span></span>         | <span data-ttu-id="f2086-462">Muž</span><span class="sxs-lookup"><span data-stu-id="f2086-462">Male</span></span>            |
| <span data-ttu-id="f2086-463">Žena</span><span class="sxs-lookup"><span data-stu-id="f2086-463">Female</span></span>       | <span data-ttu-id="f2086-464">Žena</span><span class="sxs-lookup"><span data-stu-id="f2086-464">Female</span></span>          |
| <span data-ttu-id="f2086-465">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="f2086-465">Non-specific</span></span> | <span data-ttu-id="f2086-466">*Nepodporováno*</span><span class="sxs-lookup"><span data-stu-id="f2086-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2086-467">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-467">Earning codes</span></span>

<span data-ttu-id="f2086-468">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f2086-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2086-469">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f2086-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2086-470">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="f2086-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2086-471">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f2086-471">Supported frequencies</span></span>

- <span data-ttu-id="f2086-472">Všechna</span><span class="sxs-lookup"><span data-stu-id="f2086-472">All</span></span>
- <span data-ttu-id="f2086-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2086-473">EVERYPAY</span></span>
- <span data-ttu-id="f2086-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2086-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2086-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2086-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2086-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2086-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2086-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-477">1OFMTH</span></span>
- <span data-ttu-id="f2086-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-478">LASTOFMTH</span></span>
- <span data-ttu-id="f2086-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-479">2OFMTH</span></span>
- <span data-ttu-id="f2086-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-480">3OFMTH</span></span>
- <span data-ttu-id="f2086-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-481">4OFMTH</span></span>
- <span data-ttu-id="f2086-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-482">5OFMTH</span></span>
- <span data-ttu-id="f2086-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-483">1N2OFMTH</span></span>
- <span data-ttu-id="f2086-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-484">3N4OFMTH</span></span>
- <span data-ttu-id="f2086-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-485">1N3OFMTH</span></span>
- <span data-ttu-id="f2086-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-486">1N4OFMTH</span></span>
- <span data-ttu-id="f2086-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-487">2N3OFMTH</span></span>
- <span data-ttu-id="f2086-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-488">2N4OFMTH</span></span>
- <span data-ttu-id="f2086-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2086-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2086-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2086-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2086-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2086-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2086-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2086-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2086-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2086-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2086-501">Adresy</span><span class="sxs-lookup"><span data-stu-id="f2086-501">Addresses</span></span>

<span data-ttu-id="f2086-502">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="f2086-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2086-503">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="f2086-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2086-504">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-504">Talent</span></span>          | <span data-ttu-id="f2086-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f2086-506">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="f2086-506">Country/Region</span></span>  | <span data-ttu-id="f2086-507">Kód země</span><span class="sxs-lookup"><span data-stu-id="f2086-507">Country Code</span></span>          |
| <span data-ttu-id="f2086-508">PSČ</span><span class="sxs-lookup"><span data-stu-id="f2086-508">Zip/Postal Code</span></span> | <span data-ttu-id="f2086-509">PSČ</span><span class="sxs-lookup"><span data-stu-id="f2086-509">Postal Code</span></span>           |
| <span data-ttu-id="f2086-510">Kraj</span><span class="sxs-lookup"><span data-stu-id="f2086-510">State</span></span>           | <span data-ttu-id="f2086-511">Kód státu</span><span class="sxs-lookup"><span data-stu-id="f2086-511">State Code</span></span>            |
| <span data-ttu-id="f2086-512">Město</span><span class="sxs-lookup"><span data-stu-id="f2086-512">City</span></span>            | <span data-ttu-id="f2086-513">Město</span><span class="sxs-lookup"><span data-stu-id="f2086-513">City</span></span>                  |
| <span data-ttu-id="f2086-514">Okres</span><span class="sxs-lookup"><span data-stu-id="f2086-514">County</span></span>          | <span data-ttu-id="f2086-515">Okres</span><span class="sxs-lookup"><span data-stu-id="f2086-515">County (Municipality)</span></span> |
| <span data-ttu-id="f2086-516">Ulice</span><span class="sxs-lookup"><span data-stu-id="f2086-516">Street</span></span>          | <span data-ttu-id="f2086-517">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="f2086-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f2086-518">Daňové oblasti</span><span class="sxs-lookup"><span data-stu-id="f2086-518">Tax regions</span></span>

<span data-ttu-id="f2086-519">Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy.</span><span class="sxs-lookup"><span data-stu-id="f2086-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f2086-520">Daňové oblasti jsou mapovány na Dayforce jako adresy místa.</span><span class="sxs-lookup"><span data-stu-id="f2086-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f2086-521">Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka.</span><span class="sxs-lookup"><span data-stu-id="f2086-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f2086-522">Daňová oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="f2086-522">Tax region (required)</span></span>
- <span data-ttu-id="f2086-523">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-523">Country/Region (required)</span></span>
- <span data-ttu-id="f2086-524">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f2086-524">State (required)</span></span>
- <span data-ttu-id="f2086-525">Okres</span><span class="sxs-lookup"><span data-stu-id="f2086-525">County</span></span> 
- <span data-ttu-id="f2086-526">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f2086-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f2086-527">Konfigurace dat pro generování mezd v Mexiku</span><span class="sxs-lookup"><span data-stu-id="f2086-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f2086-528">Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="f2086-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f2086-529">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="f2086-529">Departments are required on positions.</span></span>
- <span data-ttu-id="f2086-530">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f2086-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2086-531">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="f2086-531">Job types</span></span>

<span data-ttu-id="f2086-532">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="f2086-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2086-533">Typy práce jsou povinné pro zpracování mezd v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f2086-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f2086-534">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="f2086-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2086-535">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="f2086-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2086-536">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2086-537">Typ práce</span><span class="sxs-lookup"><span data-stu-id="f2086-537">Job type</span></span>   | <span data-ttu-id="f2086-538">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2086-539">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f2086-539">Hourly</span></span>     | <span data-ttu-id="f2086-540">MX hodinově</span><span class="sxs-lookup"><span data-stu-id="f2086-540">MX Hourly</span></span>   |
| <span data-ttu-id="f2086-541">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f2086-541">Salaried</span></span>   | <span data-ttu-id="f2086-542">MX Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f2086-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f2086-543">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="f2086-543">Position types</span></span> 

<span data-ttu-id="f2086-544">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="f2086-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2086-545">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="f2086-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2086-546">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2086-547">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="f2086-547">Position type</span></span>   | <span data-ttu-id="f2086-548">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2086-549">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-549">Full-time</span></span>       | <span data-ttu-id="f2086-550">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-550">Full time employee</span></span> |
| <span data-ttu-id="f2086-551">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-551">Part-time</span></span>       | <span data-ttu-id="f2086-552">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f2086-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2086-553">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="f2086-553">Reason codes</span></span>

<span data-ttu-id="f2086-554">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2086-555">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f2086-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2086-556">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2086-557">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f2086-557">Reason code</span></span>            | <span data-ttu-id="f2086-558">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-558">Description</span></span>                    | <span data-ttu-id="f2086-559">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="f2086-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f2086-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="f2086-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f2086-561">Odchod před první mzdou</span><span class="sxs-lookup"><span data-stu-id="f2086-561">Departure before first payroll</span></span> | <span data-ttu-id="f2086-562">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-562">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2086-563">RESIGNATION</span></span>            | <span data-ttu-id="f2086-564">Výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-564">Resignation</span></span>                    | <span data-ttu-id="f2086-565">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-565">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="f2086-566">PENSION</span></span>                | <span data-ttu-id="f2086-567">Důchod</span><span class="sxs-lookup"><span data-stu-id="f2086-567">Pension</span></span>                        | <span data-ttu-id="f2086-568">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-568">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2086-569">TERMINATION</span></span>            | <span data-ttu-id="f2086-570">Ukončení</span><span class="sxs-lookup"><span data-stu-id="f2086-570">Termination</span></span>                    | <span data-ttu-id="f2086-571">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-571">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2086-572">RETIREMENT</span></span>             | <span data-ttu-id="f2086-573">Důchod</span><span class="sxs-lookup"><span data-stu-id="f2086-573">Retirement</span></span>                     | <span data-ttu-id="f2086-574">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-574">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="f2086-575">ABSENTEE</span></span>               | <span data-ttu-id="f2086-576">Nepřítomný</span><span class="sxs-lookup"><span data-stu-id="f2086-576">Absentee</span></span>                       | <span data-ttu-id="f2086-577">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-577">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-578">JINÝ</span><span class="sxs-lookup"><span data-stu-id="f2086-578">OTHER</span></span>                  | <span data-ttu-id="f2086-579">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="f2086-579">Other Reasons</span></span>                  | <span data-ttu-id="f2086-580">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-580">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="f2086-581">CLOSURE</span></span>                | <span data-ttu-id="f2086-582">Obchodní uzávěrka</span><span class="sxs-lookup"><span data-stu-id="f2086-582">Business Closure</span></span>               | <span data-ttu-id="f2086-583">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-583">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2086-584">DEATH</span></span>                  | <span data-ttu-id="f2086-585">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="f2086-585">Death</span></span>                          | <span data-ttu-id="f2086-586">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-586">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2086-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f2086-588">Dovolená</span><span class="sxs-lookup"><span data-stu-id="f2086-588">Leave of Absence</span></span>               | <span data-ttu-id="f2086-589">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-589">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2086-590">CONTRACTEND</span></span>            | <span data-ttu-id="f2086-591">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="f2086-591">End of Contract</span></span>                | <span data-ttu-id="f2086-592">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f2086-592">Terminate worker</span></span>     |
| <span data-ttu-id="f2086-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2086-593">SALARYCHANGE</span></span>           | <span data-ttu-id="f2086-594">Změna platu</span><span class="sxs-lookup"><span data-stu-id="f2086-594">Change of Salary</span></span>               | <span data-ttu-id="f2086-595">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f2086-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f2086-596">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-596">Terms of employment</span></span>

<span data-ttu-id="f2086-597">Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f2086-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f2086-598">Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f2086-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f2086-599">Následující podmínky zaměstnání a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f2086-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f2086-600">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f2086-600">Terms of employment</span></span>   | <span data-ttu-id="f2086-601">popis</span><span class="sxs-lookup"><span data-stu-id="f2086-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f2086-602">Řádné</span><span class="sxs-lookup"><span data-stu-id="f2086-602">Regular</span></span>               | <span data-ttu-id="f2086-603">Řádné</span><span class="sxs-lookup"><span data-stu-id="f2086-603">Regular</span></span>     |
| <span data-ttu-id="f2086-604">Přímo</span><span class="sxs-lookup"><span data-stu-id="f2086-604">Direct</span></span>                | <span data-ttu-id="f2086-605">Přímo</span><span class="sxs-lookup"><span data-stu-id="f2086-605">Direct</span></span>      |
| <span data-ttu-id="f2086-606">Stáž</span><span class="sxs-lookup"><span data-stu-id="f2086-606">Internship</span></span>            | <span data-ttu-id="f2086-607">Stáž</span><span class="sxs-lookup"><span data-stu-id="f2086-607">Internship</span></span>  |
| <span data-ttu-id="f2086-608">Trvalé</span><span class="sxs-lookup"><span data-stu-id="f2086-608">Permanent</span></span>             | <span data-ttu-id="f2086-609">Trvalé</span><span class="sxs-lookup"><span data-stu-id="f2086-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f2086-610">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="f2086-610">Marital status</span></span>

<span data-ttu-id="f2086-611">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2086-612">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2086-613">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-613">Talent</span></span>                 | <span data-ttu-id="f2086-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f2086-615">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f2086-615">Married</span></span>                | <span data-ttu-id="f2086-616">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f2086-616">Married</span></span>                   |
| <span data-ttu-id="f2086-617">Jedno</span><span class="sxs-lookup"><span data-stu-id="f2086-617">Single</span></span>                 | <span data-ttu-id="f2086-618">Jedno</span><span class="sxs-lookup"><span data-stu-id="f2086-618">Single</span></span>                    |
| <span data-ttu-id="f2086-619">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f2086-619">Widowed</span></span>                | <span data-ttu-id="f2086-620">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f2086-620">Widowed</span></span>                   |
| <span data-ttu-id="f2086-621">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f2086-621">Divorced</span></span>               | <span data-ttu-id="f2086-622">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f2086-622">Divorced</span></span>                  |
| <span data-ttu-id="f2086-623">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="f2086-623">Registered Partnership</span></span> | <span data-ttu-id="f2086-624">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="f2086-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="f2086-625">None</span><span class="sxs-lookup"><span data-stu-id="f2086-625">None</span></span>                   | <span data-ttu-id="f2086-626">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2086-627">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f2086-627">Cohabiting</span></span>             | <span data-ttu-id="f2086-628">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f2086-629">Rod</span><span class="sxs-lookup"><span data-stu-id="f2086-629">Gender</span></span>

<span data-ttu-id="f2086-630">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2086-631">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2086-632">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-632">Talent</span></span>       | <span data-ttu-id="f2086-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f2086-634">Muž</span><span class="sxs-lookup"><span data-stu-id="f2086-634">Male</span></span>         | <span data-ttu-id="f2086-635">Muž</span><span class="sxs-lookup"><span data-stu-id="f2086-635">Male</span></span>                      |
| <span data-ttu-id="f2086-636">Žena</span><span class="sxs-lookup"><span data-stu-id="f2086-636">Female</span></span>       | <span data-ttu-id="f2086-637">Žena</span><span class="sxs-lookup"><span data-stu-id="f2086-637">Female</span></span>                    |
| <span data-ttu-id="f2086-638">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="f2086-638">Non-specific</span></span> | <span data-ttu-id="f2086-639">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f2086-640">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="f2086-640">Payment method</span></span>

<span data-ttu-id="f2086-641">Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="f2086-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f2086-642">Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2086-643">Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f2086-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2086-644">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-644">Talent</span></span>             | <span data-ttu-id="f2086-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f2086-646">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2086-646">Cash</span></span>               | <span data-ttu-id="f2086-647">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2086-647">Cash</span></span>                      |
| <span data-ttu-id="f2086-648">Elektronická platba</span><span class="sxs-lookup"><span data-stu-id="f2086-648">Electronic Payment</span></span> | <span data-ttu-id="f2086-649">Převod</span><span class="sxs-lookup"><span data-stu-id="f2086-649">Transfer</span></span>                  |
| <span data-ttu-id="f2086-650">Kontrola</span><span class="sxs-lookup"><span data-stu-id="f2086-650">Check</span></span>              | <span data-ttu-id="f2086-651">Šek</span><span class="sxs-lookup"><span data-stu-id="f2086-651">Cheque</span></span>                    |
| <span data-ttu-id="f2086-652">Bankovní směnka</span><span class="sxs-lookup"><span data-stu-id="f2086-652">Bank Draft</span></span>         | <span data-ttu-id="f2086-653">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2086-654">Další</span><span class="sxs-lookup"><span data-stu-id="f2086-654">Other</span></span>              | <span data-ttu-id="f2086-655">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f2086-656">Typ bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="f2086-656">Bank account type</span></span>

<span data-ttu-id="f2086-657">Typy bankovního účtu se používají pro elektronické platby zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="f2086-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f2086-658">Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu.</span><span class="sxs-lookup"><span data-stu-id="f2086-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f2086-659">Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f2086-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f2086-660">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-660">Talent</span></span>            | <span data-ttu-id="f2086-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f2086-662">Běžný účet</span><span class="sxs-lookup"><span data-stu-id="f2086-662">Checking Account</span></span>  | <span data-ttu-id="f2086-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="f2086-663">CheckingAccount</span></span>           |
| <span data-ttu-id="f2086-664">Mzdový účet</span><span class="sxs-lookup"><span data-stu-id="f2086-664">Payroll Account</span></span>   | <span data-ttu-id="f2086-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="f2086-665">PayrollAccount</span></span>            |
| <span data-ttu-id="f2086-666">Spořicí účet</span><span class="sxs-lookup"><span data-stu-id="f2086-666">Savings Account</span></span>   | <span data-ttu-id="f2086-667">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2086-668">BankGirot účet</span><span class="sxs-lookup"><span data-stu-id="f2086-668">BankGirot account</span></span> | <span data-ttu-id="f2086-669">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2086-670">PlusGirot účet</span><span class="sxs-lookup"><span data-stu-id="f2086-670">PlusGirot account</span></span> | <span data-ttu-id="f2086-671">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f2086-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2086-672">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f2086-672">Earning codes</span></span>

<span data-ttu-id="f2086-673">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f2086-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2086-674">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f2086-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2086-675">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="f2086-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2086-676">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f2086-676">Supported frequencies</span></span>

- <span data-ttu-id="f2086-677">Všechna</span><span class="sxs-lookup"><span data-stu-id="f2086-677">All</span></span>
- <span data-ttu-id="f2086-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2086-678">EVERYPAY</span></span>
- <span data-ttu-id="f2086-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2086-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2086-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2086-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2086-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2086-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2086-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-682">1OFMTH</span></span>
- <span data-ttu-id="f2086-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-683">LASTOFMTH</span></span>
- <span data-ttu-id="f2086-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-684">2OFMTH</span></span>
- <span data-ttu-id="f2086-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-685">3OFMTH</span></span>
- <span data-ttu-id="f2086-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-686">4OFMTH</span></span>
- <span data-ttu-id="f2086-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-687">5OFMTH</span></span>
- <span data-ttu-id="f2086-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-688">1N2OFMTH</span></span>
- <span data-ttu-id="f2086-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-689">3N4OFMTH</span></span>
- <span data-ttu-id="f2086-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-690">1N3OFMTH</span></span>
- <span data-ttu-id="f2086-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-691">1N4OFMTH</span></span>
- <span data-ttu-id="f2086-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-692">2N3OFMTH</span></span>
- <span data-ttu-id="f2086-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-693">2N4OFMTH</span></span>
- <span data-ttu-id="f2086-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2086-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2086-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2086-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2086-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2086-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2086-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2086-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2086-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2086-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2086-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2086-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2086-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2086-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2086-706">Adresy</span><span class="sxs-lookup"><span data-stu-id="f2086-706">Addresses</span></span>

<span data-ttu-id="f2086-707">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="f2086-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2086-708">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="f2086-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2086-709">Talent</span><span class="sxs-lookup"><span data-stu-id="f2086-709">Talent</span></span>              | <span data-ttu-id="f2086-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2086-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f2086-711">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="f2086-711">Country/Region</span></span>      | <span data-ttu-id="f2086-712">Kód země</span><span class="sxs-lookup"><span data-stu-id="f2086-712">Country Code</span></span>          |
| <span data-ttu-id="f2086-713">PSČ</span><span class="sxs-lookup"><span data-stu-id="f2086-713">Zip/Postal Code</span></span>     | <span data-ttu-id="f2086-714">PSČ</span><span class="sxs-lookup"><span data-stu-id="f2086-714">Postal Code</span></span>           |
| <span data-ttu-id="f2086-715">Kraj</span><span class="sxs-lookup"><span data-stu-id="f2086-715">State</span></span>               | <span data-ttu-id="f2086-716">Kód státu</span><span class="sxs-lookup"><span data-stu-id="f2086-716">State Code</span></span>            |
| <span data-ttu-id="f2086-717">Město</span><span class="sxs-lookup"><span data-stu-id="f2086-717">City</span></span>                | <span data-ttu-id="f2086-718">Město</span><span class="sxs-lookup"><span data-stu-id="f2086-718">City</span></span>                  |
| <span data-ttu-id="f2086-719">Okres</span><span class="sxs-lookup"><span data-stu-id="f2086-719">County</span></span>              | <span data-ttu-id="f2086-720">Okres</span><span class="sxs-lookup"><span data-stu-id="f2086-720">County (Municipality)</span></span> |
| <span data-ttu-id="f2086-721">Ulice</span><span class="sxs-lookup"><span data-stu-id="f2086-721">Street</span></span>              | <span data-ttu-id="f2086-722">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="f2086-722">Address Line 1</span></span>        |
| <span data-ttu-id="f2086-723">Číslo popisné</span><span class="sxs-lookup"><span data-stu-id="f2086-723">Street Number</span></span>       | <span data-ttu-id="f2086-724">Řádek adresy 2</span><span class="sxs-lookup"><span data-stu-id="f2086-724">Address Line 2</span></span>        |
| <span data-ttu-id="f2086-725">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="f2086-725">Building Complement</span></span> | <span data-ttu-id="f2086-726">Řádek adresy 5</span><span class="sxs-lookup"><span data-stu-id="f2086-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f2086-727">Číslo cestovního pasu</span><span class="sxs-lookup"><span data-stu-id="f2086-727">Passport number</span></span>

<span data-ttu-id="f2086-728">Zaměstnanci mohou deklarovat informace o cestovním pasu.</span><span class="sxs-lookup"><span data-stu-id="f2086-728">Employees can declare passport information.</span></span> <span data-ttu-id="f2086-729">Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="f2086-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f2086-730">Typ identifikace = Pas</span><span class="sxs-lookup"><span data-stu-id="f2086-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f2086-731">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="f2086-731">Issued Date</span></span>
- <span data-ttu-id="f2086-732">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="f2086-732">Expiration Date</span></span>

<span data-ttu-id="f2086-733">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**.</span><span class="sxs-lookup"><span data-stu-id="f2086-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f2086-734">Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu.</span><span class="sxs-lookup"><span data-stu-id="f2086-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f2086-735">Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.</span><span class="sxs-lookup"><span data-stu-id="f2086-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

---
title: Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce
description: Toto téma vysvětluje, jak nakonfigurovat integraci mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce pro zpracování výplat.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303551"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="be51f-103">Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be51f-104">Integrace mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="be51f-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="be51f-105">Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Talent i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="be51f-106">Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="be51f-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="be51f-107">Integrace vyžaduje specifická data z aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="be51f-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="be51f-108">Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Talent nakonfigurována tak, aby podporovala integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="be51f-109">Integrace používá následující rozsáhlé kategorie dat:</span><span class="sxs-lookup"><span data-stu-id="be51f-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="be51f-110">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="be51f-110">Human resources data</span></span>
- <span data-ttu-id="be51f-111">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="be51f-111">Compensation data</span></span>
- <span data-ttu-id="be51f-112">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="be51f-113">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="be51f-113">Worker data</span></span>

<span data-ttu-id="be51f-114">Toto téma popisuje postup, který je třeba provést při povolení integrace.</span><span class="sxs-lookup"><span data-stu-id="be51f-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="be51f-115">Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.</span><span class="sxs-lookup"><span data-stu-id="be51f-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="be51f-116">Povolení integrace</span><span class="sxs-lookup"><span data-stu-id="be51f-116">Enable the integration</span></span>

<span data-ttu-id="be51f-117">V aplikaci Talent musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="be51f-118">Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 for Finance and Operations, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="be51f-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="be51f-119">Pro zapnutí integrace v aplikaci Talent postupuje podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="be51f-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="be51f-120">Na stránce **Správa systému** zvolte **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="be51f-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="be51f-121">Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.</span><span class="sxs-lookup"><span data-stu-id="be51f-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="be51f-122">Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.</span><span class="sxs-lookup"><span data-stu-id="be51f-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="be51f-123">Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be51f-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="be51f-124">Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence.</span><span class="sxs-lookup"><span data-stu-id="be51f-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="be51f-125">Tuto frekvenci lze změnit v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="be51f-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="be51f-126">Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících tématech Azure:</span><span class="sxs-lookup"><span data-stu-id="be51f-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="be51f-127">O účtech úložiště Azure Storage</span><span class="sxs-lookup"><span data-stu-id="be51f-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="be51f-128">Konfigurace řetězců připojení Azure Storage</span><span class="sxs-lookup"><span data-stu-id="be51f-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="be51f-129">Konfigurace vašich dat</span><span class="sxs-lookup"><span data-stu-id="be51f-129">Configure your data</span></span> 

<span data-ttu-id="be51f-130">Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="be51f-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="be51f-131">Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="be51f-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="be51f-132">Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="be51f-133">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="be51f-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="be51f-134">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="be51f-134">Benefits</span></span> 

<span data-ttu-id="be51f-135">Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="be51f-136">Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="be51f-137">Plány zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="be51f-137">Benefit plans</span></span>

- <span data-ttu-id="be51f-138">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-138">Plan (required)</span></span>
- <span data-ttu-id="be51f-139">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-139">Type (required)</span></span>
- <span data-ttu-id="be51f-140">Dopad mzdy (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-140">Payroll impact (required)</span></span>
- <span data-ttu-id="be51f-141">Obnovit nedoplatky</span><span class="sxs-lookup"><span data-stu-id="be51f-141">Recover arrears</span></span>
- <span data-ttu-id="be51f-142">Způsobu provádění odpočtu</span><span class="sxs-lookup"><span data-stu-id="be51f-142">Deduction method</span></span>
- <span data-ttu-id="be51f-143">Priorita odpočtu</span><span class="sxs-lookup"><span data-stu-id="be51f-143">Deduction priority</span></span>
- <span data-ttu-id="be51f-144">Období limitu</span><span class="sxs-lookup"><span data-stu-id="be51f-144">Limit period</span></span>
- <span data-ttu-id="be51f-145">Částka limitu</span><span class="sxs-lookup"><span data-stu-id="be51f-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="be51f-146">Zam. výhody</span><span class="sxs-lookup"><span data-stu-id="be51f-146">Benefits</span></span>

- <span data-ttu-id="be51f-147">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-147">Plan (required)</span></span>
- <span data-ttu-id="be51f-148">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-148">Type (required)</span></span>
- <span data-ttu-id="be51f-149">Možnost (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-149">Option (required)</span></span>
- <span data-ttu-id="be51f-150">ID zaměstnanecké výhody (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-150">Benefit ID (required)</span></span>
- <span data-ttu-id="be51f-151">Četnost</span><span class="sxs-lookup"><span data-stu-id="be51f-151">Frequency</span></span>
- <span data-ttu-id="be51f-152">Základ</span><span class="sxs-lookup"><span data-stu-id="be51f-152">Basis</span></span>
- <span data-ttu-id="be51f-153">Částka nebo sazba</span><span class="sxs-lookup"><span data-stu-id="be51f-153">Amount or rate</span></span>
- <span data-ttu-id="be51f-154">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="be51f-155">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="be51f-155">Supported frequencies</span></span> 

- <span data-ttu-id="be51f-156">Týdně</span><span class="sxs-lookup"><span data-stu-id="be51f-156">Weekly</span></span>
- <span data-ttu-id="be51f-157">Čtrnáctidenně</span><span class="sxs-lookup"><span data-stu-id="be51f-157">Bi-weekly</span></span>
- <span data-ttu-id="be51f-158">Každých 14 dní</span><span class="sxs-lookup"><span data-stu-id="be51f-158">Semi-monthly</span></span>
- <span data-ttu-id="be51f-159">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="be51f-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="be51f-160">Podporované základy</span><span class="sxs-lookup"><span data-stu-id="be51f-160">Supported bases</span></span> 

- <span data-ttu-id="be51f-161">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="be51f-161">Fixed amount</span></span>
- <span data-ttu-id="be51f-162">Procento příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-162">Percent of earnings</span></span>
- <span data-ttu-id="be51f-163">Produktivní hodiny</span><span class="sxs-lookup"><span data-stu-id="be51f-163">Productive hours</span></span>

<span data-ttu-id="be51f-164">Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="be51f-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="be51f-165">Výběr v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-165">Selection in Talent</span></span>        | <span data-ttu-id="be51f-166">Výsledek v aplikaci Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="be51f-167">None</span><span class="sxs-lookup"><span data-stu-id="be51f-167">None</span></span>                       | <span data-ttu-id="be51f-168">Nebyla vytvořena žádná srážka.</span><span class="sxs-lookup"><span data-stu-id="be51f-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="be51f-169">Jen odpočet</span><span class="sxs-lookup"><span data-stu-id="be51f-169">Deduction only</span></span>             | <span data-ttu-id="be51f-170">Byla vytvořena srážka zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="be51f-171">Jen příspěvek</span><span class="sxs-lookup"><span data-stu-id="be51f-171">Contribution only</span></span>          | <span data-ttu-id="be51f-172">Byla vytvořena srážka zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="be51f-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="be51f-173">Odpočet a příspěvek</span><span class="sxs-lookup"><span data-stu-id="be51f-173">Deduction and contribution</span></span> | <span data-ttu-id="be51f-174">Jsou vytvořeny srážky zaměstnance a zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="be51f-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="be51f-175">Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="be51f-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="be51f-176">Definování programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="be51f-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="be51f-177">Vytvoření nové zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="be51f-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="be51f-178">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="be51f-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="be51f-179">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="be51f-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="be51f-180">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-180">Compensation</span></span> 

<span data-ttu-id="be51f-181">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="be51f-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="be51f-182">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="be51f-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="be51f-183">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="be51f-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="be51f-184">Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="be51f-185">Plány fixní kompenzace a převody mzdové sazby jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="be51f-186">Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="be51f-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="be51f-187">Další informace o plánech kompenzace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="be51f-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="be51f-188">Vytvoření plánů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="be51f-189">Vytvoření plánů variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="be51f-190">Vývoj struktury platu/kompenzace a plánů</span><span class="sxs-lookup"><span data-stu-id="be51f-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="be51f-191">Proces kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="be51f-192">Definování procesu kompenzací a výpočet výsledků</span><span class="sxs-lookup"><span data-stu-id="be51f-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="be51f-193">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="be51f-194">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="be51f-195">Práce</span><span class="sxs-lookup"><span data-stu-id="be51f-195">Jobs</span></span> 

<span data-ttu-id="be51f-196">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="be51f-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="be51f-197">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="be51f-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="be51f-198">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="be51f-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="be51f-199">Definování nových pracovních míst</span><span class="sxs-lookup"><span data-stu-id="be51f-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="be51f-200">Pozice</span><span class="sxs-lookup"><span data-stu-id="be51f-200">Positions</span></span>

<span data-ttu-id="be51f-201">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="be51f-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="be51f-202">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="be51f-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="be51f-203">Pozice existuje v oddělení.</span><span class="sxs-lookup"><span data-stu-id="be51f-203">A position exists in a department.</span></span> <span data-ttu-id="be51f-204">Ke každé pozic lze přiřadit pouze jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="be51f-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="be51f-205">Mějte na paměti následující data a konfiguraci při vytváření pozic:</span><span class="sxs-lookup"><span data-stu-id="be51f-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="be51f-206">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-206">Position (required)</span></span>
- <span data-ttu-id="be51f-207">Popis (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-207">Description (required)</span></span>
- <span data-ttu-id="be51f-208">Práce (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-208">Job (required)</span></span>
- <span data-ttu-id="be51f-209">Oddělení (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-209">Department (required)</span></span>
- <span data-ttu-id="be51f-210">Typ pozice (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-210">Position type (required)</span></span>
- <span data-ttu-id="be51f-211">Ekvivalent plného úvazku</span><span class="sxs-lookup"><span data-stu-id="be51f-211">Full-time equivalent</span></span>
- <span data-ttu-id="be51f-212">Roční normální hodiny (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="be51f-213">Placené právnickou osobu (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="be51f-214">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-214">Pay cycle (required)</span></span>
- <span data-ttu-id="be51f-215">Výchozí finanční dimenze – Nákladové středisko (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="be51f-216">Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu</span><span class="sxs-lookup"><span data-stu-id="be51f-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="be51f-217">Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="be51f-218">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="be51f-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="be51f-219">Uspořádání zaměstnanců podle oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="be51f-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="be51f-220">Nastavení pozic</span><span class="sxs-lookup"><span data-stu-id="be51f-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="be51f-221">Oddělení</span><span class="sxs-lookup"><span data-stu-id="be51f-221">Departments</span></span>

<span data-ttu-id="be51f-222">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="be51f-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="be51f-223">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="be51f-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="be51f-224">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="be51f-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="be51f-225">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="be51f-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="be51f-226">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="be51f-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="be51f-227">Vytvoření oddělení a jeho přidružení k hierarchii oddělení</span><span class="sxs-lookup"><span data-stu-id="be51f-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="be51f-228">Definování nových oddělení</span><span class="sxs-lookup"><span data-stu-id="be51f-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="be51f-229">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="be51f-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="be51f-230">Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků.</span><span class="sxs-lookup"><span data-stu-id="be51f-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="be51f-231">Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="be51f-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="be51f-232">Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období.</span><span class="sxs-lookup"><span data-stu-id="be51f-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="be51f-233">Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.</span><span class="sxs-lookup"><span data-stu-id="be51f-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="be51f-234">Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus.</span><span class="sxs-lookup"><span data-stu-id="be51f-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="be51f-235">Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="be51f-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="be51f-236">Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.</span><span class="sxs-lookup"><span data-stu-id="be51f-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="be51f-237">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="be51f-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="be51f-238">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-238">Pay cycle (required)</span></span>
- <span data-ttu-id="be51f-239">Četnost platebního cyklu (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="be51f-240">Počáteční datum období (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="be51f-241">Výchozí datum platby (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="be51f-242">Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus.</span><span class="sxs-lookup"><span data-stu-id="be51f-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="be51f-243">Před integrací musí být vytvořeno nejméně jedno platební období.</span><span class="sxs-lookup"><span data-stu-id="be51f-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="be51f-244">Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="be51f-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="be51f-245">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-245">Earning codes</span></span>

<span data-ttu-id="be51f-246">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="be51f-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be51f-247">Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="be51f-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="be51f-248">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="be51f-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="be51f-249">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-249">Earning Code (required)</span></span>
- <span data-ttu-id="be51f-250">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-250">Description</span></span>
- <span data-ttu-id="be51f-251">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="be51f-251">Unit of measure</span></span>
- <span data-ttu-id="be51f-252">Produktivní</span><span class="sxs-lookup"><span data-stu-id="be51f-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="be51f-253">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="be51f-253">Worker data</span></span>

<span data-ttu-id="be51f-254">Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy.</span><span class="sxs-lookup"><span data-stu-id="be51f-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="be51f-255">Zadané informace lze použít ke sledování pracovníků a osobních informací.</span><span class="sxs-lookup"><span data-stu-id="be51f-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="be51f-256">Pro zaměstnance lze spravovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="be51f-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="be51f-257">**Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.</span><span class="sxs-lookup"><span data-stu-id="be51f-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="be51f-258">**Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.</span><span class="sxs-lookup"><span data-stu-id="be51f-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="be51f-259">**Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.</span><span class="sxs-lookup"><span data-stu-id="be51f-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="be51f-260">**Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.</span><span class="sxs-lookup"><span data-stu-id="be51f-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="be51f-261">Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="be51f-262">Obecné informace</span><span class="sxs-lookup"><span data-stu-id="be51f-262">General information</span></span>

- <span data-ttu-id="be51f-263">Osobní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-263">Personnel number (required)</span></span>
- <span data-ttu-id="be51f-264">Jméno (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-264">First name (required)</span></span>
- <span data-ttu-id="be51f-265">Příjmení (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-265">Last name (required)</span></span>
- <span data-ttu-id="be51f-266">Druhé jméno</span><span class="sxs-lookup"><span data-stu-id="be51f-266">Middle name</span></span>
- <span data-ttu-id="be51f-267">Datum služebního věku</span><span class="sxs-lookup"><span data-stu-id="be51f-267">Seniority date</span></span>
- <span data-ttu-id="be51f-268">Známé jako</span><span class="sxs-lookup"><span data-stu-id="be51f-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="be51f-269">Osobní údaje</span><span class="sxs-lookup"><span data-stu-id="be51f-269">Personal information</span></span>

- <span data-ttu-id="be51f-270">Rodinný stav (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-270">Marital status (required)</span></span>
- <span data-ttu-id="be51f-271">Datum narození (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-271">Birth date (required)</span></span>
- <span data-ttu-id="be51f-272">Pohlaví (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-272">Gender (required)</span></span>
- <span data-ttu-id="be51f-273">Osoba s tělesným postižením</span><span class="sxs-lookup"><span data-stu-id="be51f-273">Person with disabilities</span></span>
- <span data-ttu-id="be51f-274">Země nebo oblast národnosti (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="be51f-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="be51f-275">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="be51f-275">Address information</span></span>

- <span data-ttu-id="be51f-276">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-276">Primary (required)</span></span>
- <span data-ttu-id="be51f-277">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-277">Country/region (required)</span></span>
- <span data-ttu-id="be51f-278">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-278">Postal code (required)</span></span>
- <span data-ttu-id="be51f-279">Číslo ulice (povinné) (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="be51f-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="be51f-280">Doplňující název budovy (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="be51f-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="be51f-281">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-281">City (required)</span></span>
- <span data-ttu-id="be51f-282">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-282">State (required)</span></span>
- <span data-ttu-id="be51f-283">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="be51f-284">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="be51f-284">Contact information</span></span> 

- <span data-ttu-id="be51f-285">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-285">Primary (required)</span></span>
- <span data-ttu-id="be51f-286">Kontaktní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-286">Contact number (required)</span></span>
- <span data-ttu-id="be51f-287">Linka</span><span class="sxs-lookup"><span data-stu-id="be51f-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="be51f-288">Informace o mzdě a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-288">Payroll information and earning codes</span></span>

<span data-ttu-id="be51f-289">Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby.</span><span class="sxs-lookup"><span data-stu-id="be51f-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="be51f-290">Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.</span><span class="sxs-lookup"><span data-stu-id="be51f-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="be51f-291">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-291">Earning codes</span></span>

- <span data-ttu-id="be51f-292">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-292">Position (required)</span></span>
- <span data-ttu-id="be51f-293">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-293">Earning Code (required)</span></span>
- <span data-ttu-id="be51f-294">Frekvence (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-294">Frequency (required)</span></span>
- <span data-ttu-id="be51f-295">Částka (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="be51f-296">Mzdové informace</span><span class="sxs-lookup"><span data-stu-id="be51f-296">Payroll information</span></span>

- <span data-ttu-id="be51f-297">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="be51f-297">Payment Method</span></span>
- <span data-ttu-id="be51f-298">Ekonomická oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-298">Economic Region (required)</span></span>
- <span data-ttu-id="be51f-299">ID zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="be51f-299">Employee Benefits ID</span></span>
- <span data-ttu-id="be51f-300">Národní číslo ID (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-300">National ID Number (required)</span></span>
- <span data-ttu-id="be51f-301">Číslo vojenské služby</span><span class="sxs-lookup"><span data-stu-id="be51f-301">Military Service Number</span></span>
- <span data-ttu-id="be51f-302">ID směny (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-302">Shift ID (required)</span></span>
- <span data-ttu-id="be51f-303">Daňové číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-303">Tax Number (required)</span></span>
- <span data-ttu-id="be51f-304">ID odborů (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-304">Union ID (required)</span></span>
- <span data-ttu-id="be51f-305">ID pracovního dne (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-305">Work Day ID (required)</span></span>
- <span data-ttu-id="be51f-306">Číslo pracovního povolení</span><span class="sxs-lookup"><span data-stu-id="be51f-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="be51f-307">Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**.</span><span class="sxs-lookup"><span data-stu-id="be51f-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="be51f-308">Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.</span><span class="sxs-lookup"><span data-stu-id="be51f-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="be51f-309">Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-309">Employment details</span></span>

<span data-ttu-id="be51f-310">Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="be51f-311">Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="be51f-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="be51f-312">Počáteční datum zaměstnání (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-312">Employment start date (required)</span></span>
- <span data-ttu-id="be51f-313">Koncové datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-313">Employment end date</span></span>
- <span data-ttu-id="be51f-314">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="be51f-314">Start date</span></span>
- <span data-ttu-id="be51f-315">Upravené počáteční datum</span><span class="sxs-lookup"><span data-stu-id="be51f-315">Adjusted start date</span></span>
- <span data-ttu-id="be51f-316">Datum ukončení zaměstnání (povinné při ukončení)</span><span class="sxs-lookup"><span data-stu-id="be51f-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="be51f-317">Důvod ukončení zaměstnání (povinný při ukončení)</span><span class="sxs-lookup"><span data-stu-id="be51f-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="be51f-318">Klíčová data zaměstnance se odvozují pomocí následujících informací.</span><span class="sxs-lookup"><span data-stu-id="be51f-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="be51f-319">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-319">Talent</span></span>                | <span data-ttu-id="be51f-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be51f-321">Datum posledního náboru</span><span class="sxs-lookup"><span data-stu-id="be51f-321">Most recent hire date</span></span> | <span data-ttu-id="be51f-322">Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="be51f-323">Datum výpovědi</span><span class="sxs-lookup"><span data-stu-id="be51f-323">Termination date</span></span>      | <span data-ttu-id="be51f-324">Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="be51f-325">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="be51f-325">Start date</span></span>            | <span data-ttu-id="be51f-326">Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="be51f-327">Datum původního přijetí</span><span class="sxs-lookup"><span data-stu-id="be51f-327">Original hire date</span></span>    | <span data-ttu-id="be51f-328">Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="be51f-329">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-329">Compensation</span></span>

<span data-ttu-id="be51f-330">Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="be51f-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="be51f-331">Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.</span><span class="sxs-lookup"><span data-stu-id="be51f-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="be51f-332">Datum platnosti (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-332">Effective Date (required)</span></span>
- <span data-ttu-id="be51f-333">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="be51f-333">Expiration date</span></span>
- <span data-ttu-id="be51f-334">Mzdová sazba (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-334">Pay Rate (required)</span></span>
- <span data-ttu-id="be51f-335">Převody mzdové sazby (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="be51f-336">Roční ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="be51f-337">Hodinový ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="be51f-338">Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="be51f-339">U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="be51f-340">Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="be51f-341">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="be51f-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="be51f-342">Identifikátor sociálního pojištění</span><span class="sxs-lookup"><span data-stu-id="be51f-342">Social Security identifier</span></span> 

<span data-ttu-id="be51f-343">Každý zaměstnanec musí mít jeden primární identifikátor.</span><span class="sxs-lookup"><span data-stu-id="be51f-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="be51f-344">Tento identifikátor musí být typ identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="be51f-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="be51f-345">V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.</span><span class="sxs-lookup"><span data-stu-id="be51f-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="be51f-346">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-346">Primary (required)</span></span>
- <span data-ttu-id="be51f-347">Typ identifikace = SSN</span><span class="sxs-lookup"><span data-stu-id="be51f-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="be51f-348">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="be51f-348">Issued Date</span></span>
- <span data-ttu-id="be51f-349">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="be51f-349">Expiration Date</span></span>

<span data-ttu-id="be51f-350">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="be51f-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="be51f-351">Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.</span><span class="sxs-lookup"><span data-stu-id="be51f-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="be51f-352">Bankovní účty a úhrady</span><span class="sxs-lookup"><span data-stu-id="be51f-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="be51f-353">Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="be51f-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="be51f-354">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-354">Talent</span></span>                         | <span data-ttu-id="be51f-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be51f-356">Číslo bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="be51f-357">Kód SWIFT (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-357">SWIFT code (required)</span></span>          | <span data-ttu-id="be51f-358">Pole **ID banky** použité při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="be51f-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="be51f-359">Číslo pobočky (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="be51f-360">Typ bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-360">Bank account type (required)</span></span>   | <span data-ttu-id="be51f-361">Pole **Typ účtu** použitý při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="be51f-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="be51f-362">Podporované hodnoty jsou **Běžný** a **Mzdový**.</span><span class="sxs-lookup"><span data-stu-id="be51f-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="be51f-363">Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky.</span><span class="sxs-lookup"><span data-stu-id="be51f-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="be51f-364">Jiné než zůstatkové účty budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="be51f-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="be51f-365">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="be51f-365">Address information</span></span>

<span data-ttu-id="be51f-366">Každý zaměstnanec musí mít jedno primární místo.</span><span class="sxs-lookup"><span data-stu-id="be51f-366">Every employee must have one primary location.</span></span> <span data-ttu-id="be51f-367">V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="be51f-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="be51f-368">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-368">Primary (required)</span></span>
- <span data-ttu-id="be51f-369">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-369">Country/region (required)</span></span>
- <span data-ttu-id="be51f-370">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="be51f-371">Ulice (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-371">Street (required)</span></span>
- <span data-ttu-id="be51f-372">Číslo ulice (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-372">Street Number (required)</span></span>
- <span data-ttu-id="be51f-373">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="be51f-373">Building Complement</span></span>
- <span data-ttu-id="be51f-374">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-374">City (required)</span></span>
- <span data-ttu-id="be51f-375">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-375">State (required)</span></span>
- <span data-ttu-id="be51f-376">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="be51f-377">Konfigurace dat pro generování mzdy v USA a Kanadě</span><span class="sxs-lookup"><span data-stu-id="be51f-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="be51f-378">Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="be51f-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="be51f-379">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="be51f-379">Departments are required on positions.</span></span>
- <span data-ttu-id="be51f-380">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="be51f-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="be51f-381">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="be51f-381">Job types</span></span>

<span data-ttu-id="be51f-382">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="be51f-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="be51f-383">Typy prací jsou povinné pro zpracování mezd v USA a Kanadě.</span><span class="sxs-lookup"><span data-stu-id="be51f-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="be51f-384">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="be51f-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="be51f-385">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="be51f-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="be51f-386">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="be51f-387">Typ práce</span><span class="sxs-lookup"><span data-stu-id="be51f-387">Job type</span></span>   | <span data-ttu-id="be51f-388">Popis</span><span class="sxs-lookup"><span data-stu-id="be51f-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="be51f-389">Hodinově</span><span class="sxs-lookup"><span data-stu-id="be51f-389">Hourly</span></span>     | <span data-ttu-id="be51f-390">Hodinově</span><span class="sxs-lookup"><span data-stu-id="be51f-390">Hourly</span></span>      |
| <span data-ttu-id="be51f-391">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="be51f-391">Salaried</span></span>   | <span data-ttu-id="be51f-392">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="be51f-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="be51f-393">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="be51f-393">Position types</span></span> 

<span data-ttu-id="be51f-394">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="be51f-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="be51f-395">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="be51f-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="be51f-396">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="be51f-397">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="be51f-397">Position type</span></span>   | <span data-ttu-id="be51f-398">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="be51f-399">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-399">Full-time</span></span>       | <span data-ttu-id="be51f-400">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-400">Full time employee</span></span> |
| <span data-ttu-id="be51f-401">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-401">Part-time</span></span>       | <span data-ttu-id="be51f-402">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="be51f-403">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="be51f-403">Reason codes</span></span>

<span data-ttu-id="be51f-404">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="be51f-405">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="be51f-406">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="be51f-407">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="be51f-407">Reason code</span></span>    | <span data-ttu-id="be51f-408">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-408">Description</span></span>      | <span data-ttu-id="be51f-409">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="be51f-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="be51f-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="be51f-410">RESIGNATION</span></span>    | <span data-ttu-id="be51f-411">Výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-411">Resignation</span></span>      | <span data-ttu-id="be51f-412">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-412">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="be51f-413">TERMINATION</span></span>    | <span data-ttu-id="be51f-414">Ukončení</span><span class="sxs-lookup"><span data-stu-id="be51f-414">Termination</span></span>      | <span data-ttu-id="be51f-415">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-415">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="be51f-416">RETIREMENT</span></span>     | <span data-ttu-id="be51f-417">Důchod</span><span class="sxs-lookup"><span data-stu-id="be51f-417">Retirement</span></span>       | <span data-ttu-id="be51f-418">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-418">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-419">JINÝ</span><span class="sxs-lookup"><span data-stu-id="be51f-419">OTHER</span></span>          | <span data-ttu-id="be51f-420">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="be51f-420">Other Reasons</span></span>    | <span data-ttu-id="be51f-421">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-421">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="be51f-422">DEATH</span></span>          | <span data-ttu-id="be51f-423">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="be51f-423">Death</span></span>            | <span data-ttu-id="be51f-424">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-424">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="be51f-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="be51f-426">Dovolená</span><span class="sxs-lookup"><span data-stu-id="be51f-426">Leave of Absence</span></span> | <span data-ttu-id="be51f-427">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-427">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="be51f-428">CONTRACTEND</span></span>    | <span data-ttu-id="be51f-429">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="be51f-429">End of Contract</span></span>  | <span data-ttu-id="be51f-430">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-430">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="be51f-431">SALARYCHANGE</span></span>   | <span data-ttu-id="be51f-432">Změna platu</span><span class="sxs-lookup"><span data-stu-id="be51f-432">Change of Salary</span></span> | <span data-ttu-id="be51f-433">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="be51f-434">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="be51f-434">Marital status</span></span>

<span data-ttu-id="be51f-435">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be51f-436">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="be51f-437">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-437">Talent</span></span>                 | <span data-ttu-id="be51f-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="be51f-439">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="be51f-439">Married</span></span>                | <span data-ttu-id="be51f-440">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="be51f-440">Married</span></span>              |
| <span data-ttu-id="be51f-441">Jedno</span><span class="sxs-lookup"><span data-stu-id="be51f-441">Single</span></span>                 | <span data-ttu-id="be51f-442">Jedno</span><span class="sxs-lookup"><span data-stu-id="be51f-442">Single</span></span>               |
| <span data-ttu-id="be51f-443">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="be51f-443">Widowed</span></span>                | <span data-ttu-id="be51f-444">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="be51f-444">Widowed</span></span>              |
| <span data-ttu-id="be51f-445">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="be51f-445">Divorced</span></span>               | <span data-ttu-id="be51f-446">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="be51f-446">Divorced</span></span>             |
| <span data-ttu-id="be51f-447">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="be51f-447">Registered Partnership</span></span> | <span data-ttu-id="be51f-448">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="be51f-448">Domestic Partnership</span></span> |
| <span data-ttu-id="be51f-449">None</span><span class="sxs-lookup"><span data-stu-id="be51f-449">None</span></span>                   | <span data-ttu-id="be51f-450">None</span><span class="sxs-lookup"><span data-stu-id="be51f-450">None</span></span>                 |
| <span data-ttu-id="be51f-451">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="be51f-451">Cohabiting</span></span>             | <span data-ttu-id="be51f-452">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="be51f-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="be51f-453">Rod</span><span class="sxs-lookup"><span data-stu-id="be51f-453">Gender</span></span>

<span data-ttu-id="be51f-454">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be51f-455">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="be51f-456">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-456">Talent</span></span>       | <span data-ttu-id="be51f-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="be51f-458">Muž</span><span class="sxs-lookup"><span data-stu-id="be51f-458">Male</span></span>         | <span data-ttu-id="be51f-459">Muž</span><span class="sxs-lookup"><span data-stu-id="be51f-459">Male</span></span>            |
| <span data-ttu-id="be51f-460">Žena</span><span class="sxs-lookup"><span data-stu-id="be51f-460">Female</span></span>       | <span data-ttu-id="be51f-461">Žena</span><span class="sxs-lookup"><span data-stu-id="be51f-461">Female</span></span>          |
| <span data-ttu-id="be51f-462">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="be51f-462">Non-specific</span></span> | <span data-ttu-id="be51f-463">*Nepodporováno*</span><span class="sxs-lookup"><span data-stu-id="be51f-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="be51f-464">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-464">Earning codes</span></span>

<span data-ttu-id="be51f-465">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="be51f-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be51f-466">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="be51f-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="be51f-467">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="be51f-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="be51f-468">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="be51f-468">Supported frequencies</span></span>

- <span data-ttu-id="be51f-469">Všechna</span><span class="sxs-lookup"><span data-stu-id="be51f-469">All</span></span>
- <span data-ttu-id="be51f-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="be51f-470">EVERYPAY</span></span>
- <span data-ttu-id="be51f-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="be51f-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="be51f-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="be51f-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="be51f-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="be51f-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="be51f-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-474">1OFMTH</span></span>
- <span data-ttu-id="be51f-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-475">LASTOFMTH</span></span>
- <span data-ttu-id="be51f-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-476">2OFMTH</span></span>
- <span data-ttu-id="be51f-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-477">3OFMTH</span></span>
- <span data-ttu-id="be51f-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-478">4OFMTH</span></span>
- <span data-ttu-id="be51f-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-479">5OFMTH</span></span>
- <span data-ttu-id="be51f-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-480">1N2OFMTH</span></span>
- <span data-ttu-id="be51f-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-481">3N4OFMTH</span></span>
- <span data-ttu-id="be51f-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-482">1N3OFMTH</span></span>
- <span data-ttu-id="be51f-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-483">1N4OFMTH</span></span>
- <span data-ttu-id="be51f-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-484">2N3OFMTH</span></span>
- <span data-ttu-id="be51f-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-485">2N4OFMTH</span></span>
- <span data-ttu-id="be51f-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="be51f-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="be51f-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="be51f-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="be51f-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="be51f-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="be51f-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="be51f-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="be51f-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="be51f-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="be51f-498">Adresy</span><span class="sxs-lookup"><span data-stu-id="be51f-498">Addresses</span></span>

<span data-ttu-id="be51f-499">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="be51f-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="be51f-500">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="be51f-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="be51f-501">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-501">Talent</span></span>          | <span data-ttu-id="be51f-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="be51f-503">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="be51f-503">Country/Region</span></span>  | <span data-ttu-id="be51f-504">Kód země</span><span class="sxs-lookup"><span data-stu-id="be51f-504">Country Code</span></span>          |
| <span data-ttu-id="be51f-505">PSČ</span><span class="sxs-lookup"><span data-stu-id="be51f-505">Zip/Postal Code</span></span> | <span data-ttu-id="be51f-506">PSČ</span><span class="sxs-lookup"><span data-stu-id="be51f-506">Postal Code</span></span>           |
| <span data-ttu-id="be51f-507">Kraj</span><span class="sxs-lookup"><span data-stu-id="be51f-507">State</span></span>           | <span data-ttu-id="be51f-508">Kód státu</span><span class="sxs-lookup"><span data-stu-id="be51f-508">State Code</span></span>            |
| <span data-ttu-id="be51f-509">Město</span><span class="sxs-lookup"><span data-stu-id="be51f-509">City</span></span>            | <span data-ttu-id="be51f-510">Město</span><span class="sxs-lookup"><span data-stu-id="be51f-510">City</span></span>                  |
| <span data-ttu-id="be51f-511">Okres</span><span class="sxs-lookup"><span data-stu-id="be51f-511">County</span></span>          | <span data-ttu-id="be51f-512">Okres</span><span class="sxs-lookup"><span data-stu-id="be51f-512">County (Municipality)</span></span> |
| <span data-ttu-id="be51f-513">Ulice</span><span class="sxs-lookup"><span data-stu-id="be51f-513">Street</span></span>          | <span data-ttu-id="be51f-514">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="be51f-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="be51f-515">Daňové oblasti</span><span class="sxs-lookup"><span data-stu-id="be51f-515">Tax regions</span></span>

<span data-ttu-id="be51f-516">Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy.</span><span class="sxs-lookup"><span data-stu-id="be51f-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="be51f-517">Daňové oblasti jsou mapovány na Dayforce jako adresy místa.</span><span class="sxs-lookup"><span data-stu-id="be51f-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="be51f-518">Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka.</span><span class="sxs-lookup"><span data-stu-id="be51f-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="be51f-519">Daňová oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="be51f-519">Tax region (required)</span></span>
- <span data-ttu-id="be51f-520">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-520">Country/Region (required)</span></span>
- <span data-ttu-id="be51f-521">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="be51f-521">State (required)</span></span>
- <span data-ttu-id="be51f-522">Okres</span><span class="sxs-lookup"><span data-stu-id="be51f-522">County</span></span> 
- <span data-ttu-id="be51f-523">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="be51f-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="be51f-524">Konfigurace dat pro generování mezd v Mexiku</span><span class="sxs-lookup"><span data-stu-id="be51f-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="be51f-525">Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="be51f-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="be51f-526">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="be51f-526">Departments are required on positions.</span></span>
- <span data-ttu-id="be51f-527">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="be51f-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="be51f-528">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="be51f-528">Job types</span></span>

<span data-ttu-id="be51f-529">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="be51f-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="be51f-530">Typy práce jsou povinné pro zpracování mezd v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="be51f-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="be51f-531">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="be51f-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="be51f-532">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="be51f-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="be51f-533">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="be51f-534">Typ práce</span><span class="sxs-lookup"><span data-stu-id="be51f-534">Job type</span></span>   | <span data-ttu-id="be51f-535">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="be51f-536">Hodinově</span><span class="sxs-lookup"><span data-stu-id="be51f-536">Hourly</span></span>     | <span data-ttu-id="be51f-537">MX hodinově</span><span class="sxs-lookup"><span data-stu-id="be51f-537">MX Hourly</span></span>   |
| <span data-ttu-id="be51f-538">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="be51f-538">Salaried</span></span>   | <span data-ttu-id="be51f-539">MX Stálý plat</span><span class="sxs-lookup"><span data-stu-id="be51f-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="be51f-540">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="be51f-540">Position types</span></span> 

<span data-ttu-id="be51f-541">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="be51f-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="be51f-542">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="be51f-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="be51f-543">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="be51f-544">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="be51f-544">Position type</span></span>   | <span data-ttu-id="be51f-545">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="be51f-546">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-546">Full-time</span></span>       | <span data-ttu-id="be51f-547">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-547">Full time employee</span></span> |
| <span data-ttu-id="be51f-548">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-548">Part-time</span></span>       | <span data-ttu-id="be51f-549">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="be51f-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="be51f-550">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="be51f-550">Reason codes</span></span>

<span data-ttu-id="be51f-551">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="be51f-552">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="be51f-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="be51f-553">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="be51f-554">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="be51f-554">Reason code</span></span>            | <span data-ttu-id="be51f-555">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-555">Description</span></span>                    | <span data-ttu-id="be51f-556">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="be51f-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="be51f-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="be51f-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="be51f-558">Odchod před první mzdou</span><span class="sxs-lookup"><span data-stu-id="be51f-558">Departure before first payroll</span></span> | <span data-ttu-id="be51f-559">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-559">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="be51f-560">RESIGNATION</span></span>            | <span data-ttu-id="be51f-561">Výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-561">Resignation</span></span>                    | <span data-ttu-id="be51f-562">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-562">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="be51f-563">PENSION</span></span>                | <span data-ttu-id="be51f-564">Důchod</span><span class="sxs-lookup"><span data-stu-id="be51f-564">Pension</span></span>                        | <span data-ttu-id="be51f-565">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-565">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="be51f-566">TERMINATION</span></span>            | <span data-ttu-id="be51f-567">Ukončení</span><span class="sxs-lookup"><span data-stu-id="be51f-567">Termination</span></span>                    | <span data-ttu-id="be51f-568">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-568">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="be51f-569">RETIREMENT</span></span>             | <span data-ttu-id="be51f-570">Důchod</span><span class="sxs-lookup"><span data-stu-id="be51f-570">Retirement</span></span>                     | <span data-ttu-id="be51f-571">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-571">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="be51f-572">ABSENTEE</span></span>               | <span data-ttu-id="be51f-573">Nepřítomný</span><span class="sxs-lookup"><span data-stu-id="be51f-573">Absentee</span></span>                       | <span data-ttu-id="be51f-574">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-574">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-575">JINÝ</span><span class="sxs-lookup"><span data-stu-id="be51f-575">OTHER</span></span>                  | <span data-ttu-id="be51f-576">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="be51f-576">Other Reasons</span></span>                  | <span data-ttu-id="be51f-577">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-577">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="be51f-578">CLOSURE</span></span>                | <span data-ttu-id="be51f-579">Obchodní uzávěrka</span><span class="sxs-lookup"><span data-stu-id="be51f-579">Business Closure</span></span>               | <span data-ttu-id="be51f-580">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-580">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="be51f-581">DEATH</span></span>                  | <span data-ttu-id="be51f-582">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="be51f-582">Death</span></span>                          | <span data-ttu-id="be51f-583">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-583">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="be51f-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="be51f-585">Dovolená</span><span class="sxs-lookup"><span data-stu-id="be51f-585">Leave of Absence</span></span>               | <span data-ttu-id="be51f-586">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-586">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="be51f-587">CONTRACTEND</span></span>            | <span data-ttu-id="be51f-588">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="be51f-588">End of Contract</span></span>                | <span data-ttu-id="be51f-589">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="be51f-589">Terminate worker</span></span>     |
| <span data-ttu-id="be51f-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="be51f-590">SALARYCHANGE</span></span>           | <span data-ttu-id="be51f-591">Změna platu</span><span class="sxs-lookup"><span data-stu-id="be51f-591">Change of Salary</span></span>               | <span data-ttu-id="be51f-592">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="be51f-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="be51f-593">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-593">Terms of employment</span></span>

<span data-ttu-id="be51f-594">Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="be51f-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="be51f-595">Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="be51f-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="be51f-596">Následující podmínky zaměstnání a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="be51f-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="be51f-597">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="be51f-597">Terms of employment</span></span>   | <span data-ttu-id="be51f-598">popis</span><span class="sxs-lookup"><span data-stu-id="be51f-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="be51f-599">Řádné</span><span class="sxs-lookup"><span data-stu-id="be51f-599">Regular</span></span>               | <span data-ttu-id="be51f-600">Řádné</span><span class="sxs-lookup"><span data-stu-id="be51f-600">Regular</span></span>     |
| <span data-ttu-id="be51f-601">Přímo</span><span class="sxs-lookup"><span data-stu-id="be51f-601">Direct</span></span>                | <span data-ttu-id="be51f-602">Přímo</span><span class="sxs-lookup"><span data-stu-id="be51f-602">Direct</span></span>      |
| <span data-ttu-id="be51f-603">Stáž</span><span class="sxs-lookup"><span data-stu-id="be51f-603">Internship</span></span>            | <span data-ttu-id="be51f-604">Stáž</span><span class="sxs-lookup"><span data-stu-id="be51f-604">Internship</span></span>  |
| <span data-ttu-id="be51f-605">Trvalé</span><span class="sxs-lookup"><span data-stu-id="be51f-605">Permanent</span></span>             | <span data-ttu-id="be51f-606">Trvalé</span><span class="sxs-lookup"><span data-stu-id="be51f-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="be51f-607">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="be51f-607">Marital status</span></span>

<span data-ttu-id="be51f-608">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be51f-609">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="be51f-610">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-610">Talent</span></span>                 | <span data-ttu-id="be51f-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="be51f-612">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="be51f-612">Married</span></span>                | <span data-ttu-id="be51f-613">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="be51f-613">Married</span></span>                   |
| <span data-ttu-id="be51f-614">Jedno</span><span class="sxs-lookup"><span data-stu-id="be51f-614">Single</span></span>                 | <span data-ttu-id="be51f-615">Jedno</span><span class="sxs-lookup"><span data-stu-id="be51f-615">Single</span></span>                    |
| <span data-ttu-id="be51f-616">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="be51f-616">Widowed</span></span>                | <span data-ttu-id="be51f-617">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="be51f-617">Widowed</span></span>                   |
| <span data-ttu-id="be51f-618">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="be51f-618">Divorced</span></span>               | <span data-ttu-id="be51f-619">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="be51f-619">Divorced</span></span>                  |
| <span data-ttu-id="be51f-620">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="be51f-620">Registered Partnership</span></span> | <span data-ttu-id="be51f-621">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="be51f-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="be51f-622">None</span><span class="sxs-lookup"><span data-stu-id="be51f-622">None</span></span>                   | <span data-ttu-id="be51f-623">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be51f-624">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="be51f-624">Cohabiting</span></span>             | <span data-ttu-id="be51f-625">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="be51f-626">Rod</span><span class="sxs-lookup"><span data-stu-id="be51f-626">Gender</span></span>

<span data-ttu-id="be51f-627">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be51f-628">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="be51f-629">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-629">Talent</span></span>       | <span data-ttu-id="be51f-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="be51f-631">Muž</span><span class="sxs-lookup"><span data-stu-id="be51f-631">Male</span></span>         | <span data-ttu-id="be51f-632">Muž</span><span class="sxs-lookup"><span data-stu-id="be51f-632">Male</span></span>                      |
| <span data-ttu-id="be51f-633">Žena</span><span class="sxs-lookup"><span data-stu-id="be51f-633">Female</span></span>       | <span data-ttu-id="be51f-634">Žena</span><span class="sxs-lookup"><span data-stu-id="be51f-634">Female</span></span>                    |
| <span data-ttu-id="be51f-635">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="be51f-635">Non-specific</span></span> | <span data-ttu-id="be51f-636">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="be51f-637">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="be51f-637">Payment method</span></span>

<span data-ttu-id="be51f-638">Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="be51f-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="be51f-639">Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be51f-640">Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="be51f-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="be51f-641">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-641">Talent</span></span>             | <span data-ttu-id="be51f-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="be51f-643">Hotovost</span><span class="sxs-lookup"><span data-stu-id="be51f-643">Cash</span></span>               | <span data-ttu-id="be51f-644">Hotovost</span><span class="sxs-lookup"><span data-stu-id="be51f-644">Cash</span></span>                      |
| <span data-ttu-id="be51f-645">Elektronická platba</span><span class="sxs-lookup"><span data-stu-id="be51f-645">Electronic Payment</span></span> | <span data-ttu-id="be51f-646">Převod</span><span class="sxs-lookup"><span data-stu-id="be51f-646">Transfer</span></span>                  |
| <span data-ttu-id="be51f-647">Kontrola</span><span class="sxs-lookup"><span data-stu-id="be51f-647">Check</span></span>              | <span data-ttu-id="be51f-648">Šek</span><span class="sxs-lookup"><span data-stu-id="be51f-648">Cheque</span></span>                    |
| <span data-ttu-id="be51f-649">Bankovní směnka</span><span class="sxs-lookup"><span data-stu-id="be51f-649">Bank Draft</span></span>         | <span data-ttu-id="be51f-650">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be51f-651">Další</span><span class="sxs-lookup"><span data-stu-id="be51f-651">Other</span></span>              | <span data-ttu-id="be51f-652">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="be51f-653">Typ bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="be51f-653">Bank account type</span></span>

<span data-ttu-id="be51f-654">Typy bankovního účtu se používají pro elektronické platby zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="be51f-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="be51f-655">Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu.</span><span class="sxs-lookup"><span data-stu-id="be51f-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="be51f-656">Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="be51f-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="be51f-657">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-657">Talent</span></span>            | <span data-ttu-id="be51f-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="be51f-659">Běžný účet</span><span class="sxs-lookup"><span data-stu-id="be51f-659">Checking Account</span></span>  | <span data-ttu-id="be51f-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="be51f-660">CheckingAccount</span></span>           |
| <span data-ttu-id="be51f-661">Mzdový účet</span><span class="sxs-lookup"><span data-stu-id="be51f-661">Payroll Account</span></span>   | <span data-ttu-id="be51f-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="be51f-662">PayrollAccount</span></span>            |
| <span data-ttu-id="be51f-663">Spořicí účet</span><span class="sxs-lookup"><span data-stu-id="be51f-663">Savings Account</span></span>   | <span data-ttu-id="be51f-664">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be51f-665">BankGirot účet</span><span class="sxs-lookup"><span data-stu-id="be51f-665">BankGirot account</span></span> | <span data-ttu-id="be51f-666">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be51f-667">PlusGirot účet</span><span class="sxs-lookup"><span data-stu-id="be51f-667">PlusGirot account</span></span> | <span data-ttu-id="be51f-668">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="be51f-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="be51f-669">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="be51f-669">Earning codes</span></span>

<span data-ttu-id="be51f-670">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="be51f-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be51f-671">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="be51f-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="be51f-672">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="be51f-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="be51f-673">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="be51f-673">Supported frequencies</span></span>

- <span data-ttu-id="be51f-674">Všechna</span><span class="sxs-lookup"><span data-stu-id="be51f-674">All</span></span>
- <span data-ttu-id="be51f-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="be51f-675">EVERYPAY</span></span>
- <span data-ttu-id="be51f-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="be51f-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="be51f-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="be51f-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="be51f-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="be51f-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="be51f-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-679">1OFMTH</span></span>
- <span data-ttu-id="be51f-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-680">LASTOFMTH</span></span>
- <span data-ttu-id="be51f-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-681">2OFMTH</span></span>
- <span data-ttu-id="be51f-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-682">3OFMTH</span></span>
- <span data-ttu-id="be51f-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-683">4OFMTH</span></span>
- <span data-ttu-id="be51f-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-684">5OFMTH</span></span>
- <span data-ttu-id="be51f-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-685">1N2OFMTH</span></span>
- <span data-ttu-id="be51f-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-686">3N4OFMTH</span></span>
- <span data-ttu-id="be51f-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-687">1N3OFMTH</span></span>
- <span data-ttu-id="be51f-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-688">1N4OFMTH</span></span>
- <span data-ttu-id="be51f-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-689">2N3OFMTH</span></span>
- <span data-ttu-id="be51f-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-690">2N4OFMTH</span></span>
- <span data-ttu-id="be51f-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="be51f-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="be51f-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="be51f-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="be51f-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="be51f-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="be51f-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="be51f-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="be51f-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="be51f-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="be51f-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="be51f-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="be51f-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="be51f-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="be51f-703">Adresy</span><span class="sxs-lookup"><span data-stu-id="be51f-703">Addresses</span></span>

<span data-ttu-id="be51f-704">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="be51f-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="be51f-705">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="be51f-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="be51f-706">Talent</span><span class="sxs-lookup"><span data-stu-id="be51f-706">Talent</span></span>              | <span data-ttu-id="be51f-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be51f-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="be51f-708">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="be51f-708">Country/Region</span></span>      | <span data-ttu-id="be51f-709">Kód země</span><span class="sxs-lookup"><span data-stu-id="be51f-709">Country Code</span></span>          |
| <span data-ttu-id="be51f-710">PSČ</span><span class="sxs-lookup"><span data-stu-id="be51f-710">Zip/Postal Code</span></span>     | <span data-ttu-id="be51f-711">PSČ</span><span class="sxs-lookup"><span data-stu-id="be51f-711">Postal Code</span></span>           |
| <span data-ttu-id="be51f-712">Kraj</span><span class="sxs-lookup"><span data-stu-id="be51f-712">State</span></span>               | <span data-ttu-id="be51f-713">Kód státu</span><span class="sxs-lookup"><span data-stu-id="be51f-713">State Code</span></span>            |
| <span data-ttu-id="be51f-714">Město</span><span class="sxs-lookup"><span data-stu-id="be51f-714">City</span></span>                | <span data-ttu-id="be51f-715">Město</span><span class="sxs-lookup"><span data-stu-id="be51f-715">City</span></span>                  |
| <span data-ttu-id="be51f-716">Okres</span><span class="sxs-lookup"><span data-stu-id="be51f-716">County</span></span>              | <span data-ttu-id="be51f-717">Okres</span><span class="sxs-lookup"><span data-stu-id="be51f-717">County (Municipality)</span></span> |
| <span data-ttu-id="be51f-718">Ulice</span><span class="sxs-lookup"><span data-stu-id="be51f-718">Street</span></span>              | <span data-ttu-id="be51f-719">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="be51f-719">Address Line 1</span></span>        |
| <span data-ttu-id="be51f-720">Číslo popisné</span><span class="sxs-lookup"><span data-stu-id="be51f-720">Street Number</span></span>       | <span data-ttu-id="be51f-721">Řádek adresy 2</span><span class="sxs-lookup"><span data-stu-id="be51f-721">Address Line 2</span></span>        |
| <span data-ttu-id="be51f-722">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="be51f-722">Building Complement</span></span> | <span data-ttu-id="be51f-723">Řádek adresy 5</span><span class="sxs-lookup"><span data-stu-id="be51f-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="be51f-724">Číslo cestovního pasu</span><span class="sxs-lookup"><span data-stu-id="be51f-724">Passport number</span></span>

<span data-ttu-id="be51f-725">Zaměstnanci mohou deklarovat informace o cestovním pasu.</span><span class="sxs-lookup"><span data-stu-id="be51f-725">Employees can declare passport information.</span></span> <span data-ttu-id="be51f-726">Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="be51f-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="be51f-727">Typ identifikace = Pas</span><span class="sxs-lookup"><span data-stu-id="be51f-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="be51f-728">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="be51f-728">Issued Date</span></span>
- <span data-ttu-id="be51f-729">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="be51f-729">Expiration Date</span></span>

<span data-ttu-id="be51f-730">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**.</span><span class="sxs-lookup"><span data-stu-id="be51f-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="be51f-731">Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu.</span><span class="sxs-lookup"><span data-stu-id="be51f-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="be51f-732">Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.</span><span class="sxs-lookup"><span data-stu-id="be51f-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

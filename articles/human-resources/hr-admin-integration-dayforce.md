---
title: Konfigurace integrace s aplikací Dayforce
description: Integrace mezi aplikacemi Microsoft Dynamics 365 Human Resources a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto článku. Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Human Resources i Dayforce.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d5f65672960716bee3f58c98ccce249fdbf8697
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467138"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="66e17-104">Konfigurace integrace s aplikací Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="66e17-105">Integrace mezi aplikacemi Microsoft Dynamics 365 Human Resources a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="66e17-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="66e17-106">Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Human Resources i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="66e17-107">Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66e17-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="66e17-108">Integrace vyžaduje specifická data z aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66e17-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="66e17-109">Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Human Resources nakonfigurována tak, aby podporovala integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="66e17-110">Integrace používá následující rozsáhlé kategorie dat:</span><span class="sxs-lookup"><span data-stu-id="66e17-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="66e17-111">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="66e17-111">Human resources data</span></span>
- <span data-ttu-id="66e17-112">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="66e17-112">Compensation data</span></span>
- <span data-ttu-id="66e17-113">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="66e17-114">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="66e17-114">Worker data</span></span>

<span data-ttu-id="66e17-115">Tento článek popisuje postup, který je třeba provést při povolení integrace.</span><span class="sxs-lookup"><span data-stu-id="66e17-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="66e17-116">Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.</span><span class="sxs-lookup"><span data-stu-id="66e17-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="66e17-117">Povolení integrace</span><span class="sxs-lookup"><span data-stu-id="66e17-117">Enable the integration</span></span>

<span data-ttu-id="66e17-118">V aplikaci Human Resources musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="66e17-119">Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 Finance, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="66e17-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="66e17-120">Pro zapnutí integrace v aplikaci Human Resources postupuje podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="66e17-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="66e17-121">Na stránce **Správa systému** zvolte **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="66e17-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="66e17-122">Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.</span><span class="sxs-lookup"><span data-stu-id="66e17-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="66e17-123">Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.</span><span class="sxs-lookup"><span data-stu-id="66e17-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="66e17-124">Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="66e17-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="66e17-125">Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence.</span><span class="sxs-lookup"><span data-stu-id="66e17-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="66e17-126">Tuto frekvenci lze změnit v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="66e17-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="66e17-127">Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících článcích o Azure:</span><span class="sxs-lookup"><span data-stu-id="66e17-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="66e17-128">O účtech úložiště Azure Storage</span><span class="sxs-lookup"><span data-stu-id="66e17-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="66e17-129">Konfigurace řetězců připojení Azure Storage</span><span class="sxs-lookup"><span data-stu-id="66e17-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="66e17-130">Technické podrobnosti při povolení integrace mezd</span><span class="sxs-lookup"><span data-stu-id="66e17-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="66e17-131">Zapnutí integrace mezd má dva primární efekty:</span><span class="sxs-lookup"><span data-stu-id="66e17-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="66e17-132">Je vytvořen projekt exportu dat s názvem "Export integrací mezd".</span><span class="sxs-lookup"><span data-stu-id="66e17-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="66e17-133">Tento projekt obsahuje entity a pole vyžadované pro integraci mezd.</span><span class="sxs-lookup"><span data-stu-id="66e17-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="66e17-134">Chcete-li zkontrolovat projekt, přejděte na položky **Správa systému**, vyberte dlaždici **Správa dat** a poté otevřete datový projekt ze seznamu projektů.</span><span class="sxs-lookup"><span data-stu-id="66e17-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="66e17-135">Tato dávková úloha spustí projekt exportu dat, zašifruje výsledný balík dat a přenese soubor datového balíku do koncového bodu SFTP nakonfigurovaného na obrazovce **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="66e17-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="66e17-136">Datový balík převedený na koncový bod SFTP je šifrován pomocí klíče, který je pro daný balík jedinečný.</span><span class="sxs-lookup"><span data-stu-id="66e17-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="66e17-137">Klíč je v úložišti klíčů Azure, který je přístupný pouze společnosti Ceridian.</span><span class="sxs-lookup"><span data-stu-id="66e17-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="66e17-138">Není možné dešifrovat a prověřit obsah balíčku dat.</span><span class="sxs-lookup"><span data-stu-id="66e17-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="66e17-139">Potřebujete-li zkontrolovat obsah balíčku dat, je třeba exportovat datový projekt integrace mezd ručně, stáhnout jej a poté jej otevřít.</span><span class="sxs-lookup"><span data-stu-id="66e17-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="66e17-140">Ruční export nebude používat šifrování nebo nepřenese balíček.</span><span class="sxs-lookup"><span data-stu-id="66e17-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="66e17-141">Konfigurace vašich dat</span><span class="sxs-lookup"><span data-stu-id="66e17-141">Configure your data</span></span> 

<span data-ttu-id="66e17-142">Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66e17-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="66e17-143">Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="66e17-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="66e17-144">Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="66e17-145">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="66e17-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="66e17-146">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="66e17-146">Benefits</span></span> 

<span data-ttu-id="66e17-147">Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="66e17-148">Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="66e17-149">Plány zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="66e17-149">Benefit plans</span></span>

- <span data-ttu-id="66e17-150">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-150">Plan (required)</span></span>
- <span data-ttu-id="66e17-151">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-151">Type (required)</span></span>
- <span data-ttu-id="66e17-152">Dopad mzdy (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-152">Payroll impact (required)</span></span>
- <span data-ttu-id="66e17-153">Obnovit nedoplatky</span><span class="sxs-lookup"><span data-stu-id="66e17-153">Recover arrears</span></span>
- <span data-ttu-id="66e17-154">Způsobu provádění odpočtu</span><span class="sxs-lookup"><span data-stu-id="66e17-154">Deduction method</span></span>
- <span data-ttu-id="66e17-155">Priorita odpočtu</span><span class="sxs-lookup"><span data-stu-id="66e17-155">Deduction priority</span></span>
- <span data-ttu-id="66e17-156">Období limitu</span><span class="sxs-lookup"><span data-stu-id="66e17-156">Limit period</span></span>
- <span data-ttu-id="66e17-157">Částka limitu</span><span class="sxs-lookup"><span data-stu-id="66e17-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="66e17-158">Zam. výhody</span><span class="sxs-lookup"><span data-stu-id="66e17-158">Benefits</span></span>

- <span data-ttu-id="66e17-159">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-159">Plan (required)</span></span>
- <span data-ttu-id="66e17-160">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-160">Type (required)</span></span>
- <span data-ttu-id="66e17-161">Možnost (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-161">Option (required)</span></span>
- <span data-ttu-id="66e17-162">ID zaměstnanecké výhody (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-162">Benefit ID (required)</span></span>
- <span data-ttu-id="66e17-163">Četnost</span><span class="sxs-lookup"><span data-stu-id="66e17-163">Frequency</span></span>
- <span data-ttu-id="66e17-164">Základ</span><span class="sxs-lookup"><span data-stu-id="66e17-164">Basis</span></span>
- <span data-ttu-id="66e17-165">Částka nebo sazba</span><span class="sxs-lookup"><span data-stu-id="66e17-165">Amount or rate</span></span>
- <span data-ttu-id="66e17-166">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="66e17-167">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="66e17-167">Supported frequencies</span></span> 

- <span data-ttu-id="66e17-168">Týdně</span><span class="sxs-lookup"><span data-stu-id="66e17-168">Weekly</span></span>
- <span data-ttu-id="66e17-169">Čtrnáctidenně</span><span class="sxs-lookup"><span data-stu-id="66e17-169">Bi-weekly</span></span>
- <span data-ttu-id="66e17-170">Každých 14 dní</span><span class="sxs-lookup"><span data-stu-id="66e17-170">Semi-monthly</span></span>
- <span data-ttu-id="66e17-171">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="66e17-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="66e17-172">Podporované základy</span><span class="sxs-lookup"><span data-stu-id="66e17-172">Supported bases</span></span> 

- <span data-ttu-id="66e17-173">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="66e17-173">Fixed amount</span></span>
- <span data-ttu-id="66e17-174">Procento příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-174">Percent of earnings</span></span>
- <span data-ttu-id="66e17-175">Produktivní hodiny</span><span class="sxs-lookup"><span data-stu-id="66e17-175">Productive hours</span></span>

<span data-ttu-id="66e17-176">Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="66e17-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="66e17-177">Výběr v Human Resources</span><span class="sxs-lookup"><span data-stu-id="66e17-177">Selection in Human Resources</span></span>        | <span data-ttu-id="66e17-178">Výsledek v aplikaci Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="66e17-179">Žádní</span><span class="sxs-lookup"><span data-stu-id="66e17-179">None</span></span>                       | <span data-ttu-id="66e17-180">Nebyla vytvořena žádná srážka.</span><span class="sxs-lookup"><span data-stu-id="66e17-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="66e17-181">Jen odpočet</span><span class="sxs-lookup"><span data-stu-id="66e17-181">Deduction only</span></span>             | <span data-ttu-id="66e17-182">Byla vytvořena srážka zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="66e17-183">Jen příspěvek</span><span class="sxs-lookup"><span data-stu-id="66e17-183">Contribution only</span></span>          | <span data-ttu-id="66e17-184">Byla vytvořena srážka zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="66e17-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="66e17-185">Odpočet a příspěvek</span><span class="sxs-lookup"><span data-stu-id="66e17-185">Deduction and contribution</span></span> | <span data-ttu-id="66e17-186">Jsou vytvořeny srážky zaměstnance a zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="66e17-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="66e17-187">Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="66e17-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="66e17-188">Definování programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="66e17-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="66e17-189">Vytvořit novou zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="66e17-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="66e17-190">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="66e17-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="66e17-191">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="66e17-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="66e17-192">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-192">Compensation</span></span> 

<span data-ttu-id="66e17-193">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="66e17-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="66e17-194">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="66e17-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="66e17-195">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="66e17-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="66e17-196">Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="66e17-197">Plány fixní kompenzace a převody mzdové sazby jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="66e17-198">Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="66e17-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="66e17-199">Další informace o plánech kompenzace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="66e17-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="66e17-200">Vytvoření plánů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="66e17-201">Vytvoření plánů variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="66e17-202">Vývoj struktury platu/kompenzace a plánů</span><span class="sxs-lookup"><span data-stu-id="66e17-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="66e17-203">Proces kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="66e17-204">Definování procesu kompenzací a výpočet výsledků</span><span class="sxs-lookup"><span data-stu-id="66e17-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="66e17-205">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="66e17-206">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="66e17-207">Práce</span><span class="sxs-lookup"><span data-stu-id="66e17-207">Jobs</span></span> 

<span data-ttu-id="66e17-208">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="66e17-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="66e17-209">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="66e17-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="66e17-210">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="66e17-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="66e17-211">Definování nových prací</span><span class="sxs-lookup"><span data-stu-id="66e17-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="66e17-212">Pozice</span><span class="sxs-lookup"><span data-stu-id="66e17-212">Positions</span></span>

<span data-ttu-id="66e17-213">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="66e17-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="66e17-214">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="66e17-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="66e17-215">Pozice existuje v oddělení.</span><span class="sxs-lookup"><span data-stu-id="66e17-215">A position exists in a department.</span></span> <span data-ttu-id="66e17-216">Ke každé pozic lze přiřadit pouze jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="66e17-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="66e17-217">Mějte na paměti následující data a konfiguraci při vytváření pozic:</span><span class="sxs-lookup"><span data-stu-id="66e17-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="66e17-218">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-218">Position (required)</span></span>
- <span data-ttu-id="66e17-219">Popis (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-219">Description (required)</span></span>
- <span data-ttu-id="66e17-220">Práce (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-220">Job (required)</span></span>
- <span data-ttu-id="66e17-221">Oddělení (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-221">Department (required)</span></span>
- <span data-ttu-id="66e17-222">Typ pozice (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-222">Position type (required)</span></span>
- <span data-ttu-id="66e17-223">Ekvivalent plného úvazku</span><span class="sxs-lookup"><span data-stu-id="66e17-223">Full-time equivalent</span></span>
- <span data-ttu-id="66e17-224">Roční normální hodiny (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="66e17-225">Placené právnickou osobu (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="66e17-226">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-226">Pay cycle (required)</span></span>
- <span data-ttu-id="66e17-227">Výchozí finanční dimenze – Nákladové středisko (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="66e17-228">Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu</span><span class="sxs-lookup"><span data-stu-id="66e17-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="66e17-229">Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="66e17-230">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="66e17-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="66e17-231">Uspořádání zaměstnanců podle oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="66e17-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="66e17-232">Nastavení pozic</span><span class="sxs-lookup"><span data-stu-id="66e17-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="66e17-233">Oddělení</span><span class="sxs-lookup"><span data-stu-id="66e17-233">Departments</span></span>

<span data-ttu-id="66e17-234">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="66e17-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="66e17-235">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="66e17-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="66e17-236">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="66e17-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="66e17-237">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="66e17-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="66e17-238">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="66e17-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="66e17-239">Vytvoření oddělení a jeho přidružení k hierarchii oddělení</span><span class="sxs-lookup"><span data-stu-id="66e17-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="66e17-240">Definování nových oddělení</span><span class="sxs-lookup"><span data-stu-id="66e17-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="66e17-241">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="66e17-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="66e17-242">Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků.</span><span class="sxs-lookup"><span data-stu-id="66e17-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="66e17-243">Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="66e17-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="66e17-244">Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období.</span><span class="sxs-lookup"><span data-stu-id="66e17-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="66e17-245">Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.</span><span class="sxs-lookup"><span data-stu-id="66e17-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="66e17-246">Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus.</span><span class="sxs-lookup"><span data-stu-id="66e17-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="66e17-247">Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="66e17-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="66e17-248">Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.</span><span class="sxs-lookup"><span data-stu-id="66e17-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="66e17-249">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="66e17-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="66e17-250">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-250">Pay cycle (required)</span></span>
- <span data-ttu-id="66e17-251">Četnost platebního cyklu (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="66e17-252">Počáteční datum období (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="66e17-253">Výchozí datum platby (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="66e17-254">Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus.</span><span class="sxs-lookup"><span data-stu-id="66e17-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="66e17-255">Před integrací musí být vytvořeno nejméně jedno platební období.</span><span class="sxs-lookup"><span data-stu-id="66e17-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="66e17-256">Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66e17-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="66e17-257">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-257">Earning codes</span></span>

<span data-ttu-id="66e17-258">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="66e17-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66e17-259">Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="66e17-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="66e17-260">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="66e17-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="66e17-261">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-261">Earning Code (required)</span></span>
- <span data-ttu-id="66e17-262">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-262">Description</span></span>
- <span data-ttu-id="66e17-263">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="66e17-263">Unit of measure</span></span>
- <span data-ttu-id="66e17-264">Produktivní</span><span class="sxs-lookup"><span data-stu-id="66e17-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="66e17-265">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="66e17-265">Worker data</span></span>

<span data-ttu-id="66e17-266">Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy.</span><span class="sxs-lookup"><span data-stu-id="66e17-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="66e17-267">Zadané informace lze použít ke sledování pracovníků a osobních informací.</span><span class="sxs-lookup"><span data-stu-id="66e17-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="66e17-268">Pro zaměstnance lze spravovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="66e17-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="66e17-269">**Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.</span><span class="sxs-lookup"><span data-stu-id="66e17-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="66e17-270">**Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.</span><span class="sxs-lookup"><span data-stu-id="66e17-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="66e17-271">**Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.</span><span class="sxs-lookup"><span data-stu-id="66e17-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="66e17-272">**Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.</span><span class="sxs-lookup"><span data-stu-id="66e17-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="66e17-273">Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="66e17-274">Obecné informace</span><span class="sxs-lookup"><span data-stu-id="66e17-274">General information</span></span>

- <span data-ttu-id="66e17-275">Osobní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-275">Personnel number (required)</span></span>
- <span data-ttu-id="66e17-276">Jméno (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-276">First name (required)</span></span>
- <span data-ttu-id="66e17-277">Příjmení (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-277">Last name (required)</span></span>
- <span data-ttu-id="66e17-278">Druhé jméno</span><span class="sxs-lookup"><span data-stu-id="66e17-278">Middle name</span></span>
- <span data-ttu-id="66e17-279">Datum služebního věku</span><span class="sxs-lookup"><span data-stu-id="66e17-279">Seniority date</span></span>
- <span data-ttu-id="66e17-280">Známé jako</span><span class="sxs-lookup"><span data-stu-id="66e17-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="66e17-281">Osobní údaje</span><span class="sxs-lookup"><span data-stu-id="66e17-281">Personal information</span></span>

- <span data-ttu-id="66e17-282">Rodinný stav (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-282">Marital status (required)</span></span>
- <span data-ttu-id="66e17-283">Datum narození (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-283">Birth date (required)</span></span>
- <span data-ttu-id="66e17-284">Pohlaví (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-284">Gender (required)</span></span>
- <span data-ttu-id="66e17-285">Osoba s tělesným postižením</span><span class="sxs-lookup"><span data-stu-id="66e17-285">Person with disabilities</span></span>
- <span data-ttu-id="66e17-286">Země nebo oblast národnosti (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="66e17-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="66e17-287">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="66e17-287">Address information</span></span>

- <span data-ttu-id="66e17-288">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-288">Primary (required)</span></span>
- <span data-ttu-id="66e17-289">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-289">Country/region (required)</span></span>
- <span data-ttu-id="66e17-290">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-290">Postal code (required)</span></span>
- <span data-ttu-id="66e17-291">Číslo ulice (povinné) (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="66e17-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="66e17-292">Doplňující název budovy (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="66e17-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="66e17-293">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-293">City (required)</span></span>
- <span data-ttu-id="66e17-294">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-294">State (required)</span></span>
- <span data-ttu-id="66e17-295">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="66e17-296">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="66e17-296">Contact information</span></span> 

- <span data-ttu-id="66e17-297">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-297">Primary (required)</span></span>
- <span data-ttu-id="66e17-298">Kontaktní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-298">Contact number (required)</span></span>
- <span data-ttu-id="66e17-299">Linka</span><span class="sxs-lookup"><span data-stu-id="66e17-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="66e17-300">Informace o mzdě a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-300">Payroll information and earning codes</span></span>

<span data-ttu-id="66e17-301">Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby.</span><span class="sxs-lookup"><span data-stu-id="66e17-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="66e17-302">Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.</span><span class="sxs-lookup"><span data-stu-id="66e17-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="66e17-303">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-303">Earning codes</span></span>

- <span data-ttu-id="66e17-304">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-304">Position (required)</span></span>
- <span data-ttu-id="66e17-305">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-305">Earning Code (required)</span></span>
- <span data-ttu-id="66e17-306">Frekvence (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-306">Frequency (required)</span></span>
- <span data-ttu-id="66e17-307">Částka (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="66e17-308">Mzdové informace</span><span class="sxs-lookup"><span data-stu-id="66e17-308">Payroll information</span></span>

- <span data-ttu-id="66e17-309">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="66e17-309">Payment Method</span></span>
- <span data-ttu-id="66e17-310">Ekonomická oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-310">Economic Region (required)</span></span>
- <span data-ttu-id="66e17-311">ID zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="66e17-311">Employee Benefits ID</span></span>
- <span data-ttu-id="66e17-312">Národní číslo ID (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-312">National ID Number (required)</span></span>
- <span data-ttu-id="66e17-313">Číslo vojenské služby</span><span class="sxs-lookup"><span data-stu-id="66e17-313">Military Service Number</span></span>
- <span data-ttu-id="66e17-314">ID směny (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-314">Shift ID (required)</span></span>
- <span data-ttu-id="66e17-315">Daňové číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-315">Tax Number (required)</span></span>
- <span data-ttu-id="66e17-316">ID odborů (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-316">Union ID (required)</span></span>
- <span data-ttu-id="66e17-317">ID pracovního dne (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-317">Work Day ID (required)</span></span>
- <span data-ttu-id="66e17-318">Číslo pracovního povolení</span><span class="sxs-lookup"><span data-stu-id="66e17-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="66e17-319">Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**.</span><span class="sxs-lookup"><span data-stu-id="66e17-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="66e17-320">Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.</span><span class="sxs-lookup"><span data-stu-id="66e17-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="66e17-321">Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-321">Employment details</span></span>

<span data-ttu-id="66e17-322">Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="66e17-323">Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="66e17-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="66e17-324">Počáteční datum zaměstnání (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-324">Employment start date (required)</span></span>
- <span data-ttu-id="66e17-325">Koncové datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-325">Employment end date</span></span>
- <span data-ttu-id="66e17-326">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="66e17-326">Start date</span></span>
- <span data-ttu-id="66e17-327">Upravené počáteční datum</span><span class="sxs-lookup"><span data-stu-id="66e17-327">Adjusted start date</span></span>
- <span data-ttu-id="66e17-328">Datum ukončení zaměstnání (povinné při ukončení)</span><span class="sxs-lookup"><span data-stu-id="66e17-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="66e17-329">Důvod ukončení zaměstnání (povinný při ukončení)</span><span class="sxs-lookup"><span data-stu-id="66e17-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="66e17-330">Klíčová data zaměstnance se odvozují pomocí následujících informací.</span><span class="sxs-lookup"><span data-stu-id="66e17-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="66e17-331">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-331">Human Resources</span></span>                | <span data-ttu-id="66e17-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e17-333">Datum posledního náboru</span><span class="sxs-lookup"><span data-stu-id="66e17-333">Most recent hire date</span></span> | <span data-ttu-id="66e17-334">Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="66e17-335">Datum výpovědi</span><span class="sxs-lookup"><span data-stu-id="66e17-335">Termination date</span></span>      | <span data-ttu-id="66e17-336">Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="66e17-337">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="66e17-337">Start date</span></span>            | <span data-ttu-id="66e17-338">Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="66e17-339">Datum původního přijetí</span><span class="sxs-lookup"><span data-stu-id="66e17-339">Original hire date</span></span>    | <span data-ttu-id="66e17-340">Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="66e17-341">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-341">Compensation</span></span>

<span data-ttu-id="66e17-342">Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="66e17-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="66e17-343">Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.</span><span class="sxs-lookup"><span data-stu-id="66e17-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="66e17-344">Datum platnosti (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-344">Effective Date (required)</span></span>
- <span data-ttu-id="66e17-345">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="66e17-345">Expiration date</span></span>
- <span data-ttu-id="66e17-346">Mzdová sazba (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-346">Pay Rate (required)</span></span>
- <span data-ttu-id="66e17-347">Převody mzdové sazby (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="66e17-348">Roční ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="66e17-349">Hodinový ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="66e17-350">Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="66e17-351">U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="66e17-352">Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="66e17-353">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="66e17-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="66e17-354">Identifikátor sociálního pojištění</span><span class="sxs-lookup"><span data-stu-id="66e17-354">Social Security identifier</span></span> 

<span data-ttu-id="66e17-355">Každý zaměstnanec musí mít jeden primární identifikátor.</span><span class="sxs-lookup"><span data-stu-id="66e17-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="66e17-356">Tento identifikátor musí být typ identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="66e17-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="66e17-357">V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.</span><span class="sxs-lookup"><span data-stu-id="66e17-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="66e17-358">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-358">Primary (required)</span></span>
- <span data-ttu-id="66e17-359">Typ identifikace = SSN</span><span class="sxs-lookup"><span data-stu-id="66e17-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="66e17-360">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="66e17-360">Issued Date</span></span>
- <span data-ttu-id="66e17-361">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="66e17-361">Expiration Date</span></span>

<span data-ttu-id="66e17-362">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="66e17-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="66e17-363">Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.</span><span class="sxs-lookup"><span data-stu-id="66e17-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="66e17-364">Bankovní účty a úhrady</span><span class="sxs-lookup"><span data-stu-id="66e17-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="66e17-365">Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="66e17-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="66e17-366">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-366">Human Resources</span></span>                         | <span data-ttu-id="66e17-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e17-368">Číslo bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="66e17-369">Kód SWIFT (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-369">SWIFT code (required)</span></span>          | <span data-ttu-id="66e17-370">Pole **ID banky** použité při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="66e17-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="66e17-371">Číslo pobočky (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="66e17-372">Typ bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-372">Bank account type (required)</span></span>   | <span data-ttu-id="66e17-373">Pole **Typ účtu** použitý při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="66e17-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="66e17-374">Podporované hodnoty jsou **Běžný** a **Mzdový**.</span><span class="sxs-lookup"><span data-stu-id="66e17-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="66e17-375">Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky.</span><span class="sxs-lookup"><span data-stu-id="66e17-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="66e17-376">Jiné než zůstatkové účty budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="66e17-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="66e17-377">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="66e17-377">Address information</span></span>

<span data-ttu-id="66e17-378">Každý zaměstnanec musí mít jedno primární místo.</span><span class="sxs-lookup"><span data-stu-id="66e17-378">Every employee must have one primary location.</span></span> <span data-ttu-id="66e17-379">V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="66e17-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="66e17-380">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-380">Primary (required)</span></span>
- <span data-ttu-id="66e17-381">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-381">Country/region (required)</span></span>
- <span data-ttu-id="66e17-382">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="66e17-383">Ulice (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-383">Street (required)</span></span>
- <span data-ttu-id="66e17-384">Číslo ulice (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-384">Street Number (required)</span></span>
- <span data-ttu-id="66e17-385">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="66e17-385">Building Complement</span></span>
- <span data-ttu-id="66e17-386">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-386">City (required)</span></span>
- <span data-ttu-id="66e17-387">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-387">State (required)</span></span>
- <span data-ttu-id="66e17-388">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="66e17-389">Konfigurace dat pro generování mzdy v USA a Kanadě</span><span class="sxs-lookup"><span data-stu-id="66e17-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="66e17-390">Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="66e17-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="66e17-391">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="66e17-391">Departments are required on positions.</span></span>
- <span data-ttu-id="66e17-392">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="66e17-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="66e17-393">Aplikaci Human Resources lze konfigurovat tak, aby od pozic požadovala určení oddělení.</span><span class="sxs-lookup"><span data-stu-id="66e17-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="66e17-394">Chcete-li to provést, přejděte na **Sdílené pozice lidských zdrojů > Pozice > Vyžadovat oddělení na pozicích**.</span><span class="sxs-lookup"><span data-stu-id="66e17-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="66e17-395">Doporučujeme, aby toto nastavení bylo vynuceno pro integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="66e17-396">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="66e17-396">Job types</span></span>

<span data-ttu-id="66e17-397">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="66e17-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="66e17-398">Typy prací jsou povinné pro zpracování mezd v USA a Kanadě.</span><span class="sxs-lookup"><span data-stu-id="66e17-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="66e17-399">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="66e17-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="66e17-400">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="66e17-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="66e17-401">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="66e17-402">Typ práce</span><span class="sxs-lookup"><span data-stu-id="66e17-402">Job type</span></span>   | <span data-ttu-id="66e17-403">Popis</span><span class="sxs-lookup"><span data-stu-id="66e17-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="66e17-404">Hodinově</span><span class="sxs-lookup"><span data-stu-id="66e17-404">Hourly</span></span>     | <span data-ttu-id="66e17-405">Hodinově</span><span class="sxs-lookup"><span data-stu-id="66e17-405">Hourly</span></span>      |
| <span data-ttu-id="66e17-406">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="66e17-406">Salaried</span></span>   | <span data-ttu-id="66e17-407">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="66e17-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="66e17-408">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="66e17-408">Position types</span></span> 

<span data-ttu-id="66e17-409">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="66e17-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="66e17-410">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="66e17-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="66e17-411">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="66e17-412">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="66e17-412">Position type</span></span>   | <span data-ttu-id="66e17-413">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="66e17-414">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-414">Full-time</span></span>       | <span data-ttu-id="66e17-415">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-415">Full time employee</span></span> |
| <span data-ttu-id="66e17-416">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-416">Part-time</span></span>       | <span data-ttu-id="66e17-417">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="66e17-418">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="66e17-418">Reason codes</span></span>

<span data-ttu-id="66e17-419">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="66e17-420">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="66e17-421">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="66e17-422">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="66e17-422">Reason code</span></span>    | <span data-ttu-id="66e17-423">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-423">Description</span></span>      | <span data-ttu-id="66e17-424">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="66e17-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="66e17-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="66e17-425">RESIGNATION</span></span>    | <span data-ttu-id="66e17-426">Výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-426">Resignation</span></span>      | <span data-ttu-id="66e17-427">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-427">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="66e17-428">TERMINATION</span></span>    | <span data-ttu-id="66e17-429">Ukončení</span><span class="sxs-lookup"><span data-stu-id="66e17-429">Termination</span></span>      | <span data-ttu-id="66e17-430">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-430">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="66e17-431">RETIREMENT</span></span>     | <span data-ttu-id="66e17-432">Důchod</span><span class="sxs-lookup"><span data-stu-id="66e17-432">Retirement</span></span>       | <span data-ttu-id="66e17-433">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-433">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-434">JINÝ</span><span class="sxs-lookup"><span data-stu-id="66e17-434">OTHER</span></span>          | <span data-ttu-id="66e17-435">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="66e17-435">Other Reasons</span></span>    | <span data-ttu-id="66e17-436">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-436">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="66e17-437">DEATH</span></span>          | <span data-ttu-id="66e17-438">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="66e17-438">Death</span></span>            | <span data-ttu-id="66e17-439">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-439">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="66e17-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="66e17-441">Dovolená</span><span class="sxs-lookup"><span data-stu-id="66e17-441">Leave of Absence</span></span> | <span data-ttu-id="66e17-442">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-442">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="66e17-443">CONTRACTEND</span></span>    | <span data-ttu-id="66e17-444">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="66e17-444">End of Contract</span></span>  | <span data-ttu-id="66e17-445">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-445">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="66e17-446">SALARYCHANGE</span></span>   | <span data-ttu-id="66e17-447">Změna platu</span><span class="sxs-lookup"><span data-stu-id="66e17-447">Change of Salary</span></span> | <span data-ttu-id="66e17-448">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="66e17-449">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="66e17-449">Marital status</span></span>

<span data-ttu-id="66e17-450">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66e17-451">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="66e17-452">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-452">Human Resources</span></span>                 | <span data-ttu-id="66e17-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="66e17-454">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="66e17-454">Married</span></span>                | <span data-ttu-id="66e17-455">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="66e17-455">Married</span></span>              |
| <span data-ttu-id="66e17-456">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="66e17-456">Single</span></span>                 | <span data-ttu-id="66e17-457">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="66e17-457">Single</span></span>               |
| <span data-ttu-id="66e17-458">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="66e17-458">Widowed</span></span>                | <span data-ttu-id="66e17-459">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="66e17-459">Widowed</span></span>              |
| <span data-ttu-id="66e17-460">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="66e17-460">Divorced</span></span>               | <span data-ttu-id="66e17-461">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="66e17-461">Divorced</span></span>             |
| <span data-ttu-id="66e17-462">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="66e17-462">Registered Partnership</span></span> | <span data-ttu-id="66e17-463">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="66e17-463">Domestic Partnership</span></span> |
| <span data-ttu-id="66e17-464">None</span><span class="sxs-lookup"><span data-stu-id="66e17-464">None</span></span>                   | <span data-ttu-id="66e17-465">None</span><span class="sxs-lookup"><span data-stu-id="66e17-465">None</span></span>                 |
| <span data-ttu-id="66e17-466">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="66e17-466">Cohabiting</span></span>             | <span data-ttu-id="66e17-467">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="66e17-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="66e17-468">Rod</span><span class="sxs-lookup"><span data-stu-id="66e17-468">Gender</span></span>

<span data-ttu-id="66e17-469">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66e17-470">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="66e17-471">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-471">Human Resources</span></span>       | <span data-ttu-id="66e17-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="66e17-473">Muž</span><span class="sxs-lookup"><span data-stu-id="66e17-473">Male</span></span>         | <span data-ttu-id="66e17-474">Muž</span><span class="sxs-lookup"><span data-stu-id="66e17-474">Male</span></span>            |
| <span data-ttu-id="66e17-475">Žena</span><span class="sxs-lookup"><span data-stu-id="66e17-475">Female</span></span>       | <span data-ttu-id="66e17-476">Žena</span><span class="sxs-lookup"><span data-stu-id="66e17-476">Female</span></span>          |
| <span data-ttu-id="66e17-477">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="66e17-477">Non-specific</span></span> | <span data-ttu-id="66e17-478">*Nepodporováno*</span><span class="sxs-lookup"><span data-stu-id="66e17-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="66e17-479">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-479">Earning codes</span></span>

<span data-ttu-id="66e17-480">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="66e17-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66e17-481">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="66e17-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="66e17-482">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="66e17-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="66e17-483">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="66e17-483">Supported frequencies</span></span>

- <span data-ttu-id="66e17-484">Všechna</span><span class="sxs-lookup"><span data-stu-id="66e17-484">All</span></span>
- <span data-ttu-id="66e17-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="66e17-485">EVERYPAY</span></span>
- <span data-ttu-id="66e17-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="66e17-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="66e17-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="66e17-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="66e17-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="66e17-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="66e17-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-489">1OFMTH</span></span>
- <span data-ttu-id="66e17-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-490">LASTOFMTH</span></span>
- <span data-ttu-id="66e17-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-491">2OFMTH</span></span>
- <span data-ttu-id="66e17-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-492">3OFMTH</span></span>
- <span data-ttu-id="66e17-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-493">4OFMTH</span></span>
- <span data-ttu-id="66e17-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-494">5OFMTH</span></span>
- <span data-ttu-id="66e17-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-495">1N2OFMTH</span></span>
- <span data-ttu-id="66e17-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-496">3N4OFMTH</span></span>
- <span data-ttu-id="66e17-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-497">1N3OFMTH</span></span>
- <span data-ttu-id="66e17-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-498">1N4OFMTH</span></span>
- <span data-ttu-id="66e17-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-499">2N3OFMTH</span></span>
- <span data-ttu-id="66e17-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-500">2N4OFMTH</span></span>
- <span data-ttu-id="66e17-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="66e17-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="66e17-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="66e17-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="66e17-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="66e17-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="66e17-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="66e17-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="66e17-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="66e17-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="66e17-513">Adresy</span><span class="sxs-lookup"><span data-stu-id="66e17-513">Addresses</span></span>

<span data-ttu-id="66e17-514">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="66e17-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="66e17-515">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="66e17-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="66e17-516">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-516">Human Resources</span></span>          | <span data-ttu-id="66e17-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="66e17-518">Země/region</span><span class="sxs-lookup"><span data-stu-id="66e17-518">Country/Region</span></span>  | <span data-ttu-id="66e17-519">Kód země</span><span class="sxs-lookup"><span data-stu-id="66e17-519">Country Code</span></span>          |
| <span data-ttu-id="66e17-520">PSČ</span><span class="sxs-lookup"><span data-stu-id="66e17-520">Zip/Postal Code</span></span> | <span data-ttu-id="66e17-521">PSČ</span><span class="sxs-lookup"><span data-stu-id="66e17-521">Postal Code</span></span>           |
| <span data-ttu-id="66e17-522">Kraj</span><span class="sxs-lookup"><span data-stu-id="66e17-522">State</span></span>           | <span data-ttu-id="66e17-523">Kód státu</span><span class="sxs-lookup"><span data-stu-id="66e17-523">State Code</span></span>            |
| <span data-ttu-id="66e17-524">Město</span><span class="sxs-lookup"><span data-stu-id="66e17-524">City</span></span>            | <span data-ttu-id="66e17-525">Město</span><span class="sxs-lookup"><span data-stu-id="66e17-525">City</span></span>                  |
| <span data-ttu-id="66e17-526">Okres</span><span class="sxs-lookup"><span data-stu-id="66e17-526">County</span></span>          | <span data-ttu-id="66e17-527">Okres</span><span class="sxs-lookup"><span data-stu-id="66e17-527">County (Municipality)</span></span> |
| <span data-ttu-id="66e17-528">Ulice</span><span class="sxs-lookup"><span data-stu-id="66e17-528">Street</span></span>          | <span data-ttu-id="66e17-529">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="66e17-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="66e17-530">Daňové oblasti</span><span class="sxs-lookup"><span data-stu-id="66e17-530">Tax regions</span></span>

<span data-ttu-id="66e17-531">Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy.</span><span class="sxs-lookup"><span data-stu-id="66e17-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="66e17-532">Daňové oblasti jsou mapovány na Dayforce jako adresy místa.</span><span class="sxs-lookup"><span data-stu-id="66e17-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="66e17-533">Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka.</span><span class="sxs-lookup"><span data-stu-id="66e17-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="66e17-534">Daňová oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="66e17-534">Tax region (required)</span></span>
- <span data-ttu-id="66e17-535">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-535">Country/Region (required)</span></span>
- <span data-ttu-id="66e17-536">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="66e17-536">State (required)</span></span>
- <span data-ttu-id="66e17-537">Okres</span><span class="sxs-lookup"><span data-stu-id="66e17-537">County</span></span> 
- <span data-ttu-id="66e17-538">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="66e17-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="66e17-539">Konfigurace dat pro generování mezd v Mexiku</span><span class="sxs-lookup"><span data-stu-id="66e17-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="66e17-540">Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="66e17-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="66e17-541">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="66e17-541">Departments are required on positions.</span></span>
- <span data-ttu-id="66e17-542">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="66e17-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="66e17-543">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="66e17-543">Job types</span></span>

<span data-ttu-id="66e17-544">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="66e17-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="66e17-545">Typy práce jsou povinné pro zpracování mezd v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="66e17-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="66e17-546">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="66e17-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="66e17-547">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="66e17-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="66e17-548">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="66e17-549">Typ práce</span><span class="sxs-lookup"><span data-stu-id="66e17-549">Job type</span></span>   | <span data-ttu-id="66e17-550">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="66e17-551">Hodinově</span><span class="sxs-lookup"><span data-stu-id="66e17-551">Hourly</span></span>     | <span data-ttu-id="66e17-552">MX hodinově</span><span class="sxs-lookup"><span data-stu-id="66e17-552">MX Hourly</span></span>   |
| <span data-ttu-id="66e17-553">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="66e17-553">Salaried</span></span>   | <span data-ttu-id="66e17-554">MX Stálý plat</span><span class="sxs-lookup"><span data-stu-id="66e17-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="66e17-555">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="66e17-555">Position types</span></span> 

<span data-ttu-id="66e17-556">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="66e17-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="66e17-557">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="66e17-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="66e17-558">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="66e17-559">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="66e17-559">Position type</span></span>   | <span data-ttu-id="66e17-560">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="66e17-561">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-561">Full-time</span></span>       | <span data-ttu-id="66e17-562">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-562">Full time employee</span></span> |
| <span data-ttu-id="66e17-563">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-563">Part-time</span></span>       | <span data-ttu-id="66e17-564">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="66e17-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="66e17-565">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="66e17-565">Reason codes</span></span>

<span data-ttu-id="66e17-566">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="66e17-567">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="66e17-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="66e17-568">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="66e17-569">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="66e17-569">Reason code</span></span>            | <span data-ttu-id="66e17-570">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-570">Description</span></span>                    | <span data-ttu-id="66e17-571">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="66e17-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="66e17-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="66e17-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="66e17-573">Odchod před první mzdou</span><span class="sxs-lookup"><span data-stu-id="66e17-573">Departure before first payroll</span></span> | <span data-ttu-id="66e17-574">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-574">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="66e17-575">RESIGNATION</span></span>            | <span data-ttu-id="66e17-576">Výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-576">Resignation</span></span>                    | <span data-ttu-id="66e17-577">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-577">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="66e17-578">PENSION</span></span>                | <span data-ttu-id="66e17-579">Důchod</span><span class="sxs-lookup"><span data-stu-id="66e17-579">Pension</span></span>                        | <span data-ttu-id="66e17-580">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-580">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="66e17-581">TERMINATION</span></span>            | <span data-ttu-id="66e17-582">Ukončení</span><span class="sxs-lookup"><span data-stu-id="66e17-582">Termination</span></span>                    | <span data-ttu-id="66e17-583">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-583">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="66e17-584">RETIREMENT</span></span>             | <span data-ttu-id="66e17-585">Důchod</span><span class="sxs-lookup"><span data-stu-id="66e17-585">Retirement</span></span>                     | <span data-ttu-id="66e17-586">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-586">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="66e17-587">ABSENTEE</span></span>               | <span data-ttu-id="66e17-588">Nepřítomný</span><span class="sxs-lookup"><span data-stu-id="66e17-588">Absentee</span></span>                       | <span data-ttu-id="66e17-589">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-589">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-590">JINÝ</span><span class="sxs-lookup"><span data-stu-id="66e17-590">OTHER</span></span>                  | <span data-ttu-id="66e17-591">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="66e17-591">Other Reasons</span></span>                  | <span data-ttu-id="66e17-592">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-592">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="66e17-593">CLOSURE</span></span>                | <span data-ttu-id="66e17-594">Obchodní uzávěrka</span><span class="sxs-lookup"><span data-stu-id="66e17-594">Business Closure</span></span>               | <span data-ttu-id="66e17-595">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-595">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="66e17-596">DEATH</span></span>                  | <span data-ttu-id="66e17-597">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="66e17-597">Death</span></span>                          | <span data-ttu-id="66e17-598">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-598">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="66e17-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="66e17-600">Dovolená</span><span class="sxs-lookup"><span data-stu-id="66e17-600">Leave of Absence</span></span>               | <span data-ttu-id="66e17-601">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-601">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="66e17-602">CONTRACTEND</span></span>            | <span data-ttu-id="66e17-603">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="66e17-603">End of Contract</span></span>                | <span data-ttu-id="66e17-604">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="66e17-604">Terminate worker</span></span>     |
| <span data-ttu-id="66e17-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="66e17-605">SALARYCHANGE</span></span>           | <span data-ttu-id="66e17-606">Změna platu</span><span class="sxs-lookup"><span data-stu-id="66e17-606">Change of Salary</span></span>               | <span data-ttu-id="66e17-607">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="66e17-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="66e17-608">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-608">Terms of employment</span></span>

<span data-ttu-id="66e17-609">Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="66e17-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="66e17-610">Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="66e17-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="66e17-611">Následující podmínky zaměstnání a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="66e17-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="66e17-612">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="66e17-612">Terms of employment</span></span>   | <span data-ttu-id="66e17-613">popis</span><span class="sxs-lookup"><span data-stu-id="66e17-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="66e17-614">Řádné</span><span class="sxs-lookup"><span data-stu-id="66e17-614">Regular</span></span>               | <span data-ttu-id="66e17-615">Řádné</span><span class="sxs-lookup"><span data-stu-id="66e17-615">Regular</span></span>     |
| <span data-ttu-id="66e17-616">Přímo</span><span class="sxs-lookup"><span data-stu-id="66e17-616">Direct</span></span>                | <span data-ttu-id="66e17-617">Přímo</span><span class="sxs-lookup"><span data-stu-id="66e17-617">Direct</span></span>      |
| <span data-ttu-id="66e17-618">Stáž</span><span class="sxs-lookup"><span data-stu-id="66e17-618">Internship</span></span>            | <span data-ttu-id="66e17-619">Stáž</span><span class="sxs-lookup"><span data-stu-id="66e17-619">Internship</span></span>  |
| <span data-ttu-id="66e17-620">Trvalé</span><span class="sxs-lookup"><span data-stu-id="66e17-620">Permanent</span></span>             | <span data-ttu-id="66e17-621">Trvalé</span><span class="sxs-lookup"><span data-stu-id="66e17-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="66e17-622">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="66e17-622">Marital status</span></span>

<span data-ttu-id="66e17-623">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66e17-624">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="66e17-625">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-625">Human Resources</span></span>                 | <span data-ttu-id="66e17-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="66e17-627">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="66e17-627">Married</span></span>                | <span data-ttu-id="66e17-628">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="66e17-628">Married</span></span>                   |
| <span data-ttu-id="66e17-629">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="66e17-629">Single</span></span>                 | <span data-ttu-id="66e17-630">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="66e17-630">Single</span></span>                    |
| <span data-ttu-id="66e17-631">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="66e17-631">Widowed</span></span>                | <span data-ttu-id="66e17-632">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="66e17-632">Widowed</span></span>                   |
| <span data-ttu-id="66e17-633">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="66e17-633">Divorced</span></span>               | <span data-ttu-id="66e17-634">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="66e17-634">Divorced</span></span>                  |
| <span data-ttu-id="66e17-635">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="66e17-635">Registered Partnership</span></span> | <span data-ttu-id="66e17-636">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="66e17-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="66e17-637">None</span><span class="sxs-lookup"><span data-stu-id="66e17-637">None</span></span>                   | <span data-ttu-id="66e17-638">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66e17-639">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="66e17-639">Cohabiting</span></span>             | <span data-ttu-id="66e17-640">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="66e17-641">Rod</span><span class="sxs-lookup"><span data-stu-id="66e17-641">Gender</span></span>

<span data-ttu-id="66e17-642">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66e17-643">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="66e17-644">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-644">Human Resources</span></span>       | <span data-ttu-id="66e17-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="66e17-646">Muž</span><span class="sxs-lookup"><span data-stu-id="66e17-646">Male</span></span>         | <span data-ttu-id="66e17-647">Muž</span><span class="sxs-lookup"><span data-stu-id="66e17-647">Male</span></span>                      |
| <span data-ttu-id="66e17-648">Žena</span><span class="sxs-lookup"><span data-stu-id="66e17-648">Female</span></span>       | <span data-ttu-id="66e17-649">Žena</span><span class="sxs-lookup"><span data-stu-id="66e17-649">Female</span></span>                    |
| <span data-ttu-id="66e17-650">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="66e17-650">Non-specific</span></span> | <span data-ttu-id="66e17-651">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="66e17-652">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="66e17-652">Payment method</span></span>

<span data-ttu-id="66e17-653">Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="66e17-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="66e17-654">Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="66e17-655">Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="66e17-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="66e17-656">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-656">Human Resources</span></span>             | <span data-ttu-id="66e17-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="66e17-658">Hotovost</span><span class="sxs-lookup"><span data-stu-id="66e17-658">Cash</span></span>               | <span data-ttu-id="66e17-659">Hotovost</span><span class="sxs-lookup"><span data-stu-id="66e17-659">Cash</span></span>                      |
| <span data-ttu-id="66e17-660">Elektronická platba</span><span class="sxs-lookup"><span data-stu-id="66e17-660">Electronic Payment</span></span> | <span data-ttu-id="66e17-661">Převod</span><span class="sxs-lookup"><span data-stu-id="66e17-661">Transfer</span></span>                  |
| <span data-ttu-id="66e17-662">Kontrola</span><span class="sxs-lookup"><span data-stu-id="66e17-662">Check</span></span>              | <span data-ttu-id="66e17-663">Šek</span><span class="sxs-lookup"><span data-stu-id="66e17-663">Cheque</span></span>                    |
| <span data-ttu-id="66e17-664">Bankovní směnka</span><span class="sxs-lookup"><span data-stu-id="66e17-664">Bank Draft</span></span>         | <span data-ttu-id="66e17-665">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66e17-666">Další</span><span class="sxs-lookup"><span data-stu-id="66e17-666">Other</span></span>              | <span data-ttu-id="66e17-667">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="66e17-668">Typ bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="66e17-668">Bank account type</span></span>

<span data-ttu-id="66e17-669">Typy bankovního účtu se používají pro elektronické platby zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="66e17-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="66e17-670">Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu.</span><span class="sxs-lookup"><span data-stu-id="66e17-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="66e17-671">Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="66e17-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="66e17-672">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-672">Human Resources</span></span>            | <span data-ttu-id="66e17-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="66e17-674">Běžný účet</span><span class="sxs-lookup"><span data-stu-id="66e17-674">Checking Account</span></span>  | <span data-ttu-id="66e17-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="66e17-675">CheckingAccount</span></span>           |
| <span data-ttu-id="66e17-676">Mzdový účet</span><span class="sxs-lookup"><span data-stu-id="66e17-676">Payroll Account</span></span>   | <span data-ttu-id="66e17-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="66e17-677">PayrollAccount</span></span>            |
| <span data-ttu-id="66e17-678">Spořicí účet</span><span class="sxs-lookup"><span data-stu-id="66e17-678">Savings Account</span></span>   | <span data-ttu-id="66e17-679">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66e17-680">BankGirot účet</span><span class="sxs-lookup"><span data-stu-id="66e17-680">BankGirot account</span></span> | <span data-ttu-id="66e17-681">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="66e17-682">PlusGirot účet</span><span class="sxs-lookup"><span data-stu-id="66e17-682">PlusGirot account</span></span> | <span data-ttu-id="66e17-683">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="66e17-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="66e17-684">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="66e17-684">Earning codes</span></span>

<span data-ttu-id="66e17-685">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="66e17-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="66e17-686">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="66e17-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="66e17-687">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="66e17-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="66e17-688">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="66e17-688">Supported frequencies</span></span>

- <span data-ttu-id="66e17-689">Všechna</span><span class="sxs-lookup"><span data-stu-id="66e17-689">All</span></span>
- <span data-ttu-id="66e17-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="66e17-690">EVERYPAY</span></span>
- <span data-ttu-id="66e17-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="66e17-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="66e17-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="66e17-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="66e17-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="66e17-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="66e17-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-694">1OFMTH</span></span>
- <span data-ttu-id="66e17-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-695">LASTOFMTH</span></span>
- <span data-ttu-id="66e17-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-696">2OFMTH</span></span>
- <span data-ttu-id="66e17-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-697">3OFMTH</span></span>
- <span data-ttu-id="66e17-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-698">4OFMTH</span></span>
- <span data-ttu-id="66e17-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-699">5OFMTH</span></span>
- <span data-ttu-id="66e17-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-700">1N2OFMTH</span></span>
- <span data-ttu-id="66e17-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-701">3N4OFMTH</span></span>
- <span data-ttu-id="66e17-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-702">1N3OFMTH</span></span>
- <span data-ttu-id="66e17-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-703">1N4OFMTH</span></span>
- <span data-ttu-id="66e17-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-704">2N3OFMTH</span></span>
- <span data-ttu-id="66e17-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-705">2N4OFMTH</span></span>
- <span data-ttu-id="66e17-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="66e17-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="66e17-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="66e17-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="66e17-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="66e17-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="66e17-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="66e17-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="66e17-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="66e17-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="66e17-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="66e17-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="66e17-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="66e17-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="66e17-718">Adresy</span><span class="sxs-lookup"><span data-stu-id="66e17-718">Addresses</span></span>

<span data-ttu-id="66e17-719">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="66e17-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="66e17-720">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="66e17-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="66e17-721">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="66e17-721">Human Resources</span></span>              | <span data-ttu-id="66e17-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="66e17-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="66e17-723">Země/region</span><span class="sxs-lookup"><span data-stu-id="66e17-723">Country/Region</span></span>      | <span data-ttu-id="66e17-724">Kód země</span><span class="sxs-lookup"><span data-stu-id="66e17-724">Country Code</span></span>          |
| <span data-ttu-id="66e17-725">PSČ</span><span class="sxs-lookup"><span data-stu-id="66e17-725">Zip/Postal Code</span></span>     | <span data-ttu-id="66e17-726">PSČ</span><span class="sxs-lookup"><span data-stu-id="66e17-726">Postal Code</span></span>           |
| <span data-ttu-id="66e17-727">Kraj</span><span class="sxs-lookup"><span data-stu-id="66e17-727">State</span></span>               | <span data-ttu-id="66e17-728">Kód státu</span><span class="sxs-lookup"><span data-stu-id="66e17-728">State Code</span></span>            |
| <span data-ttu-id="66e17-729">Město</span><span class="sxs-lookup"><span data-stu-id="66e17-729">City</span></span>                | <span data-ttu-id="66e17-730">Město</span><span class="sxs-lookup"><span data-stu-id="66e17-730">City</span></span>                  |
| <span data-ttu-id="66e17-731">Okres</span><span class="sxs-lookup"><span data-stu-id="66e17-731">County</span></span>              | <span data-ttu-id="66e17-732">Okres</span><span class="sxs-lookup"><span data-stu-id="66e17-732">County (Municipality)</span></span> |
| <span data-ttu-id="66e17-733">Ulice</span><span class="sxs-lookup"><span data-stu-id="66e17-733">Street</span></span>              | <span data-ttu-id="66e17-734">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="66e17-734">Address Line 1</span></span>        |
| <span data-ttu-id="66e17-735">Číslo popisné</span><span class="sxs-lookup"><span data-stu-id="66e17-735">Street Number</span></span>       | <span data-ttu-id="66e17-736">Řádek adresy 2</span><span class="sxs-lookup"><span data-stu-id="66e17-736">Address Line 2</span></span>        |
| <span data-ttu-id="66e17-737">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="66e17-737">Building Complement</span></span> | <span data-ttu-id="66e17-738">Řádek adresy 5</span><span class="sxs-lookup"><span data-stu-id="66e17-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="66e17-739">Číslo cestovního pasu</span><span class="sxs-lookup"><span data-stu-id="66e17-739">Passport number</span></span>

<span data-ttu-id="66e17-740">Zaměstnanci mohou deklarovat informace o cestovním pasu.</span><span class="sxs-lookup"><span data-stu-id="66e17-740">Employees can declare passport information.</span></span> <span data-ttu-id="66e17-741">Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="66e17-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="66e17-742">Typ identifikace = Pas</span><span class="sxs-lookup"><span data-stu-id="66e17-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="66e17-743">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="66e17-743">Issued Date</span></span>
- <span data-ttu-id="66e17-744">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="66e17-744">Expiration Date</span></span>

<span data-ttu-id="66e17-745">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**.</span><span class="sxs-lookup"><span data-stu-id="66e17-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="66e17-746">Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu.</span><span class="sxs-lookup"><span data-stu-id="66e17-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="66e17-747">Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.</span><span class="sxs-lookup"><span data-stu-id="66e17-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
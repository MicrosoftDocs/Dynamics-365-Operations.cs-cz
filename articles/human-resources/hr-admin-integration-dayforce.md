---
title: Konfigurace integrace s aplikací Dayforce
description: Integrace mezi aplikacemi Microsoft Dynamics 365 Human Resources a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto článku. Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Human Resources i Dayforce.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051490"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="f716a-104">Konfigurace integrace s aplikací Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f716a-105">Integrace mezi aplikacemi Microsoft Dynamics 365 Human Resources a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="f716a-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="f716a-106">Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Human Resources i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f716a-107">Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f716a-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="f716a-108">Integrace vyžaduje specifická data z aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f716a-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="f716a-109">Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Human Resources nakonfigurována tak, aby podporovala integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="f716a-110">Integrace používá následující rozsáhlé kategorie dat:</span><span class="sxs-lookup"><span data-stu-id="f716a-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f716a-111">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="f716a-111">Human resources data</span></span>
- <span data-ttu-id="f716a-112">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="f716a-112">Compensation data</span></span>
- <span data-ttu-id="f716a-113">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f716a-114">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="f716a-114">Worker data</span></span>

<span data-ttu-id="f716a-115">Tento článek popisuje postup, který je třeba provést při povolení integrace.</span><span class="sxs-lookup"><span data-stu-id="f716a-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f716a-116">Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.</span><span class="sxs-lookup"><span data-stu-id="f716a-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f716a-117">Povolení integrace</span><span class="sxs-lookup"><span data-stu-id="f716a-117">Enable the integration</span></span>

<span data-ttu-id="f716a-118">V aplikaci Human Resources musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f716a-119">Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 Finance, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f716a-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="f716a-120">Pro zapnutí integrace v aplikaci Human Resources postupuje podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f716a-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="f716a-121">Na stránce **Správa systému** zvolte **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="f716a-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f716a-122">Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.</span><span class="sxs-lookup"><span data-stu-id="f716a-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f716a-123">Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.</span><span class="sxs-lookup"><span data-stu-id="f716a-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f716a-124">Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f716a-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f716a-125">Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence.</span><span class="sxs-lookup"><span data-stu-id="f716a-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f716a-126">Tuto frekvenci lze změnit v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="f716a-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="f716a-127">Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících článcích o Azure:</span><span class="sxs-lookup"><span data-stu-id="f716a-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="f716a-128">O účtech úložiště Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f716a-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f716a-129">Konfigurace řetězců připojení Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f716a-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="f716a-130">Technické podrobnosti při povolení integrace mezd</span><span class="sxs-lookup"><span data-stu-id="f716a-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="f716a-131">Zapnutí integrace mezd má dva primární efekty:</span><span class="sxs-lookup"><span data-stu-id="f716a-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="f716a-132">Je vytvořen projekt exportu dat s názvem "Export integrací mezd".</span><span class="sxs-lookup"><span data-stu-id="f716a-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="f716a-133">Tento projekt obsahuje entity a pole vyžadované pro integraci mezd.</span><span class="sxs-lookup"><span data-stu-id="f716a-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="f716a-134">Chcete-li zkontrolovat projekt, přejděte na položky **Správa systému**, vyberte dlaždici **Správa dat** a poté otevřete datový projekt ze seznamu projektů.</span><span class="sxs-lookup"><span data-stu-id="f716a-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="f716a-135">Tato dávková úloha spustí projekt exportu dat, zašifruje výsledný balík dat a přenese soubor datového balíku do koncového bodu SFTP nakonfigurovaného na obrazovce **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="f716a-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="f716a-136">Datový balík převedený na koncový bod SFTP je šifrován pomocí klíče, který je pro daný balík jedinečný.</span><span class="sxs-lookup"><span data-stu-id="f716a-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="f716a-137">Klíč je v úložišti klíčů Azure, který je přístupný pouze společnosti Ceridian.</span><span class="sxs-lookup"><span data-stu-id="f716a-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="f716a-138">Není možné dešifrovat a prověřit obsah balíčku dat.</span><span class="sxs-lookup"><span data-stu-id="f716a-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="f716a-139">Potřebujete-li zkontrolovat obsah balíčku dat, je třeba exportovat datový projekt integrace mezd ručně, stáhnout jej a poté jej otevřít.</span><span class="sxs-lookup"><span data-stu-id="f716a-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="f716a-140">Ruční export nebude používat šifrování nebo nepřenese balíček.</span><span class="sxs-lookup"><span data-stu-id="f716a-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="f716a-141">Pro případy, kdy jsou integrační soubory odesílány z prostředí Dynamics 365 Human Resources UAT nebo Sandbox do testovacího prostředí Ceridian Dayforce můžete použít následující adresu URL trezoru klíčů: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="f716a-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="f716a-142">Konfigurace vašich dat</span><span class="sxs-lookup"><span data-stu-id="f716a-142">Configure your data</span></span> 

<span data-ttu-id="f716a-143">Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f716a-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="f716a-144">Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="f716a-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f716a-145">Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f716a-146">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="f716a-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f716a-147">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="f716a-147">Benefits</span></span> 

<span data-ttu-id="f716a-148">Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f716a-149">Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f716a-150">Plány zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f716a-150">Benefit plans</span></span>

- <span data-ttu-id="f716a-151">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-151">Plan (required)</span></span>
- <span data-ttu-id="f716a-152">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-152">Type (required)</span></span>
- <span data-ttu-id="f716a-153">Dopad mzdy (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-153">Payroll impact (required)</span></span>
- <span data-ttu-id="f716a-154">Obnovit nedoplatky</span><span class="sxs-lookup"><span data-stu-id="f716a-154">Recover arrears</span></span>
- <span data-ttu-id="f716a-155">Způsobu provádění odpočtu</span><span class="sxs-lookup"><span data-stu-id="f716a-155">Deduction method</span></span>
- <span data-ttu-id="f716a-156">Priorita odpočtu</span><span class="sxs-lookup"><span data-stu-id="f716a-156">Deduction priority</span></span>
- <span data-ttu-id="f716a-157">Období limitu</span><span class="sxs-lookup"><span data-stu-id="f716a-157">Limit period</span></span>
- <span data-ttu-id="f716a-158">Částka limitu</span><span class="sxs-lookup"><span data-stu-id="f716a-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f716a-159">Zam. výhody</span><span class="sxs-lookup"><span data-stu-id="f716a-159">Benefits</span></span>

- <span data-ttu-id="f716a-160">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-160">Plan (required)</span></span>
- <span data-ttu-id="f716a-161">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-161">Type (required)</span></span>
- <span data-ttu-id="f716a-162">Možnost (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-162">Option (required)</span></span>
- <span data-ttu-id="f716a-163">ID zaměstnanecké výhody (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-163">Benefit ID (required)</span></span>
- <span data-ttu-id="f716a-164">Četnost</span><span class="sxs-lookup"><span data-stu-id="f716a-164">Frequency</span></span>
- <span data-ttu-id="f716a-165">Základ</span><span class="sxs-lookup"><span data-stu-id="f716a-165">Basis</span></span>
- <span data-ttu-id="f716a-166">Částka nebo sazba</span><span class="sxs-lookup"><span data-stu-id="f716a-166">Amount or rate</span></span>
- <span data-ttu-id="f716a-167">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f716a-168">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f716a-168">Supported frequencies</span></span> 

- <span data-ttu-id="f716a-169">Týdně</span><span class="sxs-lookup"><span data-stu-id="f716a-169">Weekly</span></span>
- <span data-ttu-id="f716a-170">Čtrnáctidenně</span><span class="sxs-lookup"><span data-stu-id="f716a-170">Bi-weekly</span></span>
- <span data-ttu-id="f716a-171">Každých 14 dní</span><span class="sxs-lookup"><span data-stu-id="f716a-171">Semi-monthly</span></span>
- <span data-ttu-id="f716a-172">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="f716a-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f716a-173">Podporované základy</span><span class="sxs-lookup"><span data-stu-id="f716a-173">Supported bases</span></span> 

- <span data-ttu-id="f716a-174">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="f716a-174">Fixed amount</span></span>
- <span data-ttu-id="f716a-175">Procento příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-175">Percent of earnings</span></span>
- <span data-ttu-id="f716a-176">Produktivní hodiny</span><span class="sxs-lookup"><span data-stu-id="f716a-176">Productive hours</span></span>

<span data-ttu-id="f716a-177">Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="f716a-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f716a-178">Výběr v Human Resources</span><span class="sxs-lookup"><span data-stu-id="f716a-178">Selection in Human Resources</span></span>        | <span data-ttu-id="f716a-179">Výsledek v aplikaci Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f716a-180">Žádní</span><span class="sxs-lookup"><span data-stu-id="f716a-180">None</span></span>                       | <span data-ttu-id="f716a-181">Nebyla vytvořena žádná srážka.</span><span class="sxs-lookup"><span data-stu-id="f716a-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="f716a-182">Jen odpočet</span><span class="sxs-lookup"><span data-stu-id="f716a-182">Deduction only</span></span>             | <span data-ttu-id="f716a-183">Byla vytvořena srážka zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f716a-184">Jen příspěvek</span><span class="sxs-lookup"><span data-stu-id="f716a-184">Contribution only</span></span>          | <span data-ttu-id="f716a-185">Byla vytvořena srážka zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="f716a-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f716a-186">Odpočet a příspěvek</span><span class="sxs-lookup"><span data-stu-id="f716a-186">Deduction and contribution</span></span> | <span data-ttu-id="f716a-187">Jsou vytvořeny srážky zaměstnance a zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="f716a-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f716a-188">Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="f716a-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="f716a-189">Definování programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f716a-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f716a-190">Vytvořit novou zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="f716a-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f716a-191">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="f716a-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f716a-192">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="f716a-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f716a-193">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-193">Compensation</span></span> 

<span data-ttu-id="f716a-194">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="f716a-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f716a-195">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f716a-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f716a-196">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f716a-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f716a-197">Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f716a-198">Plány fixní kompenzace a převody mzdové sazby jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f716a-199">Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="f716a-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f716a-200">Další informace o plánech kompenzace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="f716a-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="f716a-201">Vytvoření plánů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f716a-202">Vytvoření plánů variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f716a-203">Vývoj struktury platu/kompenzace a plánů</span><span class="sxs-lookup"><span data-stu-id="f716a-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f716a-204">Proces kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f716a-205">Definování procesu kompenzací a výpočet výsledků</span><span class="sxs-lookup"><span data-stu-id="f716a-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f716a-206">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f716a-207">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f716a-208">Práce</span><span class="sxs-lookup"><span data-stu-id="f716a-208">Jobs</span></span> 

<span data-ttu-id="f716a-209">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="f716a-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f716a-210">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="f716a-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f716a-211">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="f716a-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f716a-212">Definování nových prací</span><span class="sxs-lookup"><span data-stu-id="f716a-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f716a-213">Pozice</span><span class="sxs-lookup"><span data-stu-id="f716a-213">Positions</span></span>

<span data-ttu-id="f716a-214">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="f716a-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="f716a-215">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="f716a-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f716a-216">Pozice existuje v oddělení.</span><span class="sxs-lookup"><span data-stu-id="f716a-216">A position exists in a department.</span></span> <span data-ttu-id="f716a-217">Ke každé pozic lze přiřadit pouze jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="f716a-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f716a-218">Mějte na paměti následující data a konfiguraci při vytváření pozic:</span><span class="sxs-lookup"><span data-stu-id="f716a-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f716a-219">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-219">Position (required)</span></span>
- <span data-ttu-id="f716a-220">Popis (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-220">Description (required)</span></span>
- <span data-ttu-id="f716a-221">Práce (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-221">Job (required)</span></span>
- <span data-ttu-id="f716a-222">Oddělení (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-222">Department (required)</span></span>
- <span data-ttu-id="f716a-223">Typ pozice (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-223">Position type (required)</span></span>
- <span data-ttu-id="f716a-224">Ekvivalent plného úvazku</span><span class="sxs-lookup"><span data-stu-id="f716a-224">Full-time equivalent</span></span>
- <span data-ttu-id="f716a-225">Roční normální hodiny (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="f716a-226">Placené právnickou osobu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f716a-227">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-227">Pay cycle (required)</span></span>
- <span data-ttu-id="f716a-228">Výchozí finanční dimenze – Nákladové středisko (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f716a-229">Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f716a-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f716a-230">Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f716a-231">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="f716a-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f716a-232">Uspořádání zaměstnanců podle oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="f716a-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f716a-233">Nastavení pozic</span><span class="sxs-lookup"><span data-stu-id="f716a-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f716a-234">Oddělení</span><span class="sxs-lookup"><span data-stu-id="f716a-234">Departments</span></span>

<span data-ttu-id="f716a-235">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="f716a-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f716a-236">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="f716a-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f716a-237">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="f716a-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f716a-238">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="f716a-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f716a-239">Další informace naleznete v následujících článcích:</span><span class="sxs-lookup"><span data-stu-id="f716a-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f716a-240">Vytvoření oddělení a jeho přidružení k hierarchii oddělení</span><span class="sxs-lookup"><span data-stu-id="f716a-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f716a-241">Definování nových oddělení</span><span class="sxs-lookup"><span data-stu-id="f716a-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f716a-242">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="f716a-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="f716a-243">Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků.</span><span class="sxs-lookup"><span data-stu-id="f716a-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f716a-244">Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="f716a-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f716a-245">Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období.</span><span class="sxs-lookup"><span data-stu-id="f716a-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f716a-246">Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.</span><span class="sxs-lookup"><span data-stu-id="f716a-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f716a-247">Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus.</span><span class="sxs-lookup"><span data-stu-id="f716a-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f716a-248">Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="f716a-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f716a-249">Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.</span><span class="sxs-lookup"><span data-stu-id="f716a-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f716a-250">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f716a-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f716a-251">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-251">Pay cycle (required)</span></span>
- <span data-ttu-id="f716a-252">Četnost platebního cyklu (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f716a-253">Počáteční datum období (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f716a-254">Výchozí datum platby (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f716a-255">Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus.</span><span class="sxs-lookup"><span data-stu-id="f716a-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f716a-256">Před integrací musí být vytvořeno nejméně jedno platební období.</span><span class="sxs-lookup"><span data-stu-id="f716a-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f716a-257">Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f716a-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f716a-258">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-258">Earning codes</span></span>

<span data-ttu-id="f716a-259">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f716a-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f716a-260">Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f716a-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f716a-261">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f716a-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f716a-262">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-262">Earning Code (required)</span></span>
- <span data-ttu-id="f716a-263">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-263">Description</span></span>
- <span data-ttu-id="f716a-264">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="f716a-264">Unit of measure</span></span>
- <span data-ttu-id="f716a-265">Produktivní</span><span class="sxs-lookup"><span data-stu-id="f716a-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f716a-266">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="f716a-266">Worker data</span></span>

<span data-ttu-id="f716a-267">Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy.</span><span class="sxs-lookup"><span data-stu-id="f716a-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f716a-268">Zadané informace lze použít ke sledování pracovníků a osobních informací.</span><span class="sxs-lookup"><span data-stu-id="f716a-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f716a-269">Pro zaměstnance lze spravovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="f716a-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f716a-270">**Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.</span><span class="sxs-lookup"><span data-stu-id="f716a-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f716a-271">**Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.</span><span class="sxs-lookup"><span data-stu-id="f716a-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f716a-272">**Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.</span><span class="sxs-lookup"><span data-stu-id="f716a-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f716a-273">**Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.</span><span class="sxs-lookup"><span data-stu-id="f716a-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f716a-274">Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f716a-275">Obecné informace</span><span class="sxs-lookup"><span data-stu-id="f716a-275">General information</span></span>

- <span data-ttu-id="f716a-276">Osobní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-276">Personnel number (required)</span></span>
- <span data-ttu-id="f716a-277">Jméno (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-277">First name (required)</span></span>
- <span data-ttu-id="f716a-278">Příjmení (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-278">Last name (required)</span></span>
- <span data-ttu-id="f716a-279">Druhé jméno</span><span class="sxs-lookup"><span data-stu-id="f716a-279">Middle name</span></span>
- <span data-ttu-id="f716a-280">Datum služebního věku</span><span class="sxs-lookup"><span data-stu-id="f716a-280">Seniority date</span></span>
- <span data-ttu-id="f716a-281">Známé jako</span><span class="sxs-lookup"><span data-stu-id="f716a-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f716a-282">Osobní údaje</span><span class="sxs-lookup"><span data-stu-id="f716a-282">Personal information</span></span>

- <span data-ttu-id="f716a-283">Rodinný stav (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-283">Marital status (required)</span></span>
- <span data-ttu-id="f716a-284">Datum narození (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-284">Birth date (required)</span></span>
- <span data-ttu-id="f716a-285">Pohlaví (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-285">Gender (required)</span></span>
- <span data-ttu-id="f716a-286">Osoba s tělesným postižením</span><span class="sxs-lookup"><span data-stu-id="f716a-286">Person with disabilities</span></span>
- <span data-ttu-id="f716a-287">Země nebo oblast národnosti (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f716a-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f716a-288">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="f716a-288">Address information</span></span>

- <span data-ttu-id="f716a-289">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-289">Primary (required)</span></span>
- <span data-ttu-id="f716a-290">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-290">Country/region (required)</span></span>
- <span data-ttu-id="f716a-291">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-291">Postal code (required)</span></span>
- <span data-ttu-id="f716a-292">Číslo ulice (povinné) (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f716a-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f716a-293">Doplňující název budovy (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f716a-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f716a-294">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-294">City (required)</span></span>
- <span data-ttu-id="f716a-295">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-295">State (required)</span></span>
- <span data-ttu-id="f716a-296">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f716a-297">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="f716a-297">Contact information</span></span> 

- <span data-ttu-id="f716a-298">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-298">Primary (required)</span></span>
- <span data-ttu-id="f716a-299">Kontaktní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-299">Contact number (required)</span></span>
- <span data-ttu-id="f716a-300">Linka</span><span class="sxs-lookup"><span data-stu-id="f716a-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f716a-301">Informace o mzdě a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-301">Payroll information and earning codes</span></span>

<span data-ttu-id="f716a-302">Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby.</span><span class="sxs-lookup"><span data-stu-id="f716a-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f716a-303">Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.</span><span class="sxs-lookup"><span data-stu-id="f716a-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f716a-304">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-304">Earning codes</span></span>

- <span data-ttu-id="f716a-305">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-305">Position (required)</span></span>
- <span data-ttu-id="f716a-306">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-306">Earning Code (required)</span></span>
- <span data-ttu-id="f716a-307">Frekvence (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-307">Frequency (required)</span></span>
- <span data-ttu-id="f716a-308">Částka (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f716a-309">Mzdové informace</span><span class="sxs-lookup"><span data-stu-id="f716a-309">Payroll information</span></span>

- <span data-ttu-id="f716a-310">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="f716a-310">Payment Method</span></span>
- <span data-ttu-id="f716a-311">Ekonomická oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-311">Economic Region (required)</span></span>
- <span data-ttu-id="f716a-312">ID zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f716a-312">Employee Benefits ID</span></span>
- <span data-ttu-id="f716a-313">Národní číslo ID (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-313">National ID Number (required)</span></span>
- <span data-ttu-id="f716a-314">Číslo vojenské služby</span><span class="sxs-lookup"><span data-stu-id="f716a-314">Military Service Number</span></span>
- <span data-ttu-id="f716a-315">ID směny (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-315">Shift ID (required)</span></span>
- <span data-ttu-id="f716a-316">Daňové číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-316">Tax Number (required)</span></span>
- <span data-ttu-id="f716a-317">ID odborů (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-317">Union ID (required)</span></span>
- <span data-ttu-id="f716a-318">ID pracovního dne (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-318">Work Day ID (required)</span></span>
- <span data-ttu-id="f716a-319">Číslo pracovního povolení</span><span class="sxs-lookup"><span data-stu-id="f716a-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f716a-320">Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**.</span><span class="sxs-lookup"><span data-stu-id="f716a-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f716a-321">Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.</span><span class="sxs-lookup"><span data-stu-id="f716a-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f716a-322">Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-322">Employment details</span></span>

<span data-ttu-id="f716a-323">Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f716a-324">Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f716a-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f716a-325">Počáteční datum zaměstnání (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-325">Employment start date (required)</span></span>
- <span data-ttu-id="f716a-326">Koncové datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-326">Employment end date</span></span>
- <span data-ttu-id="f716a-327">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="f716a-327">Start date</span></span>
- <span data-ttu-id="f716a-328">Upravené počáteční datum</span><span class="sxs-lookup"><span data-stu-id="f716a-328">Adjusted start date</span></span>
- <span data-ttu-id="f716a-329">Datum ukončení zaměstnání (povinné při ukončení)</span><span class="sxs-lookup"><span data-stu-id="f716a-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f716a-330">Důvod ukončení zaměstnání (povinný při ukončení)</span><span class="sxs-lookup"><span data-stu-id="f716a-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f716a-331">Klíčová data zaměstnance se odvozují pomocí následujících informací.</span><span class="sxs-lookup"><span data-stu-id="f716a-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f716a-332">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-332">Human Resources</span></span>                | <span data-ttu-id="f716a-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f716a-334">Datum posledního náboru</span><span class="sxs-lookup"><span data-stu-id="f716a-334">Most recent hire date</span></span> | <span data-ttu-id="f716a-335">Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f716a-336">Datum výpovědi</span><span class="sxs-lookup"><span data-stu-id="f716a-336">Termination date</span></span>      | <span data-ttu-id="f716a-337">Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f716a-338">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="f716a-338">Start date</span></span>            | <span data-ttu-id="f716a-339">Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f716a-340">Datum původního přijetí</span><span class="sxs-lookup"><span data-stu-id="f716a-340">Original hire date</span></span>    | <span data-ttu-id="f716a-341">Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f716a-342">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-342">Compensation</span></span>

<span data-ttu-id="f716a-343">Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f716a-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f716a-344">Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.</span><span class="sxs-lookup"><span data-stu-id="f716a-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f716a-345">Datum platnosti (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-345">Effective Date (required)</span></span>
- <span data-ttu-id="f716a-346">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="f716a-346">Expiration date</span></span>
- <span data-ttu-id="f716a-347">Mzdová sazba (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-347">Pay Rate (required)</span></span>
- <span data-ttu-id="f716a-348">Převody mzdové sazby (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f716a-349">Roční ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="f716a-350">Hodinový ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="f716a-351">Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f716a-352">U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f716a-353">Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f716a-354">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="f716a-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f716a-355">Identifikátor sociálního pojištění</span><span class="sxs-lookup"><span data-stu-id="f716a-355">Social Security identifier</span></span> 

<span data-ttu-id="f716a-356">Každý zaměstnanec musí mít jeden primární identifikátor.</span><span class="sxs-lookup"><span data-stu-id="f716a-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f716a-357">Tento identifikátor musí být typ identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f716a-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f716a-358">V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.</span><span class="sxs-lookup"><span data-stu-id="f716a-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f716a-359">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-359">Primary (required)</span></span>
- <span data-ttu-id="f716a-360">Typ identifikace = SSN</span><span class="sxs-lookup"><span data-stu-id="f716a-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f716a-361">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="f716a-361">Issued Date</span></span>
- <span data-ttu-id="f716a-362">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="f716a-362">Expiration Date</span></span>

<span data-ttu-id="f716a-363">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f716a-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f716a-364">Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.</span><span class="sxs-lookup"><span data-stu-id="f716a-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f716a-365">Bankovní účty a úhrady</span><span class="sxs-lookup"><span data-stu-id="f716a-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="f716a-366">Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="f716a-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f716a-367">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-367">Human Resources</span></span>                         | <span data-ttu-id="f716a-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f716a-369">Číslo bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f716a-370">Kód SWIFT (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-370">SWIFT code (required)</span></span>          | <span data-ttu-id="f716a-371">Pole **ID banky** použité při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f716a-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f716a-372">Číslo pobočky (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f716a-373">Typ bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-373">Bank account type (required)</span></span>   | <span data-ttu-id="f716a-374">Pole **Typ účtu** použitý při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f716a-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f716a-375">Podporované hodnoty jsou **Běžný** a **Mzdový**.</span><span class="sxs-lookup"><span data-stu-id="f716a-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f716a-376">Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky.</span><span class="sxs-lookup"><span data-stu-id="f716a-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f716a-377">Jiné než zůstatkové účty budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="f716a-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f716a-378">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="f716a-378">Address information</span></span>

<span data-ttu-id="f716a-379">Každý zaměstnanec musí mít jedno primární místo.</span><span class="sxs-lookup"><span data-stu-id="f716a-379">Every employee must have one primary location.</span></span> <span data-ttu-id="f716a-380">V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="f716a-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f716a-381">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-381">Primary (required)</span></span>
- <span data-ttu-id="f716a-382">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-382">Country/region (required)</span></span>
- <span data-ttu-id="f716a-383">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="f716a-384">Ulice (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-384">Street (required)</span></span>
- <span data-ttu-id="f716a-385">Číslo ulice (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-385">Street Number (required)</span></span>
- <span data-ttu-id="f716a-386">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="f716a-386">Building Complement</span></span>
- <span data-ttu-id="f716a-387">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-387">City (required)</span></span>
- <span data-ttu-id="f716a-388">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-388">State (required)</span></span>
- <span data-ttu-id="f716a-389">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f716a-390">Konfigurace dat pro generování mzdy v USA a Kanadě</span><span class="sxs-lookup"><span data-stu-id="f716a-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f716a-391">Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="f716a-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f716a-392">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="f716a-392">Departments are required on positions.</span></span>
- <span data-ttu-id="f716a-393">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f716a-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f716a-394">Aplikaci Human Resources lze konfigurovat tak, aby od pozic požadovala určení oddělení.</span><span class="sxs-lookup"><span data-stu-id="f716a-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="f716a-395">Chcete-li to provést, přejděte na **Sdílené pozice lidských zdrojů > Pozice > Vyžadovat oddělení na pozicích**.</span><span class="sxs-lookup"><span data-stu-id="f716a-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f716a-396">Doporučujeme, aby toto nastavení bylo vynuceno pro integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f716a-397">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="f716a-397">Job types</span></span>

<span data-ttu-id="f716a-398">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="f716a-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f716a-399">Typy prací jsou povinné pro zpracování mezd v USA a Kanadě.</span><span class="sxs-lookup"><span data-stu-id="f716a-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f716a-400">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="f716a-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f716a-401">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="f716a-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f716a-402">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f716a-403">Typ práce</span><span class="sxs-lookup"><span data-stu-id="f716a-403">Job type</span></span>   | <span data-ttu-id="f716a-404">Popis</span><span class="sxs-lookup"><span data-stu-id="f716a-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f716a-405">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f716a-405">Hourly</span></span>     | <span data-ttu-id="f716a-406">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f716a-406">Hourly</span></span>      |
| <span data-ttu-id="f716a-407">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f716a-407">Salaried</span></span>   | <span data-ttu-id="f716a-408">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f716a-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f716a-409">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="f716a-409">Position types</span></span> 

<span data-ttu-id="f716a-410">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="f716a-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f716a-411">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="f716a-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f716a-412">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f716a-413">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="f716a-413">Position type</span></span>   | <span data-ttu-id="f716a-414">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f716a-415">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-415">Full-time</span></span>       | <span data-ttu-id="f716a-416">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-416">Full time employee</span></span> |
| <span data-ttu-id="f716a-417">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-417">Part-time</span></span>       | <span data-ttu-id="f716a-418">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f716a-419">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="f716a-419">Reason codes</span></span>

<span data-ttu-id="f716a-420">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f716a-421">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f716a-422">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f716a-423">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f716a-423">Reason code</span></span>    | <span data-ttu-id="f716a-424">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-424">Description</span></span>      | <span data-ttu-id="f716a-425">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="f716a-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f716a-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f716a-426">RESIGNATION</span></span>    | <span data-ttu-id="f716a-427">Výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-427">Resignation</span></span>      | <span data-ttu-id="f716a-428">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-428">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f716a-429">TERMINATION</span></span>    | <span data-ttu-id="f716a-430">Ukončení</span><span class="sxs-lookup"><span data-stu-id="f716a-430">Termination</span></span>      | <span data-ttu-id="f716a-431">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-431">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f716a-432">RETIREMENT</span></span>     | <span data-ttu-id="f716a-433">Důchod</span><span class="sxs-lookup"><span data-stu-id="f716a-433">Retirement</span></span>       | <span data-ttu-id="f716a-434">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-434">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-435">JINÝ</span><span class="sxs-lookup"><span data-stu-id="f716a-435">OTHER</span></span>          | <span data-ttu-id="f716a-436">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="f716a-436">Other Reasons</span></span>    | <span data-ttu-id="f716a-437">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-437">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="f716a-438">DEATH</span></span>          | <span data-ttu-id="f716a-439">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="f716a-439">Death</span></span>            | <span data-ttu-id="f716a-440">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-440">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f716a-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f716a-442">Dovolená</span><span class="sxs-lookup"><span data-stu-id="f716a-442">Leave of Absence</span></span> | <span data-ttu-id="f716a-443">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-443">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f716a-444">CONTRACTEND</span></span>    | <span data-ttu-id="f716a-445">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="f716a-445">End of Contract</span></span>  | <span data-ttu-id="f716a-446">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-446">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f716a-447">SALARYCHANGE</span></span>   | <span data-ttu-id="f716a-448">Změna platu</span><span class="sxs-lookup"><span data-stu-id="f716a-448">Change of Salary</span></span> | <span data-ttu-id="f716a-449">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f716a-450">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="f716a-450">Marital status</span></span>

<span data-ttu-id="f716a-451">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f716a-452">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f716a-453">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-453">Human Resources</span></span>                 | <span data-ttu-id="f716a-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f716a-455">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f716a-455">Married</span></span>                | <span data-ttu-id="f716a-456">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f716a-456">Married</span></span>              |
| <span data-ttu-id="f716a-457">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="f716a-457">Single</span></span>                 | <span data-ttu-id="f716a-458">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="f716a-458">Single</span></span>               |
| <span data-ttu-id="f716a-459">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f716a-459">Widowed</span></span>                | <span data-ttu-id="f716a-460">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f716a-460">Widowed</span></span>              |
| <span data-ttu-id="f716a-461">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f716a-461">Divorced</span></span>               | <span data-ttu-id="f716a-462">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f716a-462">Divorced</span></span>             |
| <span data-ttu-id="f716a-463">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="f716a-463">Registered Partnership</span></span> | <span data-ttu-id="f716a-464">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="f716a-464">Domestic Partnership</span></span> |
| <span data-ttu-id="f716a-465">None</span><span class="sxs-lookup"><span data-stu-id="f716a-465">None</span></span>                   | <span data-ttu-id="f716a-466">None</span><span class="sxs-lookup"><span data-stu-id="f716a-466">None</span></span>                 |
| <span data-ttu-id="f716a-467">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f716a-467">Cohabiting</span></span>             | <span data-ttu-id="f716a-468">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f716a-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f716a-469">Rod</span><span class="sxs-lookup"><span data-stu-id="f716a-469">Gender</span></span>

<span data-ttu-id="f716a-470">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f716a-471">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f716a-472">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-472">Human Resources</span></span>       | <span data-ttu-id="f716a-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f716a-474">Muž</span><span class="sxs-lookup"><span data-stu-id="f716a-474">Male</span></span>         | <span data-ttu-id="f716a-475">Muž</span><span class="sxs-lookup"><span data-stu-id="f716a-475">Male</span></span>            |
| <span data-ttu-id="f716a-476">Žena</span><span class="sxs-lookup"><span data-stu-id="f716a-476">Female</span></span>       | <span data-ttu-id="f716a-477">Žena</span><span class="sxs-lookup"><span data-stu-id="f716a-477">Female</span></span>          |
| <span data-ttu-id="f716a-478">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="f716a-478">Non-specific</span></span> | <span data-ttu-id="f716a-479">*Nepodporováno*</span><span class="sxs-lookup"><span data-stu-id="f716a-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f716a-480">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-480">Earning codes</span></span>

<span data-ttu-id="f716a-481">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f716a-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f716a-482">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f716a-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f716a-483">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="f716a-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f716a-484">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f716a-484">Supported frequencies</span></span>

- <span data-ttu-id="f716a-485">Všechna</span><span class="sxs-lookup"><span data-stu-id="f716a-485">All</span></span>
- <span data-ttu-id="f716a-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f716a-486">EVERYPAY</span></span>
- <span data-ttu-id="f716a-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f716a-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f716a-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f716a-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f716a-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f716a-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f716a-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-490">1OFMTH</span></span>
- <span data-ttu-id="f716a-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-491">LASTOFMTH</span></span>
- <span data-ttu-id="f716a-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-492">2OFMTH</span></span>
- <span data-ttu-id="f716a-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-493">3OFMTH</span></span>
- <span data-ttu-id="f716a-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-494">4OFMTH</span></span>
- <span data-ttu-id="f716a-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-495">5OFMTH</span></span>
- <span data-ttu-id="f716a-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-496">1N2OFMTH</span></span>
- <span data-ttu-id="f716a-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-497">3N4OFMTH</span></span>
- <span data-ttu-id="f716a-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-498">1N3OFMTH</span></span>
- <span data-ttu-id="f716a-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-499">1N4OFMTH</span></span>
- <span data-ttu-id="f716a-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-500">2N3OFMTH</span></span>
- <span data-ttu-id="f716a-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-501">2N4OFMTH</span></span>
- <span data-ttu-id="f716a-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="f716a-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="f716a-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f716a-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f716a-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f716a-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f716a-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f716a-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f716a-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f716a-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f716a-514">Adresy</span><span class="sxs-lookup"><span data-stu-id="f716a-514">Addresses</span></span>

<span data-ttu-id="f716a-515">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="f716a-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f716a-516">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="f716a-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f716a-517">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-517">Human Resources</span></span>          | <span data-ttu-id="f716a-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f716a-519">Země/region</span><span class="sxs-lookup"><span data-stu-id="f716a-519">Country/Region</span></span>  | <span data-ttu-id="f716a-520">Kód země</span><span class="sxs-lookup"><span data-stu-id="f716a-520">Country Code</span></span>          |
| <span data-ttu-id="f716a-521">PSČ</span><span class="sxs-lookup"><span data-stu-id="f716a-521">Zip/Postal Code</span></span> | <span data-ttu-id="f716a-522">PSČ</span><span class="sxs-lookup"><span data-stu-id="f716a-522">Postal Code</span></span>           |
| <span data-ttu-id="f716a-523">Kraj</span><span class="sxs-lookup"><span data-stu-id="f716a-523">State</span></span>           | <span data-ttu-id="f716a-524">Kód státu</span><span class="sxs-lookup"><span data-stu-id="f716a-524">State Code</span></span>            |
| <span data-ttu-id="f716a-525">Město</span><span class="sxs-lookup"><span data-stu-id="f716a-525">City</span></span>            | <span data-ttu-id="f716a-526">Město</span><span class="sxs-lookup"><span data-stu-id="f716a-526">City</span></span>                  |
| <span data-ttu-id="f716a-527">Okres</span><span class="sxs-lookup"><span data-stu-id="f716a-527">County</span></span>          | <span data-ttu-id="f716a-528">Okres</span><span class="sxs-lookup"><span data-stu-id="f716a-528">County (Municipality)</span></span> |
| <span data-ttu-id="f716a-529">Ulice</span><span class="sxs-lookup"><span data-stu-id="f716a-529">Street</span></span>          | <span data-ttu-id="f716a-530">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="f716a-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f716a-531">Daňové oblasti</span><span class="sxs-lookup"><span data-stu-id="f716a-531">Tax regions</span></span>

<span data-ttu-id="f716a-532">Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy.</span><span class="sxs-lookup"><span data-stu-id="f716a-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f716a-533">Daňové oblasti jsou mapovány na Dayforce jako adresy místa.</span><span class="sxs-lookup"><span data-stu-id="f716a-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f716a-534">Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka.</span><span class="sxs-lookup"><span data-stu-id="f716a-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f716a-535">Daňová oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="f716a-535">Tax region (required)</span></span>
- <span data-ttu-id="f716a-536">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-536">Country/Region (required)</span></span>
- <span data-ttu-id="f716a-537">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="f716a-537">State (required)</span></span>
- <span data-ttu-id="f716a-538">Okres</span><span class="sxs-lookup"><span data-stu-id="f716a-538">County</span></span> 
- <span data-ttu-id="f716a-539">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="f716a-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f716a-540">Konfigurace dat pro generování mezd v Mexiku</span><span class="sxs-lookup"><span data-stu-id="f716a-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f716a-541">Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="f716a-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f716a-542">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="f716a-542">Departments are required on positions.</span></span>
- <span data-ttu-id="f716a-543">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="f716a-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f716a-544">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="f716a-544">Job types</span></span>

<span data-ttu-id="f716a-545">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="f716a-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f716a-546">Typy práce jsou povinné pro zpracování mezd v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="f716a-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f716a-547">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="f716a-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f716a-548">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="f716a-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f716a-549">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f716a-550">Typ práce</span><span class="sxs-lookup"><span data-stu-id="f716a-550">Job type</span></span>   | <span data-ttu-id="f716a-551">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f716a-552">Hodinově</span><span class="sxs-lookup"><span data-stu-id="f716a-552">Hourly</span></span>     | <span data-ttu-id="f716a-553">MX hodinově</span><span class="sxs-lookup"><span data-stu-id="f716a-553">MX Hourly</span></span>   |
| <span data-ttu-id="f716a-554">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f716a-554">Salaried</span></span>   | <span data-ttu-id="f716a-555">MX Stálý plat</span><span class="sxs-lookup"><span data-stu-id="f716a-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f716a-556">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="f716a-556">Position types</span></span> 

<span data-ttu-id="f716a-557">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="f716a-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f716a-558">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="f716a-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f716a-559">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f716a-560">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="f716a-560">Position type</span></span>   | <span data-ttu-id="f716a-561">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f716a-562">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-562">Full-time</span></span>       | <span data-ttu-id="f716a-563">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-563">Full time employee</span></span> |
| <span data-ttu-id="f716a-564">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-564">Part-time</span></span>       | <span data-ttu-id="f716a-565">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="f716a-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f716a-566">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="f716a-566">Reason codes</span></span>

<span data-ttu-id="f716a-567">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f716a-568">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="f716a-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f716a-569">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f716a-570">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="f716a-570">Reason code</span></span>            | <span data-ttu-id="f716a-571">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-571">Description</span></span>                    | <span data-ttu-id="f716a-572">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="f716a-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f716a-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="f716a-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f716a-574">Odchod před první mzdou</span><span class="sxs-lookup"><span data-stu-id="f716a-574">Departure before first payroll</span></span> | <span data-ttu-id="f716a-575">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-575">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f716a-576">RESIGNATION</span></span>            | <span data-ttu-id="f716a-577">Výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-577">Resignation</span></span>                    | <span data-ttu-id="f716a-578">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-578">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="f716a-579">PENSION</span></span>                | <span data-ttu-id="f716a-580">Důchod</span><span class="sxs-lookup"><span data-stu-id="f716a-580">Pension</span></span>                        | <span data-ttu-id="f716a-581">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-581">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f716a-582">TERMINATION</span></span>            | <span data-ttu-id="f716a-583">Ukončení</span><span class="sxs-lookup"><span data-stu-id="f716a-583">Termination</span></span>                    | <span data-ttu-id="f716a-584">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-584">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f716a-585">RETIREMENT</span></span>             | <span data-ttu-id="f716a-586">Důchod</span><span class="sxs-lookup"><span data-stu-id="f716a-586">Retirement</span></span>                     | <span data-ttu-id="f716a-587">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-587">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="f716a-588">ABSENTEE</span></span>               | <span data-ttu-id="f716a-589">Nepřítomný</span><span class="sxs-lookup"><span data-stu-id="f716a-589">Absentee</span></span>                       | <span data-ttu-id="f716a-590">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-590">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-591">JINÝ</span><span class="sxs-lookup"><span data-stu-id="f716a-591">OTHER</span></span>                  | <span data-ttu-id="f716a-592">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="f716a-592">Other Reasons</span></span>                  | <span data-ttu-id="f716a-593">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-593">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="f716a-594">CLOSURE</span></span>                | <span data-ttu-id="f716a-595">Obchodní uzávěrka</span><span class="sxs-lookup"><span data-stu-id="f716a-595">Business Closure</span></span>               | <span data-ttu-id="f716a-596">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-596">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="f716a-597">DEATH</span></span>                  | <span data-ttu-id="f716a-598">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="f716a-598">Death</span></span>                          | <span data-ttu-id="f716a-599">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-599">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f716a-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f716a-601">Dovolená</span><span class="sxs-lookup"><span data-stu-id="f716a-601">Leave of Absence</span></span>               | <span data-ttu-id="f716a-602">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-602">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f716a-603">CONTRACTEND</span></span>            | <span data-ttu-id="f716a-604">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="f716a-604">End of Contract</span></span>                | <span data-ttu-id="f716a-605">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="f716a-605">Terminate worker</span></span>     |
| <span data-ttu-id="f716a-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f716a-606">SALARYCHANGE</span></span>           | <span data-ttu-id="f716a-607">Změna platu</span><span class="sxs-lookup"><span data-stu-id="f716a-607">Change of Salary</span></span>               | <span data-ttu-id="f716a-608">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="f716a-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f716a-609">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-609">Terms of employment</span></span>

<span data-ttu-id="f716a-610">Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f716a-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f716a-611">Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="f716a-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f716a-612">Následující podmínky zaměstnání a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="f716a-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f716a-613">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="f716a-613">Terms of employment</span></span>   | <span data-ttu-id="f716a-614">popis</span><span class="sxs-lookup"><span data-stu-id="f716a-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f716a-615">Řádné</span><span class="sxs-lookup"><span data-stu-id="f716a-615">Regular</span></span>               | <span data-ttu-id="f716a-616">Řádné</span><span class="sxs-lookup"><span data-stu-id="f716a-616">Regular</span></span>     |
| <span data-ttu-id="f716a-617">Přímo</span><span class="sxs-lookup"><span data-stu-id="f716a-617">Direct</span></span>                | <span data-ttu-id="f716a-618">Přímo</span><span class="sxs-lookup"><span data-stu-id="f716a-618">Direct</span></span>      |
| <span data-ttu-id="f716a-619">Stáž</span><span class="sxs-lookup"><span data-stu-id="f716a-619">Internship</span></span>            | <span data-ttu-id="f716a-620">Stáž</span><span class="sxs-lookup"><span data-stu-id="f716a-620">Internship</span></span>  |
| <span data-ttu-id="f716a-621">Trvalé</span><span class="sxs-lookup"><span data-stu-id="f716a-621">Permanent</span></span>             | <span data-ttu-id="f716a-622">Trvalé</span><span class="sxs-lookup"><span data-stu-id="f716a-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f716a-623">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="f716a-623">Marital status</span></span>

<span data-ttu-id="f716a-624">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f716a-625">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f716a-626">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-626">Human Resources</span></span>                 | <span data-ttu-id="f716a-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f716a-628">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f716a-628">Married</span></span>                | <span data-ttu-id="f716a-629">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="f716a-629">Married</span></span>                   |
| <span data-ttu-id="f716a-630">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="f716a-630">Single</span></span>                 | <span data-ttu-id="f716a-631">Jednotlivé</span><span class="sxs-lookup"><span data-stu-id="f716a-631">Single</span></span>                    |
| <span data-ttu-id="f716a-632">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f716a-632">Widowed</span></span>                | <span data-ttu-id="f716a-633">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="f716a-633">Widowed</span></span>                   |
| <span data-ttu-id="f716a-634">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f716a-634">Divorced</span></span>               | <span data-ttu-id="f716a-635">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="f716a-635">Divorced</span></span>                  |
| <span data-ttu-id="f716a-636">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="f716a-636">Registered Partnership</span></span> | <span data-ttu-id="f716a-637">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="f716a-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="f716a-638">None</span><span class="sxs-lookup"><span data-stu-id="f716a-638">None</span></span>                   | <span data-ttu-id="f716a-639">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f716a-640">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="f716a-640">Cohabiting</span></span>             | <span data-ttu-id="f716a-641">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f716a-642">Rod</span><span class="sxs-lookup"><span data-stu-id="f716a-642">Gender</span></span>

<span data-ttu-id="f716a-643">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f716a-644">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f716a-645">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-645">Human Resources</span></span>       | <span data-ttu-id="f716a-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f716a-647">Muž</span><span class="sxs-lookup"><span data-stu-id="f716a-647">Male</span></span>         | <span data-ttu-id="f716a-648">Muž</span><span class="sxs-lookup"><span data-stu-id="f716a-648">Male</span></span>                      |
| <span data-ttu-id="f716a-649">Žena</span><span class="sxs-lookup"><span data-stu-id="f716a-649">Female</span></span>       | <span data-ttu-id="f716a-650">Žena</span><span class="sxs-lookup"><span data-stu-id="f716a-650">Female</span></span>                    |
| <span data-ttu-id="f716a-651">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="f716a-651">Non-specific</span></span> | <span data-ttu-id="f716a-652">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f716a-653">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="f716a-653">Payment method</span></span>

<span data-ttu-id="f716a-654">Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="f716a-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f716a-655">Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f716a-656">Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f716a-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f716a-657">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-657">Human Resources</span></span>             | <span data-ttu-id="f716a-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f716a-659">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f716a-659">Cash</span></span>               | <span data-ttu-id="f716a-660">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f716a-660">Cash</span></span>                      |
| <span data-ttu-id="f716a-661">Elektronická platba</span><span class="sxs-lookup"><span data-stu-id="f716a-661">Electronic Payment</span></span> | <span data-ttu-id="f716a-662">Převod</span><span class="sxs-lookup"><span data-stu-id="f716a-662">Transfer</span></span>                  |
| <span data-ttu-id="f716a-663">Kontrola</span><span class="sxs-lookup"><span data-stu-id="f716a-663">Check</span></span>              | <span data-ttu-id="f716a-664">Šek</span><span class="sxs-lookup"><span data-stu-id="f716a-664">Cheque</span></span>                    |
| <span data-ttu-id="f716a-665">Bankovní směnka</span><span class="sxs-lookup"><span data-stu-id="f716a-665">Bank Draft</span></span>         | <span data-ttu-id="f716a-666">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f716a-667">Další</span><span class="sxs-lookup"><span data-stu-id="f716a-667">Other</span></span>              | <span data-ttu-id="f716a-668">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f716a-669">Typ bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="f716a-669">Bank account type</span></span>

<span data-ttu-id="f716a-670">Typy bankovního účtu se používají pro elektronické platby zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="f716a-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f716a-671">Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu.</span><span class="sxs-lookup"><span data-stu-id="f716a-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f716a-672">Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="f716a-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f716a-673">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-673">Human Resources</span></span>            | <span data-ttu-id="f716a-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f716a-675">Běžný účet</span><span class="sxs-lookup"><span data-stu-id="f716a-675">Checking Account</span></span>  | <span data-ttu-id="f716a-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="f716a-676">CheckingAccount</span></span>           |
| <span data-ttu-id="f716a-677">Mzdový účet</span><span class="sxs-lookup"><span data-stu-id="f716a-677">Payroll Account</span></span>   | <span data-ttu-id="f716a-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="f716a-678">PayrollAccount</span></span>            |
| <span data-ttu-id="f716a-679">Spořicí účet</span><span class="sxs-lookup"><span data-stu-id="f716a-679">Savings Account</span></span>   | <span data-ttu-id="f716a-680">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f716a-681">BankGirot účet</span><span class="sxs-lookup"><span data-stu-id="f716a-681">BankGirot account</span></span> | <span data-ttu-id="f716a-682">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f716a-683">PlusGirot účet</span><span class="sxs-lookup"><span data-stu-id="f716a-683">PlusGirot account</span></span> | <span data-ttu-id="f716a-684">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="f716a-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f716a-685">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="f716a-685">Earning codes</span></span>

<span data-ttu-id="f716a-686">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="f716a-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f716a-687">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="f716a-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f716a-688">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="f716a-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f716a-689">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="f716a-689">Supported frequencies</span></span>

- <span data-ttu-id="f716a-690">Všechna</span><span class="sxs-lookup"><span data-stu-id="f716a-690">All</span></span>
- <span data-ttu-id="f716a-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f716a-691">EVERYPAY</span></span>
- <span data-ttu-id="f716a-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f716a-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f716a-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f716a-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f716a-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f716a-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f716a-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-695">1OFMTH</span></span>
- <span data-ttu-id="f716a-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-696">LASTOFMTH</span></span>
- <span data-ttu-id="f716a-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-697">2OFMTH</span></span>
- <span data-ttu-id="f716a-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-698">3OFMTH</span></span>
- <span data-ttu-id="f716a-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-699">4OFMTH</span></span>
- <span data-ttu-id="f716a-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-700">5OFMTH</span></span>
- <span data-ttu-id="f716a-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-701">1N2OFMTH</span></span>
- <span data-ttu-id="f716a-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-702">3N4OFMTH</span></span>
- <span data-ttu-id="f716a-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-703">1N3OFMTH</span></span>
- <span data-ttu-id="f716a-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-704">1N4OFMTH</span></span>
- <span data-ttu-id="f716a-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-705">2N3OFMTH</span></span>
- <span data-ttu-id="f716a-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-706">2N4OFMTH</span></span>
- <span data-ttu-id="f716a-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="f716a-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="f716a-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f716a-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f716a-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f716a-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f716a-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f716a-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f716a-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f716a-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f716a-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f716a-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f716a-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f716a-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f716a-719">Adresy</span><span class="sxs-lookup"><span data-stu-id="f716a-719">Addresses</span></span>

<span data-ttu-id="f716a-720">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="f716a-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f716a-721">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="f716a-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f716a-722">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="f716a-722">Human Resources</span></span>              | <span data-ttu-id="f716a-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f716a-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f716a-724">Země/region</span><span class="sxs-lookup"><span data-stu-id="f716a-724">Country/Region</span></span>      | <span data-ttu-id="f716a-725">Kód země</span><span class="sxs-lookup"><span data-stu-id="f716a-725">Country Code</span></span>          |
| <span data-ttu-id="f716a-726">PSČ</span><span class="sxs-lookup"><span data-stu-id="f716a-726">Zip/Postal Code</span></span>     | <span data-ttu-id="f716a-727">PSČ</span><span class="sxs-lookup"><span data-stu-id="f716a-727">Postal Code</span></span>           |
| <span data-ttu-id="f716a-728">Kraj</span><span class="sxs-lookup"><span data-stu-id="f716a-728">State</span></span>               | <span data-ttu-id="f716a-729">Kód státu</span><span class="sxs-lookup"><span data-stu-id="f716a-729">State Code</span></span>            |
| <span data-ttu-id="f716a-730">Město</span><span class="sxs-lookup"><span data-stu-id="f716a-730">City</span></span>                | <span data-ttu-id="f716a-731">Město</span><span class="sxs-lookup"><span data-stu-id="f716a-731">City</span></span>                  |
| <span data-ttu-id="f716a-732">Okres</span><span class="sxs-lookup"><span data-stu-id="f716a-732">County</span></span>              | <span data-ttu-id="f716a-733">Okres</span><span class="sxs-lookup"><span data-stu-id="f716a-733">County (Municipality)</span></span> |
| <span data-ttu-id="f716a-734">Ulice</span><span class="sxs-lookup"><span data-stu-id="f716a-734">Street</span></span>              | <span data-ttu-id="f716a-735">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="f716a-735">Address Line 1</span></span>        |
| <span data-ttu-id="f716a-736">Číslo popisné</span><span class="sxs-lookup"><span data-stu-id="f716a-736">Street Number</span></span>       | <span data-ttu-id="f716a-737">Řádek adresy 2</span><span class="sxs-lookup"><span data-stu-id="f716a-737">Address Line 2</span></span>        |
| <span data-ttu-id="f716a-738">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="f716a-738">Building Complement</span></span> | <span data-ttu-id="f716a-739">Řádek adresy 5</span><span class="sxs-lookup"><span data-stu-id="f716a-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f716a-740">Číslo cestovního pasu</span><span class="sxs-lookup"><span data-stu-id="f716a-740">Passport number</span></span>

<span data-ttu-id="f716a-741">Zaměstnanci mohou deklarovat informace o cestovním pasu.</span><span class="sxs-lookup"><span data-stu-id="f716a-741">Employees can declare passport information.</span></span> <span data-ttu-id="f716a-742">Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="f716a-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f716a-743">Typ identifikace = Pas</span><span class="sxs-lookup"><span data-stu-id="f716a-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f716a-744">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="f716a-744">Issued Date</span></span>
- <span data-ttu-id="f716a-745">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="f716a-745">Expiration Date</span></span>

<span data-ttu-id="f716a-746">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**.</span><span class="sxs-lookup"><span data-stu-id="f716a-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f716a-747">Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu.</span><span class="sxs-lookup"><span data-stu-id="f716a-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f716a-748">Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.</span><span class="sxs-lookup"><span data-stu-id="f716a-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce
description: Toto téma vysvětluje, jak nakonfigurovat integraci mezi aplikacemi Microsoft Dynamics 365 Talent a Ceridian Dayforce pro zpracování výplat.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898521"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="0a057-103">Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="0a057-104">Integrace mezi aplikacemi Microsoft Dynamics 365 Talent a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="0a057-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="0a057-105">Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Talent i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="0a057-106">Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="0a057-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="0a057-107">Integrace vyžaduje specifická data z aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="0a057-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="0a057-108">Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Talent nakonfigurována tak, aby podporovala integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="0a057-109">Integrace používá následující rozsáhlé kategorie dat:</span><span class="sxs-lookup"><span data-stu-id="0a057-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="0a057-110">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="0a057-110">Human resources data</span></span>
- <span data-ttu-id="0a057-111">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="0a057-111">Compensation data</span></span>
- <span data-ttu-id="0a057-112">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="0a057-113">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="0a057-113">Worker data</span></span>

<span data-ttu-id="0a057-114">Toto téma popisuje postup, který je třeba provést při povolení integrace.</span><span class="sxs-lookup"><span data-stu-id="0a057-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="0a057-115">Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.</span><span class="sxs-lookup"><span data-stu-id="0a057-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="0a057-116">Povolení integrace</span><span class="sxs-lookup"><span data-stu-id="0a057-116">Enable the integration</span></span>

<span data-ttu-id="0a057-117">V aplikaci Talent musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="0a057-118">Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 Finance, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a057-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="0a057-119">Pro zapnutí integrace v aplikaci Talent postupuje podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="0a057-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="0a057-120">Na stránce **Správa systému** zvolte **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="0a057-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="0a057-121">Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.</span><span class="sxs-lookup"><span data-stu-id="0a057-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="0a057-122">Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.</span><span class="sxs-lookup"><span data-stu-id="0a057-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="0a057-123">Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0a057-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="0a057-124">Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence.</span><span class="sxs-lookup"><span data-stu-id="0a057-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="0a057-125">Tuto frekvenci lze změnit v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="0a057-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="0a057-126">Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících tématech Azure:</span><span class="sxs-lookup"><span data-stu-id="0a057-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="0a057-127">O účtech úložiště Azure Storage</span><span class="sxs-lookup"><span data-stu-id="0a057-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="0a057-128">Konfigurace řetězců připojení Azure Storage</span><span class="sxs-lookup"><span data-stu-id="0a057-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="0a057-129">Technické podrobnosti při povolení integrace mezd</span><span class="sxs-lookup"><span data-stu-id="0a057-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="0a057-130">Zapnutí integrace mezd má dva primární efekty:</span><span class="sxs-lookup"><span data-stu-id="0a057-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="0a057-131">Je vytvořen projekt exportu dat s názvem "Export integrací mezd".</span><span class="sxs-lookup"><span data-stu-id="0a057-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="0a057-132">Tento projekt obsahuje entity a pole vyžadované pro integraci mezd.</span><span class="sxs-lookup"><span data-stu-id="0a057-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="0a057-133">Chcete-li zkontrolovat projekt, přejděte na položky **Správa systému**, vyberte dlaždici **Správa dat** a poté otevřete datový projekt ze seznamu projektů.</span><span class="sxs-lookup"><span data-stu-id="0a057-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="0a057-134">Tato dávková úloha spustí projekt exportu dat, zašifruje výsledný balík dat a přenese soubor datového balíku do koncového bodu SFTP nakonfigurovaného na obrazovce **Konfigurace integrace**.</span><span class="sxs-lookup"><span data-stu-id="0a057-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="0a057-135">Datový balík převedený na koncový bod SFTP je šifrován pomocí klíče, který je pro daný balík jedinečný.</span><span class="sxs-lookup"><span data-stu-id="0a057-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="0a057-136">Klíč je v úložišti klíčů Azure, který je přístupný pouze společnosti Ceridian.</span><span class="sxs-lookup"><span data-stu-id="0a057-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="0a057-137">Není možné dešifrovat a prověřit obsah balíčku dat.</span><span class="sxs-lookup"><span data-stu-id="0a057-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="0a057-138">Potřebujete-li zkontrolovat obsah balíčku dat, je třeba exportovat datový projekt integrace mezd ručně, stáhnout jej a poté jej otevřít.</span><span class="sxs-lookup"><span data-stu-id="0a057-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="0a057-139">Ruční export nebude používat šifrování nebo nepřenese balíček.</span><span class="sxs-lookup"><span data-stu-id="0a057-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="0a057-140">Konfigurace vašich dat</span><span class="sxs-lookup"><span data-stu-id="0a057-140">Configure your data</span></span> 

<span data-ttu-id="0a057-141">Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="0a057-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="0a057-142">Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="0a057-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="0a057-143">Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="0a057-144">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="0a057-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="0a057-145">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="0a057-145">Benefits</span></span> 

<span data-ttu-id="0a057-146">Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="0a057-147">Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="0a057-148">Plány zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="0a057-148">Benefit plans</span></span>

- <span data-ttu-id="0a057-149">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-149">Plan (required)</span></span>
- <span data-ttu-id="0a057-150">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-150">Type (required)</span></span>
- <span data-ttu-id="0a057-151">Dopad mzdy (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-151">Payroll impact (required)</span></span>
- <span data-ttu-id="0a057-152">Obnovit nedoplatky</span><span class="sxs-lookup"><span data-stu-id="0a057-152">Recover arrears</span></span>
- <span data-ttu-id="0a057-153">Způsobu provádění odpočtu</span><span class="sxs-lookup"><span data-stu-id="0a057-153">Deduction method</span></span>
- <span data-ttu-id="0a057-154">Priorita odpočtu</span><span class="sxs-lookup"><span data-stu-id="0a057-154">Deduction priority</span></span>
- <span data-ttu-id="0a057-155">Období limitu</span><span class="sxs-lookup"><span data-stu-id="0a057-155">Limit period</span></span>
- <span data-ttu-id="0a057-156">Částka limitu</span><span class="sxs-lookup"><span data-stu-id="0a057-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="0a057-157">Zam. výhody</span><span class="sxs-lookup"><span data-stu-id="0a057-157">Benefits</span></span>

- <span data-ttu-id="0a057-158">Plán (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-158">Plan (required)</span></span>
- <span data-ttu-id="0a057-159">Typ (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-159">Type (required)</span></span>
- <span data-ttu-id="0a057-160">Možnost (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-160">Option (required)</span></span>
- <span data-ttu-id="0a057-161">ID zaměstnanecké výhody (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-161">Benefit ID (required)</span></span>
- <span data-ttu-id="0a057-162">Četnost</span><span class="sxs-lookup"><span data-stu-id="0a057-162">Frequency</span></span>
- <span data-ttu-id="0a057-163">Základ</span><span class="sxs-lookup"><span data-stu-id="0a057-163">Basis</span></span>
- <span data-ttu-id="0a057-164">Částka nebo sazba</span><span class="sxs-lookup"><span data-stu-id="0a057-164">Amount or rate</span></span>
- <span data-ttu-id="0a057-165">Kód příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="0a057-166">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="0a057-166">Supported frequencies</span></span> 

- <span data-ttu-id="0a057-167">Týdně</span><span class="sxs-lookup"><span data-stu-id="0a057-167">Weekly</span></span>
- <span data-ttu-id="0a057-168">Čtrnáctidenně</span><span class="sxs-lookup"><span data-stu-id="0a057-168">Bi-weekly</span></span>
- <span data-ttu-id="0a057-169">Každých 14 dní</span><span class="sxs-lookup"><span data-stu-id="0a057-169">Semi-monthly</span></span>
- <span data-ttu-id="0a057-170">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="0a057-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="0a057-171">Podporované základy</span><span class="sxs-lookup"><span data-stu-id="0a057-171">Supported bases</span></span> 

- <span data-ttu-id="0a057-172">Pevná částka</span><span class="sxs-lookup"><span data-stu-id="0a057-172">Fixed amount</span></span>
- <span data-ttu-id="0a057-173">Procento příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-173">Percent of earnings</span></span>
- <span data-ttu-id="0a057-174">Produktivní hodiny</span><span class="sxs-lookup"><span data-stu-id="0a057-174">Productive hours</span></span>

<span data-ttu-id="0a057-175">Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="0a057-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="0a057-176">Výběr v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-176">Selection in Talent</span></span>        | <span data-ttu-id="0a057-177">Výsledek v aplikaci Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0a057-178">None</span><span class="sxs-lookup"><span data-stu-id="0a057-178">None</span></span>                       | <span data-ttu-id="0a057-179">Nebyla vytvořena žádná srážka.</span><span class="sxs-lookup"><span data-stu-id="0a057-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="0a057-180">Jen odpočet</span><span class="sxs-lookup"><span data-stu-id="0a057-180">Deduction only</span></span>             | <span data-ttu-id="0a057-181">Byla vytvořena srážka zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="0a057-182">Jen příspěvek</span><span class="sxs-lookup"><span data-stu-id="0a057-182">Contribution only</span></span>          | <span data-ttu-id="0a057-183">Byla vytvořena srážka zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="0a057-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="0a057-184">Odpočet a příspěvek</span><span class="sxs-lookup"><span data-stu-id="0a057-184">Deduction and contribution</span></span> | <span data-ttu-id="0a057-185">Jsou vytvořeny srážky zaměstnance a zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="0a057-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="0a057-186">Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="0a057-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="0a057-187">Definování programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="0a057-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="0a057-188">Vytvoření nové zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="0a057-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="0a057-189">Definování pravidel a zásad nároků na zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="0a057-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="0a057-190">Registrace a odebrání zaměstnaneckých výhod pracovníků</span><span class="sxs-lookup"><span data-stu-id="0a057-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="0a057-191">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-191">Compensation</span></span> 

<span data-ttu-id="0a057-192">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="0a057-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="0a057-193">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="0a057-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="0a057-194">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="0a057-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="0a057-195">Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="0a057-196">Plány fixní kompenzace a převody mzdové sazby jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="0a057-197">Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="0a057-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="0a057-198">Další informace o plánech kompenzace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="0a057-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="0a057-199">Vytvoření plánů fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="0a057-200">Vytvoření plánů variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="0a057-201">Vývoj struktury platu/kompenzace a plánů</span><span class="sxs-lookup"><span data-stu-id="0a057-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="0a057-202">Proces kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="0a057-203">Definování procesu kompenzací a výpočet výsledků</span><span class="sxs-lookup"><span data-stu-id="0a057-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="0a057-204">Přihlášení zaměstnance k plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="0a057-205">Přihlášení zaměstnance k plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="0a057-206">Práce</span><span class="sxs-lookup"><span data-stu-id="0a057-206">Jobs</span></span> 

<span data-ttu-id="0a057-207">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="0a057-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="0a057-208">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="0a057-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0a057-209">Nastavení komponent práce</span><span class="sxs-lookup"><span data-stu-id="0a057-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="0a057-210">Definování nových pracovních míst</span><span class="sxs-lookup"><span data-stu-id="0a057-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="0a057-211">Pozice</span><span class="sxs-lookup"><span data-stu-id="0a057-211">Positions</span></span>

<span data-ttu-id="0a057-212">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="0a057-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="0a057-213">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="0a057-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="0a057-214">Pozice existuje v oddělení.</span><span class="sxs-lookup"><span data-stu-id="0a057-214">A position exists in a department.</span></span> <span data-ttu-id="0a057-215">Ke každé pozic lze přiřadit pouze jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a057-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="0a057-216">Mějte na paměti následující data a konfiguraci při vytváření pozic:</span><span class="sxs-lookup"><span data-stu-id="0a057-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="0a057-217">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-217">Position (required)</span></span>
- <span data-ttu-id="0a057-218">Popis (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-218">Description (required)</span></span>
- <span data-ttu-id="0a057-219">Práce (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-219">Job (required)</span></span>
- <span data-ttu-id="0a057-220">Oddělení (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-220">Department (required)</span></span>
- <span data-ttu-id="0a057-221">Typ pozice (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-221">Position type (required)</span></span>
- <span data-ttu-id="0a057-222">Ekvivalent plného úvazku</span><span class="sxs-lookup"><span data-stu-id="0a057-222">Full-time equivalent</span></span>
- <span data-ttu-id="0a057-223">Roční normální hodiny (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="0a057-224">Placené právnickou osobu (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="0a057-225">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-225">Pay cycle (required)</span></span>
- <span data-ttu-id="0a057-226">Výchozí finanční dimenze – Nákladové středisko (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="0a057-227">Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu</span><span class="sxs-lookup"><span data-stu-id="0a057-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="0a057-228">Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="0a057-229">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="0a057-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0a057-230">Uspořádání zaměstnanců podle oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="0a057-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="0a057-231">Nastavení pozic</span><span class="sxs-lookup"><span data-stu-id="0a057-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="0a057-232">Oddělení</span><span class="sxs-lookup"><span data-stu-id="0a057-232">Departments</span></span>

<span data-ttu-id="0a057-233">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="0a057-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="0a057-234">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="0a057-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="0a057-235">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="0a057-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="0a057-236">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="0a057-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="0a057-237">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="0a057-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0a057-238">Vytvoření oddělení a jeho přidružení k hierarchii oddělení</span><span class="sxs-lookup"><span data-stu-id="0a057-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="0a057-239">Definování nových oddělení</span><span class="sxs-lookup"><span data-stu-id="0a057-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="0a057-240">Platební cykly a platební období</span><span class="sxs-lookup"><span data-stu-id="0a057-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="0a057-241">Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků.</span><span class="sxs-lookup"><span data-stu-id="0a057-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="0a057-242">Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="0a057-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="0a057-243">Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období.</span><span class="sxs-lookup"><span data-stu-id="0a057-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="0a057-244">Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.</span><span class="sxs-lookup"><span data-stu-id="0a057-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="0a057-245">Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus.</span><span class="sxs-lookup"><span data-stu-id="0a057-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="0a057-246">Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="0a057-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="0a057-247">Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.</span><span class="sxs-lookup"><span data-stu-id="0a057-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="0a057-248">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="0a057-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0a057-249">Platební cyklus (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-249">Pay cycle (required)</span></span>
- <span data-ttu-id="0a057-250">Četnost platebního cyklu (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="0a057-251">Počáteční datum období (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="0a057-252">Výchozí datum platby (první platební období je povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="0a057-253">Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus.</span><span class="sxs-lookup"><span data-stu-id="0a057-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="0a057-254">Před integrací musí být vytvořeno nejméně jedno platební období.</span><span class="sxs-lookup"><span data-stu-id="0a057-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="0a057-255">Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="0a057-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="0a057-256">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-256">Earning codes</span></span>

<span data-ttu-id="0a057-257">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="0a057-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a057-258">Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="0a057-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="0a057-259">Následující informace se používají v aplikaci Dayforce:</span><span class="sxs-lookup"><span data-stu-id="0a057-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0a057-260">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-260">Earning Code (required)</span></span>
- <span data-ttu-id="0a057-261">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-261">Description</span></span>
- <span data-ttu-id="0a057-262">Měrná jednotka</span><span class="sxs-lookup"><span data-stu-id="0a057-262">Unit of measure</span></span>
- <span data-ttu-id="0a057-263">Produktivní</span><span class="sxs-lookup"><span data-stu-id="0a057-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="0a057-264">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="0a057-264">Worker data</span></span>

<span data-ttu-id="0a057-265">Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy.</span><span class="sxs-lookup"><span data-stu-id="0a057-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="0a057-266">Zadané informace lze použít ke sledování pracovníků a osobních informací.</span><span class="sxs-lookup"><span data-stu-id="0a057-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="0a057-267">Pro zaměstnance lze spravovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="0a057-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="0a057-268">**Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.</span><span class="sxs-lookup"><span data-stu-id="0a057-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="0a057-269">**Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.</span><span class="sxs-lookup"><span data-stu-id="0a057-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="0a057-270">**Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.</span><span class="sxs-lookup"><span data-stu-id="0a057-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="0a057-271">**Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.</span><span class="sxs-lookup"><span data-stu-id="0a057-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="0a057-272">Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="0a057-273">Obecné informace</span><span class="sxs-lookup"><span data-stu-id="0a057-273">General information</span></span>

- <span data-ttu-id="0a057-274">Osobní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-274">Personnel number (required)</span></span>
- <span data-ttu-id="0a057-275">Jméno (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-275">First name (required)</span></span>
- <span data-ttu-id="0a057-276">Příjmení (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-276">Last name (required)</span></span>
- <span data-ttu-id="0a057-277">Druhé jméno</span><span class="sxs-lookup"><span data-stu-id="0a057-277">Middle name</span></span>
- <span data-ttu-id="0a057-278">Datum služebního věku</span><span class="sxs-lookup"><span data-stu-id="0a057-278">Seniority date</span></span>
- <span data-ttu-id="0a057-279">Známé jako</span><span class="sxs-lookup"><span data-stu-id="0a057-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="0a057-280">Osobní údaje</span><span class="sxs-lookup"><span data-stu-id="0a057-280">Personal information</span></span>

- <span data-ttu-id="0a057-281">Rodinný stav (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-281">Marital status (required)</span></span>
- <span data-ttu-id="0a057-282">Datum narození (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-282">Birth date (required)</span></span>
- <span data-ttu-id="0a057-283">Pohlaví (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-283">Gender (required)</span></span>
- <span data-ttu-id="0a057-284">Osoba s tělesným postižením</span><span class="sxs-lookup"><span data-stu-id="0a057-284">Person with disabilities</span></span>
- <span data-ttu-id="0a057-285">Země nebo oblast národnosti (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0a057-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="0a057-286">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="0a057-286">Address information</span></span>

- <span data-ttu-id="0a057-287">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-287">Primary (required)</span></span>
- <span data-ttu-id="0a057-288">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-288">Country/region (required)</span></span>
- <span data-ttu-id="0a057-289">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-289">Postal code (required)</span></span>
- <span data-ttu-id="0a057-290">Číslo ulice (povinné) (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0a057-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="0a057-291">Doplňující název budovy (pouze pro Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0a057-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="0a057-292">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-292">City (required)</span></span>
- <span data-ttu-id="0a057-293">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-293">State (required)</span></span>
- <span data-ttu-id="0a057-294">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="0a057-295">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="0a057-295">Contact information</span></span> 

- <span data-ttu-id="0a057-296">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-296">Primary (required)</span></span>
- <span data-ttu-id="0a057-297">Kontaktní číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-297">Contact number (required)</span></span>
- <span data-ttu-id="0a057-298">Linka</span><span class="sxs-lookup"><span data-stu-id="0a057-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="0a057-299">Informace o mzdě a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-299">Payroll information and earning codes</span></span>

<span data-ttu-id="0a057-300">Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby.</span><span class="sxs-lookup"><span data-stu-id="0a057-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="0a057-301">Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.</span><span class="sxs-lookup"><span data-stu-id="0a057-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="0a057-302">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-302">Earning codes</span></span>

- <span data-ttu-id="0a057-303">Pozice (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-303">Position (required)</span></span>
- <span data-ttu-id="0a057-304">Kód příjmů (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-304">Earning Code (required)</span></span>
- <span data-ttu-id="0a057-305">Frekvence (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-305">Frequency (required)</span></span>
- <span data-ttu-id="0a057-306">Částka (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="0a057-307">Mzdové informace</span><span class="sxs-lookup"><span data-stu-id="0a057-307">Payroll information</span></span>

- <span data-ttu-id="0a057-308">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="0a057-308">Payment Method</span></span>
- <span data-ttu-id="0a057-309">Ekonomická oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-309">Economic Region (required)</span></span>
- <span data-ttu-id="0a057-310">ID zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="0a057-310">Employee Benefits ID</span></span>
- <span data-ttu-id="0a057-311">Národní číslo ID (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-311">National ID Number (required)</span></span>
- <span data-ttu-id="0a057-312">Číslo vojenské služby</span><span class="sxs-lookup"><span data-stu-id="0a057-312">Military Service Number</span></span>
- <span data-ttu-id="0a057-313">ID směny (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-313">Shift ID (required)</span></span>
- <span data-ttu-id="0a057-314">Daňové číslo (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-314">Tax Number (required)</span></span>
- <span data-ttu-id="0a057-315">ID odborů (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-315">Union ID (required)</span></span>
- <span data-ttu-id="0a057-316">ID pracovního dne (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-316">Work Day ID (required)</span></span>
- <span data-ttu-id="0a057-317">Číslo pracovního povolení</span><span class="sxs-lookup"><span data-stu-id="0a057-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="0a057-318">Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**.</span><span class="sxs-lookup"><span data-stu-id="0a057-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="0a057-319">Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.</span><span class="sxs-lookup"><span data-stu-id="0a057-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="0a057-320">Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-320">Employment details</span></span>

<span data-ttu-id="0a057-321">Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="0a057-322">Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a057-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="0a057-323">Počáteční datum zaměstnání (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-323">Employment start date (required)</span></span>
- <span data-ttu-id="0a057-324">Koncové datum zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-324">Employment end date</span></span>
- <span data-ttu-id="0a057-325">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="0a057-325">Start date</span></span>
- <span data-ttu-id="0a057-326">Upravené počáteční datum</span><span class="sxs-lookup"><span data-stu-id="0a057-326">Adjusted start date</span></span>
- <span data-ttu-id="0a057-327">Datum ukončení zaměstnání (povinné při ukončení)</span><span class="sxs-lookup"><span data-stu-id="0a057-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="0a057-328">Důvod ukončení zaměstnání (povinný při ukončení)</span><span class="sxs-lookup"><span data-stu-id="0a057-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="0a057-329">Klíčová data zaměstnance se odvozují pomocí následujících informací.</span><span class="sxs-lookup"><span data-stu-id="0a057-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="0a057-330">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-330">Talent</span></span>                | <span data-ttu-id="0a057-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a057-332">Datum posledního náboru</span><span class="sxs-lookup"><span data-stu-id="0a057-332">Most recent hire date</span></span> | <span data-ttu-id="0a057-333">Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0a057-334">Datum výpovědi</span><span class="sxs-lookup"><span data-stu-id="0a057-334">Termination date</span></span>      | <span data-ttu-id="0a057-335">Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0a057-336">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="0a057-336">Start date</span></span>            | <span data-ttu-id="0a057-337">Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="0a057-338">Datum původního přijetí</span><span class="sxs-lookup"><span data-stu-id="0a057-338">Original hire date</span></span>    | <span data-ttu-id="0a057-339">Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="0a057-340">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-340">Compensation</span></span>

<span data-ttu-id="0a057-341">Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a057-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="0a057-342">Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.</span><span class="sxs-lookup"><span data-stu-id="0a057-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="0a057-343">Datum platnosti (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-343">Effective Date (required)</span></span>
- <span data-ttu-id="0a057-344">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="0a057-344">Expiration date</span></span>
- <span data-ttu-id="0a057-345">Mzdová sazba (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-345">Pay Rate (required)</span></span>
- <span data-ttu-id="0a057-346">Převody mzdové sazby (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="0a057-347">Roční ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="0a057-348">Hodinový ekvivalent (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="0a057-349">Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="0a057-350">U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="0a057-351">Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="0a057-352">Identifikační čísla</span><span class="sxs-lookup"><span data-stu-id="0a057-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="0a057-353">Identifikátor sociálního pojištění</span><span class="sxs-lookup"><span data-stu-id="0a057-353">Social Security identifier</span></span> 

<span data-ttu-id="0a057-354">Každý zaměstnanec musí mít jeden primární identifikátor.</span><span class="sxs-lookup"><span data-stu-id="0a057-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="0a057-355">Tento identifikátor musí být typ identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="0a057-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="0a057-356">V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.</span><span class="sxs-lookup"><span data-stu-id="0a057-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="0a057-357">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-357">Primary (required)</span></span>
- <span data-ttu-id="0a057-358">Typ identifikace = SSN</span><span class="sxs-lookup"><span data-stu-id="0a057-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="0a057-359">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="0a057-359">Issued Date</span></span>
- <span data-ttu-id="0a057-360">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="0a057-360">Expiration Date</span></span>

<span data-ttu-id="0a057-361">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**.</span><span class="sxs-lookup"><span data-stu-id="0a057-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="0a057-362">Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.</span><span class="sxs-lookup"><span data-stu-id="0a057-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="0a057-363">Bankovní účty a úhrady</span><span class="sxs-lookup"><span data-stu-id="0a057-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="0a057-364">Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.</span><span class="sxs-lookup"><span data-stu-id="0a057-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="0a057-365">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-365">Talent</span></span>                         | <span data-ttu-id="0a057-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a057-367">Číslo bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="0a057-368">Kód SWIFT (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-368">SWIFT code (required)</span></span>          | <span data-ttu-id="0a057-369">Pole **ID banky** použité při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="0a057-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="0a057-370">Číslo pobočky (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="0a057-371">Typ bankovního účtu (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-371">Bank account type (required)</span></span>   | <span data-ttu-id="0a057-372">Pole **Typ účtu** použitý při zpracování mzdy v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="0a057-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="0a057-373">Podporované hodnoty jsou **Běžný** a **Mzdový**.</span><span class="sxs-lookup"><span data-stu-id="0a057-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="0a057-374">Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky.</span><span class="sxs-lookup"><span data-stu-id="0a057-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="0a057-375">Jiné než zůstatkové účty budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="0a057-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="0a057-376">Informace adresy</span><span class="sxs-lookup"><span data-stu-id="0a057-376">Address information</span></span>

<span data-ttu-id="0a057-377">Každý zaměstnanec musí mít jedno primární místo.</span><span class="sxs-lookup"><span data-stu-id="0a057-377">Every employee must have one primary location.</span></span> <span data-ttu-id="0a057-378">V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="0a057-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="0a057-379">Primární (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-379">Primary (required)</span></span>
- <span data-ttu-id="0a057-380">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-380">Country/region (required)</span></span>
- <span data-ttu-id="0a057-381">PSČ (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="0a057-382">Ulice (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-382">Street (required)</span></span>
- <span data-ttu-id="0a057-383">Číslo ulice (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-383">Street Number (required)</span></span>
- <span data-ttu-id="0a057-384">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="0a057-384">Building Complement</span></span>
- <span data-ttu-id="0a057-385">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-385">City (required)</span></span>
- <span data-ttu-id="0a057-386">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-386">State (required)</span></span>
- <span data-ttu-id="0a057-387">Okres (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="0a057-388">Konfigurace dat pro generování mzdy v USA a Kanadě</span><span class="sxs-lookup"><span data-stu-id="0a057-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="0a057-389">Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="0a057-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="0a057-390">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="0a057-390">Departments are required on positions.</span></span>
- <span data-ttu-id="0a057-391">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a057-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="0a057-392">Aplikaci Talent lze konfigurovat tak, aby od pozic požadovala určení oddělení.</span><span class="sxs-lookup"><span data-stu-id="0a057-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="0a057-393">Chcete-li to provést, přejděte na **Sdílené pozice lidských zdrojů > Pozice > Vyžadovat oddělení na pozicích**.</span><span class="sxs-lookup"><span data-stu-id="0a057-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="0a057-394">Doporučujeme, aby toto nastavení bylo vynuceno pro integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="0a057-395">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="0a057-395">Job types</span></span>

<span data-ttu-id="0a057-396">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="0a057-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0a057-397">Typy prací jsou povinné pro zpracování mezd v USA a Kanadě.</span><span class="sxs-lookup"><span data-stu-id="0a057-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="0a057-398">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="0a057-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0a057-399">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="0a057-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0a057-400">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0a057-401">Typ práce</span><span class="sxs-lookup"><span data-stu-id="0a057-401">Job type</span></span>   | <span data-ttu-id="0a057-402">Popis</span><span class="sxs-lookup"><span data-stu-id="0a057-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0a057-403">Hodinově</span><span class="sxs-lookup"><span data-stu-id="0a057-403">Hourly</span></span>     | <span data-ttu-id="0a057-404">Hodinově</span><span class="sxs-lookup"><span data-stu-id="0a057-404">Hourly</span></span>      |
| <span data-ttu-id="0a057-405">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="0a057-405">Salaried</span></span>   | <span data-ttu-id="0a057-406">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="0a057-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="0a057-407">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="0a057-407">Position types</span></span> 

<span data-ttu-id="0a057-408">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="0a057-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0a057-409">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="0a057-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0a057-410">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0a057-411">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="0a057-411">Position type</span></span>   | <span data-ttu-id="0a057-412">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0a057-413">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-413">Full-time</span></span>       | <span data-ttu-id="0a057-414">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-414">Full time employee</span></span> |
| <span data-ttu-id="0a057-415">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-415">Part-time</span></span>       | <span data-ttu-id="0a057-416">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0a057-417">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="0a057-417">Reason codes</span></span>

<span data-ttu-id="0a057-418">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0a057-419">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0a057-420">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0a057-421">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="0a057-421">Reason code</span></span>    | <span data-ttu-id="0a057-422">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-422">Description</span></span>      | <span data-ttu-id="0a057-423">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="0a057-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="0a057-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0a057-424">RESIGNATION</span></span>    | <span data-ttu-id="0a057-425">Výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-425">Resignation</span></span>      | <span data-ttu-id="0a057-426">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-426">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0a057-427">TERMINATION</span></span>    | <span data-ttu-id="0a057-428">Ukončení</span><span class="sxs-lookup"><span data-stu-id="0a057-428">Termination</span></span>      | <span data-ttu-id="0a057-429">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-429">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0a057-430">RETIREMENT</span></span>     | <span data-ttu-id="0a057-431">Důchod</span><span class="sxs-lookup"><span data-stu-id="0a057-431">Retirement</span></span>       | <span data-ttu-id="0a057-432">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-432">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-433">JINÝ</span><span class="sxs-lookup"><span data-stu-id="0a057-433">OTHER</span></span>          | <span data-ttu-id="0a057-434">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="0a057-434">Other Reasons</span></span>    | <span data-ttu-id="0a057-435">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-435">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="0a057-436">DEATH</span></span>          | <span data-ttu-id="0a057-437">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="0a057-437">Death</span></span>            | <span data-ttu-id="0a057-438">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-438">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0a057-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="0a057-440">Dovolená</span><span class="sxs-lookup"><span data-stu-id="0a057-440">Leave of Absence</span></span> | <span data-ttu-id="0a057-441">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-441">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0a057-442">CONTRACTEND</span></span>    | <span data-ttu-id="0a057-443">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="0a057-443">End of Contract</span></span>  | <span data-ttu-id="0a057-444">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-444">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a057-445">SALARYCHANGE</span></span>   | <span data-ttu-id="0a057-446">Změna platu</span><span class="sxs-lookup"><span data-stu-id="0a057-446">Change of Salary</span></span> | <span data-ttu-id="0a057-447">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="0a057-448">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="0a057-448">Marital status</span></span>

<span data-ttu-id="0a057-449">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a057-450">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a057-451">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-451">Talent</span></span>                 | <span data-ttu-id="0a057-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="0a057-453">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="0a057-453">Married</span></span>                | <span data-ttu-id="0a057-454">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="0a057-454">Married</span></span>              |
| <span data-ttu-id="0a057-455">Jedno</span><span class="sxs-lookup"><span data-stu-id="0a057-455">Single</span></span>                 | <span data-ttu-id="0a057-456">Jedno</span><span class="sxs-lookup"><span data-stu-id="0a057-456">Single</span></span>               |
| <span data-ttu-id="0a057-457">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="0a057-457">Widowed</span></span>                | <span data-ttu-id="0a057-458">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="0a057-458">Widowed</span></span>              |
| <span data-ttu-id="0a057-459">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="0a057-459">Divorced</span></span>               | <span data-ttu-id="0a057-460">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="0a057-460">Divorced</span></span>             |
| <span data-ttu-id="0a057-461">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="0a057-461">Registered Partnership</span></span> | <span data-ttu-id="0a057-462">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="0a057-462">Domestic Partnership</span></span> |
| <span data-ttu-id="0a057-463">None</span><span class="sxs-lookup"><span data-stu-id="0a057-463">None</span></span>                   | <span data-ttu-id="0a057-464">None</span><span class="sxs-lookup"><span data-stu-id="0a057-464">None</span></span>                 |
| <span data-ttu-id="0a057-465">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="0a057-465">Cohabiting</span></span>             | <span data-ttu-id="0a057-466">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="0a057-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="0a057-467">Rod</span><span class="sxs-lookup"><span data-stu-id="0a057-467">Gender</span></span>

<span data-ttu-id="0a057-468">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a057-469">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a057-470">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-470">Talent</span></span>       | <span data-ttu-id="0a057-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="0a057-472">Muž</span><span class="sxs-lookup"><span data-stu-id="0a057-472">Male</span></span>         | <span data-ttu-id="0a057-473">Muž</span><span class="sxs-lookup"><span data-stu-id="0a057-473">Male</span></span>            |
| <span data-ttu-id="0a057-474">Žena</span><span class="sxs-lookup"><span data-stu-id="0a057-474">Female</span></span>       | <span data-ttu-id="0a057-475">Žena</span><span class="sxs-lookup"><span data-stu-id="0a057-475">Female</span></span>          |
| <span data-ttu-id="0a057-476">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="0a057-476">Non-specific</span></span> | <span data-ttu-id="0a057-477">*Nepodporováno*</span><span class="sxs-lookup"><span data-stu-id="0a057-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0a057-478">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-478">Earning codes</span></span>

<span data-ttu-id="0a057-479">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="0a057-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a057-480">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="0a057-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0a057-481">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="0a057-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0a057-482">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="0a057-482">Supported frequencies</span></span>

- <span data-ttu-id="0a057-483">Všechna</span><span class="sxs-lookup"><span data-stu-id="0a057-483">All</span></span>
- <span data-ttu-id="0a057-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0a057-484">EVERYPAY</span></span>
- <span data-ttu-id="0a057-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0a057-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0a057-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0a057-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0a057-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0a057-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0a057-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-488">1OFMTH</span></span>
- <span data-ttu-id="0a057-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-489">LASTOFMTH</span></span>
- <span data-ttu-id="0a057-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-490">2OFMTH</span></span>
- <span data-ttu-id="0a057-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-491">3OFMTH</span></span>
- <span data-ttu-id="0a057-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-492">4OFMTH</span></span>
- <span data-ttu-id="0a057-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-493">5OFMTH</span></span>
- <span data-ttu-id="0a057-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-494">1N2OFMTH</span></span>
- <span data-ttu-id="0a057-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-495">3N4OFMTH</span></span>
- <span data-ttu-id="0a057-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-496">1N3OFMTH</span></span>
- <span data-ttu-id="0a057-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-497">1N4OFMTH</span></span>
- <span data-ttu-id="0a057-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-498">2N3OFMTH</span></span>
- <span data-ttu-id="0a057-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-499">2N4OFMTH</span></span>
- <span data-ttu-id="0a057-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="0a057-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="0a057-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0a057-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0a057-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0a057-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0a057-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0a057-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0a057-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0a057-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0a057-512">Adresy</span><span class="sxs-lookup"><span data-stu-id="0a057-512">Addresses</span></span>

<span data-ttu-id="0a057-513">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="0a057-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0a057-514">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="0a057-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0a057-515">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-515">Talent</span></span>          | <span data-ttu-id="0a057-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="0a057-517">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="0a057-517">Country/Region</span></span>  | <span data-ttu-id="0a057-518">Kód země</span><span class="sxs-lookup"><span data-stu-id="0a057-518">Country Code</span></span>          |
| <span data-ttu-id="0a057-519">PSČ</span><span class="sxs-lookup"><span data-stu-id="0a057-519">Zip/Postal Code</span></span> | <span data-ttu-id="0a057-520">PSČ</span><span class="sxs-lookup"><span data-stu-id="0a057-520">Postal Code</span></span>           |
| <span data-ttu-id="0a057-521">Kraj</span><span class="sxs-lookup"><span data-stu-id="0a057-521">State</span></span>           | <span data-ttu-id="0a057-522">Kód státu</span><span class="sxs-lookup"><span data-stu-id="0a057-522">State Code</span></span>            |
| <span data-ttu-id="0a057-523">Město</span><span class="sxs-lookup"><span data-stu-id="0a057-523">City</span></span>            | <span data-ttu-id="0a057-524">Město</span><span class="sxs-lookup"><span data-stu-id="0a057-524">City</span></span>                  |
| <span data-ttu-id="0a057-525">Okres</span><span class="sxs-lookup"><span data-stu-id="0a057-525">County</span></span>          | <span data-ttu-id="0a057-526">Okres</span><span class="sxs-lookup"><span data-stu-id="0a057-526">County (Municipality)</span></span> |
| <span data-ttu-id="0a057-527">Ulice</span><span class="sxs-lookup"><span data-stu-id="0a057-527">Street</span></span>          | <span data-ttu-id="0a057-528">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="0a057-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="0a057-529">Daňové oblasti</span><span class="sxs-lookup"><span data-stu-id="0a057-529">Tax regions</span></span>

<span data-ttu-id="0a057-530">Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy.</span><span class="sxs-lookup"><span data-stu-id="0a057-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="0a057-531">Daňové oblasti jsou mapovány na Dayforce jako adresy místa.</span><span class="sxs-lookup"><span data-stu-id="0a057-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="0a057-532">Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a057-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="0a057-533">Daňová oblast (povinná)</span><span class="sxs-lookup"><span data-stu-id="0a057-533">Tax region (required)</span></span>
- <span data-ttu-id="0a057-534">Země/oblast (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-534">Country/Region (required)</span></span>
- <span data-ttu-id="0a057-535">Stát (povinný)</span><span class="sxs-lookup"><span data-stu-id="0a057-535">State (required)</span></span>
- <span data-ttu-id="0a057-536">Okres</span><span class="sxs-lookup"><span data-stu-id="0a057-536">County</span></span> 
- <span data-ttu-id="0a057-537">Město (povinné)</span><span class="sxs-lookup"><span data-stu-id="0a057-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="0a057-538">Konfigurace dat pro generování mezd v Mexiku</span><span class="sxs-lookup"><span data-stu-id="0a057-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="0a057-539">Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:</span><span class="sxs-lookup"><span data-stu-id="0a057-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="0a057-540">Pro pozice jsou požadována oddělení.</span><span class="sxs-lookup"><span data-stu-id="0a057-540">Departments are required on positions.</span></span>
- <span data-ttu-id="0a057-541">Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a057-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="0a057-542">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="0a057-542">Job types</span></span>

<span data-ttu-id="0a057-543">Typy prací se používají pro seskupení podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="0a057-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0a057-544">Typy práce jsou povinné pro zpracování mezd v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="0a057-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="0a057-545">Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu.</span><span class="sxs-lookup"><span data-stu-id="0a057-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0a057-546">Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.</span><span class="sxs-lookup"><span data-stu-id="0a057-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0a057-547">Následující typy práce a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0a057-548">Typ práce</span><span class="sxs-lookup"><span data-stu-id="0a057-548">Job type</span></span>   | <span data-ttu-id="0a057-549">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0a057-550">Hodinově</span><span class="sxs-lookup"><span data-stu-id="0a057-550">Hourly</span></span>     | <span data-ttu-id="0a057-551">MX hodinově</span><span class="sxs-lookup"><span data-stu-id="0a057-551">MX Hourly</span></span>   |
| <span data-ttu-id="0a057-552">Stálý plat</span><span class="sxs-lookup"><span data-stu-id="0a057-552">Salaried</span></span>   | <span data-ttu-id="0a057-553">MX Stálý plat</span><span class="sxs-lookup"><span data-stu-id="0a057-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="0a057-554">Typy pozic</span><span class="sxs-lookup"><span data-stu-id="0a057-554">Position types</span></span> 

<span data-ttu-id="0a057-555">Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná.</span><span class="sxs-lookup"><span data-stu-id="0a057-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0a057-556">Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="0a057-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0a057-557">Následující typy pozic a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0a057-558">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="0a057-558">Position type</span></span>   | <span data-ttu-id="0a057-559">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0a057-560">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-560">Full-time</span></span>       | <span data-ttu-id="0a057-561">Zaměstnanec na plný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-561">Full time employee</span></span> |
| <span data-ttu-id="0a057-562">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-562">Part-time</span></span>       | <span data-ttu-id="0a057-563">Zaměstnanec na částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="0a057-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0a057-564">Kódy důvodu</span><span class="sxs-lookup"><span data-stu-id="0a057-564">Reason codes</span></span>

<span data-ttu-id="0a057-565">Kódy důvodů poskytují informace o stavu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0a057-566">Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a057-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0a057-567">Následující kódy důvodů a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0a057-568">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="0a057-568">Reason code</span></span>            | <span data-ttu-id="0a057-569">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-569">Description</span></span>                    | <span data-ttu-id="0a057-570">Použitelné scénáře</span><span class="sxs-lookup"><span data-stu-id="0a057-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="0a057-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="0a057-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="0a057-572">Odchod před první mzdou</span><span class="sxs-lookup"><span data-stu-id="0a057-572">Departure before first payroll</span></span> | <span data-ttu-id="0a057-573">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-573">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0a057-574">RESIGNATION</span></span>            | <span data-ttu-id="0a057-575">Výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-575">Resignation</span></span>                    | <span data-ttu-id="0a057-576">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-576">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="0a057-577">PENSION</span></span>                | <span data-ttu-id="0a057-578">Důchod</span><span class="sxs-lookup"><span data-stu-id="0a057-578">Pension</span></span>                        | <span data-ttu-id="0a057-579">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-579">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0a057-580">TERMINATION</span></span>            | <span data-ttu-id="0a057-581">Ukončení</span><span class="sxs-lookup"><span data-stu-id="0a057-581">Termination</span></span>                    | <span data-ttu-id="0a057-582">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-582">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0a057-583">RETIREMENT</span></span>             | <span data-ttu-id="0a057-584">Důchod</span><span class="sxs-lookup"><span data-stu-id="0a057-584">Retirement</span></span>                     | <span data-ttu-id="0a057-585">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-585">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="0a057-586">ABSENTEE</span></span>               | <span data-ttu-id="0a057-587">Nepřítomný</span><span class="sxs-lookup"><span data-stu-id="0a057-587">Absentee</span></span>                       | <span data-ttu-id="0a057-588">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-588">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-589">JINÝ</span><span class="sxs-lookup"><span data-stu-id="0a057-589">OTHER</span></span>                  | <span data-ttu-id="0a057-590">Jiné důvody</span><span class="sxs-lookup"><span data-stu-id="0a057-590">Other Reasons</span></span>                  | <span data-ttu-id="0a057-591">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-591">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="0a057-592">CLOSURE</span></span>                | <span data-ttu-id="0a057-593">Obchodní uzávěrka</span><span class="sxs-lookup"><span data-stu-id="0a057-593">Business Closure</span></span>               | <span data-ttu-id="0a057-594">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-594">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="0a057-595">DEATH</span></span>                  | <span data-ttu-id="0a057-596">Úmrtí</span><span class="sxs-lookup"><span data-stu-id="0a057-596">Death</span></span>                          | <span data-ttu-id="0a057-597">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-597">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0a057-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="0a057-599">Dovolená</span><span class="sxs-lookup"><span data-stu-id="0a057-599">Leave of Absence</span></span>               | <span data-ttu-id="0a057-600">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-600">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0a057-601">CONTRACTEND</span></span>            | <span data-ttu-id="0a057-602">Konec smlouvy</span><span class="sxs-lookup"><span data-stu-id="0a057-602">End of Contract</span></span>                | <span data-ttu-id="0a057-603">Dát pracovníkovi výpověď</span><span class="sxs-lookup"><span data-stu-id="0a057-603">Terminate worker</span></span>     |
| <span data-ttu-id="0a057-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a057-604">SALARYCHANGE</span></span>           | <span data-ttu-id="0a057-605">Změna platu</span><span class="sxs-lookup"><span data-stu-id="0a057-605">Change of Salary</span></span>               | <span data-ttu-id="0a057-606">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a057-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="0a057-607">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-607">Terms of employment</span></span>

<span data-ttu-id="0a057-608">Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a057-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="0a057-609">Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a057-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="0a057-610">Následující podmínky zaměstnání a popisy jsou povinné.</span><span class="sxs-lookup"><span data-stu-id="0a057-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="0a057-611">Podmínky zaměstnání</span><span class="sxs-lookup"><span data-stu-id="0a057-611">Terms of employment</span></span>   | <span data-ttu-id="0a057-612">popis</span><span class="sxs-lookup"><span data-stu-id="0a057-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="0a057-613">Řádné</span><span class="sxs-lookup"><span data-stu-id="0a057-613">Regular</span></span>               | <span data-ttu-id="0a057-614">Řádné</span><span class="sxs-lookup"><span data-stu-id="0a057-614">Regular</span></span>     |
| <span data-ttu-id="0a057-615">Přímo</span><span class="sxs-lookup"><span data-stu-id="0a057-615">Direct</span></span>                | <span data-ttu-id="0a057-616">Přímo</span><span class="sxs-lookup"><span data-stu-id="0a057-616">Direct</span></span>      |
| <span data-ttu-id="0a057-617">Stáž</span><span class="sxs-lookup"><span data-stu-id="0a057-617">Internship</span></span>            | <span data-ttu-id="0a057-618">Stáž</span><span class="sxs-lookup"><span data-stu-id="0a057-618">Internship</span></span>  |
| <span data-ttu-id="0a057-619">Trvalé</span><span class="sxs-lookup"><span data-stu-id="0a057-619">Permanent</span></span>             | <span data-ttu-id="0a057-620">Trvalé</span><span class="sxs-lookup"><span data-stu-id="0a057-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="0a057-621">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="0a057-621">Marital status</span></span>

<span data-ttu-id="0a057-622">Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a057-623">Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a057-624">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-624">Talent</span></span>                 | <span data-ttu-id="0a057-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="0a057-626">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="0a057-626">Married</span></span>                | <span data-ttu-id="0a057-627">Ženatý/vdaná</span><span class="sxs-lookup"><span data-stu-id="0a057-627">Married</span></span>                   |
| <span data-ttu-id="0a057-628">Jedno</span><span class="sxs-lookup"><span data-stu-id="0a057-628">Single</span></span>                 | <span data-ttu-id="0a057-629">Jedno</span><span class="sxs-lookup"><span data-stu-id="0a057-629">Single</span></span>                    |
| <span data-ttu-id="0a057-630">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="0a057-630">Widowed</span></span>                | <span data-ttu-id="0a057-631">Vdovec/vdova</span><span class="sxs-lookup"><span data-stu-id="0a057-631">Widowed</span></span>                   |
| <span data-ttu-id="0a057-632">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="0a057-632">Divorced</span></span>               | <span data-ttu-id="0a057-633">Rozvedený/rozvedená</span><span class="sxs-lookup"><span data-stu-id="0a057-633">Divorced</span></span>                  |
| <span data-ttu-id="0a057-634">Registrované partnerství</span><span class="sxs-lookup"><span data-stu-id="0a057-634">Registered Partnership</span></span> | <span data-ttu-id="0a057-635">Domácí partnerství</span><span class="sxs-lookup"><span data-stu-id="0a057-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="0a057-636">None</span><span class="sxs-lookup"><span data-stu-id="0a057-636">None</span></span>                   | <span data-ttu-id="0a057-637">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a057-638">Společná domácnost</span><span class="sxs-lookup"><span data-stu-id="0a057-638">Cohabiting</span></span>             | <span data-ttu-id="0a057-639">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="0a057-640">Rod</span><span class="sxs-lookup"><span data-stu-id="0a057-640">Gender</span></span>

<span data-ttu-id="0a057-641">Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a057-642">Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a057-643">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-643">Talent</span></span>       | <span data-ttu-id="0a057-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="0a057-645">Muž</span><span class="sxs-lookup"><span data-stu-id="0a057-645">Male</span></span>         | <span data-ttu-id="0a057-646">Muž</span><span class="sxs-lookup"><span data-stu-id="0a057-646">Male</span></span>                      |
| <span data-ttu-id="0a057-647">Žena</span><span class="sxs-lookup"><span data-stu-id="0a057-647">Female</span></span>       | <span data-ttu-id="0a057-648">Žena</span><span class="sxs-lookup"><span data-stu-id="0a057-648">Female</span></span>                    |
| <span data-ttu-id="0a057-649">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="0a057-649">Non-specific</span></span> | <span data-ttu-id="0a057-650">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="0a057-651">Způsob platby</span><span class="sxs-lookup"><span data-stu-id="0a057-651">Payment method</span></span>

<span data-ttu-id="0a057-652">Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="0a057-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="0a057-653">Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a057-654">Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a057-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a057-655">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-655">Talent</span></span>             | <span data-ttu-id="0a057-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="0a057-657">Hotovost</span><span class="sxs-lookup"><span data-stu-id="0a057-657">Cash</span></span>               | <span data-ttu-id="0a057-658">Hotovost</span><span class="sxs-lookup"><span data-stu-id="0a057-658">Cash</span></span>                      |
| <span data-ttu-id="0a057-659">Elektronická platba</span><span class="sxs-lookup"><span data-stu-id="0a057-659">Electronic Payment</span></span> | <span data-ttu-id="0a057-660">Převod</span><span class="sxs-lookup"><span data-stu-id="0a057-660">Transfer</span></span>                  |
| <span data-ttu-id="0a057-661">Kontrola</span><span class="sxs-lookup"><span data-stu-id="0a057-661">Check</span></span>              | <span data-ttu-id="0a057-662">Šek</span><span class="sxs-lookup"><span data-stu-id="0a057-662">Cheque</span></span>                    |
| <span data-ttu-id="0a057-663">Bankovní směnka</span><span class="sxs-lookup"><span data-stu-id="0a057-663">Bank Draft</span></span>         | <span data-ttu-id="0a057-664">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a057-665">Další</span><span class="sxs-lookup"><span data-stu-id="0a057-665">Other</span></span>              | <span data-ttu-id="0a057-666">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="0a057-667">Typ bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="0a057-667">Bank account type</span></span>

<span data-ttu-id="0a057-668">Typy bankovního účtu se používají pro elektronické platby zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="0a057-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="0a057-669">Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu.</span><span class="sxs-lookup"><span data-stu-id="0a057-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="0a057-670">Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.</span><span class="sxs-lookup"><span data-stu-id="0a057-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="0a057-671">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-671">Talent</span></span>            | <span data-ttu-id="0a057-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="0a057-673">Běžný účet</span><span class="sxs-lookup"><span data-stu-id="0a057-673">Checking Account</span></span>  | <span data-ttu-id="0a057-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="0a057-674">CheckingAccount</span></span>           |
| <span data-ttu-id="0a057-675">Mzdový účet</span><span class="sxs-lookup"><span data-stu-id="0a057-675">Payroll Account</span></span>   | <span data-ttu-id="0a057-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="0a057-676">PayrollAccount</span></span>            |
| <span data-ttu-id="0a057-677">Spořicí účet</span><span class="sxs-lookup"><span data-stu-id="0a057-677">Savings Account</span></span>   | <span data-ttu-id="0a057-678">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a057-679">BankGirot účet</span><span class="sxs-lookup"><span data-stu-id="0a057-679">BankGirot account</span></span> | <span data-ttu-id="0a057-680">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a057-681">PlusGirot účet</span><span class="sxs-lookup"><span data-stu-id="0a057-681">PlusGirot account</span></span> | <span data-ttu-id="0a057-682">*Nepodporováno v Mexiku*</span><span class="sxs-lookup"><span data-stu-id="0a057-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0a057-683">Kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="0a057-683">Earning codes</span></span>

<span data-ttu-id="0a057-684">Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají.</span><span class="sxs-lookup"><span data-stu-id="0a057-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a057-685">Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.</span><span class="sxs-lookup"><span data-stu-id="0a057-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0a057-686">Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.</span><span class="sxs-lookup"><span data-stu-id="0a057-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0a057-687">Podporované intervaly</span><span class="sxs-lookup"><span data-stu-id="0a057-687">Supported frequencies</span></span>

- <span data-ttu-id="0a057-688">Všechna</span><span class="sxs-lookup"><span data-stu-id="0a057-688">All</span></span>
- <span data-ttu-id="0a057-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0a057-689">EVERYPAY</span></span>
- <span data-ttu-id="0a057-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0a057-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0a057-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0a057-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0a057-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0a057-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0a057-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-693">1OFMTH</span></span>
- <span data-ttu-id="0a057-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-694">LASTOFMTH</span></span>
- <span data-ttu-id="0a057-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-695">2OFMTH</span></span>
- <span data-ttu-id="0a057-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-696">3OFMTH</span></span>
- <span data-ttu-id="0a057-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-697">4OFMTH</span></span>
- <span data-ttu-id="0a057-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-698">5OFMTH</span></span>
- <span data-ttu-id="0a057-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-699">1N2OFMTH</span></span>
- <span data-ttu-id="0a057-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-700">3N4OFMTH</span></span>
- <span data-ttu-id="0a057-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-701">1N3OFMTH</span></span>
- <span data-ttu-id="0a057-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-702">1N4OFMTH</span></span>
- <span data-ttu-id="0a057-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-703">2N3OFMTH</span></span>
- <span data-ttu-id="0a057-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-704">2N4OFMTH</span></span>
- <span data-ttu-id="0a057-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="0a057-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="0a057-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a057-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0a057-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0a057-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0a057-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0a057-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0a057-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a057-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0a057-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0a057-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0a057-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a057-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0a057-717">Adresy</span><span class="sxs-lookup"><span data-stu-id="0a057-717">Addresses</span></span>

<span data-ttu-id="0a057-718">Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat.</span><span class="sxs-lookup"><span data-stu-id="0a057-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0a057-719">Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.</span><span class="sxs-lookup"><span data-stu-id="0a057-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0a057-720">Talent</span><span class="sxs-lookup"><span data-stu-id="0a057-720">Talent</span></span>              | <span data-ttu-id="0a057-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a057-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="0a057-722">Země nebo oblast</span><span class="sxs-lookup"><span data-stu-id="0a057-722">Country/Region</span></span>      | <span data-ttu-id="0a057-723">Kód země</span><span class="sxs-lookup"><span data-stu-id="0a057-723">Country Code</span></span>          |
| <span data-ttu-id="0a057-724">PSČ</span><span class="sxs-lookup"><span data-stu-id="0a057-724">Zip/Postal Code</span></span>     | <span data-ttu-id="0a057-725">PSČ</span><span class="sxs-lookup"><span data-stu-id="0a057-725">Postal Code</span></span>           |
| <span data-ttu-id="0a057-726">Kraj</span><span class="sxs-lookup"><span data-stu-id="0a057-726">State</span></span>               | <span data-ttu-id="0a057-727">Kód státu</span><span class="sxs-lookup"><span data-stu-id="0a057-727">State Code</span></span>            |
| <span data-ttu-id="0a057-728">Město</span><span class="sxs-lookup"><span data-stu-id="0a057-728">City</span></span>                | <span data-ttu-id="0a057-729">Město</span><span class="sxs-lookup"><span data-stu-id="0a057-729">City</span></span>                  |
| <span data-ttu-id="0a057-730">Okres</span><span class="sxs-lookup"><span data-stu-id="0a057-730">County</span></span>              | <span data-ttu-id="0a057-731">Okres</span><span class="sxs-lookup"><span data-stu-id="0a057-731">County (Municipality)</span></span> |
| <span data-ttu-id="0a057-732">Ulice</span><span class="sxs-lookup"><span data-stu-id="0a057-732">Street</span></span>              | <span data-ttu-id="0a057-733">Řádek adresy 1</span><span class="sxs-lookup"><span data-stu-id="0a057-733">Address Line 1</span></span>        |
| <span data-ttu-id="0a057-734">Číslo popisné</span><span class="sxs-lookup"><span data-stu-id="0a057-734">Street Number</span></span>       | <span data-ttu-id="0a057-735">Řádek adresy 2</span><span class="sxs-lookup"><span data-stu-id="0a057-735">Address Line 2</span></span>        |
| <span data-ttu-id="0a057-736">Doplňující název budovy</span><span class="sxs-lookup"><span data-stu-id="0a057-736">Building Complement</span></span> | <span data-ttu-id="0a057-737">Řádek adresy 5</span><span class="sxs-lookup"><span data-stu-id="0a057-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="0a057-738">Číslo cestovního pasu</span><span class="sxs-lookup"><span data-stu-id="0a057-738">Passport number</span></span>

<span data-ttu-id="0a057-739">Zaměstnanci mohou deklarovat informace o cestovním pasu.</span><span class="sxs-lookup"><span data-stu-id="0a057-739">Employees can declare passport information.</span></span> <span data-ttu-id="0a057-740">Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.</span><span class="sxs-lookup"><span data-stu-id="0a057-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="0a057-741">Typ identifikace = Pas</span><span class="sxs-lookup"><span data-stu-id="0a057-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="0a057-742">Datum vydání</span><span class="sxs-lookup"><span data-stu-id="0a057-742">Issued Date</span></span>
- <span data-ttu-id="0a057-743">Datum vypršení platnosti</span><span class="sxs-lookup"><span data-stu-id="0a057-743">Expiration Date</span></span>

<span data-ttu-id="0a057-744">Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**.</span><span class="sxs-lookup"><span data-stu-id="0a057-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="0a057-745">Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu.</span><span class="sxs-lookup"><span data-stu-id="0a057-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="0a057-746">Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.</span><span class="sxs-lookup"><span data-stu-id="0a057-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

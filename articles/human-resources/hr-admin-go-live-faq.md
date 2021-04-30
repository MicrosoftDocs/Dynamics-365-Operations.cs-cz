---
title: Často kladené dotazy týkající se ostrého nasazení
description: Toto téma uvádí často kladené otázky o tom, jak převést projekt implementace Dynamics 365 Human Resources do živého provozu.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892316"
---
# <a name="go-live-faq"></a><span data-ttu-id="4848f-103">Často kladené dotazy týkající se ostrého nasazení</span><span class="sxs-lookup"><span data-stu-id="4848f-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4848f-104">Toto téma uvádí často kladené otázky o tom, jak převést projekt implementace Dynamics 365 Human Resources do živého provozu.</span><span class="sxs-lookup"><span data-stu-id="4848f-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="4848f-105">Kdy mohu nakonfigurovat a požádat o své provozní prostředí?</span><span class="sxs-lookup"><span data-stu-id="4848f-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="4848f-106">Provozní prostředí je obvykle nasazeno po splnění následujících kritérií:</span><span class="sxs-lookup"><span data-stu-id="4848f-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="4848f-107">Všechna přizpůsobení jsou kompletní.</span><span class="sxs-lookup"><span data-stu-id="4848f-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="4848f-108">Uživatelské akceptační testování (UAT) je dokončeno.</span><span class="sxs-lookup"><span data-stu-id="4848f-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="4848f-109">Zákazník se odhlásil od řešení.</span><span class="sxs-lookup"><span data-stu-id="4848f-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="4848f-110">Pro spuštění nejsou žádné problémy s blokováním.</span><span class="sxs-lookup"><span data-stu-id="4848f-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="4848f-111">Pokud jsou v této fázi kvalifikovaní zákazníci, tým Microsoft FastTrack bude spolupracovat s projektovým týmem, aby provedli test naživo.</span><span class="sxs-lookup"><span data-stu-id="4848f-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="4848f-112">Jaké jsou předpoklady pro nasazení produkčního prostředí?</span><span class="sxs-lookup"><span data-stu-id="4848f-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="4848f-113">Seznam předpokladů najdete v části  [Připravte se na přechod do živého provozu](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="4848f-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="4848f-114">Co je to test naživo?</span><span class="sxs-lookup"><span data-stu-id="4848f-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="4848f-115">Test naživo je součástí  [Programu Microsoft FastTrack](/dynamics365/fasttrack/).</span><span class="sxs-lookup"><span data-stu-id="4848f-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="4848f-116">Během této kontroly architekt řešení posoudí, zda je implementační projekt připraven na úspěšné vyjmutí a spuštění.</span><span class="sxs-lookup"><span data-stu-id="4848f-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="4848f-117">Tato kontrola je povinná pro každý implementační projekt, než budete moci požádat o uvedení do provozu v produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="4848f-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="4848f-118">Naše prostředí Sandbox jsou nasazena v datovém centru ve střední USA.</span><span class="sxs-lookup"><span data-stu-id="4848f-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="4848f-119">Chceme, aby naše produkční prostředí byla nasazena v datovém centru na západě USA.</span><span class="sxs-lookup"><span data-stu-id="4848f-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="4848f-120">Mohu ve své produkční konfiguraci vybrat jako datové centrum Západ USA?</span><span class="sxs-lookup"><span data-stu-id="4848f-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="4848f-121">LCS vás neomezuje ve výběru jiného datového centra při nasazení prostředí lidských zdrojů, ale důrazně doporučujeme nevybírat jiné datové centrum.</span><span class="sxs-lookup"><span data-stu-id="4848f-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="4848f-122">Pokud chcete, aby se vaše produkční prostředí nacházelo v západoamerickém datovém centru, měli byste nejprve znovu nasadit prostředí sandboxu do západoamerického datového centra, otestovat je a odhlásit se.</span><span class="sxs-lookup"><span data-stu-id="4848f-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="4848f-123">Informace o výběru správného datového centra najdete v části [Síťové požadavky](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="4848f-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="4848f-124">Jakou úroveň přístupu mám k prostředkům Azure pro mé prostředí lidských zdrojů?</span><span class="sxs-lookup"><span data-stu-id="4848f-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="4848f-125">Přístup do prostředí lidských zdrojů je omezený.</span><span class="sxs-lookup"><span data-stu-id="4848f-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="4848f-126">Nelze získat přístup k virtuálnímu počítači (VM) nebo Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="4848f-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="4848f-127">Také nemůžete získat přístup k databázi prostřednictvím Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="4848f-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="4848f-128">I když nemůžete získat přístup ke svým prostředkům Azure nebo prostředí Dynamics 365 Human Resources přímo, existují další funkce, které můžete použít pro přístup k vašim datům:</span><span class="sxs-lookup"><span data-stu-id="4848f-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="4848f-129">Můžete nasadit databázi Azure SQL ve vašem vlastním klientovi Azure a k synchronizaci dat použít funkci Bring Your Own Database (BYOD).</span><span class="sxs-lookup"><span data-stu-id="4848f-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="4848f-130">Další informace viz [Použití vlastní databáze (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="4848f-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="4848f-131">Můžete použít integraci Dataverse pro synchronizaci vybraných entit s databází Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4848f-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="4848f-132">Další informace naleznete v části [Tabulky Dataverse](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="4848f-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="4848f-133">Jak často je moje produkční databáze zálohována?</span><span class="sxs-lookup"><span data-stu-id="4848f-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="4848f-134">Databáze jsou chráněny automatickým zálohováním na následujících frekvencích:</span><span class="sxs-lookup"><span data-stu-id="4848f-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="4848f-135">Typ zálohy</span><span class="sxs-lookup"><span data-stu-id="4848f-135">Type of backup</span></span> | <span data-ttu-id="4848f-136">Četnost</span><span class="sxs-lookup"><span data-stu-id="4848f-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="4848f-137">Úplná záloha databáze</span><span class="sxs-lookup"><span data-stu-id="4848f-137">Full database backup</span></span> | <span data-ttu-id="4848f-138">Týdně</span><span class="sxs-lookup"><span data-stu-id="4848f-138">Weekly</span></span> |
| <span data-ttu-id="4848f-139">Rozdílová záloha databáze</span><span class="sxs-lookup"><span data-stu-id="4848f-139">Differential database backup</span></span> | <span data-ttu-id="4848f-140">Každých 12-24 hodin</span><span class="sxs-lookup"><span data-stu-id="4848f-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="4848f-141">Záloha protokolu transakcí</span><span class="sxs-lookup"><span data-stu-id="4848f-141">Transaction log backup</span></span> | <span data-ttu-id="4848f-142">Každých 5 až 10 minut</span><span class="sxs-lookup"><span data-stu-id="4848f-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="4848f-143">Microsoft si ponechává dostatečné zálohy, aby umožnil Point in Time Restore (PITR) během posledních 14 dnů.</span><span class="sxs-lookup"><span data-stu-id="4848f-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="4848f-144">Další informace naleznete v tématu  [Další informace týkající se automatické zálohy databáze SQL](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="4848f-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="4848f-145">Mohu požádat o kopii zálohy mé produkční databáze?</span><span class="sxs-lookup"><span data-stu-id="4848f-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="4848f-146">Č.</span><span class="sxs-lookup"><span data-stu-id="4848f-146">No.</span></span> <span data-ttu-id="4848f-147">Můžete však odeslat požadavek na aktualizaci databáze, abyste zkopírovali produkční prostředí do prostředí Sandbox.</span><span class="sxs-lookup"><span data-stu-id="4848f-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="4848f-148">Můžete nasadit databázi Azure SQL ve vašem vlastním klientovi Azure a k synchronizaci dat použít funkci BYOD z vašeho provozního prostředí.</span><span class="sxs-lookup"><span data-stu-id="4848f-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="4848f-149">Další informace viz [Použití vlastní databáze (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="4848f-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="4848f-150">Jak přesunu své prostředí Sandbox do produkce pro spuštění?</span><span class="sxs-lookup"><span data-stu-id="4848f-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="4848f-151">Protože funkce kopírování není k dispozici pro přesun vašeho prostředí ze Sandbox do produkčního prostředí, musíte k přesunu dat do produkčního prostředí použít datové balíčky.</span><span class="sxs-lookup"><span data-stu-id="4848f-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="4848f-152">Během celého projektu doporučujeme udržovat jasný seznam entit nakonfigurovaných ve vašem sandboxu.</span><span class="sxs-lookup"><span data-stu-id="4848f-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="4848f-153">Poté otestujte proces vyjmutí a migrace veškerých datových balíčků potřebných k uvedení do provozu.</span><span class="sxs-lookup"><span data-stu-id="4848f-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="4848f-154">Až budete připraveni k provozu, musíte ručně přesunout všechny datové balíčky do produkčního prostředí.</span><span class="sxs-lookup"><span data-stu-id="4848f-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="4848f-155">Co mám dělat, když je moje produkční prostředí nefunkční?</span><span class="sxs-lookup"><span data-stu-id="4848f-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="4848f-156">Chcete-li nahlásit výpadek produkčního prostředí, postupujte podle postupu popsaného v [Nahlásit výpadek produkce](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span><span class="sxs-lookup"><span data-stu-id="4848f-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="4848f-157">Viz také</span><span class="sxs-lookup"><span data-stu-id="4848f-157">See also</span></span>

 [<span data-ttu-id="4848f-158">Příprava pro ostré nasazení</span><span class="sxs-lookup"><span data-stu-id="4848f-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
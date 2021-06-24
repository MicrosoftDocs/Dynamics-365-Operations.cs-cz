---
title: Požadavky nastavení velikosti hardwaru pro místní prostředí
description: Toto téma uvádí požadavky nastavení velikosti hardwaru pro místní prostředí.
author: sericks007
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 1ef427ff57c79b64a2435edd902e09a7d99e81d9
ms.sourcegitcommit: 4a508bd11267f24eeb774af57faa56369beacf51
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2021
ms.locfileid: "6168722"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="e5b11-103">Požadavky nastavení velikosti hardwaru pro místní prostředí</span><span class="sxs-lookup"><span data-stu-id="e5b11-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5b11-104">Než zahájíte proces nastavení velikosti hardwaru a infrastruktury pro místní prostředí, seznamte se s informacemi z témat [Požadavky na systém pro nasazení v cloudu](system-requirements.md) a [Pokyny k nastavení a nasazení](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), abyste dobře rozuměli základní infrastruktuře.</span><span class="sxs-lookup"><span data-stu-id="e5b11-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="e5b11-105">Věnujte velkou pozornost doporučeným postupům nastavení systému pro dosažení optimálního výkonu.</span><span class="sxs-lookup"><span data-stu-id="e5b11-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="e5b11-106">Po kontrole dokumentace můžete zahájit proces odhadu transakčních a souběžných uživatelských objemů a nastavení velikosti prostředí na základě průměrné základní propustnosti.</span><span class="sxs-lookup"><span data-stu-id="e5b11-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="e5b11-107">Koeficienty, které ovlivňují nastavení velikosti</span><span class="sxs-lookup"><span data-stu-id="e5b11-107">Factors that affect sizing</span></span>

<span data-ttu-id="e5b11-108">Všechny faktory na následujícím obrázku přispívají k nastavení velikosti.</span><span class="sxs-lookup"><span data-stu-id="e5b11-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="e5b11-109">Čím podrobnější informace jsou shromážděny tím přesnější nastavení velikosti můžete určit.</span><span class="sxs-lookup"><span data-stu-id="e5b11-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="e5b11-110">Nastavení velikosti hardwaru bez podpůrných dat bude pravděpodobně nepřesné.</span><span class="sxs-lookup"><span data-stu-id="e5b11-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="e5b11-111">Minimální absolutní požadavek na potřebná data nejvyšší vytížení řádku transakce za hodinu.</span><span class="sxs-lookup"><span data-stu-id="e5b11-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="e5b11-112">[![Nastavení velikosti hardwaru pro místní prostředí](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="e5b11-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="e5b11-113">Při pohledu zleva doprava je prvním a nejdůležitějším faktorem potřebným pro přesný odhad nastavení velikosti profil transakce nebo charakteristika transakce.</span><span class="sxs-lookup"><span data-stu-id="e5b11-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="e5b11-114">Je důležité vždy najít maximální objem transakcí za hodinu.</span><span class="sxs-lookup"><span data-stu-id="e5b11-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="e5b11-115">Pokud existuje více vrcholných období, je nutné tato období přesně definovat.</span><span class="sxs-lookup"><span data-stu-id="e5b11-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="e5b11-116">Tak, jako rozumíte vytížení, které ovlivňuje infrastrukturu, bude nutné pochopit další podrobnosti o těchto faktorech:</span><span class="sxs-lookup"><span data-stu-id="e5b11-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="e5b11-117">**Transakce** -- obvykle transakce mají během dne nebo týdne určité špičky.</span><span class="sxs-lookup"><span data-stu-id="e5b11-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="e5b11-118">Většinou to závisí na typu transakce.</span><span class="sxs-lookup"><span data-stu-id="e5b11-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="e5b11-119">Záznamy o čase a výdajích obvykle zobrazují největší vytížení jednou za týden, zatímco záznamy prodejní objednávky jsou často hromadné kvůli integraci nebo během dne poklesnou.</span><span class="sxs-lookup"><span data-stu-id="e5b11-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="e5b11-120">**Počet souběžných uživatelů** – číslo souběžných je druhý nejdůležitější koeficient pro změnu velikosti.</span><span class="sxs-lookup"><span data-stu-id="e5b11-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="e5b11-121">Nelze spolehlivě získat odhady velikosti na základě počtu souběžných uživatelů, takže pokud to je jediný údaj, který máte k dispozici, odhadněte přibližný počet a znovu ho zkontrolujte, když máte více údajů.</span><span class="sxs-lookup"><span data-stu-id="e5b11-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="e5b11-122">Definice přesného počtu souběžných uživatelů znamená, že:</span><span class="sxs-lookup"><span data-stu-id="e5b11-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="e5b11-123">Jmenovaní uživatele nejsou souběžní uživatelé.</span><span class="sxs-lookup"><span data-stu-id="e5b11-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="e5b11-124">Souběžní uživatelé jsou vždy podmnožinou jmenovaných uživatelů.</span><span class="sxs-lookup"><span data-stu-id="e5b11-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="e5b11-125">Vrcholné pracovní vytížení definuje maximální souběžnost pro třídění.</span><span class="sxs-lookup"><span data-stu-id="e5b11-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="e5b11-126">Kritéria souběžných uživatelů znamenají, že uživatel splňuje všechna následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="e5b11-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="e5b11-127">Přihlášený.</span><span class="sxs-lookup"><span data-stu-id="e5b11-127">Logged on.</span></span>
    - <span data-ttu-id="e5b11-128">Pracovní transakce/dotazy v době výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e5b11-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="e5b11-129">Není nečinná relace.</span><span class="sxs-lookup"><span data-stu-id="e5b11-129">Not an idle session.</span></span>

- <span data-ttu-id="e5b11-130">**Složení dat** – jedná se většinou o způsob nastavení a konfigurace vašeho systému.</span><span class="sxs-lookup"><span data-stu-id="e5b11-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="e5b11-131">Například počet právnických osob, které máte, kolik položek, počet úrovní kusovníku a jak komplexní bude nastavení zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="e5b11-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="e5b11-132">Každý z těchto faktorů může mít malý vliv na výkon, takže lze tyto faktory vyrovnat pomocí inteligentních voleb z hlediska infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e5b11-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="e5b11-133">**Rozšíření** – přizpůsobení může být jednoduché, nebo komplexní.</span><span class="sxs-lookup"><span data-stu-id="e5b11-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="e5b11-134">Počet úprav a složitost a má odlišný dopad na velikost potřebné infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e5b11-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="e5b11-135">Pro komplexní přizpůsobení je doporučeno provést vyhodnocení výkonu pro zajištění, že nejsou pouze testovány s ohledem na účinnosti, ale také porozumět tomu, jaké jsou potřeby infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e5b11-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="e5b11-136">To je ještě důležitější, pokud nejsou rozšíření kódovaná podle doporučených postupů pro výkon a škálovatelnost.</span><span class="sxs-lookup"><span data-stu-id="e5b11-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="e5b11-137">**Vykazování a analýzy** – tyto koeficienty obvykle obsahují provádění náročných dotazů proti různým databázím v systému.</span><span class="sxs-lookup"><span data-stu-id="e5b11-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="e5b11-138">Princip a snížení četnosti při spouštění sestav výdajů vám pomůže pochopit jejich dopady.</span><span class="sxs-lookup"><span data-stu-id="e5b11-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="e5b11-139">**Řešení třetí strany** – tato řešení jako ISV, mají stejné důsledky a doporučení jako rozšíření.</span><span class="sxs-lookup"><span data-stu-id="e5b11-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="e5b11-140">Změna velikosti prostředí</span><span class="sxs-lookup"><span data-stu-id="e5b11-140">Sizing your environment</span></span>

<span data-ttu-id="e5b11-141">Abyste mohli porozumět požadavkům nastavení velikosti, je nutné znát maximální objem transakcí, které je nutné zpracovat.</span><span class="sxs-lookup"><span data-stu-id="e5b11-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="e5b11-142">Většina pomocných systémů jako Management Reporter nebo SSRS je méně náročných.</span><span class="sxs-lookup"><span data-stu-id="e5b11-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="e5b11-143">Tento dokument se proto zaměřuje většinou na server AOS a SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5b11-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="e5b11-144">Obecně se vrstvy výpočtu škálují a je třeba nastavit je způsobem N+1, tj. pokud vytvoříte odhad tři AOS, přidejte čtvrtou AOS.</span><span class="sxs-lookup"><span data-stu-id="e5b11-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="e5b11-145">Úrovně databáze by měly být nastaveny ve vždy snadno dostupném nastavení.</span><span class="sxs-lookup"><span data-stu-id="e5b11-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="e5b11-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="e5b11-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="e5b11-147">Nastavení velikosti</span><span class="sxs-lookup"><span data-stu-id="e5b11-147">Sizing</span></span>

- <span data-ttu-id="e5b11-148">Řádky transakce 3K až 15K za hodinu na základní databázový server.</span><span class="sxs-lookup"><span data-stu-id="e5b11-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="e5b11-149">Typický poměr AOS-to-SQL 3:1 pro primární SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5b11-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="e5b11-150">Další jádra jsou nutná podle zvolené dostupnost konfigurace.</span><span class="sxs-lookup"><span data-stu-id="e5b11-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="e5b11-151">Zpracování náročných databázových operací může vrátit 2:1.</span><span class="sxs-lookup"><span data-stu-id="e5b11-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="e5b11-152">Odchylky ovlivňují následující faktory:</span><span class="sxs-lookup"><span data-stu-id="e5b11-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="e5b11-153">Používané nastavení parametru.</span><span class="sxs-lookup"><span data-stu-id="e5b11-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="e5b11-154">Úrovně rozšíření</span><span class="sxs-lookup"><span data-stu-id="e5b11-154">Levels of extensions.</span></span>
    - <span data-ttu-id="e5b11-155">Použití dalších funkcí, jako jsou například výstrahy a protokol databáze.</span><span class="sxs-lookup"><span data-stu-id="e5b11-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="e5b11-156">Protokolování databáze dále sníží propustnost za hodinu na základ pod 3K řádky.</span><span class="sxs-lookup"><span data-stu-id="e5b11-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="e5b11-157">Složitost složení dat – jednoduchá účtová osnova vs. podrobná účtová osnova má vliv na propustnost (jako příklad).</span><span class="sxs-lookup"><span data-stu-id="e5b11-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="e5b11-158">Popis transakce.</span><span class="sxs-lookup"><span data-stu-id="e5b11-158">Transaction characterization.</span></span>
    - <span data-ttu-id="e5b11-159">2 GB paměti na 16 GB pro každé jádro.</span><span class="sxs-lookup"><span data-stu-id="e5b11-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="e5b11-160">Pomocné databáze na Databázovm serveru, jako je například SSRS databáze a aplikace Management reporter.</span><span class="sxs-lookup"><span data-stu-id="e5b11-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="e5b11-161">Dočasné databáze = počet souborů jako fyzických procesorů 15 % velikosti databáze.</span><span class="sxs-lookup"><span data-stu-id="e5b11-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="e5b11-162">Velikost SAN a propustnosti na základě celkové objemu/použití souběžných transakce.</span><span class="sxs-lookup"><span data-stu-id="e5b11-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="e5b11-163">Vysoká dostupnost</span><span class="sxs-lookup"><span data-stu-id="e5b11-163">High availability</span></span>

<span data-ttu-id="e5b11-164">Doporučujeme vždy využít serveru SQL Server v jednom seskupení nebo zrcadlení nastavení.</span><span class="sxs-lookup"><span data-stu-id="e5b11-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="e5b11-165">Druhý uzel SQL by měl mít stejný počet jader jako primární.</span><span class="sxs-lookup"><span data-stu-id="e5b11-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="e5b11-166">Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="e5b11-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="e5b11-167">Nastavení velikosti AD FS je popsáno v tématu [Dokumentace kapacity serveru AD FS](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="e5b11-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="e5b11-168">[Tabulka třídění](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) je k dispozici pro plánování počtu instancí v nasazení.</span><span class="sxs-lookup"><span data-stu-id="e5b11-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="e5b11-169">Server AOS (Online a dávka)</span><span class="sxs-lookup"><span data-stu-id="e5b11-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="e5b11-170">Nastavení velikosti</span><span class="sxs-lookup"><span data-stu-id="e5b11-170">Sizing</span></span>

- <span data-ttu-id="e5b11-171">Nastavení velikosti podle objemu nebo použití transakce</span><span class="sxs-lookup"><span data-stu-id="e5b11-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="e5b11-172">2K až 6K řádek na jádro</span><span class="sxs-lookup"><span data-stu-id="e5b11-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="e5b11-173">16 GB na instanci</span><span class="sxs-lookup"><span data-stu-id="e5b11-173">16 GB per instance</span></span>
    - <span data-ttu-id="e5b11-174">Standardní políčko – 4 až 24 jader</span><span class="sxs-lookup"><span data-stu-id="e5b11-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="e5b11-175">10 až 15 uživatelů Enterprise na jádro</span><span class="sxs-lookup"><span data-stu-id="e5b11-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="e5b11-176">15 až 25 uživatelů Activity na jádro</span><span class="sxs-lookup"><span data-stu-id="e5b11-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="e5b11-177">25 až 50 členů týmu na jádro</span><span class="sxs-lookup"><span data-stu-id="e5b11-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="e5b11-178">Dávka</span><span class="sxs-lookup"><span data-stu-id="e5b11-178">Batch</span></span>

    - <span data-ttu-id="e5b11-179">1 až 4 dávkové podprocesy na jádro</span><span class="sxs-lookup"><span data-stu-id="e5b11-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="e5b11-180">Velikost podle popisu okna dávky</span><span class="sxs-lookup"><span data-stu-id="e5b11-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="e5b11-181">Všimněte si, že server AOS, Správa dat a Dávka jsou ve stejné roli v Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e5b11-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="e5b11-182">Je nutné použít nastavení velikosti pro tyto tři pracovní zatížení v kombinaci a ne je oddělovat jako v Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="e5b11-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="e5b11-183">V tomto poli se použijí koeficienty stejného typu pro SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5b11-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="e5b11-184">Vysoká dostupnost</span><span class="sxs-lookup"><span data-stu-id="e5b11-184">High availability</span></span>

- <span data-ttu-id="e5b11-185">Ujistěte se, že máte nejméně 1 až 2 další dostupné AOS než v odhadu.</span><span class="sxs-lookup"><span data-stu-id="e5b11-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="e5b11-186">Potřebujete alespoň 3 až 4 virtuální hostitele k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e5b11-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="e5b11-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="e5b11-187">Management reporter</span></span>

<span data-ttu-id="e5b11-188">Ve většině případů, pokud se často nepoužívají by měly doporučené minimální požadavky používající dva uzly dobře fungovat.</span><span class="sxs-lookup"><span data-stu-id="e5b11-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="e5b11-189">Pouze v případech velkého vytížení potřebujete více uzlů než dva.</span><span class="sxs-lookup"><span data-stu-id="e5b11-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="e5b11-190">Nastavte měřítko podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="e5b11-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="e5b11-191">služba SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="e5b11-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="e5b11-192">Pro všeobecnou dostupnost lze nasadit pouze jeden uzel SSRS.</span><span class="sxs-lookup"><span data-stu-id="e5b11-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="e5b11-193">Při testování sledujte uzel SSRS a zvyšte počet jader k dispozici pro SSRS podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="e5b11-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="e5b11-194">Ujistěte se, že máte k dispozici předem konfigurovaný sekundární uzel dostupný na virtuálním hostiteli, než je na virtuálním počítači SSRS.</span><span class="sxs-lookup"><span data-stu-id="e5b11-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="e5b11-195">To je důležité, pokud se jedná o problém s virtuálním počítačem, který je hostitelem SSRS nebo virtuálním hostitelem.</span><span class="sxs-lookup"><span data-stu-id="e5b11-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="e5b11-196">V takovém případě je nutné je vyměnit.</span><span class="sxs-lookup"><span data-stu-id="e5b11-196">If this the case, they would need to be replaced.</span></span>

<span data-ttu-id="e5b11-197">Počínaje verzí 10.0.17 je možné nakonfigurovat další uzly SSRS pro dosažení vysoké dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="e5b11-197">Starting with version 10.0.17, it is possible to configure additional SSRS nodes to achieve high availability.</span></span> <span data-ttu-id="e5b11-198">Další informace viz [Konfigurace vysoké dostupnosti pro uzly SQL Server Reporting Services (SSRS)](../../dev-itpro/deployment/onprem-ssrsha.md).</span><span class="sxs-lookup"><span data-stu-id="e5b11-198">For more information, see [Configure high availability for SQL Server Reporting Services (SSRS) nodes](../../dev-itpro/deployment/onprem-ssrsha.md).</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="e5b11-199">Orchestrátor prostředí</span><span class="sxs-lookup"><span data-stu-id="e5b11-199">Environment Orchestrator</span></span>

<span data-ttu-id="e5b11-200">Služba Orchestrator je služba pro správu nasazení a související komunikace s LCS.</span><span class="sxs-lookup"><span data-stu-id="e5b11-200">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="e5b11-201">Tato služba je nasazena jako primární služba Service Fabric a vyžaduje alespoň tři virtuální počítače.</span><span class="sxs-lookup"><span data-stu-id="e5b11-201">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="e5b11-202">Tato služba je umístěna společně se službami Service Fabric orchestration.</span><span class="sxs-lookup"><span data-stu-id="e5b11-202">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="e5b11-203">Měly být nastaveny na velké vytížení clusteru.</span><span class="sxs-lookup"><span data-stu-id="e5b11-203">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="e5b11-204">Další informace najdete v části [Naplánujte a připravte nasazení svého samostatného clusteru Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span><span class="sxs-lookup"><span data-stu-id="e5b11-204">For more information, see [Plan and prepare your Service Fabric Standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="e5b11-205">Virtualizace a předplatné</span><span class="sxs-lookup"><span data-stu-id="e5b11-205">Virtualization and oversubscription</span></span>

<span data-ttu-id="e5b11-206">Důležité služby jako server AOS by měly být hostované ve virtuálních hostitelích s vyhrazenými prostředky – jádra, paměť a disk.</span><span class="sxs-lookup"><span data-stu-id="e5b11-206">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

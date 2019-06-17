<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="hardware-sizing-on-premises-environments.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>hardware-sizing-on-premises-environments.e242d0.4832a056a99e0f7521e022982b7db7b16d7064a3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4832a056a99e0f7521e022982b7db7b16d7064a3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\fin-and-ops\get-started\hardware-sizing-on-premises-environments.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Požadavky nastavení velikosti hardwaru pro místní prostředí</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic lists the hardware sizing requirements for an on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma uvádí požadavky nastavení velikosti hardwaru pro místní prostředí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Požadavky nastavení velikosti hardwaru pro místní prostředí</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the <bpt id="p1">[</bpt>System requirements<ept id="p1">](system-requirements.md)</ept> and <bpt id="p2">[</bpt>Setup and deployment instructions<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept> to gain a solid understanding off the underlying infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Než zahájíte proces nastavení velikosti hardwaru a infrastruktury pro místní prostředí, seznamte se s informacemi z témat <bpt id="p1">[</bpt>Požadavky na systém<ept id="p1">](system-requirements.md)</ept> a <bpt id="p2">[</bpt>Pokyny k nastavení a nasazení<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept>, abyste dobře rozuměli základní infrastruktuře.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Pay close attention to the system setup best practices for optimum performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Věnujte velkou pozornost doporučeným postupům nastavení systému pro dosažení optimálního výkonu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po kontrole dokumentace můžete zahájit proces odhadu transakčních a souběžných uživatelských objemů a nastavení velikosti prostředí na základě průměrné základní propustnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Factors that affect sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koeficienty, které ovlivňují nastavení velikosti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>All the factors shown in the following illustration contribute to sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Všechny faktory na následujícím obrázku přispívají k nastavení velikosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The more detailed information that is collected, the more precisely you can determine sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Čím podrobnější informace jsou shromážděny tím přesnější nastavení velikosti můžete určit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Hardware sizing, without supporting data, is likely to be inaccurate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení velikosti hardwaru bez podpůrných dat bude pravděpodobně nepřesné.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The absolute minimum requirement for necessary data is the peak transaction line load per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Minimální absolutní požadavek na potřebná data nejvyšší vytížení řádku transakce za hodinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Hardware sizing for on-premises environments<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nastavení velikosti hardwaru pro místní prostředí<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při pohledu zleva doprava je prvním a nejdůležitějším faktorem potřebným pro přesný odhad nastavení velikosti profil transakce nebo charakteristika transakce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It's important to always find the peak transactional volume per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je důležité vždy najít maximální objem transakcí za hodinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If there are multiple peak periods, then these periods need to be accurately defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud existuje více vrcholných období, je nutné tato období přesně definovat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tak, jako rozumíte vytížení, které ovlivňuje infrastrukturu, bude nutné pochopit další podrobnosti o těchto faktorech:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Transactions<ept id="p1">**</ept> – Typically transactions have certain peaks throughout the day/week.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Transakce<ept id="p1">**</ept> -- obvykle transakce mají během dne nebo týdne určité špičky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This mostly depends on the transaction type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Většinou to závisí na typu transakce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Záznamy o čase a výdajích obvykle zobrazují největší vytížení jednou za týden, zatímco záznamy prodejní objednávky jsou často hromadné kvůli integraci nebo během dne poklesnou.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Number of concurrent users<ept id="p1">**</ept> – The number of concurrent users is the second most important sizing factor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Počet souběžných uživatelů<ept id="p1">**</ept> – číslo souběžných je druhý nejdůležitější koeficient pro změnu velikosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nelze spolehlivě získat odhady velikosti na základě počtu souběžných uživatelů, takže pokud to je jediný údaj, který máte k dispozici, odhadněte přibližný počet a znovu ho zkontrolujte, když máte více údajů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>An accurate concurrent user definition means that:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definice přesného počtu souběžných uživatelů znamená, že:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Named users are not concurrent users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jmenovaní uživatele nejsou souběžní uživatelé.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Concurrent users are always a subset of named users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Souběžní uživatelé jsou vždy podmnožinou jmenovaných uživatelů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Peak workload defines the maximum concurrency for sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vrcholné pracovní vytížení definuje maximální souběžnost pro třídění.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Criteria for concurrent users is that the user meets all the following criteria:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kritéria souběžných uživatelů znamenají, že uživatel splňuje všechna následující kritéria:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Logged on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přihlášený.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Working transactions/inquiries at the time of counting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pracovní transakce/dotazy v době výpočtu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Not an idle session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Není nečinná relace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Data composition<ept id="p1">**</ept> – This is mostly about how your system will be set up and configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Složení dat<ept id="p1">**</ept> – jedná se většinou o způsob nastavení a konfigurace vašeho systému.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například počet právnických osob, které máte, kolik položek, počet úrovní kusovníku a jak komplexní bude nastavení zabezpečení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Každý z těchto faktorů může mít malý vliv na výkon, takže lze tyto faktory vyrovnat pomocí inteligentních voleb z hlediska infrastruktury.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Extensions<ept id="p1">**</ept> – Customizations can be simple or complex.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Rozšíření<ept id="p1">**</ept> – přizpůsobení může být jednoduché, nebo komplexní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Počet úprav a složitost a má odlišný dopad na velikost potřebné infrastruktury.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro komplexní přizpůsobení je doporučeno provést vyhodnocení výkonu pro zajištění, že nejsou pouze testovány s ohledem na účinnosti, ale také porozumět tomu, jaké jsou potřeby infrastruktury.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This is even more critical when the extensions are not coded according to best practices for performance and scalability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">To je ještě důležitější, pokud nejsou rozšíření kódovaná podle doporučených postupů pro výkon a škálovatelnost.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Reporting and analytics<ept id="p1">**</ept> – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Vykazování a analýzy<ept id="p1">**</ept> – tyto koeficienty obvykle obsahují provádění náročných dotazů proti různým databázím v databázových systémech Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Princip a snížení četnosti při spouštění sestav výdajů vám pomůže pochopit jejich dopady.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Third-party solutions<ept id="p1">**</ept> – These solutions, like ISVs, have the same implications and recommendations as extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Řešení třetí strany<ept id="p1">**</ept> – tato řešení jako ISV, mají stejné důsledky a doporučení jako rozšíření.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Sizing your Finance and Operations environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení prostředí Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Abyste mohli porozumět požadavkům nastavení velikosti, je nutné znát maximální objem transakcí, které je nutné zpracovat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Většina pomocných systémů jako Management Reporter nebo SSRS je méně náročných.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>As a result, this document focuses mostly on AOS and SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento dokument se proto zaměřuje většinou na server AOS a SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obecně se vrstvy výpočtu škálují a je třeba nastavit je způsobem N+1, tj. pokud vytvoříte odhad tři AOS, přidejte čtvrtou AOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The database tier should be set up in an Always On highly-available setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úrovně databáze by měly být nastaveny ve vždy snadno dostupném nastavení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>SQL Server (OLTP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server (OLTP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení velikosti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>3K to 15K transaction lines per hour per core on DB server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Řádky transakce 3K až 15K za hodinu na základní databázový server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Typický poměr AOS-to-SQL 3:1 pro primární SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Additional cores are required based on the chosen high availability configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další jádra jsou nutná podle zvolené dostupnost konfigurace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Processing database-heavy operations may regress this to 2:1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování náročných databázových operací může vrátit 2:1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The following factors influence variations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odchylky ovlivňují následující faktory:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Parameter settings in use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Používané nastavení parametru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Levels of extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úrovně rozšíření</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Usage of additional functionality, such as database log and alerts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Použití dalších funkcí, jako jsou například výstrahy a protokol databáze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Extreme database logging will further reduce throughput per hour per core below 3K lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Protokolování databáze dále sníží propustnost za hodinu na základ pod 3K řádky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Složitost složení dat – jednoduchá účtová osnova vs. podrobná účtová osnova má vliv na propustnost (jako příklad).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Popis transakce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>2 GB to 16 GB memory for each core.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 GB paměti na 16 GB pro každé jádro.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Auxiliary databases on DB server such as Management reporter and SSRS databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pomocné databáze na Databázovm serveru, jako je například SSRS databáze a aplikace Management reporter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Temp DB = 15% of DB size, with as many files as physical processors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dočasné databáze = počet souborů jako fyzických procesorů 15 % velikosti databáze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>SAN size and throughput based on total concurrent transaction volume/usage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velikost SAN a propustnosti na základě celkové objemu/použití souběžných transakce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vysoká dostupnost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>We recommend always utilizing SQL Server in either a cluster or mirroring setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doporučujeme vždy využít serveru SQL Server v jednom seskupení nebo zrcadlení nastavení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The second SQL node should have the same number of cores as the primary node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Druhý uzel SQL by měl mít stejný počet jader jako primární.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Active Directory Federation Services (AD FS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory Federation Services (AD FS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For AD FS sizing, see the <bpt id="p1">[</bpt>AD FS Server Capacity documentation<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro nastavení velikosti AD FS viz <bpt id="p1">[</bpt>Dokumentace kapacity serveru AD FS<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A <bpt id="p1">[</bpt>sizing spreadsheet<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept> is available for planning the number of instances in your deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Tabulka třídění<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept> je k dispozici pro plánování počtu instancí v nasazení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>AOS (Online and batch)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Server AOS (Online a dávka)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení velikosti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Sizing by transaction volume/usage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení velikosti podle objemu nebo použití transakce</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>2K to 6K lines per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2K až 6K řádek na jádro</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>16 GB per instance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">16 GB na instanci</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Standard box – 4 to 24 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Standardní políčko – 4 až 24 jader</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>10 to 15 Enterprise users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10 až 15 uživatelů Enterprise na jádro</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>15 to 25 Activity users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">15 až 25 uživatelů Activity na jádro</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>25 to 50 Team members per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">25 až 50 členů týmu na jádro</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Batch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dávka</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>1 to 4 batch threads per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 až 4 dávkové podprocesy na jádro</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Size based on batch window characterization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velikost podle popisu okna dávky</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Všimněte si, že server AOS, Správa dat a Dávka jsou ve stejné roli v Service Fabric.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je nutné použít nastavení velikosti pro tyto tři pracovní zatížení v kombinaci a ne je oddělovat jako v Microsoft Dynamics AX 2012.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The same variability factors for SQL Server apply here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto poli se použijí koeficienty stejného typu pro SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vysoká dostupnost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Ensure that you have at least 1 to 2 more AOS available than you estimate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že máte nejméně 1 až 2 další dostupné AOS než v odhadu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Ensure that you have at least 3 to 4 virtual hosts available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Potřebujete alespoň 3 až 4 virtuální hostitele k dispozici.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Management reporter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ve většině případů, pokud se často nepoužívají by měly doporučené minimální požadavky používající dva uzly dobře fungovat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Only in cases where there is heavy use will you need more than two nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pouze v případech velkého vytížení potřebujete více uzlů než dva.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Please scale as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavte měřítko podle potřeby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>SQL Server Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">služba SQL Server Reporting Services</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>For the general availability release, only one SSRS node can be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro všeobecnou dostupnost lze nasadit pouze jeden uzel SSRS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při testování sledujte uzel SSRS a zvyšte počet jader k dispozici pro SSRS podle potřeby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že máte k dispozici předem konfigurovaný sekundární uzel dostupný na virtuálním hostiteli, než je na virtuálním počítači SSRS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">To je důležité, pokud se jedná o problém s virtuálním počítačem, který je hostitelem SSRS nebo virtuálním hostitelem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If this the case, they would need to be replaced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V takovém případě je nutné je vyměnit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Environment Orchestrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Orchestrátor prostředí</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The Orchestrator service is the service that manages your deployment and the related communication with LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Služba Orchestrator je služba pro správu nasazení a související komunikace s LCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>This service is deployed as the primary Service Fabric service and requires at least three VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato služba je nasazena jako primární služba Service Fabric a vyžaduje alespoň tři virtuální počítače.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This service is co-located with the Service Fabric orchestration services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato služba je umístěna společně se službami Service Fabric orchestration.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This and should be sized to the peak load of the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Měly být nastaveny na velké vytížení clusteru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>For more information, see <bpt id="p1">[</bpt>Service Fabric cluster capacity planning considerations<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další informace naleznete v tématu <bpt id="p1">[</bpt>Aspekty plánování kapacity clusteru Service Fabric<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Virtualization and oversubscription</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Virtualizace a předplatné</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Důležité služby jako server AOS by měly být hostované ve virtuálních hostitelích s vyhrazenými prostředky – jádra, paměť a disk.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
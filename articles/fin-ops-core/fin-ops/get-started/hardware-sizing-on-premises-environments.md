---
title: Požadavky nastavení velikosti hardwaru pro místní prostředí
description: Toto téma uvádí požadavky nastavení velikosti hardwaru pro místní prostředí.
author: sericks007
manager: AnnBe
ms.date: 11/27/2019
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
ms.openlocfilehash: 07bbfa7c655a7125e0a9c61d2af2ba49b45782b0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570866"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Požadavky nastavení velikosti hardwaru pro místní prostředí

[!include [banner](../includes/banner.md)]

Než zahájíte proces nastavení velikosti hardwaru a infrastruktury pro místní prostředí, seznamte se s informacemi z témat [Požadavky na systém pro nasazení v cloudu](system-requirements.md) a [Pokyny k nastavení a nasazení](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), abyste dobře rozuměli základní infrastruktuře.

> [!NOTE]
> Věnujte velkou pozornost doporučeným postupům nastavení systému pro dosažení optimálního výkonu.

Po kontrole dokumentace můžete zahájit proces odhadu transakčních a souběžných uživatelských objemů a nastavení velikosti prostředí na základě průměrné základní propustnosti.

## <a name="factors-that-affect-sizing"></a>Koeficienty, které ovlivňují nastavení velikosti

Všechny faktory na následujícím obrázku přispívají k nastavení velikosti. Čím podrobnější informace jsou shromážděny tím přesnější nastavení velikosti můžete určit. Nastavení velikosti hardwaru bez podpůrných dat bude pravděpodobně nepřesné. Minimální absolutní požadavek na potřebná data nejvyšší vytížení řádku transakce za hodinu.

[![Nastavení velikosti hardwaru pro místní prostředí](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Při pohledu zleva doprava je prvním a nejdůležitějším faktorem potřebným pro přesný odhad nastavení velikosti profil transakce nebo charakteristika transakce. Je důležité vždy najít maximální objem transakcí za hodinu. Pokud existuje více vrcholných období, je nutné tato období přesně definovat.

Tak, jako rozumíte vytížení, které ovlivňuje infrastrukturu, bude nutné pochopit další podrobnosti o těchto faktorech:

- **Transakce** -- obvykle transakce mají během dne nebo týdne určité špičky. Většinou to závisí na typu transakce. Záznamy o čase a výdajích obvykle zobrazují největší vytížení jednou za týden, zatímco záznamy prodejní objednávky jsou často hromadné kvůli integraci nebo během dne poklesnou.
- **Počet souběžných uživatelů** – číslo souběžných je druhý nejdůležitější koeficient pro změnu velikosti. Nelze spolehlivě získat odhady velikosti na základě počtu souběžných uživatelů, takže pokud to je jediný údaj, který máte k dispozici, odhadněte přibližný počet a znovu ho zkontrolujte, když máte více údajů. Definice přesného počtu souběžných uživatelů znamená, že:

    - Jmenovaní uživatele nejsou souběžní uživatelé.
    - Souběžní uživatelé jsou vždy podmnožinou jmenovaných uživatelů. 
    - Vrcholné pracovní vytížení definuje maximální souběžnost pro třídění.

    Kritéria souběžných uživatelů znamenají, že uživatel splňuje všechna následující kritéria:

    - Přihlášený.
    - Pracovní transakce/dotazy v době výpočtu.
    - Není nečinná relace.

- **Složení dat** – jedná se většinou o způsob nastavení a konfigurace vašeho systému. Například počet právnických osob, které máte, kolik položek, počet úrovní kusovníku a jak komplexní bude nastavení zabezpečení. Každý z těchto faktorů může mít malý vliv na výkon, takže lze tyto faktory vyrovnat pomocí inteligentních voleb z hlediska infrastruktury.
- **Rozšíření** – přizpůsobení může být jednoduché, nebo komplexní. Počet úprav a složitost a má odlišný dopad na velikost potřebné infrastruktury. Pro komplexní přizpůsobení je doporučeno provést vyhodnocení výkonu pro zajištění, že nejsou pouze testovány s ohledem na účinnosti, ale také porozumět tomu, jaké jsou potřeby infrastruktury. To je ještě důležitější, pokud nejsou rozšíření kódovaná podle doporučených postupů pro výkon a škálovatelnost.
- **Vykazování a analýzy** – tyto koeficienty obvykle obsahují provádění náročných dotazů proti různým databázím v systému. Princip a snížení četnosti při spouštění sestav výdajů vám pomůže pochopit jejich dopady.
- **Řešení třetí strany** – tato řešení jako ISV, mají stejné důsledky a doporučení jako rozšíření.

## <a name="sizing-your-environment"></a>Změna velikosti prostředí

Abyste mohli porozumět požadavkům nastavení velikosti, je nutné znát maximální objem transakcí, které je nutné zpracovat. Většina pomocných systémů jako Management Reporter nebo SSRS je méně náročných. Tento dokument se proto zaměřuje většinou na server AOS a SQL Server.

> [!NOTE]
> Obecně se vrstvy výpočtu škálují a je třeba nastavit je způsobem N+1, tj. pokud vytvoříte odhad tři AOS, přidejte čtvrtou AOS. Úrovně databáze by měly být nastaveny ve vždy snadno dostupném nastavení.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Nastavení velikosti

- Řádky transakce 3K až 15K za hodinu na základní databázový server.
- Typický poměr AOS-to-SQL 3:1 pro primární SQL Server. Další jádra jsou nutná podle zvolené dostupnost konfigurace.

    - Zpracování náročných databázových operací může vrátit 2:1.

- Odchylky ovlivňují následující faktory:

    - Používané nastavení parametru.
    - Úrovně rozšíření
    - Použití dalších funkcí, jako jsou například výstrahy a protokol databáze. Protokolování databáze dále sníží propustnost za hodinu na základ pod 3K řádky.
    - Složitost složení dat – jednoduchá účtová osnova vs. podrobná účtová osnova má vliv na propustnost (jako příklad).
    - Popis transakce.
    - 2 GB paměti na 16 GB pro každé jádro.
    - Pomocné databáze na Databázovm serveru, jako je například SSRS databáze a aplikace Management reporter.
    - Dočasné databáze = počet souborů jako fyzických procesorů 15 % velikosti databáze.
    - Velikost SAN a propustnosti na základě celkové objemu/použití souběžných transakce.

### <a name="high-availability"></a>Vysoká dostupnost

Doporučujeme vždy využít serveru SQL Server v jednom seskupení nebo zrcadlení nastavení. Druhý uzel SQL by měl mít stejný počet jader jako primární.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)

Nastavení velikosti AD FS je popsáno v tématu [Dokumentace kapacity serveru AD FS](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

[Tabulka třídění](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) je k dispozici pro plánování počtu instancí v nasazení.

## <a name="aos-online-and-batch"></a>Server AOS (Online a dávka)

### <a name="sizing"></a>Nastavení velikosti

- Nastavení velikosti podle objemu nebo použití transakce

    - 2K až 6K řádek na jádro
    - 16 GB na instanci
    - Standardní políčko – 4 až 24 jader
    - 10 až 15 uživatelů Enterprise na jádro
    - 15 až 25 uživatelů Activity na jádro
    - 25 až 50 členů týmu na jádro

- Dávka

    - 1 až 4 dávkové podprocesy na jádro
    - Velikost podle popisu okna dávky

- Všimněte si, že server AOS, Správa dat a Dávka jsou ve stejné roli v Service Fabric. Je nutné použít nastavení velikosti pro tyto tři pracovní zatížení v kombinaci a ne je oddělovat jako v Microsoft Dynamics AX 2012.
- V tomto poli se použijí koeficienty stejného typu pro SQL Server.

### <a name="high-availability"></a>Vysoká dostupnost

- Ujistěte se, že máte nejméně 1 až 2 další dostupné AOS než v odhadu.
- Potřebujete alespoň 3 až 4 virtuální hostitele k dispozici.

## <a name="management-reporter"></a>Management Reporter

Ve většině případů, pokud se často nepoužívají by měly doporučené minimální požadavky používající dva uzly dobře fungovat. Pouze v případech velkého vytížení potřebujete více uzlů než dva. Nastavte měřítko podle potřeby.

## <a name="sql-server-reporting-services"></a>služba SQL Server Reporting Services

Pro všeobecnou dostupnost lze nasadit pouze jeden uzel SSRS. Při testování sledujte uzel SSRS a zvyšte počet jader k dispozici pro SSRS podle potřeby. Ujistěte se, že máte k dispozici předem konfigurovaný sekundární uzel dostupný na virtuálním hostiteli, než je na virtuálním počítači SSRS. To je důležité, pokud se jedná o problém s virtuálním počítačem, který je hostitelem SSRS nebo virtuálním hostitelem. V takovém případě je nutné je vyměnit.

## <a name="environment-orchestrator"></a>Orchestrátor prostředí

Služba Orchestrator je služba pro správu nasazení a související komunikace s LCS. Tato služba je nasazena jako primární služba Service Fabric a vyžaduje alespoň tři virtuální počítače. Tato služba je umístěna společně se službami Service Fabric orchestration. Měly být nastaveny na velké vytížení clusteru. Další informace najdete v části [Naplánujte a připravte nasazení svého samostatného clusteru Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Virtualizace a předplatné

Důležité služby jako server AOS by měly být hostované ve virtuálních hostitelích s vyhrazenými prostředky – jádra, paměť a disk.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
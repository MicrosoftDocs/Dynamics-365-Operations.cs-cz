---
title: "Systémové požadavky"
description: "Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 Finance and Operations, edici Enterprise pro cloudové a místní nasazení."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: cs-cz
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Systémové požadavky

[!include[banner](../includes/banner.md)]


Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 Finance and Operations, edici Enterprise pro cloudové a místní nasazení. Před tím, než nainstalujete Finance and Operations, ověřte, že systém se kterým pracujete, splňuje nebo přesahuje minimální požadavky na síť, hardware a software.


## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office
V cloudovém a místním nasazení Finance and Operations jsou podporovány následující aplikace Office.
-   Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Konkrétní systémové požadavky pro cloudové nasazení
## <a name="network-requirements"></a>Požadavky na síť
-   Finance and Operations je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Toto je čekací doba z prohlížeče klienta datového centra Microsoft Azure, který je hostitelem aplikace Finance and Operations. Doporučujeme otestovat čekací dobu v síti na stránkách <http://www.azurespeed.com>.
-   Požadavky na šířku pásma pro Finance and Operations závisí na vašem scénáři. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s). Pro scénáře, které mají vysoké požadavky na zatížení, jako jsou pracovní prostory, nebo scénáře, které obsahují rozsáhlé přizpůsobení, se však doporučuje větší šířka pásma.

Obecně je aplikace Finance and Operations optimalizována pro Internet. Počet opakovaných cest z klienta prohlížeče do datového centra Azure je velmi nízký a celé pracovní zatížení se komprimuje. 

> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma použijte verzi preview aplikace Finance and Operations.

## <a name="net-framework-requirements"></a>Požadavky systému .NET Framework
Finance and Operations vyžaduje rozhraní .NET Framework verze 4.6.2 pro všechny aplikace click-once, jako je agent směrování dokumentů. Pokyny k instalaci naleznete v tématu [Instalace rozhraní.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče
Webová aplikace může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:


-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10
-   Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. 

> [!NOTE]
> -   K zachycení snímků obrazovek, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalovánu předběžnou verzi doplňku Chrome. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Editor pracovního postupu je spuštěn jako aplikace ClickOnce. Aplikace ClickOnce podporují pouze Microsoft Edge and Internet Explorer (v podporované verzi systému Microsoft Windows). Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.
> -   Návrhář sestav pro finanční vykazování je uveden jako aplikace ClickOnce. Vyžaduje 64bitový kompatibilní operační systém. Pokud používáte Chrome, je nutné nainstalovat doplněk ClickOnce, abyste mohli stáhnout klienta návrháře sestav. Pokud používáte Chrome s anonymním režimem, zkontrolujte, zda je povoleno rozšíření ClickOnce pro anonymní režim.
> -   K zobrazení náhledu souborů PDF doporučujeme používat prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Podporované webové prohlížeče pro Retail Cloud POS

Retail Cloud POS může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:

-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1 nebo Windows 7

## <a name="retail-modern-pos-requirements"></a>Požadavky na Retail Modern POS
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Retail Modern POS je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.
-   Retail Modern POS je podporován pouze v edicích Windows 10 Pro, Enterprise a Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimální systémové požadavky

-   Minimální podporované rozlišení je 1280×1024.
-   Počítač s Retail Modern POS musí splňovat tyto požadavky:
    -   Musí mít alespoň dvoujádrový procesor, který se běží při nejméně 2 gigahertzech (GHz).
    -   Musí mít alespoň 3 gigabajty (GB) paměti RAM.
    -   Musí mít přístup k Internetu.

## <a name="retail-hardware-station-requirements"></a>Požadavky na Základní balíček Retail hardware station
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Retail hardware station je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.
-   Retail hardware station je podporována v následujících operačních systémech:
    -   Edice Windows 7 Professional, Enterprise a Ultimate 
    
    > [!NOTE]
    > Windows 7 jsou podporovány pouze pokud je v systému ručně instalován Internet Explorer 11.

    -   Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimální systémové požadavky

Počítač musí splňovat všechny požadavky na systém pro instalaci a používání následujících položek:

-   Internetová informační služba (IIS)
-   Hardware třetí strany

## <a name="retail-store-scale-unit-requirements"></a>Požadavky na základní balíček Retail Store Scale Unit
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Retail Store Scale Unit je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.
-   Retail Store Scale Unit je podporována v následujících operačních systémech:
    -   Edice Windows 7 Professional, Enterprise a Ultimate
    -   Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimální systémové požadavky

-   4 GB paměti RAM
-   1,6 GHz maximální rychlost procesoru na jádro (minimum jsou dvě jádra.)
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

### <a name="recommended-system-requirements"></a>Doporučené systémové požadavky

-   6 GB paměti RAM
-   Procesor s nejvyšší rychlostí CPU 2,4 GHz i7 (nebo ekvivalentní) na jádro (doporučují se čtyři jádra.)
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

## <a name="connector-requirements"></a>Požadavky na konektor
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Konektor pro aplikaci Microsoft Dynamics AX má dva samostatné instalační programy, službu **Async Server Connector** a **Real-time service for Dynamics AX 2012 R3**.
-   Obě komponenty jsou 32bitové aplikace, ale lze ji používat v architektuře x86 a x64.
-   Obě součásti jsou podporovány v následujících operačních systémech:
    -   Edice Windows 7 Professional, Enterprise a Ultimate
    -   Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimální systémové požadavky

-   2 GB RAM paměti, 4 GB doporučené paměti RAM
-   1,6 GHz maximální rychlost procesoru na jádro (minimum jsou dvě jádra.)
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

## <a name="requirements-for-development-on-local-vms"></a>Požadavky na vývoj na místních virtuálních počítačích
Informace o požadavcích na vývoj na místních virtuálních počítačích (VM) naleznete v tématu [místní spuštění virtuálního počítače](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Konkrétní systémové požadavky pro místní nasazení

## <a name="network-requirements"></a>Požadavky na síť
Finance and Operations (místní) mohou pracovat v sítích, které využívají Internet Protocol Version 4 (IPv4) nebo Internet Protocol Version 6 (IPv6). Když plánujete svůj systém, vezměte do úvahy vaše síťové prostředí a dodržujte následující pokyny.

### <a name="network-response-time"></a>Doba odezvy sítě
Následující tabulka obsahuje minimální požadavky na síť pro připojení mezi webovým prohlížečem a Application Object Server (AOS) a pro připojení mezi AOS a databází v místním systému.

| Hodnota     | Webový prohlížeč - AOS | AOS - databáze                                            |
|-----------|--------------------|------------------------------------------------------------|
| Šířka pásma | 50 KBps na uživatele   | 100 MBps                                                   |
| Latence   | < 250 - 300 ms       | < 1 ms (pouze LAN). AOS a databáze musí být sloučeny. |

- Finance and Operations (místní) je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence představuje latenci z prohlížeče do datového centra, které hostuje Finance and Operations.
- Požadavky na šířku pásma pro Finance and Operations (místní) závisí na vašem scénáři. Typické scénáře požadují šířku pásma více než 50 kilobajtů za sekundu (KBps) mezi prohlížečem a serverem Finance and Operations. Pro scénáře, které mají vysoké požadavky na zatížení, jako jsou pracovní prostory, nebo scénáře, které obsahují rozsáhlé přizpůsobení, se však doporučuje větší šířka pásma, která závisí na používání.
Taková nasazení, kdy jsou AOS a serverová databáze SQL Server jsou v jiných datových centrech, nejsou podporovány. AOS a serverová databáze SQL Server musí být sloučeny. Všeobecně vzato je Finance and Operations optimalizována tak, by omezila opakované cesty mezi prohlížečem a serverem. Počet opakovaných cest z klienta prohlížeče do datového centra je buď rovný nule nebo jedné pro každou uživatelskou interakci a zatížení je tak komprimováno.

> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Doporučujeme použít simulaci z reálného života proti neprodukčnímu prostředí aplikace Finance and Operations jakožto nejlepší měřidlo výkonu pro váš konkrétní případ. 

### <a name="lan-environments"></a>prostředí LAN
V prostředí místní sítě (LAN) není vyžadováno, aby vzdálená plocha Windows ve Microsoft Windows Server byla připojená k Finance and Operations. Mohlo by to být však vyžadováno pro servisní operace na virtuálních počítačích, které tvoří serverová nasazení.

### <a name="wan-environments"></a>prostředí WAN
V prostředí dálkové sítě (WAN) není vyžadováno, aby vzdálená plocha Windows ve Microsoft Windows Server byla připojená k Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Požadavky na internetové připojení
Finance and Operations (místní) nevyžaduje internetové připojení z pracovních stanic koncových uživatelů. Některé funkce však nebudou bez internetového připojení k dispozici.

| Klient prohlížeče | Intranetový scénář bez internetového připojení je místem návrhu pro volbu místního nasazení. Některé funkce, které vyžadují cloudové služby, nebudou k dispozici, jako např. knihovny Nápověda a Průvodce úkolem (Task guide) v LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | AOS a vrstva Service Fabric musí být schopny komunikovat s LCS. Místní klient založený na prohlížeči nevyžaduje přístup na internet.                                                                                |
| Telemetrie      | Telemetrická data mohou být ztraceny, pokud dojde k dlouhým přerušením připojení. Přerušení připojení do LCS neovlivňuje funkčnost místní aplikace.                                                |
| LCS            | Připojení k LCS je vyžadováno pro nasazení, nasazení kódu a servisní operace.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Přenos telemetrických dat do cloudu
Většina telemetrie je uložena lokálně a lze zobrazit pomocí Event Viewer v Microsoft Windows. Malá podskupina telemetrických událostí je přenesena do telemetrického potrubí Microsoft v cloudu pro účely diagnostiky. Informace o zákaznících a identifikovatelné údaje o konečných uživatelích nejsou součástí telemetrie odesílané do společnosti Microsoft. Názvy virtuálních počítačů jsou posílány do společnosti Microsoft, aby pomohly správě prostředí a diagnostice z portálu LCS.

## <a name="domain-requirements"></a>Požadavky na doménu
Když instalujete Finance and Operations (místní), zvažte následující požadavky na doménu:

- Virtuální počítače, které hostují komponenty Finance and Operations (místní), musí patřit do domény služby Active Directory. Služba Active Directory Domain Services (AD DS) musí být konfigurována v nativním režimu.
- Virtuální počítače, na kterých běží komponenty Finance and Operations (místní), musí mít přístup k sobě navzájem dle konfigurace ve službě Active Directory Domain Services. 
- Ovladač domény musí být provozován na Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Požadavky na hardware
Tato sekce popisuje hardware potřebný pro provoz Finance and Operations (místní).
Konkrétní hardware se bude lišit v závislosti na systémové konfiguraci, složení dat a aplikacích a funkcích, které se rozhodnete využívat. Zde je několik faktorů, které by mohly ovlivnit volbu patřičného hardwaru pro Finance and Operations (místní):

- Počet transakcí za hodinu.
- Počet souběžných uživatelů.

## <a name="minimum-infrastructure-requirements"></a>Minimální požadavky na infrastrukturu
Finance and Operations (místní) používají Microsoft Azure Service Fabric pro hostování služeb AOS, dávky, správu dat, management reporter a orchestrátor prostředí. Služby Microsoft SQL Server Reporting Services (SSRS) nejsou hostovány v clusteru Service Fabric.
SQL Server musí být nastaven ve vysoce dostupném nastavení HADRON, která má alespoň dva uzly pro produkční užívání.
Následující obrázek ukazuje minimální doporučený počet uzlů ve vašem clusteru Service Fabric.

[![doporučený počet uzlů pro cluster Service Fabric](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Požadavky na procesor a RAM
V následující tabulce najdete seznam procesorů a množství random-access memory (RAM), které jsou vyžadovány pro každou z rolí požadovanou pro provoz možnosti nasazení. Pro více informací si přečtěte doporučené minimální požadavky pro samostatný cluster Service Fabric [Naplánujte a připravte svůj cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Pokud je ve stejném počítači nainstalován i jiný software Microsoft, systém musí také vyhovovat požadavkům na hardware pro daný software. Doporučujeme vám, abyste omezili další serverové aplikace na tom samém počítači jako AOS na 1 gigabajt (GB) RAM.

**Velikost dle role a topologický typ**

| Topologie   | Role (typ uzlu)              | Doporučená jádra procesoru | Doporučená paměť (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Výroba | AOS, správa dat, dávky   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | služba SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrátor                  | 4                           | 16                      |
| Sandbox    | AOS, správa dat, dávky   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | služba SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrátor                  | 4                           | 16                      |

**Odhad minimální velikosti pro nasazení produkce a sandboxu**\*

| Topologie                                  | Role                          | Počet případů |
|-------------------------------------------|-------------------------------|---------------------|
| Výroba                                | AOS (správa dat, dávky)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | služba SQL Server Reporting Services | 1                   |
|                                           | Orchestrátor\*\*                | 3                   |
| Sandbox                                   | AOS, správa dat, dávky   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | služba SQL Server Reporting Services | 1                   |
|                                           | Orchestrátor                  | 3                   |
| *Topologie Summary Production a Sandbox* |                               | 16                  |

\*Tato množství jsou ověřovány našimi zkušebními zákazníky mohou být upraveny dle potřeby na základě této zpětné vazby.

\*\*Orchestrátor je vyhrazen coby primární typ uzlu a bude použit také pro provoz služeb Service Fabric.

**Počáteční odhady pro Backend SQL Server a AD**

[![Počáteční odhady pro Backend SQL Server a AD](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*Velikost SQL Server velmi závisí na pracovní zátěži. Pro více informací viz sekce [Rozsah hardwaru pro místní nasazení](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Skladování

- **AOS** - Aplikace Finance and Operations (místní) bude využívat část Server Message Block (SMB) 3.0 pro ukládání nestrukturovaných dat. Pro více informací viz [Storage Spaces Direct ve Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – realistické možnosti:
    - Vysoce dostupná disková jednotka SSD.
    - Síť paměťových oblastí (SAN) optimalizovaná pro průchodnost OLTP.
    - Vysoce výkonné Přímo připojené úložné zařízení (DAS) 
- **IOPS pro SQL a správu dat** – Paměť jak pro správu dat, tak i SQL Server by měla mít alespoň 2 000 vstupních / výstupních operací za sekundu (IOPS). Produkční IOPS závisí na počtu faktorů. Pro více informací viz sekce "Rozsah hardwaru pro místní nasazení". 
- **IOPS virtuálního stroje** – Každý virtuální stroj by měl mít alespoň 100 IOPS pro zápis.

## <a name="virtual-host-requirements"></a>Požadavky na virtuálního hostitele
Když nastavujete virtuálního hostitele pro prostředí Finance and Operations (místní), použijte následující příručky: [Naplánujte a připravte váš cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) a [Popis clusteru service fabric](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Každý virtuální hostitel by měl mít dostatek jader pro navrhovanou kapacitu infrastruktury. Je možné mít více pokročilých konfigurací, kdy SQL Server je umístěn ve fyzickém hardwaru a vše ostatní je virtuální. Pokud je SQL Server virtuální, diskový subsystém by měl být rychlý SAN nebo ekvivalent. Ve všech případech se ujistěte, že virtuální hostitel je základně nastaven jako vysoce přístupný a redundantní Ve všech případech, kdy je použita virtualizace, by neměly být prováděny žádné snímky virtuálních počítačů.

## <a name="software-requirements-for-all-server-computers"></a>Požadavky na software pro všechny serverové počítače
Před tím, než lze nainstalovat komponenty Finance and Operations (místní), musí být v počítači přítomen následující software:

- Microsoft .NET Framework 4.5.1 nebo vyšší
- Service Fabric - více informací najdete v [Naplánujte a připravte váš cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Podporované serverové operační systémy
Následující tabulka obsahuje seznam serverových operačních systémů, které jsou podporovány pro komponenty Finance and Operations.

| Operační systém                                     | Poznámky                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter nebo Standard | Tyto požadavky jsou pro databáze a cluster Service Fabric, který hostuje AOS. |

## <a name="software-requirements-for-database-servers"></a>Požadavky na software pro databázové servery

- Podporovány jsou pouze 64bitové verze SQL Server 2016.
- V produkčním prostředí doporučujeme nainstalovat nejnovější kumulativní aktualizaci (CU) pro SQL Server verzi, kterou používáte.
- Finance and Operations (místní) podporují kolace Unicode, které rozlišují malá a velká písmena, akcenty, kanatypy a šířku. Kolace musí být shodná s místním nastavením Windows na počítači, který provozuje AOS. Pokud provádíte novou instalaci, doporučujeme vám vybrat kolaci Windows místo kolace SQL Server. Více informací o tom, jak zvolit kolaci pro databázi SQL Serveru, najdete v [Dokumentaci pro SQL Server](/sql/sql-server/sql-server-technical-documentation).
Následující tabulka obsahuje seznam SQL Server verzí, které jsou podporovány pro databáze Finance and Operations. Více informací najdete v minimálních požadavcích na hardware pro [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016)

| Požadavek                                                      | Poznámky                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition nebo Enterprise Edition | Pro požadavky na hardware pro SQL Server viz [Požadavky na hardware a software pro instalaci SQL Serveru 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Požadavky na software pro klientské počítače
Webová aplikace Finance and Operations může být provozována na jakémkoliv přístroji, který obsahuje webový prohlížeč kompatibilní s HTML5.0. Konkrétní kombinace přístroj / prohlížeč, které potvrdil Microsoft:

- Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
- Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
- Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10
- Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Požadavky na software pro služby Active Directory Federation Services 
Active Directory Federation Services (AD FS) na Windows Server 2016

Řadič domény musí být Windows Server 2012 R2 nebo pozdější s funkční úrovní domény 2012 R2 nebo vyšší.

Více informací o funkčních úrovních domény najdete v: 
- [Co jsou funkční úrovně Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Porozumění funkčním úrovním domén Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Požadavky na hardware a software pro retailové komponenty
Finance and Operations (místní) v současnosti neobsahuje retailové komponenty.

<a name="see-also"></a>Viz také
--------

[Získání kopie Dynamics 365 for Finance and Operations, Enterprise edition ve verzi pro hodnocení](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)


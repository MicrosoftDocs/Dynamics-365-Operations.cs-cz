---
title: "Konkrétní systémové požadavky pro místní nasazení"
description: "Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení on-premises."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: cs-cz
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Konkrétní systémové požadavky pro místní nasazení

[!include[banner](../includes/banner.md)]

Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení on-premises. Před tím, než nainstalujete Finance and Operations, je-li tento krok vhodný, ověřte, že systém se kterým pracujete, splňuje nebo přesahuje minimální požadavky na síť, hardware a software.

## <a name="network-requirements"></a>Požadavky na síť
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) může pracovat na sítích, které používají Internet Protocol Version 4 (IPv4) nebo Internet Protocol Version 6 (IPv6). Když plánujete svůj systém, vezměte do úvahy vaše síťové prostředí a dodržujte následující pokyny.

### <a name="network-response-time"></a>Doba odezvy sítě
Následující tabulka obsahuje minimální požadavky na síť pro připojení mezi webovým prohlížečem a Application Object Server (AOS) a pro připojení mezi AOS a databází v místním systému.

| Hodnota     | Webový prohlížeč - AOS                      | AOS - databáze |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Šířka pásma | 50 kilobajtů za sekundu (kb/s) na uživatele | 100 megabajtů za sekundu (MB/s) |
| Latence   | Méně než 250 – 300 milisekund (ms)     | Méně než 1 ms (pouze místní síť [LAN]). AOS a databáze musí být sloučeny. |

- Finance and Operations (místní) je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence představuje latenci z prohlížeče do datového centra, které hostuje Finance and Operations.
- Požadavky na šířku pásma pro Finance and Operations (místní) závisí na vašem scénáři. Typické scénáře požadují šířku pásma více než 50 kilobajtů za sekundu (kb/s) mezi prohlížečem a serverem Finance and Operations. Pro scénáře, které mají vysoké požadavky na zatížení, jako jsou pracovní prostory, nebo scénáře, které obsahují rozsáhlé přizpůsobení, se však doporučuje větší šířka pásma. Konkrétní šířka pásma závisí na použití.

Taková nasazení, kdy jsou AOS a serverová databáze Microsoft SQL Server jsou v jiných datových centrech, nejsou podporovány. AOS a SQL Server databáze musí být sloučeny. 

Všeobecně vzato je Finance and Operations optimalizována tak, by omezila opakované cesty mezi prohlížečem a serverem. Počet opakovaných cest z klienta prohlížeče do datového centra je buď rovný nule nebo jedné pro každou uživatelskou interakci a zatížení je tak komprimováno.

> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Doporučujeme použít simulaci z reálného života proti neprodukčnímu prostředí aplikace Finance and Operations jakožto nejlepší měřidlo výkonu pro váš konkrétní případ. 

### <a name="lan-environments"></a>prostředí LAN
V prostředí místní sítě (LAN) není vyžadováno, aby vzdálená plocha Windows ve Microsoft Windows Server byla připojená k Finance and Operations. Mohla by však být vyžadována vzdálená plocha pro servisní operace na virtuálních počítačích, které tvoří serverová nasazení.

### <a name="wan-environments"></a>prostředí WAN
V prostředí dálkové sítě (WAN) není vyžadováno, aby vzdálená plocha Windows ve Microsoft Windows Server byla připojená k Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Požadavky na internetové připojení
Finance and Operations (on-premises) nevyžaduje internetové připojení z pracovních stanic koncových uživatelů. Některé funkce však nebudou bez internetového připojení k dispozici.

|                    |   |
|--------------------|---|
| **Klient prohlížeče** | Intranetový scénář bez internetového připojení je místem návrhu pro volbu místního nasazení. Některé funkce, které vyžadují cloudové služby, nebudou k dispozici, jako například knihovny Nápověda a Průvodce úkolem ve službě Microsoft Dynamics Lifecycle Services (LCS). |
| **Server**         | AOS nebo vrstva Microsoft Azure Service Fabric musí být schopny komunikovat s LCS. Místní klient založený na prohlížeči nevyžaduje přístup na internet. |
| **Telemetrie**      | Telemetrická data mohou být ztraceny, pokud dojde k dlouhým přerušením připojení. Přerušení připojení do LCS neovlivňuje funkčnost místní aplikace. |
| **LCS**            | Připojení k LCS je vyžadováno pro nasazení, nasazení kódu a servisní operace. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Přenos telemetrických dat do cloudu
Většina telemetrických dat je uložena lokálně a lze je zobrazit pomocí Prohlížeče událostí v Microsoft Windows. Malá podskupina telemetrických událostí je přenesena do telemetrického potrubí Microsoft v cloudu pro účely diagnostiky. Informace o zákaznících a identifikovatelné údaje o uživatelích nejsou součástí telemetrických dat odesílaných do společnosti Microsoft. Názvy virtuálních počítačů jsou posílány do společnosti Microsoft, aby pomohly se správou prostředí a diagnostikou z portálu LCS.

## <a name="domain-requirements"></a>Požadavky na doménu
Když instalujete Finance and Operations (místní), zvažte následující požadavky na doménu:

- Virtuální počítače, které hostují komponenty Finance and Operations (on-premises), musí patřit do domény služby Active Directory. Služba Active Directory Domain Services (AD DS) musí být konfigurována v nativním režimu.
- Virtuální počítače, na kterých běží komponenty Finance and Operations (on-premises), musí mít přístup k sobě navzájem. Tento přístup se konfiguruje v AD DS. 
- Řadič domény musí být Microsoft Windows Server 2012 R2 nebo pozdější, s funkční úrovní domény 2012 R2 nebo vyšší.

## <a name="hardware-requirements"></a>Požadavky na hardware
Tato sekce popisuje hardware potřebný pro provoz Finance and Operations (on-premises).

Konkrétní hardware se liší v závislosti na systémové konfiguraci, složení dat a aplikacích a funkcích, které se rozhodnete využívat. Zde je několik faktorů, které mohou ovlivnit volbu patřičného hardwaru pro Finance and Operations (on-premises):

- Počet transakcí za hodinu
- Počet souběžných uživatelů

## <a name="minimum-infrastructure-requirements"></a>Minimální požadavky na infrastrukturu
Finance and Operations (místní) používají Service Fabric pro hostování služeb AOS, dávky, správu dat, management reporter a orchestrátor prostředí. 

SQL Server musí mít vysoce dostupné nastavení HADRON, která má alespoň dva uzly pro produkční užívání.

Následující obrázek ukazuje minimální počet uzlů doporučený pro váš cluster Service Fabric.

[![Doporučený počet uzlů pro cluster Service Fabric](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Požadavky na procesor a RAM
V následujících tabulkách najdete seznam procesorů a množství random-access memory (RAM), které jsou vyžadovány pro každou roli požadovanou pro provoz možnosti nasazení. Pro více informací si přečtěte doporučené minimální požadavky pro samostatný cluster Service Fabric v tématu [Naplánujte a připravte svůj cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Pokud je ve stejném počítači nainstalován i jiný software Microsoft, systém musí také vyhovovat požadavkům na hardware pro daný software. Pokud jsou nainstalované jiné serverové aplikace na stejném počítači jako AOS, doporučujeme, abyste omezili tyto serverové aplikace na 1 gigabajt (GB) RAM.

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

**Odhad minimální velikosti pro nasazení produkce a sandboxu\***

| Topologie                                        | Role                          | Počet případů |
|-------------------------------------------------|-------------------------------|---------------------|
| Výroba                                      | AOS (správa dat, dávky)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | služba SQL Server Reporting Services | 1                   |
|                                                 | Orchestrátor\*\*              | 3                   |
| Sandbox                                         | AOS, správa dat, dávky   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | služba SQL Server Reporting Services | 1                   |
|                                                 | Orchestrátor                  | 3                   |
| *Souhrn topologií pro produkci a Sandbox* |                               | *16*                |

\* Čísla v této tabulce se ověřují našimi zkušebními zákazníky a mohou být upravena na základě zpětné vazby od těchto zákazníků.

\*\* Orchestrátor je vyhrazen jako primární typ uzlu a bude použit také pro provoz služeb Service Fabric.

**Počáteční odhady pro Backend SQL Server a AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Role</th>
<th>Virtuální počítače/Instance</th>
<th>Jádra</th>
<th>Celkový počet jader</th>
<th>Paměť na instanci (GB)</th>
<th>Celková paměť (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Sdílená infrastruktura</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Souborový server/Síť paměťových oblastí/Uložiště s vysokou dostupností</td>
<td colspan="5"><p>Úložiště back-endu musí být založeno na diskových jednotkách SSD na síti paměťových oblastí (SAN).</p>
<p>Velikost a propustnost vstupně-výstupních operací za sekundu (IOPS) vychází z velikosti pracovního zatížení.</p></td>
</tr>
<tr>
<td>Služba Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Souhrn pro sdílenou infrastrukturu</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*Velikost SQL Server velmi závisí na pracovní zátěži. Pro více informací viz téma [Rozsah hardwaru pro prostředí on-premises](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Skladování

- **AOS** – Aplikace Finance and Operations (on-premises) používá Server Message Block (SMB) 3.0 pro ukládání nestrukturovaných dat. Pro více informací viz [Storage Spaces Direct ve Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Jsou vhodné následující možnosti:

    - Nastavení SSD s vysokou dostupností
    - SAN, která je optimalizována pro propustnost OLTP
    - Vysoce výkonné přímo připojené úložné zařízení (DAS) 

- **SQL Server a IOPS správy dat** – Paměť jak pro správu dat, tak i SQL Server by měla mít alespoň 2 000 IOPS. Produkční IOPS závisí na počtu faktorů. Pro více informací viz téma [Rozsah hardwaru pro prostředí on-premises](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – Každý virtuální počítač by měla mít alespoň 100 IOPS pro zápis.

## <a name="virtual-host-requirements"></a>Požadavky na virtuálního hostitele
Když nastavujete virtuálního hostitele pro prostředí Finance and Operations (on-premises), použijte následující příručky v tématu: [Naplánujte a připravte váš cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) a [Popis clusteru Service Fabric](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Každý virtuální hostitel by měl mít dostatek jader pro navrhovanou kapacitu infrastruktury. Je možné mít více pokročilých konfigurací, kdy SQL Server je umístěn ve fyzickém hardwaru a vše ostatní je virtuální. Pokud je SQL Server virtuální, diskový subsystém by měl být rychlý SAN nebo ekvivalent. Ve všech případech se ujistěte, že virtuální hostitel je základně nastaven jako vysoce přístupný a redundantní Ve všech případech, kdy je použita virtualizace, by neměly být prováděny žádné snímky virtuálních počítačů.

## <a name="software-requirements-for-all-server-computers"></a>Požadavky na software pro všechny serverové počítače
Před tím, než lze nainstalovat komponenty Finance and Operations (místní), musí být v počítači přítomen následující software:

- Rozhraní Microsoft .NET Framework verze 4.5.1 nebo vyšší
- Service Fabric

Více informací najdete v [Naplánujte a připravte váš cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Podporované serverové operační systémy
Následující tabulka obsahuje seznam serverových operačních systémů, které jsou podporovány pro komponenty Finance and Operations.

| Operační systém                                     | Poznámky |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter nebo Standard | Tyto požadavky jsou pro databáze a cluster Service Fabric, který hostuje AOS. |

## <a name="software-requirements-for-database-servers"></a>Požadavky na software pro databázové servery

- Podporovány jsou pouze 64bitové verze SQL Server 2016.
- V produkčním prostředí doporučujeme nainstalovat nejnovější kumulativní aktualizaci (CU) pro SQL Server verzi, kterou používáte.
- Finance and Operations (místní) podporují kolace Unicode, které rozlišují malá a velká písmena, akcenty, kanatypy a šířku. Kolace musí být shodná s místním nastavením Windows na počítači, který provozuje AOS. Pokud provádíte novou instalaci, doporučujeme vám vybrat kolaci Windows místo kolace SQL Server. Více informací o tom, jak zvolit kolaci pro databázi SQL Serveru, najdete v [Dokumentaci pro SQL Server](/sql/sql-server/sql-server-technical-documentation).

Následující tabulka obsahuje seznam SQL Server verzí, které jsou podporovány pro databáze Finance and Operations. Více informací najdete v minimálních požadavcích na hardware pro [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016)

| Požadavek                                                      | Poznámky |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition nebo Enterprise Edition | Pro požadavky na hardware pro SQL Server viz [Požadavky na hardware a software pro instalaci SQL Serveru 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Požadavky na software pro aplikační objektový server (AOS) 
- Služby SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Požadavky na software pro server sestav (BI)
- Služby SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Požadavky na software pro klientské počítače
Webová aplikace Finance and Operations může být provozována na jakémkoliv přístroji, který má webový prohlížeč kompatibilní s HTML 5.0. Zde jsou některé konkrétní kombinace zařízení/prohlížeč, které potvrdil Microsoft:

- Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
- Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
- Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10
- Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Požadavky na software pro služby Active Directory Federation Services 
Je vyžadován Active Directory Federation Services (AD FS) na Windows Server 2016.

Řadič domény musí být Windows Server 2012 R2 nebo pozdější, s funkční úrovní domény 2012 R2 nebo vyšší. Více informací o funkčních úrovních domény najdete na následujících stránkách:

- [Co jsou funkční úrovně Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Porozumění funkčním úrovním domén Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office
V cloudovém a místním nasazení Finance and Operations jsou podporovány následující aplikace Microsoft Office:

-   Chcete-li používat doplňky aplikace Microsoft Excel a Microsoft Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [Řešení problémů s integrací se sadou Office](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Požadavky na hardware a software pro retailové komponenty
Finance and Operations (on-premises) v současnosti neobsahuje komponenty Retail.


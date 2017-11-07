---
title: "Systémové požadavky pro nasazení cloudu"
description: "Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení cloudu."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: 7fe11966b27eb0793a47835e05e465d809bf3407
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Systémové požadavky pro nasazení cloudu

[!include[banner](../includes/banner.md)]

Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení cloudu. Před tím, než nainstalujete Finance and Operations, je-li tento krok vhodný, ověřte, že systém se kterým pracujete, splňuje nebo přesahuje minimální požadavky na síť, hardware a software.

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče
Webová aplikace může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:

-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10
-   Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. 

> [!NOTE]
> -   Musíte nainstalovat předběžnou verzi doplňku Chrome, abyste umožnili záznamníku úloh pořídit snímky obrazovky a zahrnout je do generovaných dokumentů aplikace Microsoft Word. <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   Editor pracovního postupu je spuštěn jako aplikace ClickOnce. Aplikace ClickOnce podporují pouze Microsoft Edge and Internet Explorer (v podporované verzi systému Microsoft Windows). Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.
> -   Návrhář sestav pro finanční vykazování je uveden jako aplikace ClickOnce. Vyžaduje 64bitový kompatibilní operační systém. Pokud používáte Chrome, je nutné nainstalovat doplněk ClickOnce, abyste mohli stáhnout klienta Návrháře sestav. Pokud používáte Chrome s anonymním režimem, zkontrolujte, zda je povoleno rozšíření ClickOnce pro anonymní režim.
> -   K zobrazení náhledu souborů PDF doporučujeme používat prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Podporované webové prohlížeče pro Retail Cloud POS

Retail Cloud POS může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:

-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1 nebo Windows 7

## <a name="network-requirements"></a>Požadavky na síť
-   Finance and Operations je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence je latence z prohlížeče klienta datového centra Microsoft Azure, který je hostitelem aplikace Finance and Operations. Doporučujeme otestovat čekací dobu v síti na stránkách <http://www.azurespeed.com>.
-   Požadavky na šířku pásma pro Finance and Operations závisí na vašem scénáři. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s). Pro scénáře, které mají vysoké požadavky na zatížení, jako jsou pracovní prostory, nebo scénáře, které obsahují rozsáhlé přizpůsobení, se však doporučuje větší šířka pásma.

Obecně je aplikace Finance and Operations optimalizována pro Internet. Počet opakovaných cest z klienta prohlížeče do datového centra Azure je velmi nízký a celé pracovní zatížení se komprimuje. 

> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Zákazníci, kteří mají pochybnosti ohledně požadavků na šířku pásma by měli použít verzi preview aplikace Finance and Operations.

## <a name="net-framework-requirements"></a>Požadavky systému .NET Framework
Finance and Operations vyžaduje rozhraní Microsoft .NET Framework verze 4.6.2 pro všechny aplikace ClickOnce, jako je agent směrování dokumentů. Pokyny k instalaci naleznete v tématu [Instalace rozhraní.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office
V cloudovém a místním nasazení Finance and Operations jsou podporovány následující aplikace Microsoft Office:

-   Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [Řešení problémů s integrací se sadou Office](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

## <a name="retail-modern-pos-requirements"></a>Požadavky na Retail Modern POS

> [!NOTE]
> Pokud Retail Modern POS bude používat offline databázi, počítač musí splňovat všechny požadavky na systém pro aplikaci Microsoft SQL Server. Offline databáze Retail Modern POS bude pracovat na serveru Microsoft SQL Server 2012 s aktualizací Service Pack 3 nebo vyšší, Microsoft SQL Server 2014 s aktualizací Service Pack 2 nebo vyšší a Microsoft SQL Server 2016. Doporučujeme vždy použít nejnovější verzi, která je k dispozici, a nainstalovat všechny poslední aktualizace.

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

-   Konektor pro aplikaci Microsoft Dynamics AX má dva samostatné instalační programy, jeden pro službu Async Server Connector a jeden pro Real-time service for Dynamics AX 2012 R3.
-   Obě komponenty jsou 32bitové aplikace, ale lze je používat v architektuře x86 i x64.
-   Obě součásti jsou podporovány v následujících operačních systémech:

    -   Edice Windows 7 Professional, Enterprise a Ultimate
    -   Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB
    -   Microsoft Windows Server 2012 R2 a Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimální systémové požadavky
-   2 GB RAM paměti (4 GB doporučené paměti RAM)
-   1,6 GHz maximální rychlost procesoru na jádro (minimum jsou dvě jádra.)
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

## <a name="requirements-for-development-on-local-vms"></a>Požadavky na vývoj na místních virtuálních počítačích
Informace o požadavcích na vývoj na místních virtuálních počítačích (VM) naleznete v tématu [místní spuštění virtuálního počítače](../../dev-itpro/dev-tools/access-instances.md).


## <a name="see-also"></a>Viz také

[Získání kopie Dynamics 365 for Finance and Operations, Enterprise edition ve verzi pro hodnocení](../../dev-itpro/dev-tools/get-evaluation-copy.md)


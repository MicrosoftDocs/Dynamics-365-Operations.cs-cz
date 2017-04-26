---
title: "Systémové požadavky"
description: "Toto téma uvádí požadavky na systém pro aktuální verzi aplikace Microsoft Dynamics 365 pro operace."
author: sericks007
manager: AnnBe
ms.date: 2016-02-25 22 - 43 - 40
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Systémové požadavky

Toto téma uvádí požadavky na systém pro aktuální verzi aplikace Microsoft Dynamics 365 pro operace.

<a name="supported-web-browsers"></a>Podporované webové prohlížeče
----------------------

365 Microsoft Dynamics pro operace webové aplikace lze spustit v kterémkoli z následujících webových prohlížečů, které se zadaným operačním systémem:

-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo 10 nexu Google tablet
-   Apple Safari (nejnovější veřejně dostupná verze) na Mac OS X 10.10 (Yosemite) nebo 10.11 (El Capitan), 10.12 (Sierra) nebo Apple iPad

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. **Poznámky:**

-   K zachycení bitové kopie, které jsou generovány z Záznamník úkolů a zahrnout je do dokumentů aplikace Microsoft Word, musí mít příponu Chrome nainstalována. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Editor pracovního postupu je spuštěn jako ClickOnce aplikace. ClickOnce aplikace podporují pouze Edge Microsoft a aplikaci Internet Explorer (na podporovanou verzi systému Microsoft Windows). Editor pracovního postupu ClickOnce aplikace vyžaduje 64-bit kompatibilní operační systém.
-   Jako ClickOnce aplikace je spuštěna návrháře sestav pro finanční vykazování. Vyžaduje 64-bit kompatibilní operační systém. Pokud používáte Chrome, je nutné nainstalovat rozšíření ClickOnce Chcete-li stáhnout klienta návrháře sestav. Pokud používáte Chrome incognito režim, ujistěte se, že rozšíření ClickOnce je povolena také pro incognito režim.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Podporované webové prohlížeče pro Retail Cloud POS

Program Retail POS Cloud pro Dynamics 365 pro operace lze spustit v kterémkoli z následujících webových prohlížečů, které se zadaným operačním systémem:

-   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
-   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
-   Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1 nebo Windows 7

## <a name="network-requirements"></a>Požadavky na síť
-   Dynamics 365 pro operace je určena pro sítě s čekací dobou menší než 150 milisekund (ms). Toto je čekací doba z prohlížeče klienta Microsoft Azure datového centra, který je hostitelem 365 Dynamics pro operace. Doporučujeme otestovat čekací doby v síti na <http://www.azurespeed.com>.
-   Požadavky na šířku pásma pro Dynamics 365 pro operace závisí na váš scénář. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s). Pro scénáře, které mají vysoké payload požadavky, například pracovní prostory nebo situacích, které obsahují rozsáhlé přizpůsobení však je vhodné větší šířku pásma.

Obecně 365 Dynamics pro operace je optimalizována pro Internet. Je velmi malý počet výměnami zpráv z prohlížeče klienta Azure datového centra a celá datová část je komprimován. **Upozornění:** požadavky na šířku pásma z umístění klienta není vypočítat vynásobením počtu uživatelů požadavky minimální šířku pásma. Souběžné využití dané umístění je velmi obtížné vyčíslit. Pro zákazníky, kteří kladou důraz na požadavky na šířku pásma použijte náhled verze Dynamics 365 pro operace.

## <a name="net-framework-requirements"></a>Požadavky na rozhraní.NET Framework
Dynamics 365 pro operace vyžaduje rozhraní.NET Framework 4.6.2 verze pro všechny click-jednou aplikací, například agent směrování dokumentu. Pokyny k instalaci naleznete v tématu [instalace rozhraní.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Podporovaných aplikací Microsoft Office
-   Chcete-li spustit aplikaci Microsoft Excel a Word doplňky, musí mít Microsoft Office 2016 pro Windows nebo Mac nainstalována. Další informace o požadavcích na verzi naleznete v tématu [řešení problémů integrace sady Office](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Chcete-li zobrazit dokumenty, které jsou generovány pomocí exportu do aplikace Excel nebo exportovat do aplikace Word funkce, musí mít Microsoft Office 2007 nebo novější.

## <a name="retail-modern-pos-requirements"></a>Retail POS moderní požadavky
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Program Retail POS moderní je 32bitová aplikace, ale bude spuštěn na x86 a x64 architektury.
-   Program Retail POS moderní je podporována pouze u edice Windows 10 Pro, Enterprise a Enterprise dlouhý termín údržby větev (LTSB).

### <a name="minimum-system-requirements"></a>Minimální požadavky na systém

-   Minimální podporované rozlišení je 1280 × 1024.
-   Program Retail POS moderní kompatibilní s počítači musí splňovat tyto požadavky:
    -   Musí mít, alespoň dvoujádrový procesor, který se spustí na ne méně než 2 gigahertzů (GHz).
    -   Musí mít, alespoň 3 gigabajty (GB) paměti RAM.
    -   Musí mít přístup k Internetu.

## <a name="retail-hardware-station-requirements"></a>Požadavky na Retail hardware station
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Retail hardware station je 32bitová aplikace, ale bude spuštěn na x86 a x64 architektury.
-   Retail hardware station je podporován v následujících operačních systémech:
    -   Edice Windows 7 Professional, Enterprise a Ultimate **Poznámka:** Windows 7 je podporován pouze v případě ruční instalace aplikace Internet Explorer 11 v systému.
    -   Windows 8.1 Update 1 Professional, Enterprise a Embedded edice
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimální požadavky na systém

Počítač musí splňovat všechny požadavky na systém pro instalaci a používání následujících položek:

-   Internetová informační služba (IIS)
-   Hardwaru jiných výrobců

## <a name="retail-store-scale-unit-requirements"></a>Maloobchodní jednotky měřítka úložiště požadavky
### <a name="supported-operating-systems"></a>Podporované operační systémy

-   Maloobchodní skladové jednotky měřítka je 32bitová aplikace, ale bude spuštěn na x86 a x64 architektury.
-   Maloobchodní skladové jednotky měřítka je podporován v následujících operačních systémech:
    -   Edice Windows 7 Professional, Enterprise a Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise a Embedded edice
    -   Edice Windows 10 Pro, Enterprise a Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimální požadavky na systém

-   4 GB paměti RAM
-   1,6 GHz maximální rychlost procesoru na základní (dvě jádra jsou minimální).
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

### <a name="recommended-system-requirements"></a>Doporučené systémové požadavky

-   6 GB RAM
-   2.4 rychlost GHz i7 (nebo ekvivalentní) špičky využití procesoru na základní (doporučuje se čtyřmi jádry.)
-   Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)

## <a name="requirements-for-development-on-local-vms"></a>Požadavky na rozvoj na místní VMs
Informace o požadavcích pro rozvoj místních virtuálních počítačů (VMs) naleznete v tématu [VM systémem místního](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Viz také
--------

[Získejte zkušební kopie systému Dynamics 365 pro operace](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)



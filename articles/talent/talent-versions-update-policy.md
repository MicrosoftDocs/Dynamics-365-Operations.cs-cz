---
title: "Zásady aktualizace a systémové požadavky pro Dynamics 365 for Talent"
description: "V tomto tématu je uveden seznam požadavků pro aplikaci Dynamics 365 for Talent. Jsou zde také popsány zásady aktualizací."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: Talent, update policy, requirements, system requirements
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bcc8464d34c35423e86c963c6b493fc09db4472
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>Zásady aktualizace a systémové požadavky pro Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]


V tomto tématu je uveden seznam požadavků pro aplikaci Microsoft Dynamics 365 for Talent. Jsou zde také popsány zásady aktualizací.

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče

Webová aplikace Microsoft Dynamics 365 Talent může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému: 

*   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
*   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
*   Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10
*   Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. 

> [!NOTE]
> * K zachycení bitových kopií, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalováno rozšíření Chrome. 
> * Editor pracovního postupu je spuštěn jako aplikace ClickOnce. Aplikace ClickOnce podporují pouze Microsoft Edge and Internet Explorer (v podporované verzi systému Microsoft Windows). Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.
> * K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.
Požadavky na síť
> * Aplikace Dynamics 365 for Talent je určena pro sítě s čekací dobou 250–300 milisekund (ms) nebo méně. Toto je čekací doba z prohlížeče klienta datového centra Microsoft Azure, který je hostitelem aplikace Dynamics 365 for Talent. Doporučujeme, abyste vyzkoušeli latenci sítě na [www.azurespeed.com] (http://www.azurespeed.com "Test latence Azure").
> * Požadavky na šířku pásma pro Dynamics 365 for Talent závisí na vašem scénáři. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).

> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Dynamics 365 for Talent.

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office

*   Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v části [Řešení problémů s integrací se sadou Office] (../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací se sadou Office]").
*   Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

## <a name="update-policy"></a>Zásady aktualizace

Aplikace Microsoft Dynamics 365 for Talent se servisuje jako cloudová nabídka. Aktualizace pro aplikaci Dynamics 365 for Talent jsou nepřetržité a automaticky aplikované společností Microsoft.

Aktualizace jsou vydávány v pravidelných intervalech a použijí se na všechna prostředí.  Aplikace Dynamics 365 for Talent je podporována v souladu se zásadami [Životní cyklus podpory od společnosti Microsoft] (https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Životní cyklus podpory od společnosti Microsoft"), které poskytují konzistentní a předpověditelné pokyny pro dostupnost podpory produktu.


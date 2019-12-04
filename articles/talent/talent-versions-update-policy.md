---
title: Systémové požadavky aplikace Talent
description: Toto téma obsahuje požadavky na Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0bd7d7051dd01834f306e165af55d740192b99e0
ms.sourcegitcommit: caeb24027831efccbc316ff8e7f9e62b42010d65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/19/2019
ms.locfileid: "2818472"
---
# <a name="talent-system-requirements"></a>Systémové požadavky aplikace Talent

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány požadavky pro aplikaci Microsoft Dynamics 365 Talent, včetně aplikací Attract, Onboard a Core HR. Dále jsou zde uvedeny země a oblasti, ve kterých je Talent k dispozici, a informace o jazycích a lokalizaci dat aplikace Talent. Navíc toto téma obsahuje zásady aktualizace pro aplikaci Talent.

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče

Aplikace Microsoft Dynamics 365 Talent může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému: 

*   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
*   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
*   Google Chrome (nejnovější veřejně dostupná verze)
*   Apple Safari (nejnovější veřejně dostupná verze)

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. 

> [!NOTE]
> * K zachycení bitových kopií, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalováno rozšíření Chrome. 
> * Editor pracovního postupu je spuštěn jako aplikace ClickOnce. Pouze Microsoft Edge a Internet Explorer (podporované verze Microsoft Windows) podporují aplikace ClickOnce. Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.
> * K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.
>   Požadavky na síť
> * Dynamics 365 Talent je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje aplikaci Talent. Doporučujeme otestovat čekací dobu v síti na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").
> * Požadavky na šířku pásma pro Talent závisí na danému scénáři. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).
> 
> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Talent.

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office

* Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací s Office").
* Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

## <a name="regional-availability-languages-and-localization"></a>Regionální dostupnost, jazyky a lokalizace

Můžete si stáhnout PDF soubor se zeměmi, oblastmi a jazyky, které Talent podporuje, na [Mezinárodní dostupnosti Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Zatímco je uživatelské rozhraní lokalizováno do jiných jazyků, budou všechna uživatelská data uložena v jazyce, ve kterém byla zadána. E-maily a šablony můžete vytvářet v jiných jazycích, ale data jako informace o plánování budou v tomto okamžiku k dispozici pouze v angličtině.

Pokud jste vývojáři a máte zájem o vytváření vlastních nastavení specifických pro zemi nebo oblast, nebo o vytváření řešení pro zemi nebo oblast, která není aktuálně podporována společností Microsoft, prohlédněte si část [Globalizace](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


---
title: Systémové požadavky
description: Tento článek popisuje požadavky pro Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e7d7389c1bcf0f6024464e37b36d39efae5b832
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111754"
---
# <a name="system-requirements"></a>Systémové požadavky

Tento článek popisuje požadavky pro Microsoft Dynamics 365 Human Resources. Dále jsou zde uvedeny země a oblasti, ve kterých je aplikace Human Resources k dispozici, a informace o jazycích a lokalizaci dat aplikace Human Resources.

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče

Aplikace Human Resources může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému: 

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
> * Human Resources je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje aplikaci Human Resources. Doporučujeme otestovat čekací dobu v síti na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").
> * Požadavky na šířku pásma pro Human Resources závisí na daném scénáři. Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).
> 
> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Human Resources.

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office

* Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací s Office").
* Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

## <a name="regional-availability-languages-and-localization"></a>Regionální dostupnost, jazyky a lokalizace

Můžete si stáhnout PDF soubor se zeměmi, oblastmi a jazyky, které Human Resources podporuje, na [Mezinárodní dostupnosti Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Zatímco je uživatelské rozhraní lokalizováno do jiných jazyků, budou všechna uživatelská data uložena v jazyce, ve kterém byla zadána. E-maily a šablony můžete vytvářet v jiných jazycích, ale data jako informace o plánování budou v tomto okamžiku k dispozici pouze v angličtině.

Pokud jste vývojáři a máte zájem o vytváření vlastních nastavení specifických pro zemi nebo oblast, nebo o vytváření řešení pro zemi nebo oblast, která není aktuálně podporována společností Microsoft, prohlédněte si část [Globalizace](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
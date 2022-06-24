---
title: Systémové požadavky
description: Tento článek uvádí seznam systémových požadavků na Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07d14dfe0e6b53c9489c284520a24b97d9887fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879330"
---
# <a name="system-requirements"></a>Systémové požadavky

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek uvádí seznam systémových požadavků na Microsoft Dynamics 365 Human Resources. Dále jsou zde uvedeny země a oblasti, ve kterých je aplikace Human Resources k dispozici, a informace o jazycích a lokalizaci dat aplikace Human Resources.

## <a name="supported-web-browsers"></a>Podporované webové prohlížeče

Uživatelé mohou k aplikaci Microsoft Dynamics 365 Human Resources přistupovat v kterémkoli z následujících webových prohlížečů v určeném operačním systému: 

*   Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10
*   Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7
*   Google Chrome (nejnovější veřejně dostupná verze)
*   Apple Safari (nejnovější veřejně dostupná verze)

Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru. 

## <a name="special-considerations"></a>Speciální předpoklady

* Chcete-li umožnit záznamníku úloh pořídit snímky obrazovky a zahrnout je do generovaných dokumentů aplikace Microsoft Word, musíte nainstalovat předběžnou verzi doplňku Chrome.
* Editor pracovního postupu je spuštěn jako aplikace ClickOnce. Pouze Microsoft Edge a Internet Explorer (podporované verze Microsoft Windows) podporují aplikace ClickOnce. Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.
* K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.

## <a name="network-requirements"></a>Požadavky na síť

* Human Resources je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně. Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje aplikaci Human Resources. Doporučujeme otestovat čekací dobu v síti na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").
* Požadavky na šířku pásma pro Human Resources závisí na daném scénáři. Běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).
 
> [!WARNING]
> Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma. Souběžné využití daného umístění je velmi obtížné vypočítat. Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Human Resources.

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office

* Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac. Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací s Office").
* Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.

## <a name="regional-availability-languages-and-localization"></a>Regionální dostupnost, jazyky a lokalizace

Můžete si stáhnout PDF soubor se zeměmi, oblastmi a jazyky, které Human Resources podporuje, na [Mezinárodní dostupnosti Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Zatímco je uživatelské rozhraní lokalizováno do jiných jazyků, budou všechna uživatelská data uložena v jazyce, ve kterém byla zadána. E-maily a šablony můžete vytvářet v jiných jazycích, ale data jako informace o plánování budou v tomto okamžiku k dispozici pouze v angličtině.

Pokud jste vývojáři a máte zájem o vytváření vlastních nastavení specifických pro zemi nebo oblast, nebo o vytváření řešení pro zemi nebo oblast, která není aktuálně podporována společností Microsoft, prohlédněte si část [Globalizace](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]

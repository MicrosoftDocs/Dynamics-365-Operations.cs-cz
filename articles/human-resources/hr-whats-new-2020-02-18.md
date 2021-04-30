---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (18. února 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 18. únoru 2020.
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8109826df93f9916914a2db3876ee0f9107985f9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890951"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (18. února 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.2903. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="platform-update-32"></a>Aktualizace platformy 32 

Nyní je k dispozici aktualizace platformy 32. Další informace naleznete v tématu [Co je nového nebo změněné v aktualizaci Platform update 32 pro Finance and Operations (únor 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Vyhledávací hodnoty se pamatují při změně možností zobrazení ve zjednodušeném formuláři zaměstnanců (383833)

Nový formulář **Pracovníka** nyní pamatuje hodnoty vyhledávání, když změníte možnosti zobrazení a použijete změny.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Souhrnné dlaždice správy kompenzací v náhledu funkce přesměrovat na nesprávný formulář (401861)

Dlaždice správy pevné a variabilní kompenzace nyní zobrazují správné záznamy ve formuláři nový **pracovník**. Týká se pouze zjednodušené funkce náhledu formuláře zaměstnance. Tuto funkci náhledu lze povolit ve **Správě funkcí**. Další informace naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Prázdné pole stavu pro některé záznamy požadavků na dovolenou v Dataverse (414915)

Tato změna opravuje problém v Dataverse v případě, že je pole **Stav** v požadavku na dovolenou nastaveno na **Zkontrolovat**. Dataverse nyní odráží stav.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Analýza mezer v dovednostech je možná pouze pro přiřazenou úlohu (411390)

Nyní můžete provést analýzu mezer v dovednostech u kterékoli úlohy definované v modulu Human Resources.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Systémovou měnu nelze synchronizovat z Dataverse do modulu Human Resources v nových prostředích (418011)

Systémovou měnu v Dataverse lze nyní synchronizovat s Human Resources.

## <a name="in-preview"></a>Náhled

- [Funkce náhledu pracovního volna a absence](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Funkce náhledu správy zaměstnaneckých výhod](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Již brzy

### <a name="updated-dataverse-solution"></a>Aktualizované řešení služby Dataverse

Nové řešení Dataverse bude brzy k dispozici po provedení následujících změn:

| Popis | Změna |
| ----------------------------------------- | --- |
| Změny entity **práce/pozice** | Přidána **Oblast kompenzace**</br>Přidání **finančních dimenzí** |
| Změny entity **pracovníka** | Přidání **sekvence jmen**</br>Přidaná možnost **Práce z domova**</br>Přidán **jazyk**</br>Přidáno **Datum služebního věku**</br>Přidáno **Datum výročí**</br>Přidáno **Datum původního přijetí** |
| Změny **entity zaměstnání** | Přidání **finančních dimenzí**</br>Přidán **Důvod pro výpověď**</br>**Datum ukončení** přejmenováno z **data přechodu**</br>Přidáno **datum zkušební doby** |
| Změny entity **adresy pracovníka** | Přidána **Adresa ulice**</br>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis |
| Nové entity nastavení s nastavením variabilní kompenzace | **Typ plánu variabilní kompenzace**</br>**Plán variabilní kompenzace**</br>**Pravidla připsání**</br>**Úroveň plánu variabilní kompenzace** |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | Byla přidána **entita pracovního kalendáře** |
| Nová entita **Mzdové podrobnosti o pozici** | Byla přidána položka **Mzdové podrobnosti o pozici**. |
| Nová entita **Pozice** | Byla přidána položka **Pozice**. Nová entita **Nadpis** bude zahrnuta do procesu synchronizace mezi lidskými zdroji a Dataverse. Na počátku nebude odkazovat z entit **Pracovní pozice** nebo **Úloha**. |

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
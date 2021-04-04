---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (12. února 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 12. únoru 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f03c0230949ceb974d4b4d22623c80a1509eeb32
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463807"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (12. února 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.2867. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Existující entity CompFixedEmpls a HcmPersonImage by měly být přístupné z OData (414178)

V tomto týdenním vydání jsou entity **CompFixedEmpls** a **HcmPersonImage** nyní veřejné a dostupné prostřednictvím ODAta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Odstranění zaměstnání z Dataverse nefunguje, pokud nejsou aktivní podrobnosti o zaměstnání (403193)

Tato změna nyní umožňuje odstranit zaměstnání pomocí Dataverse v případě, že neexistují žádné aktivní podrobnosti o zaměstnání.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Změny workflowu registrace kurzu dokončení a chyby po druhém schválení (409749)

Workflow registrace kurzu byl aktualizován za účelem povolení více schvalujících.

## <a name="in-preview"></a>Náhled

Od 3. února 2020 jsou k dispozici následující funkce náhledu:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Již brzy

### <a name="platform-update-32"></a>Aktualizace platformy 32 

Brzy bude k dispozici aktualizace platformy č. 32. [Další informace o aktualizaci platformy číslo 32 naleznete zde](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

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
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
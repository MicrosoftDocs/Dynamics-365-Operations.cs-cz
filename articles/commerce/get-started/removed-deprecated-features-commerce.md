---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443911"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.11
### <a name="data-action-hooks"></a>Zavěšení datových akcí
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce háčků datových akcí byla zastaralá kvůli problémům s výkonem. |
| **Nahrazeno jinou funkcí?**   | Doporučuje se místo toho použít [přepisy akce dat](../e-commerce-extensibility/data-action-overrides.md) ke změně obchodní logiky ve vrstvě akce dat.|
| **Ovlivněné oblasti produktu**         | Akce dat rozšiřitelnosti elektronického obchodování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>Operace POS 803 – Vyzvednutí a příjem
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Operace stahování a přijímání jsou zastaralé kvůli novému přepracování operací. |
| **Nahrazeno jinou funkcí?**   | Ano. Je nahrazen dvěma novými operacemi POS: příchozí operace (804) a odchozí operace (805).|
| **Ovlivněné oblasti produktu**         | Aplikace Pokladní místo (POS) |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od vydání 10.0.10 již operace vyzvednutí a přijetí nebude mít žádné nové aktualizace funkcí. V budoucích verzích budou pro tuto operaci provedeny pouze kritické opravy chyb. Doporučuje se, aby všichni zákazníci přešli na nové [příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) a [odchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), které budou nadále součástí našeho dlouhodobého přehledu aplikací. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Rozhraní API obchodu GetProductAvailabilities a GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Byla vytvořena nová optimalizovaná rozhraní API nahrazující rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. |
| **Nahrazeno jinou funkcí?**   | Ano: Nahrazuje je rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability. |
| **Ovlivněné oblasti produktu**         | Sada SDK pro elektronický obchod |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ukončeno: Od vydání 10.0.7 nebudou investovány žádné technické prostředky do rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. Organizace, které používají tato API ve svých implementacích elektronického obchodování, by měly přejít na nová rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability a povolit [Funkci pro optimalizaci dostupnosti produktu](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).

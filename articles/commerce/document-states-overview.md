---
title: Stavy dokumentu a životního cyklu
description: V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770428"
---
# <a name="document-states-and-lifecycle"></a>Stavy dokumentu a životního cyklu

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Popisy stavů dokumentu

V tématu [Prvky stránky](page-elements-overview.md) jsou uvedeny různé typy dokumentů v systému správy obsahu (CMS). Tyto typy dokumentů mohou mít v nástroji pro tvorbu obsahu několik stavů. Stavy dokumentu pomáhají předcházet konfliktům dat a posilují správy verzí. Určují, kdo může dokumenty měnit, kdy lze dokumenty změnit a kdy mohou změny zobrazit jiní uživatelé.

V následující tabulce jsou uvedeny možné stavy dokumentu pro prvky stránky v řešení Commerce.

| Stav dokumentu | Popis |
|---|---|
| Rezervováno | Je-li položka CMS rezervována pro vás, nemůže být upravována jinými ověřenými uživateli systému. Jakékoli změny položky, které provedete, budou viditelné pouze pro vás. |
| Vráceno | Při vrácení položky CMS se změnami jsou všechny změny viditelné pro ostatní ověřené uživatele systému a tito uživatelé si pak mohou položku rezervovat a upravit. Při každém vrácení se změnami se vytvoří záznam verze dokumentu v historii položky. |
| Publikováno | Je-li publikována položka CMS, je vložena na živý web a může být v Internetu zjistitelná neověřenými externími uživateli. Položky lze publikovat pouze v případě, že byly vráceny se změnami. |
| Uloženo | Změny provedené u rezervované položky CMS lze uložit do CMS před tím, než je položka vrácena se změnami nebo publikována. Tyto uložené změny nejsou viditelné pro ostatní ověřené uživatele systému, dokud není položka vrácena se změnami. Nejsou viditelné pro externí uživatele, dokud není položka publikována. |
| Zahozená rezervace | Pokud dojde k zahození rezervované položky CMS, budou odstraněny všechny uložené změny a položka bude vrácena na verzi, která byla naposledy vrácena se změnami. |

## <a name="additional-resources"></a>Další zdroje

[Způsoby přidání obsahu](add-manage-content.md)

[Glosář modelu stránky](page-elements-overview.md)

[Práce s moduly](work-with-modules.md)

[Práce s fragmenty](work-with-fragments.md)

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Přizpůsobení navigace na webu](customize-site-navigation.md)

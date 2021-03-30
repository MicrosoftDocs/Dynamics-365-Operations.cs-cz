---
title: Stavy dokumentu a životního cyklu
description: V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 457b1ac7afb8cad57399572acf429d208db917af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230527"
---
# <a name="document-states-and-lifecycle"></a>Stavy dokumentu a životního cyklu

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány různé stavy dokumentu pro prvky stránky v řešení Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Popisy stavů dokumentu

V tématu [Prvky stránky](page-elements-overview.md) jsou uvedeny různé typy dokumentů v systému správy obsahu (CMS). Tyto typy dokumentů mohou mít v nástroji pro tvorbu obsahu několik stavů. Stavy dokumentu pomáhají předcházet konfliktům dat a posilují správy verzí. Určují, kdo může dokumenty měnit, kdy lze dokumenty změnit a kdy mohou změny zobrazit jiní uživatelé.

V následující tabulce jsou uvedeny možné stavy dokumentu pro prvky stránky v řešení Commerce.

| Stav dokumentu      | Akce konfigurátoru webu        | popis                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Rezervováno         | Vyberte možnost **Upravit**.           | Příslušný dokument je rezervován pro vás. V době, kdy je dokument v tomto stavu, nemůže být změněn jinými ověřenými uživateli systému a veškeré změny provedené v dokumentu jsou viditelné pouze pro vás. |
| Uloženo               | Zvolte **Uložit**.           | Změny provedené v rezervovaném dokumentu budou uloženy do databáze, ale dokument ještě nebyl vrácen se změnami ani publikován. Tyto uložené změny nejsou viditelné pro ostatní ověřené uživatele systému, dokud autor nevybere **Dokončit úpravy**. Nejsou viditelné pro externí uživatele, dokud není položka publikována. |
| Zahozená rezervace | Vyberte **Zrušit úpravy**.  | Všechny změny v rezervovaném dokumentu budou odstraněny a položka se vrátí k poslední verzi, která byla vrácena se změnami. |
| Vráceno          | Vyberte **Dokončit úpravy**. | Upravený dokument je vrácen se změnami. Všechny změny jsou viditelné pro ostatní ověřené uživatele systému a tito uživatelé pak mohou dokument upravovat. Při každém vrácení se změnami se vytvoří záznam verze dokumentu v historii položky. |
| Publikováno           | Zvolte **Publikovat**.        | Dokument je publikován a změny jsou vloženy do živého pracoviště a mohou být vyřízeny externími uživateli. Položky lze publikovat pouze v případě, že byly nejprve vráceny se změnami výběrem **Dokončit úpravy**. |

## <a name="additional-resources"></a>Další prostředky

[Způsoby přidání obsahu](add-manage-content.md)

[Glosář modelu stránky](page-elements-overview.md)

[Práce s publikovacími skupinami](publish-groups.md)

[Povolení a používání sdílení napříč kanály](cross-channel-sharing.md)

[Práce s moduly](work-with-modules.md)

[Práce s fragmenty](work-with-fragments.md)

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Přizpůsobení navigace na webu](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
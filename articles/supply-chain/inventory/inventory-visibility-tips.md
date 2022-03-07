---
title: Tipy ohledně doplňku Viditelnost zásob
description: Toto téma obsahuje několik tipů, které byste měli zvážit při nastavení a použití doplňku Viditelnost zásob.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920794"
---
# <a name="inventory-visibility-tips"></a>Tipy ohledně doplňku Viditelnost zásob

[!include [banner](../includes/banner.md)]

Zde je několik tipů, které byste měli zvážit při nastavení a použití doplňku Viditelnost zásob:

- V současné době podporuje doplněk Viditelnost zásob pouze prostředí Microsoft Dataverse, která byla vytvořena pomocí Microsoft Dynamics Lifecycle Services (LCS). Pokud vaše prostředí Dataverse bylo vytvořeno jiným způsobem (například pomocí centra pro správu Power Apps) a pokud je propojeno s vaším prostředím Dynamics 365 Supply Chain Management, musíte nejprve požádat produktový tým pro Viditelnost zásob a vyřešit problém s mapováním. Tým můžete kontaktovat na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tým vám dá vědět, až bude vaše prostředí připraveno k instalaci doplňku Viditelnost zásob.
- Pokud máte více než jedno prostředí LCS, vytvořte jinou aplikaci Azure Active Directory (Azure AD) pro každé prostředí. Pokud k instalaci doplňku Viditelnost zásob pro různá prostředí použijete stejné ID aplikace a ID klienta, u starších prostředí dojde k problému s tokenem. Platná bude pouze poslední instance doplňku Viditelnost zásob, která byla nainstalována.
- Doplněk Viditelnost zásob není aktuálně podporován v cloudových prostředích. Je podporován pouze pro prostředí úrovně 2+.
- Aplikační programovací rozhraní (API) aktuálně podporuje dotazování až 100 jednotlivých položek podle hodnoty `ProductID`. V každém dotazu také může být zadáno více hodnot `SiteID` a `LocationID`. Maximální limit je definován jako `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Zdroj dat `fno` je vyhrazen pro Supply Chain Management. Pokud je váš doplněk Viditelnost zásob integrován s prostředím Supply Chain Management, doporučujeme neodstraňovat konfigurace související s `fno` ve [zdroji dat](inventory-visibility-configuration.md#data-source-configuration).
- V současné době se [konfigurace oddílu](inventory-visibility-configuration.md#partition-configuration) skládá ze dvou základních dimenzí (`SiteId` a `LocationId`), které ukazují, jak jsou data distribuována. Operace ve stejném oddílu mohou poskytovat vyšší výkon za nižší náklady. Ve výchozím nastavení obsahuje řešení tuto konfiguraci oddílu. Z tohoto důvodu ji *nemusíte sami definovat*. Nepřizpůsobujte výchozí konfiguraci oddílu. Pokud ji odstraníte nebo změníte, pravděpodobně způsobíte neočekávanou chybu.
- Základní dimenze, které jsou definovány v konfiguraci oddílu, by neměly být definovány v [konfiguraci hierarchie indexu produktu](inventory-visibility-configuration.md#index-configuration).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

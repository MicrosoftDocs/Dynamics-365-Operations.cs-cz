---
title: Tipy pro Inventory Visibility
description: Tento článek obsahuje několik tipů, které byste měli zvážit při nastavení a použití doplňku Viditelnost zásob.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306078"
---
# <a name="inventory-visibility-tips"></a>Tipy ohledně doplňku Viditelnost zásob

[!include [banner](../includes/banner.md)]

Zde je několik tipů, které byste měli zvážit při nastavení a použití doplňku Viditelnost zásob:

- V současné době podporuje doplněk Viditelnost zásob pouze prostředí Microsoft Dataverse, která byla vytvořena pomocí Microsoft Dynamics Lifecycle Services (LCS). Pokud vaše prostředí Dataverse bylo vytvořeno jiným způsobem (například pomocí centra pro správu Power Apps) a pokud je propojeno s vaším prostředím Dynamics 365 Supply Chain Management, musíte nejprve požádat produktový tým pro Viditelnost zásob a vyřešit problém s mapováním. Tým můžete kontaktovat na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tým vám dá vědět, až bude vaše prostředí připraveno k instalaci doplňku Viditelnost zásob.
- Pokud máte více než jedno prostředí LCS, vytvořte jinou aplikaci Azure Active Directory (Azure AD) pro každé prostředí. Pokud k instalaci doplňku Viditelnost zásob pro různá prostředí použijete stejné ID aplikace a ID klienta, u starších prostředí dojde k problému s tokenem. Platná bude pouze poslední instance doplňku Viditelnost zásob, která byla nainstalována.
- Doplněk Viditelnost zásob není aktuálně podporován v cloudových prostředích. Je podporován pouze pro prostředí úrovně 2+.
- Aplikační programovací rozhraní (API) aktuálně podporuje dotazování až 100 jednotlivých položek podle hodnoty `ProductID`. V každém dotazu také může být zadáno více hodnot `SiteID` a `LocationID`. Maximální limit je definován jako `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Hromadné API může vrátit maximálně 512 záznamů pro každý požadavek.
- Zdroj dat `fno` je vyhrazen pro Supply Chain Management. Pokud je váš doplněk Viditelnost zásob integrován s prostředím Supply Chain Management, doporučujeme neodstraňovat konfigurace související s `fno` ve [zdroji dat](inventory-visibility-configuration.md#data-source-configuration).
- Viditelnost inventáře nemůže změnit žádná data pro zdroj dat `fno`. Tok dat je jednosměrný, což znamená, že veškeré změny množství pro zdroj dat `fno` musí pocházet z vašeho prostředí Supply Chain Management. Proto nemůžete použít API k odesílání žádostí o změnu nebo rezervaci dostupného množství pro zdroj dat `fno`.
- Pokud do svého prostředí Supply Chain Management přidáte jedno nebo více nových opatření, měli byste je přidat také do Viditelnosti zásob. Všechny změny množství pro nová opatření však musí pocházet z vašeho prostředí Supply Chain Management.
- V současné době se [konfigurace oddílu](inventory-visibility-configuration.md#partition-configuration) skládá ze dvou základních dimenzí (`SiteId` a `LocationId`), které ukazují, jak jsou data distribuována. Operace ve stejném oddílu mohou poskytovat vyšší výkon za nižší náklady. Ve výchozím nastavení obsahuje řešení tuto konfiguraci oddílu. Z tohoto důvodu ji *nemusíte sami definovat*. Nepřizpůsobujte výchozí konfiguraci oddílu. Pokud ji odstraníte nebo změníte, pravděpodobně způsobíte neočekávanou chybu.
- Základní dimenze, které jsou definovány v konfiguraci oddílu, by neměly být definovány v [konfiguraci hierarchie indexu produktu](inventory-visibility-configuration.md#index-configuration).
- [Konfigurace hierarchie indexu produktu](inventory-visibility-configuration.md#index-configuration) musí obsahovat alespoň jednu hierarchii indexu (například obsahující základní dimezni `Empty`), jinak dotazy selžou s chybou „Nebyla nastavena žádná hierarchie indexu.“
- Zdroj dat `@iv` je předdefinovaný zdroj dat a fyzické míry definované v `@iv` s předponou `@` jsou předem definovaná opatření. Tyto míry jsou předdefinovanou konfigurací pro funkci alokace, takže je neměňte ani neodstraňujte, protože při používání funkce alokace pravděpodobně narazíte na neočekávané chyby.
- K předdefinované vypočítané míře `@iv.@available_to_allocate` můžete přidat nové fyzické míry, ale nesmíte změnit její název.
- Pokud obnovíte databázi Supply Chain Management, může obnovená databáze obsahovat data, která již nejsou konzistentní s daty dříve synchronizovanými pomocí Viditelnosti zásob v Dataverse. Tato nekonzistence dat může způsobit systémové chyby a další problémy. Proto je důležité, abyste vždy vyčistili všechna související data viditelnosti zásob z Dataverse před obnovením databáze Supply Chain Management. Informace naleznete na [Vyčistěte data viditelnosti zásob z Dataverse před obnovením databáze Supply Chain Management](inventory-visibility-setup.md#restore-environment-database)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

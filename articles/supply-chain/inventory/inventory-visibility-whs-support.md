---
title: Podpora Viditelnosti zásob u položek WMS
description: Tento článek popisuje podporu Viditelnosti zásob u položek, které jsou povoleny ve skladových procesech (položky WMS).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762732"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Podpora Viditelnosti zásob u položek WMS

[!include [banner](../includes/banner.md)]

Tento článek popisuje podporu Viditelnosti zásob u položek, které jsou povoleny ve skladových procesech (WMS). Funkce, která přidává tuto schopnost do Viditelnosti zásob, se jmenuje *Rozšířené řízení skladu*.

## <a name="wms-items"></a>Položky WMS

Položka WMS je položka, která je povolena pro WMS a zpracovává se ve skladu, který také podporuje WMS.

Více informací o WMS a modulu **Správa skladu** v Microsoft Dynamics 365 Supply Chain Management najdete v článku [Přehled skladového hospodářství](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Rozsah funkce

Funkce Rozšířené WMS pro Viditelnost zásob se zaměřuje na okamžité výpočty množství, které jsou založeny na dotazech na zásoby na skladě. Tato funkce není určena k tomu, aby vám umožnila používat Viditelnost zásob ke správě činností zpracování skladu obecně. Viditelnost zásob svým uživatelům neodhaluje koncepty specifické pro sklad. Zde je několik příkladů těchto konceptů:

- Hierarchie rezervací
- Zda má položka nebo sklad povoleno WMS
- ID skupiny klasifikace jednotek
- Procesy specifické pro sklad, jako jsou zásilky, nakládky, vlny a práce

Viditelnost zásob odvozuje tyto informace na základě dat odeslaných ze Supply Chain Management. Data specifická pro WMS (jinými slovy data z tabulky `WHSInventReserve`) uživatelé nevidí.

Když použijete funkci Rozšířené WMS pro Viditelnost zásob, všechny výsledky dotazů budou totožné s výsledky dotazů, které jsou vytvořeny přímo v Supply Chain Management. Nebudou však totožné s výsledky dotazů vytvořených pomocí mobilní aplikace Warehouse Management, protože mobilní aplikace používá mírně odlišnou logiku výpočtu.

## <a name="when-to-use-the-feature"></a>Kdy použít tuto funkci

Doporučujeme použít funkci WMS pro Viditelnost inventáře ve scénářích, kde jsou splněny všechny následující podmínky:

- Synchronizujete data Supply Chain Management s Viditelností zásob.
- Používáte WMS v Supply Chain Management.
- Uživatelé provádějí rezervace pro položky WMS pod úrovní skladu (například na úrovni registrační značky, protože zpracováváte práci ve skladu).

V jiných scénářích budou výsledky dotazů na aktuální zásoby na skladě stejné, bez ohledu na to, zda je povolena funkce Rozšířené WMS pro Viditelnost zásob. Výkon aplikace bude navíc lepší, pokud tuto funkci v těchto scénářích nepovolíte, protože snížíte počet výpočtů a režii.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Povolení funkce WMS pro Viditelnost zásob

Chcete-li povolit funkci WMS pro Viditelnost zásob, postupujte takto.

1. Přihlaste se do prostředí Supply Chain Management jako správce.
1. Otevřete pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce v tomto pořadí:

    1. *Integrace viditelnosti zásob*
    1. *Povolte skladové položky ve viditelnosti zásob*

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry integrace Viditelnosti zásob**.
1. Na kartě **Povolit položky WMS** nastavte možnost **Povolit položky WMS** na *Ano*.
1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace** a potom na kartě **Správa funkcí** zapněte funkci *Rozšířené WHS*.
1. V Supply Chain Management přejděte do uzlu **Řízení zásob \> Periodické úlohy \> Integrace Viditelnosti zásob**.
1. V podokně akcí vyberte **Zakázat**, chcete-li dočasně zakázat Viditelnost zásob.
1. V podokně Akce vyberte možnost **Povolit**, když chcete Viditelnost zásob znovu povolit. Doplněk se znovu načte a nová funkce je nyní povolena. Vaše data související s WMS se začnou synchronizovat s Viditelností zásob.

## <a name="query-on-hand-quantities-of-wms-items"></a>Dotaz na množství položek WMS na skladě

Chcete-li se dotazovat na položky WMS, použijte totéž [aplikační programovací rozhraní (API) a syntaxi zpráv](inventory-visibility-api.md) které používáte u ne-WMS položek. Nemusíte zadávat, zda položka je, či není položkou WMS. Viditelnost zásob automaticky rozlišuje položky na základě uložených dat.

Výsledky z dotazů na položky WMS jsou v podstatě stejné jako výsledky pro ne-WMS položky. Jediný rozdíl je v tom, že následující fyzické míry ze zdroje dat `fno` se v Supply Chain Management počítají na základě logiky WMS:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Všechny ostatní fyzické míry se počítají tak, jak jsou, když je vypnutá funkce WMS pro Viditelnost zásob.

Podrobné informace o tom, jak fungují výpočty množství na skladě WMS u položek WMS, najdete v článku [Rezervace ve správě skladu](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Zobrazení seznamu a datová entita pro položky WMS

Stránka **Předběžné načtení souhrnu viditelnosti zásob** obsahuje zobrazení entity *Výsledky předběžného načtení indexového dotazu na zásoby na skladě*. Na rozdíl od entity *Souhrn zásob* poskytuje entita *Výsledky předběžného načtení indexového dotazu na zásoby na skladě* seznam zásob produktů na skladě spolu s vybranými dimenzemi. Viditelnost zásob synchronizuje předem načtená souhrnná data každých 15 minut.

Pokud používáte viditelnost zásob s položkami WMS a chcete zobrazit seznam položek WMS, doporučujeme zapnout funkci *Předem načíst souhrn viditelnosti zásob* (viz také [Předem načíst zjednodušený dotaz na skladové zásoby](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Odpovídající datová entita v Dataverse ukládá výsledek předběžného načtení dotazu, který se aktualizuje každých 15 minut. Název datové entity je `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Entita Dataverse je jen ke čtení. Data můžete zobrazit a exportovat v entitách Viditelnost zásob, ale **nemůžete je upravit**.

Změny množství položek WMS, které jsou uloženy ve zdroji dat Supply Chain Management (`fno`), jsou zakázány. Toto chování odpovídá chování ostatních funkcí viditelnosti zásob. Toto omezení je vynuceno, aby se zabránilo konfliktům.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>Kompatibilita položek WMS pro další funkce ve viditelnosti zásob

Jsou podporovány [předběžné rezervace](inventory-visibility-reservations.md) a [alokace zásob](inventory-visibility-allocation.md) položek WMS. Do výpočtů předběžných rezervací a alokací můžete zahrnout fyzické míry související s WMS.

## <a name="calculate-available-to-promise-quantities"></a>Výpočet množství, která lze slíbit

Řešení plně podporuje funkci [Lze slíbit (ATP)](inventory-visibility-available-to-promise.md) u WMS položek. Můžete definovat výpočty ATP, aniž byste se museli starat o podrobnosti pro WMS specifické.

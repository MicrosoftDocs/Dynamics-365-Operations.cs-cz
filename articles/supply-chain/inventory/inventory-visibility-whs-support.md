---
title: Podpora Viditelnosti zásob u položek WMS
description: Tento článek popisuje podporu Viditelnosti zásob u položek, které jsou povoleny ve skladových procesech (položky WMS).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066603"
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

Doporučujeme použít funkci Rozšířené WMS pro Viditelnost inventáře ve scénářích, kde jsou splněny všechny následující podmínky:

- Synchronizujete data Supply Chain Management s Viditelností zásob.
- Používáte WMS v Supply Chain Management.
- Uživatelé provádějí rezervace pro položky WMS na jiných úrovních, než je úroveň skladu (například proto, že používáte práci ve skladu).

V jiných scénářích budou výsledky dotazů na aktuální zásoby na skladě stejné, bez ohledu na to, zda je povolena funkce Rozšířené WMS pro Viditelnost zásob. Výkon aplikace bude navíc lepší, pokud tuto funkci v těchto scénářích nepovolíte, protože snížíte počet výpočtů a režii.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Povolení funkce Rozšířené WMS pro Viditelnost zásob

Chcete-li povolit funkci Rozšířené WMS pro Viditelnost zásob, postupujte takto.

1. Přihlaste se do prostředí Supply Chain Management jako správce.
1. Otevřete pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce v tomto pořadí:

    1. *Integrace viditelnosti zásob*
    1. *Povolte skladové položky ve viditelnosti zásob*

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry integrace Viditelnosti zásob**.
1. Na kartě **Povolit položky WMS** nastavte možnost **Povolit položky WMS** na *Ano*.
1. Přihlaste se do Power Apps.
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

Všechny ostatní fyzické míry se počítají tak, jak jsou, když je vypnutá funkce Rozšířené WMS pro Viditelnost zásob.

Podrobné informace o tom, jak fungují výpočty množství na skladě WMS u položek WMS, najdete v článku [Rezervace ve správě skladu](https://www.microsoft.com/download/details.aspx?id=43284).

Datové entity exportované do Dataverse zatím nemohou aktualizovat množství u položek WMS. Množství, která jsou zobrazena v datových entitách, jsou správná jak u ne-WMS položek, tak u množství, která nejsou ovlivněna logikou WMS (tj. `AvailPhysical`,`AvailOrdered`,`ReservPhysical` a `ReservOrdered` ve zdroji dat `fno`).

Změny množství položek WMS, které jsou uloženy ve zdroji dat Supply Chain Management, jsou zakázány. Pokud jde o další funkce Viditelnosti zásob, toto omezení je vynuceno, aby se zabránilo konfliktům.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Předběžná rezervace položek WMS ve Viditelnosti zásob

Obecně platí, že [předběžné rezervace](inventory-visibility-reservations.md) položek WMS jsou podporovány. Do výpočtů předběžných rezervací můžete zahrnout fyzické míry související s WMS. 

Známým omezením je nemožnost použít výpočet *k dispozici pro rezervaci* u položek WMS. Pokud tedy existuje rezervace nad aktuálními dimenzemi, kde dochází k předběžné rezervaci, výpočet *k dispozici pro rezervaci* je nesprávný. Předběžné rezervace nebudou ovlivněny, když je v [rozhraní API pro předběžné rezervace](inventory-visibility-api.md#create-one-reservation-event) zakázána možnost **ifCheckAvailForReserv**.

Toto omezení platí také pro funkce a přizpůsobení, které jsou založeny na předběžných rezervacích (jako je alokace).

## <a name="calculate-available-to-promise-quantities"></a>Výpočet množství, která lze slíbit

Řešení plně podporuje funkci [Lze slíbit (ATP)](inventory-visibility-available-to-promise.md) u WMS položek. Můžete definovat výpočty ATP, aniž byste se museli starat o podrobnosti pro WMS specifické.

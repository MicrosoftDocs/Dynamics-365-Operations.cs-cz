---
title: Podpora Viditelnosti zásob u položek WHS
description: Toto téma popisuje podporu Viditelnosti zásob u položek, které jsou povoleny v rozšířených skladových procesech (položky WHS).
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
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625384"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Podpora Viditelnosti zásob u položek WHS

[!include [banner](../includes/banner.md)]

Toto téma popisuje podporu Viditelnosti zásob u položek, které jsou povoleny v rozšířených skladových procesech (položky WHS). Funkce, která přidává tuto schopnost do Viditelnosti zásob, se jmenuje *Rozšířené řízení skladu*.

## <a name="whs-items"></a>Položky WHS

Položka WHS je položka, která je povolena v rozšířených skladových procesech (WHS) a zpracovává se ve skladu, který také podporuje WHS.

Více informací o WHS a modulu **Správa skladu** v Microsoft Dynamics 365 Supply Chain Management najdete v článku [Přehled skladového hospodářství](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Rozsah funkce

Funkce Rozšířené WHS pro Viditelnost zásob se zaměřuje na okamžité výpočty množství, které jsou založeny na dotazech na zásoby na skladě. Tato funkce není určena k tomu, aby vám umožnila používat Viditelnost zásob ke správě činností zpracování skladu obecně. Viditelnost zásob svým uživatelům neodhaluje koncepty specifické pro sklad. Zde je několik příkladů těchto konceptů:

- Hierarchie rezervací
- Zda má položka nebo sklad povoleno WHS
- ID skupiny klasifikace jednotek
- Procesy specifické pro sklad, jako jsou zásilky, nakládky, vlny a práce

Viditelnost zásob odvozuje tyto informace na základě dat odeslaných ze Supply Chain Management. Data specifická pro WHS (jinými slovy data z tabulky `WHSInventReserve`) uživatelé nevidí.

Když použijete funkci Rozšířené WHS pro Viditelnost zásob, všechny výsledky dotazů budou totožné s výsledky dotazů, které jsou vytvořeny přímo v Supply Chain Management. Nebudou však totožné s výsledky dotazů vytvořených pomocí mobilní aplikace Warehouse Management, protože mobilní aplikace používá mírně odlišnou logiku výpočtu.

## <a name="when-to-use-the-feature"></a>Kdy použít tuto funkci

Doporučujeme použít funkci Rozšířené WHS pro Viditelnost inventáře ve scénářích, kde jsou splněny všechny následující podmínky:

- Synchronizujete data Supply Chain Management s Viditelností zásob.
- Používáte WHS v Supply Chain Management.
- Uživatelé provádějí rezervace pro položky WHS na jiných úrovních, než je úroveň skladu (například proto, že používáte práci ve skladu).

V jiných scénářích budou výsledky dotazů na aktuální zásoby na skladě stejné, bez ohledu na to, zda je povolena funkce Rozšířené WHS pro Viditelnost zásob. Výkon aplikace bude navíc lepší, pokud tuto funkci v těchto scénářích nepovolíte, protože snížíte počet výpočtů a režii.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Povolení funkce Rozšířené WHS pro Viditelnost zásob

Chcete-li povolit funkci Rozšířené WHS pro Viditelnost zásob, postupujte takto.

1. Přihlaste se do prostředí Supply Chain Management jako správce.
1. Otevřete pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce v tomto pořadí:

    1. *Integrace viditelnosti zásob*
    1. *Povolte skladové položky ve viditelnosti zásob*

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry integrace Viditelnosti zásob**.
1. Na kartě **Povolit položky WHS** nastavte možnost **Povolit položky WHS** na *Ano*.
1. Přihlaste se do Power Apps.
1. Otevřete stránku **Konfigurace** a potom na kartě **Správa funkcí** zapněte funkci *Rozšířené WHS*.
1. V Supply Chain Management přejděte do uzlu **Řízení zásob \> Periodické úlohy \> Integrace Viditelnosti zásob**.
1. V podokně akcí vyberte **Zakázat**, chcete-li dočasně zakázat Viditelnost zásob.
1. V podokně Akce vyberte možnost **Povolit**, když chcete Viditelnost zásob znovu povolit. Doplněk se znovu načte a nová funkce je nyní povolena. Vaše data související s WHS se začnou synchronizovat s Viditelností zásob.

## <a name="query-on-hand-quantities-of-whs-items"></a>Dotaz na množství položek WHS na skladě

Chcete-li se dotazovat na položky WHS, použijte totéž [aplikační programovací rozhraní (API) a syntaxi zpráv](inventory-visibility-api.md) které používáte u ne-WHS položek. Nemusíte zadávat, zda položka je či není položkou WHS. Viditelnost zásob automaticky rozlišuje položky na základě uložených dat.

Výsledky z dotazů na položky WHS jsou v podstatě stejné jako výsledky pro ne-WHS položky. Jediný rozdíl je v tom, že následující fyzické míry ze zdroje dat `fno` se v Supply Chain Management počítají na základě logiky WHS:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Všechny ostatní fyzické míry se počítají tak, jak jsou, když je vypnutá funkce Rozšířené WHS pro Viditelnost zásob.

Podrobné informace o tom, jak fungují výpočty množství na skladě WHS u položek WHS, najdete v článku [Rezervace ve správě skladu](https://www.microsoft.com/download/details.aspx?id=43284).

Datové entity exportované do Dataverse zatím nemohou aktualizovat množství u položek WHS. Množství, která jsou zobrazena v datových entitách, jsou správná jak u ne-WHS položek, tak u množství, která nejsou ovlivněna logikou WHS (tj. `AvailPhysical`,`AvailOrdered`,`ReservPhysical` a `ReservOrdered` ve zdroji dat `fno`).

Změny množství položek WHS, které jsou uloženy ve zdroji dat Supply Chain Management, jsou zakázány. Pokud jde o další funkce Viditelnosti zásob, toto omezení je vynuceno, aby se zabránilo konfliktům.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Předběžná rezervace položek WHS ve Viditelnosti zásob

Obecně platí, že [předběžné rezervace](inventory-visibility-reservations.md) položek WHS jsou podporovány. Do výpočtů předběžných rezervací můžete zahrnout fyzické míry související s WHS. 

Známým omezením je nemožnost použít výpočet *k dispozici pro rezervaci* u položek WHS. Pokud tedy existuje rezervace nad aktuálními dimenzemi, kde dochází k předběžné rezervaci, výpočet *k dispozici pro rezervaci* je nesprávný. Předběžné rezervace nebudou ovlivněny, když je v [rozhraní API pro předběžné rezervace](inventory-visibility-api.md#create-one-reservation-event) zakázána možnost **ifCheckAvailForReserv**.

Toto omezení platí také pro funkce a přizpůsobení, které jsou založeny na předběžných rezervacích (jako je alokace).

## <a name="calculate-available-to-promise-quantities"></a>Výpočet množství, která lze slíbit

Řešení plně podporuje funkci [Lze slíbit (ATP)](inventory-visibility-available-to-promise.md) u WHS položek. Můžete definovat výpočty ATP, aniž byste se museli starat o podrobnosti pro WHS specifické.

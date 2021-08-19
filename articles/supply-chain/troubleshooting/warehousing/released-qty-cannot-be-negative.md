---
title: Nelze aktualizovat řádek nákladu, protože uvolněné množství by bylo záporné
description: K tomuto problému dochází, když by aktualizace nebo odstranění řádku nákladu způsobila záporné uvolněné množství.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728452"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Nelze aktualizovat řádek nákladu, protože uvolněné množství by bylo záporné

Kód chyby: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když by aktualizace nebo odstranění řádku nákladu způsobila záporné uvolněné množství. V tomto případě při pokusu o aktualizaci nebo odstranění řádku nákladu systém zobrazí následující chybovou zprávu:

> Uvolněné množství nemůže být pro položku %1, šarže %2 záporné.

Proto nemůžete aktualizovat ani odstranit řádek nákladu.

## <a name="cause"></a>Příčina

Poté, co aktualizujete nebo odstraníte řádek nákladu, systém aktualizuje uvolněné množství souvisejícího prodejního řádku (*whsSalesLine.ReleaseQty*). Systém vyhodnotí uvolněné množství a pokud zjistí, že uvolněné množství řádku bude po aktualizaci záporné, nedovolí vám řádek aktualizovat ani smazat. K tomuto ověření dochází vždy, když se pokusíte aktualizovat buď množství, nebo měrnou jednotku řádku nákladu pomocí různých akcí, jako je například odstranění řádku nákladu, odstranění zásilky, změna množství řádku nákladu, snížení odebraného množství a krátkodobé vyskladnění.

Nejčastější hlavní příčinou tohoto problému je změna v převodu jednotek, která se používá u otevřených řádků nákladu. Například převod jednotek při vydání prodejní objednávky byl *50 Ea = 1 PL*. Než však byla související expedice nákladu dokončena, převod jednotek byl změněn na *100 Ea = 1 PL*.

## <a name="resolution"></a>Řešení

Řešením je vrátit změny převodu jednotek, aktualizovat nebo odstranit řádek nákladu a poté převod znovu implementovat. Dokud nebude problém vyřešen, musíte zabránit dalším nákladům, které zahrnují položku způsobující problém. V opačném případě mohou být nové převody použity pro jiné náklady, které jsou již otevřeny.

Chcete-li problém opravit, proveďte následující úkoly:

1. Zkontrolujte převod jednotek, který byl použit pro řádek nákladu.
2. Zkontrolujte aktuální převod jednotek pro položku a proveďte úpravy, které umožní aktualizaci nebo odstranění řádku nákladu.
3. Aktualizujte nebo odstraňte řádek nákladu a vraťte úpravy převodů jednotek.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Kontrola převodu jednotek, který byl použit pro řádek nákladu

Pomocí následujícího postupu zkontrolujte řádky nákladu a poznamenejte si převod jednotek, který byl použit pro řádek nákladu.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte náklad zahrnující řádek nákladu, který nelze odstranit ani aktualizovat.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. V horní mřížce vyberte příslušné ID práce.
1. Na kartě **Všeobecné** v dolní části stránky, vypočítejte konverzní poměr mezi **Množstvím skladové zásoby** a **Množstvím práce**. Poznamenejte si poměr.
1. Tento postup opakujte pro všechna relevantní ID práce, abyste se ujistili, že byl použit stejný převod.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Kontrola aktuálního převodu jednotek u položky a provedení úprav

Následujícím způsobem zkontrolujte převod jednotek produktu a proveďte úpravy, abyste se ujistili, že převod jednotky je zarovnán s řádkem nákladu.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete příslušný produkt a přejděte na jeho stránku **Podrobnosti o uvolněném produktu**.
1. V podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Převody jednotek**.
1. Vyberte převod mezi jednotkami a proveďte úpravy s využitím převodu, který jste našli v předchozí části.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Aktualizace nebo odstranění řádku nákladu a vrácení úprav převodů jednotek

Pomocí následujícího postupu můžete podle potřeby zpracovat řádek nákladu a vrátit převody jednotek.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Otevřete náklad zahrnující řádek nákladu, který nelze odstranit ani aktualizovat.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Podle potřeby pokračujte v požadovaných akcích. (Například odstraňte řádek nákladu nebo změňte jeho množství.)
1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete příslušný produkt a přejděte na jeho stránku **Podrobnosti o uvolněném produktu**.
1. V podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Převody jednotek**.
1. Vyberte převod mezi jednotkami a vraťte úpravy provedené v předchozí části.

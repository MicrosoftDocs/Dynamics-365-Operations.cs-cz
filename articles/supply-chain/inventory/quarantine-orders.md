---
title: "Karanténní příkazy"
description: "Tento článek popisuje použití karanténních příkazů k blokování zásob."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a>Karanténní příkazy

[!include[banner](../includes/banner.md)]


Tento článek popisuje použití karanténních příkazů k blokování zásob.

Karanténní příkazy lze použít k blokování zásob. Můžete například chtít umístit do karantény položky z důvodů kontroly kvality. Sklad, který byl umístěn do karantény, je převeden do karanténního skladu. **Poznámka:** Pokud používáte rozšířené procesy správy skladu (v modulu Řízení skladu), zpracování karanténní objednávky se používá pouze pro vrácení prodejní objednávky.

## <a name="quarantine-onhand-inventory-items"></a>Karanténní zásoby položek na skladě
Při umístění položek do karantény můžete vytvořit karanténní příkazy ručně nebo systém nastavit tak, aby vytvářel karanténní příkazy automaticky při zpracování příchozích. Pokud chcete automaticky vytvořit karanténní příkazy, zaškrtněte možnost **Řízení karantény** na kartě **Zásady zásob** na stránce **Skupiny modelů položek**. Je nutné také určit výchozí karanténní sklad v poli **Karanténní sklad** pro přijímací sklady. Když jsou zásoby fyzicky na skladě zaznamenány v nákupní objednávce nebo výrobní zakázce, položky umístěné do karantény jsou automaticky přesunuty do karanténního skladu v aplikaci Microsoft Dynamics 365 for Finance and Operations. K tomuto pohybu dochází, pokud se změní stav karanténního příkazu na **Zahájeno**. Při ručním vytváření karanténních příkazů, není požadováno, aby v přidružené skupině modelů položek položka byla nastavena pro řízení karantény. Za tímto účelem je nutné zadat zásob na skladě, která mají být umístěny do karantény, a karanténní sklad, který má být použit. Můžete použít stavy karanténních příkazů pro usnadnění plánování procesu.

## <a name="quarantine-order-statuses"></a>Stavy karanténního příkazu
Karanténní příkazy mohou mít tyto stavy:

-   Vytvořeno
-   Zahájeno
-   Ohlášeno jako dokončené
-   Ukončeno

### <a name="created"></a>Vytvořeno

Jestliže byla ručně vytvořena karanténní objednávka, ale položka ještě není uložena do karanténního skladu, karanténní příkaz obdrží stav **Vytvořeno**. Vygenerují se dvě skladové transakce. Jedna je transakce výdeje, která může mít stav **Na objednávce**, **Rezervované – fyzicky** nebo **Vyskladněno**. Druhá je příjmová transakce, která může mít v karanténním skladu stav **Objednáno** nebo **Registrováno**. Rezervaci, vyskladnění a aktualizaci registrace zásob můžete provádět pomocí obvyklých procesů.

### <a name="started"></a>Zahájeno

Když je karanténní příkaz ve stavu **Zahájeno** jsou pak položky přesunuty z obyčejného skladu do karanténního skladu a vytvoří se dvě skladové transakce. Jedna transakce se nachází ve stavu **Odečteno** a jiné transakce nachází ve stavu **Přijato**. Zároveň se vytvoří také dvě skladové transakce k zajištění zpětného převodu. Tyto transakce nejsou datovány. Jedna transakce se nachází ve stavu **Rezervované – fyzicky** a jiné transakce nachází ve stavu **Objednáno**.

### <a name="reported-as-finished"></a>Ohlášeno jako dokončené

Klepnutím na položku **Ohlásit jako dokončené** můžete ohlásit zahájený karanténní příkaz jako dokončený. Položka je uvolněna z karantény, ale ještě nebyla přesunuta zpět do běžného skladu. Přesun zpět do běžného skladu je možné zpracovat pomocí deníku doručení položky, který může být inicializován během procesu Vykázat jako dokončené.

### <a name="ended"></a>Ukončeno

Když je karanténní příkaz ukončen, je položka přesunuta z karanténního skladu zpět do běžného skladu. Stav transakce zboží je v karanténním skladu nastaven na hodnotu **Prodáno** a v běžném skladu na **Koupeno**.

## <a name="quarantine-order-scrap"></a>Vyřazení karanténních příkazů
Jako součást procesu karanténní objednávky je možné zásoby vyřadit. Při zpracování vyřazených zásob bude stav zásob nastaven na **Prodáno** podle transakce výdeje z karanténního skladu.

<a name="see-also"></a>Viz také
--------

[Blokování zásob](inventory-blocking.md)


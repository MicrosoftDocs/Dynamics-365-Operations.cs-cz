---
title: Karanténní příkazy
description: Toto téma popisuje jak použít karanténní příkazy k blokování zásob.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956175"
---
# <a name="quarantine-orders"></a>Karanténní příkazy

[!include [banner](../includes/banner.md)]

Toto téma popisuje jak použít karanténní příkazy k blokování zásob.

Karanténní příkazy vám umožňují blokovat zásoby. Můžete například chtít umístit do karantény položky z důvodů kontroly kvality. Sklad, který byl umístěn do karantény, je převeden do karanténního skladu.

> [!NOTE]
> Pokud používáte rozšířené procesy správy skladu (v modulu Řízení skladu), zpracování karanténního příkazu se používá pouze pro vrácení prodejní objednávky.

## <a name="quarantine-on-hand-inventory-items"></a>Karanténní zásoby položek na skladě

Při umístění položek do karantény můžete vytvořit karanténní příkazy ručně nebo systém nastavit tak, aby vytvářel karanténní příkazy automaticky při zpracování příchozích.

Chcete-li nastavit systém tak, aby automaticky generoval karanténní příkazy, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Zásoby \> Skupiny modelu položky**.
1. Vyberte relevantní skupinu modelu v podokně seznamu, nebo vytvořte novou skupinu modelu.
1. Na záložce s náhledem **Zásady zásob** zaškrtněte políčko **Řízení karantény**.
1. Zavřete stránku.
1. V poli **Karanténní sklad** pro přijímací sklady zadejte výchozí karanténní sklad.

Pokud položka, která je zaregistrována jako přijatá ve skladu, patří do skupiny modelů, kde je vybráno zaškrtávací políčko **Řízení karantény**, systém pro ni vygeneruje karanténní příkaz. Karanténní příkaz dává pracovníkům pokyn, aby položku přesunuli do karanténního skladu.

Při ručním vytváření karanténních příkazů na stránce **Karanténní příkazy** není požadováno, aby v přidružené skupině modelů položek byla položka nastavena pro řízení karantény. Za tímto účelem je nutné zadat zásob na skladě, která mají být umístěny do karantény, a karanténní sklad, který má být použit. Můžete použít stavy karanténních příkazů pro usnadnění plánování procesu.

## <a name="quarantine-order-statuses"></a>Stavy karanténního příkazu

Karanténní příkazy mohou mít tyto stavy:

- Vytvořeno
- Zahájeno
- Ohlášeno jako dokončené
- Ukončeno

### <a name="created"></a>Vytvořeno

Jestliže byla ručně vytvořena karanténní objednávka, ale položka ještě není uložena do karanténního skladu, karanténní příkaz obdrží stav **Vytvořeno**. Vygenerují se dvě skladové transakce. Jedna je transakce výdeje, která může mít stav **Na objednávce**, **Rezervované – fyzicky** nebo **Vyskladněno**. Druhá je příjmová transakce, která může mít v karanténním skladu stav **Objednáno** nebo **Registrováno**. Rezervaci, vyskladnění a aktualizaci registrace zásob můžete provádět pomocí obvyklých procesů.

### <a name="started"></a>Zahájeno

Když je karanténní příkaz ve stavu **Zahájeno** jsou pak položky přesunuty z obyčejného skladu do karanténního skladu a vytvoří se dvě skladové transakce. Jedna transakce se nachází ve stavu **Odečteno** a jiné transakce nachází ve stavu **Přijato**. Zároveň se vytvoří také dvě skladové transakce k zajištění zpětného převodu. Tyto transakce nejsou datovány. Jedna transakce se nachází ve stavu **Rezervované – fyzicky** a jiné transakce nachází ve stavu **Objednáno**.

### <a name="reported-as-finished"></a>Ohlášeno jako dokončené

Chcete-li nahlásit zahájený karanténní příkaz jako dokončený, otevřete příkaz a vyberte v podokně akcí možnost **Oznámit jako dokončené**. Položka je uvolněna z karantény, ale ještě nebyla přesunuta zpět do běžného skladu. Přesun zpět do běžného skladu je možné zpracovat pomocí deníku doručení položky, který může být inicializován během procesu oznámení jako dokončeno.

### <a name="ended"></a>Ukončeno

Když je karanténní příkaz ukončen, je položka přesunuta z karanténního skladu zpět do běžného skladu. Stav transakce zboží je v karanténním skladu nastaven na hodnotu *Prodáno* a v běžném skladu na *Koupeno*.

## <a name="quarantine-order-scrap"></a>Vyřazení karanténních příkazů

Jako součást procesu karanténní objednávky je možné zásoby vyřadit. Při zpracování vyřazených zásob je stav zásob nastaven na *Prodáno* podle transakce výdeje z karanténního skladu.

## <a name="additional-resources"></a>Další zdroje

- [Blokování zásob](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

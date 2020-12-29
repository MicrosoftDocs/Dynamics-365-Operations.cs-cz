---
title: Odstraňování problémů s rezervacemi v řízení skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645111"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Odstraňování problémů s rezervacemi v řízení skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s rezervacemi skladu v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Zobrazuje se mi následující chybová zpráva: „Nelze odebrat rezervace, protože existuje práce, která závisí na rezervacích."

### <a name="issue-description"></a>Popis problému

Na řádku prodeje nemůžete zrušit rezervaci zásob, protože proti řádku je otevřená práce.

### <a name="issue-resolution"></a>Řešení problému

Prozkoumejte, zda existuje práce skupiny balení, která přepravuje položku z balicí stanice na jiné místo (např *Nákladová brána*). Zkontrolujte záznamy na stránkách **Protokol historie vytvoření práce** a **Podrobnosti o práci**, abyste zjistili, co fyzicky rezervuje zásoby, a poté dokončete nebo odstraňte práci, abyste rezervaci uvolnili.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Zobrazuje se následující chybová zpráva: „Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2...."

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze. Následuje úplné znění chybové zprávy:

> Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2 s rozměry Velikost =%3, Barva =%4, Dodatky =%5, Místo =%6, Sklad =%7, Umístění =%8, Stav zásob = K dispozici, Registrační značka =%9, Číslo šarže =%10 pro referenční ID %11 na ID šarže %12.

### <a name="issue-resolution"></a>Řešení problému

Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství. Například tyto transakce mohou otevřít objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Zobrazuje se následující chybová zpráva: „Fyzicky na skladě ... nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.“

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze. Následuje úplné znění chybové zprávy:

> Fyzicky na skladě Místo =%1, Sklad =%2, Stav zásob = Dostupné, Číslo šarže =%3, Majitel =%4: %5 nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.

### <a name="issue-resolution"></a>Řešení problému

Tento problém je pravděpodobně způsoben otevřenou prací. Buď dokončete práci, nebo přijměte bez vytvoření práce. Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství. Například tyto transakce mohou být otevřené objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Zobrazuje se následující chybová zpráva: „Aby bylo možné přiřadit vlně, musí řádky nákladu určit rozměry nad umístěním. Chcete-li přiřadit tyto rozměry, zarezervujte a znovu vytvořte řádek nákladu. “

### <a name="issue-description"></a>Popis problému

Pokud používáte položku, která má hierarchii rezervace "dávka nad" (s dimenzí **Číslo šarže** umístěnou *nad* dimenzí **Umístění**), příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu** pro částečné množství nefunguje. Zobrazí se tato chybová zpráva a pro částečné množství se nevytvoří žádná práce.

Pokud však používáte položku, která má hierarchii rezervace "dávka pod" (s dimenzí **Číslo šarže** umístěnou *pod* dimenzí **Umístění**), můžete uvolnit náklad ze stránky **Pracovní plocha plánování nákladu** pro částečné množství.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Pokud vložíte dimenzi nad dimenzi **Umístění** v hierarchii rezervací, musí být zadána před uvolněním do skladu. Společnost Microsoft vyhodnotila tento problém a zjistila, že se jedná o omezení funkcí během uvolnění do skladu z pracovní plochy plánování nákladu. Částečná množství nelze uvolnit, pokud je není apecifikována jedna nebo více dimenzí nad **Umístěním**.

Další informace viz [Flexibilní zásada rezervace dimenze na úrovni skladu](flexible-warehouse-level-dimension-reservation.md).

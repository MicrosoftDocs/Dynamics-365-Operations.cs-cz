---
title: Fyzické a finanční aktualizace
description: Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29c1c0727487992a478552d94b5bbe8684d0550
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967451"
---
# <a name="physical-and-financial-updates"></a>Fyzické a finanční aktualizace

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství. 

Skladové transakce lze fyzicky nebo finančně aktualizovat v aplikaci Dynamics 365 Supply Chain Management. Některé typy fyzických a finančních transakcí zvyšují skladové množství, zatímco jiné je snižují.

## <a name="physical-increases"></a>Fyzické zvýšení
Při zaúčtování fyzické transakce se záznam transakce nachází ve stavu **Přijato**. Skladové množství fyzicky zvyšují následující transakce:

-   příjem nákupní objednávky,
-   prodejní objednávka – vrácení dodacího listu,
-   ohlášení výrobní zakázky jako dokončené,
-   vedlejší produkt na výdejce výrobní zakázky.

## <a name="financial-increases"></a>Finanční zvýšení
Při zaúčtování finanční příjmové transakce se záznam transakce zvyšující množství nachází ve stavu **Koupeno**. Skladové množství finančně zvyšují následující transakce:

-   Faktury dodavatele
-   faktura nákupní objednávky pro vrácení,
-   náklady výrobní zakázky,
-   skladové deníky s kladným množstvím, jako je například pohyb, ztráta a zisk, inventura, kusovníky a převod.

## <a name="transactions-that-increase-quantity"></a>Transakce, které zvyšují množství
Transakce zvyšují množství jsou zaúčtovány podle klouzavého průměru nákladové ceny. Vypočtená průběžná průměrná nákladová cena je založena na cenách jednotlivých transakcí pro jednotlivé dimenze zásob, které jsou finančně sledovány. Informace o průběžných průměrných nákladových cenách naleznete v tématu [Průběžné průměrné nákladové ceny](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transakce, které snižují množství
Vypočtený klouzavý průměr nákladové ceny se použije, když je transakce snižující množství zúčtována, bez ohledu na to, který skladový model je k těmto zásobám přiřazen. Transakce snižující množství nesmí být označeny pro jinou transakci před zaúčtováním. Je-li fyzické množství na skladě záporné, použijí se náklady zásob definované pro danou položku na stránce **Zboží**. 

> [!NOTE]
> Je-li povolena funkce několika pracovišť, náklady budou představovat náklady na zásoby definované pro pracoviště na stránce **Výchozí nastavení objednávky**.

## <a name="physical-issues-vs-financial-issues"></a>Fyzické výdeje vs finanční výdeje
Při zaúčtování transakce fyzického výdeje se záznam transakce nachází ve stavu **Odečteno**. Mezi fyzické výdeje patří následující transakce:

-   výrobní zakázka - deník výdejek,
-   prodejní objednávka – dodací list,
-   nákupní objednávka – vrácení dodacího listu.

Při zaúčtování finanční transakce se záznam transakce nachází ve stavu **Prodáno**. Mezi finanční výdeje patří následující transakce:

-   Ukončení výrobní zakázky
-   faktura prodejní objednávky,
-   Vrácení faktury dodavatele
-   skladové deníky se záporným množstvím, jako je například pohyb, ztráta a zisk, inventura, kusovníky a převod.

Transakce snižující množství jsou zaúčtovány podle klouzavého průměru nákladové ceny. Proces uzávěrky skladu je tedy vyžadován pro vyrovnání výdejových transakcí příjmovými transakcemi podle modelu zásob, která je přiřazen jednotlivým položkám.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
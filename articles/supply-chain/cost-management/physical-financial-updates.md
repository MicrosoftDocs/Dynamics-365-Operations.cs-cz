---
title: Fyzické a finanční aktualizace
description: Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547879"
---
# <a name="physical-and-financial-updates"></a>Fyzické a finanční aktualizace

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství. 

Skladové transakce lze fyzicky nebo finančně aktualizovat v aplikaci Microsoft Dynamics 365 for Finance and Operations. Některé typy fyzických a finančních transakcí zvyšují skladové množství, zatímco jiné je snižují.

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
Transakce zvyšují množství jsou zaúčtovány podle klouzavého průměru nákladové ceny. Aplikace Dynamics 365 for Finance and Operations vypočítá průběžnou průměrnou nákladovou cenu založenou na cenách jednotlivých transakcí pro jednotlivé dimenze zásob, které jsou finančně sledovány. Informace o průběžných průměrných nákladových cenách naleznete v tématu [Průběžné průměrné nákladové ceny](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transakce, které snižují množství
Aplikace Finance and Operations používá vypočtený klouzavý průměr nákladové ceny, když je transakce snižující množství zúčtována, bez ohledu na to, který skladový model je k těmto zásobám přiřazen. Transakce snižující množství nesmí být označeny pro jinou transakci před zaúčtováním. Je-li fyzické množství na skladě záporné, aplikace Finance and Operations použije náklady zásob definované pro danou položku na stránce **Zboží**. **Poznámka:** Je-li povolena funkce několika pracovišť, náklady budou představovat náklady na zásoby definované pro pracoviště na stránce **Výchozí nastavení objednávky**.

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




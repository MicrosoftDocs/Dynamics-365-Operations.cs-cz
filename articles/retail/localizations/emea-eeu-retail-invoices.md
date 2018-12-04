---
title: "Faktury odběratele a objednávky prodejní vratky ve východoevropských zemích v aplikaci Retail"
description: "Toto téma popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích."
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: 20ae19fb03acb075b6553b95808779c905bcd31b
ms.contentlocale: cs-cz
ms.lasthandoff: 10/24/2018

---

# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Faktury odběratele a objednávky prodejní vratky ve východoevropských zemích v aplikaci Retail


[!include [banner](../../includes/banner.md)]

Toto téma popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích.

Můžete nastavit následující informace pro faktury odběratelů a objednávky prodejní vratky, které jsou generovány v Retail POS.

- Můžete použít skupiny DPH ke zpracování vratek pomocí objednávek prodejní vratky. Přejděte na možnost **Maloobchod > Nastavení centrály > Parametry > Parametry maloobchodu**. Otevřete kartu **Zaúčtování > Faktura** a potom nastavte **Použít skupinu prodejní daně pro vrácení** na **Ano**. 

  * K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem, vyberte skupinu DPH na stránce **Odběratelé** na pevné záložce **Maloobchod** v poli **Skupina DPH pro vrácení**. Pokud zaúčtujete objednávky prodejní vratky pro odběratele, řádek objednávky prodejní vratky bude aktualizován skupinou DPH pro vrácení, které je zadané ve formuláři **Odběratelé**.
  
  * K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem v Retail POS vyberte skupinu DPH na stránce **Obchody** na pevné záložce **Obecné** v poli **Skupina DPH pro vrácení**. Pokud zaúčtujete objednávky prodejní vratky pro odběratele v maloobchodě, bude řádek objednávky prodejní vratky aktualizován skupinou DPH pro vrácení, která jsou zadaná na stránce **Obchody**.

- Můžete použít datum zaúčtování maloobchodní faktury odběratele nebo objednávky prodejní vratky jako prodejní datum faktury nebo vratky, pokud faktura nebo vratka nemá výchozí datum prodeje. Přejděte na možnost **Maloobchod > Nastavení centrály > Parametry > Parametry maloobchodu**. Otevřete kartu **Zaúčtování > Faktura** a potom nastavte **Použít datum zaúčtování jako datum prodeje** na **Ano**.

- Můžete použít číselnou řadu poskytnutou finančními úřady k číslování faktur odběratele a objednávek prodejní vratky pro zákazníky v Lotyšsku a Litvě. 

  * Přejděte na **Správa organizace > Číselné řady > Správa čítačů**. Musí existovat záznam, kde **Modul** = **Prodej** a **Typ** = **Faktura**.

  * Přejděte na **Správa organizace > Číselné řady > Nastavení číslování faktur**. Zaškrtněte políčko **Maloobchod** pro pořadové číslo řádku, který se používá k číslování faktur odběratele.


---
title: Faktury odběratele a vrácení prodejních objednávek ve východoevropských zemích
description: Tento článek popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích.
author: EvgenyPopovMBS
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: josaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.search.industry: Retail
ms.openlocfilehash: 6ebf3740b9ae93cecd5592a5564574e7f49ab5b4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286545"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Faktury odběratele a vrácení prodejních objednávek ve východoevropských zemích


[!include [banner](../../includes/banner.md)]

Tento článek popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích.

Můžete nastavit následující informace pro faktury odběratelů a objednávky prodejní vratky, které jsou generovány v Retail POS.

- Můžete použít skupiny DPH ke zpracování vratek pomocí objednávek prodejní vratky. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**. Otevřete kartu **Zaúčtování \> Faktura** a potom nastavte **Použít skupinu prodejní daně pro vrácení** na **Ano**.

    * K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem, vyberte skupinu DPH na stránce **Odběratelé** na pevné záložce **Commerce** v poli **Skupina DPH pro vrácení**. Pokud zaúčtujete objednávky prodejní vratky pro odběratele, řádek objednávky prodejní vratky bude aktualizován skupinou DPH pro vrácení, které je zadané ve formuláři **Odběratelé**.
    * K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem v Retail POS vyberte skupinu DPH na stránce **Obchody** na pevné záložce **Obecné** v poli **Skupina DPH pro vrácení**. Pokud zaúčtujete objednávky prodejní vratky pro odběratele v obchodě, bude řádek objednávky prodejní vratky aktualizován skupinou DPH pro vrácení, která jsou zadaná na stránce **Obchody**.

- Můžete použít datum zaúčtování faktury odběratele nebo objednávky prodejní vratky jako prodejní datum faktury nebo vratky, pokud faktura nebo vratka nemá výchozí datum prodeje. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**. Otevřete kartu **Zaúčtování \> Faktura** a potom nastavte **Použít datum zaúčtování jako datum prodeje** na **Ano**.
- Můžete použít číselnou řadu poskytnutou finančními úřady k číslování faktur odběratele a objednávek prodejní vratky pro zákazníky v Lotyšsku a Litvě.

    * Přejděte na **Správa organizace \> Číselné řady \> Správa čítačů**. Musí existovat záznam, kde **Modul** = **Prodej** a **Typ** = **Faktura**.
    * Přejděte na **Správa organizace \> Číselné řady \> Nastavení číslování faktur**. Zaškrtněte políčko **Commerce** pro pořadové číslo řádku, který se používá k číslování faktur odběratele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

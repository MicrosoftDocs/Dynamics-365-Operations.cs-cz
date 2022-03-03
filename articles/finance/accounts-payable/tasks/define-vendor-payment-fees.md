---
title: Definování platebních poplatků dodavatelů
description: Nastavte poplatky pro platby dodavatelů.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109813"
---
# <a name="define-vendor-payment-fees"></a>Definování platebních poplatků dodavatelů

[!include [banner](../../includes/banner.md)]

Nastavte poplatky pro platby dodavatelů. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte do nabídky **Závazky > Nastavení platby > Platební poplatek**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **ID poplatku**.
    * **ID poplatku** by mělo nabízet popis v případě, že bude tento poplatek použit (například "EFT_Fee").  
4. Zadejte hodnotu do pole **Název**.
5. Zadejte hodnotu do pole **Popis poplatku**.
    * Přidejte popis a poskytněte tak více podrobností o tom, kdy je poplatek vyměřen.  
6. V poli **Náklady** vyberte **dodavatele** nebo **hlavní knihu**.
    * **Hlavní kniha** se používá, pokud bude poplatek zanesen do výdajů pro vaši organizaci. **Dodavatel** se používá, pokud bude poplatek zanesen dodavateli.  
7. Zadejte hlavní účet, pokud budou poplatky zaneseny.
    * Tato volba je k dispozici pouze tehdy, pokud jako možnost **Náklady** vyberete **Hlavní kniha**.  
8. Vyberte deník, u kterého lze použít tento poplatek. 
    * Pro platební poplatky dodavatele vyberte deník Úhrady dodavateli.  
9. Klikněte na tlačítko **Uložit**.
10. Klikněte na **Nastavení platebního poplatku**.
    * Pokračujte k **Nastavení platebních poplatků** a definujte, kdy má poplatek být upraven na výchozí pro deník, který jste vybrali.  
11. Vyberte možnost **Tabulka**, **Skupina** nebo **Vše**.
    * **Tabulka** slouží k výběru jednoho bankovního účtu, **Skupina** slouží k výběru bankovní skupiny a **Vše** umožňuje použití tohoto nastavení poplatků pro všechny bankovní účty.  
12. Vyberte bankovní účet nebo bankovní skupinu.
    * Vyhledávání zobrazí bankovní skupinu, pokud jste vybrali možnost **Skupina**, a bude popisovat bankovní účty, jestliže jste vybrali **Tabulka**.  
13. Vyberte metodu platby, pro kterou se vyhodnotí tento poplatek.
14. Vyberte **specifikaci platby** pro vybraný způsob platby.
    * **Specifikace platby** se používají pro platbu metodou elektronického převodu finančních prostředků.  
15. Určete, zda poplatek budou procenta, částka nebo interval.
16. Zadejte procento nebo částku poplatku.
    * Pokud je **Poplatek** procentuální hodnotu, zadejte procento. Pokud je **Poplatek** částkou, zadejte částku poplatku. U **poplatku** ve formě intervalu použijte kartu **Interval** k definování vrstvených poplatků.  
17. V poli **Měna poplatku** vyberte měnu, v níž bude poplatek vyměřen.
    * Tato měna je pro poplatek. Měna platby slouží k definování toho, kdy se pravidla poplatku musí vyhodnotit na základě měny platby. Například vaše banka může účtovat poplatek, když je provedena platba v EUR, ale pro všechny ostatní platby není určen poplatek.  
18. Klikněte na tlačítko **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

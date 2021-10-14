---
title: Zkontrolovat nesrovnalosti v cenách v mezipodnikových objednávkách
description: Toto téma vysvětluje, jak kontrolovat nesrovnalosti v cenách v mezipodnikových objednávkách
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548139"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Zkontrolovat nesrovnalosti v cenách v mezipodnikových objednávkách

[!include [banner](../../includes/banner.md)]

Tento postup můžete použít ke kontrole neshod v cenách mezipodnikových objednávek.

1. Přejděte na stránku **Zásobování a zdroje \> Periodické \> Vyčistit \> Zkontrolovat nesrovnalosti v cenách v mezipodnikových objednávkách**.
1. Nastavte dávkovou úlohu, pokud je třeba, a potom výběrem tlačítka **OK** zkontrolujte ceny a slevy u mezipodnikových prodejních a nákupních objednávek. Stránku zavřete bez provedení kontroly výběrem tlačítka **Zrušit**.

    > [!TIP]
    > Pokud vzniknou problémy synchronizace nebo problémy s cenami, budou uvedeny v informační zprávě, která se zobrazí. Tuto informační zprávu si můžete vytisknout.

1. Objednávku otevřete v aktuální právnické osobě výběrem příslušného řádku informační zprávy. Objednávku u související právnické osoby otevřete výběrem možnosti **Mezipodnikové** a pak **Mezipodniková nákupní objednávka** nebo **Mezipodniková prodejní objednávka**.

    > [!NOTE]
    > Chcete-li povolit aktualizaci mezipodnikové objednávky:
    >
    > 1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
    > 1. V části Podokno akcí vyberte kartu **Obecné** a potom vyberte možnost **Mezipodnikové**.
    > 1. Na stránce **Mezipodnikové** vyberte **Zásady nákupních objednávek** nebo **Zásady prodejních objednávek**.
    > 1. V obou oblastech vyberte **Povolit úpravu ceny** a **Povolit úpravy slev**.

1. Otevřete příslušnou mezipodnikovou objednávku z umístění, ve kterém chcete vést cenu.
1. U každého řádku objednávky změňte pole **Jednotková cena** řádku a pak jej změňte zpět na původní hodnotu. Změňte pole **Sleva** v řádku oběma směry a změňte příslušná pole **Nákupní poplatky** nebo **Prodejní poplatky** oběma směry. Tato změna hodnot oběma směry spustí synchronizaci cen, slev a nákladů z tohoto řádku mezipodnikové objednávky do odkazovaného řádku mezipodnikové objednávky, aby byly automaticky vyrovnány.

    > [!NOTE]
    > Tato synchronizace bude platná, pouze pokud nebyla mezipodniková prodejní objednávka fakturována. Jestliže byla faktura mezipodnikové prodejní objednávky zaúčtována a byl vytvořen deník faktur odběratele, je nutné změny provést přímo na řádcích mezipodnikové nákupní objednávky nastavením cen, slev a vedlejších nákladů tak, aby se shodovaly s uvedenými údaji v deníku mezipodnikových faktur odběratele. Jestliže tento krok neprovedete, nebude faktura za mezipodnikovou nákupní objednávku zaúčtována, protože v součtech objednávek budou nesrovnalosti.

1. Opakujte postup až do úplné synchronizace mezipodnikových prodejních a nákupních objednávek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Vytvoření nákupní objednávky řízené rozpočtem
description: Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821362"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Vytvoření nákupní objednávky řízené rozpočtem

[!include [banner](../../includes/banner.md)]

Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu. Tento záznam používá v ukázkových datech společnost USMF.


## <a name="review-the-budget-control-configuration"></a>Zkontrolujte konfiguraci kontroly rozpočtu
1. Přejděte na Rozpočtování > Nastavení > Kontrola rozpočtu > Konfigurace kontroly rozpočtu.
2. Klikněte na kartu Dostupné rozpočtové prostředky.
3. Klepněte na kartu Dokumenty a deníky.
4. Klepněte na kartu Definovat pravidla kontroly rozpočtu.
5. Klepněte na kartu Definovat rozpočtové skupiny.
6. Zavřete stránku.

## <a name="create-the-purchase-order-header"></a>Vytvoření záhlaví nákupní objednávky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
4. Rozbalte sekci Obecné.
5. Do pole Datum účtování nastavte datum 2016-01-01.
6. Klikněte na tlačítko OK.

## <a name="add-a-purchase-order-line"></a>Přidání řádku nákupní objednávky
1. V Kategorie zásobování zadejte nebo vyberte hodnotu.
2. Nastavte množství na „2“.
3. V poli Jednotka zadejte nebo vyberte hodnotu.
4. Nastavte jednotkovou cenu na 10000.
5. Klepněte na tlačítko Finanční údaje.
6. Klikněte na možnost Distribuovat částky.
7. Do pole Účet hlavní knihy zadejte hodnotu 601300-001-023--.
8. Zavřete stránku.

## <a name="perform-budget-checking"></a>Provést kontrolu rozpočtu
1. Klepněte na tlačítko Finanční údaje.
2. Klikněte na Provést kontrolu rozpočtu.
3. Klepněte na tlačítko Finanční údaje.
4. Klikněte na Zobrazit chyby a varování kontroly rozpočtu.
5. Klikněte na tlačítko Zavřít.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
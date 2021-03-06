---
title: Řešení potíží s konfigurátorem produktu
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s konfigurátorem produktu.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841544"
---
# <a name="troubleshoot-the-product-configurator"></a>Řešení potíží s konfigurátorem produktu

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s konfigurátorem produktu.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Text položky je přepsán, když konfiguruji produkt na řádku prodejní objednávky.

### <a name="issue-description"></a>Popis problému

K tomuto problému dochází, když vytvoříte řádek prodejní objednávky pro konfigurovatelnou položku a poté upravíte text položky. Když položku konfigurujete a poté vyberete **OK**, text je přepsán standardním textem.

### <a name="issue-resolution"></a>Řešení problému

Toto chování se očekává. Textové pole obsahuje název varianty, který se vyplní až po konfiguraci řádku. Proto musíte změnit text po nakonfigurování řádku, ne dříve.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Atributy celého čísla jsou při výpočtu konfiguračních modelů produktu nesprávně zaokrouhleny.

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít, když provedete následující řadu akcí:

1. Na produkčním konfiguračním modelu nastavte následující atributy:

    - Vstup (celé číslo)
    - Procento (desetinné)
    - Výsledek (celé číslo)

2. Vytvořte výpočet, který má následující výraz:

    *Výsledek* = *Vstup* × *Procento* ÷ 100

V takovém případě není výsledek celého čísla vždy správně zaokrouhlený. Například vstup je 1 000 a procento je 2,40. Proto očekáváte, že celočíselný výsledek bude 24, protože 2,40 procent z 1 000 je 24 (nebo 24,00 v desetinné formě). Místo toho je výsledek zobrazen jako 23. Když je však procento 2,39, výpočet se zaokrouhlí na 24 místo 23. Když je procento 2,5 výpočet se zaokrouhlí na 25 podle očekávání.

### <a name="issue-resolution"></a>Řešení problému

K tomuto problému dochází kvůli způsobu, jakým Microsoft Solver Foundation interně představuje čísla pomocí zlomků. V předchozím příkladu je výsledek výpočtu, kde je procento 2,40, reprezentován jako 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Když .NET převede tuto hodnotu na celé číslo, vrátí 23.

Toto chování se nezmění, protože na něm závisí jiné scénáře. V předchozím příkladu můžete problém vyřešit zavedením dalšího desetinného atributu a výpočtu.

Například můžete nastavit na produkčním konfiguračním modelu následující atributy:

- Vstup (celé číslo)
- Procento (desetinné)
- ResultDecimal (desetinné)
- ResultInteger (celé číslo)

Poté můžete přidat následující výpočty:

- *ResultDecimal* = *Vstup* × *Procento* ÷ 100
- *ResultInteger* = *ResultDecimal*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
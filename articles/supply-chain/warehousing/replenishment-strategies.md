---
title: Strategie doplňování
description: Toto téma poskytuje informace o strategiích doplňování a vysvětluje, jak můžete pomocí pole Strategie doplňování na řádcích šablon doplňování poptávky vlny vybrat, jak se doplnění provádí.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a66d48c6636f9f2012c92945868728d8430c1cbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256032"
---
# <a name="replenishment-strategies"></a>Strategie doplňování

[!include [banner](../includes/banner.md)]

Šablony, které jsou definovány na stránce **Šablony doplňování**, obsahují řádky šablony doplňování poptávky vlny, které vám umožňují vybrat, jak se doplnění provádí. Každý řádek nyní obsahuje a pole **Strategie doplňování**.

Strategie *Množství poptávky vlny* je výchozí strategie. Jedná se o strategii doplňování, která byla použita před zavedením pole **Strategie doplňování**. Směrnice skladového místa se používá k vyhledání míst, která lze doplnit. Poté tato místa doplňuje, dokud není pokryta poptávka.

Strategie *Maximální kapacita skladového místa* zavádí některé nové funkce. Stejně jako strategie *Množství poptávky vlny* tato strategie používá směrnice skladového místa doplňování k vyhledání míst, která lze doplnit, a poté tato místa doplňuje, dokud není pokryta poptávka. Liší se od strategie *Množství poptávky vlny* v tom, že všechna doplňovaná místa jsou doplněna na svou maximální kapacitu, jak je definována skladovacími limity místa. Strategie *Maximální kapacita skladového místa* se snaží vytvořit práci, která přinese požadované množství plus nějaké další množství, aby vyplnila místa, která se doplňují. V některých případech však tento pokus může selhat. Například hromadná umístění nemusí mít dostatek zásob k pokrytí extra množství. V těchto případech systém detekuje poruchu a pokusí se o obnovení.

Hlavní sezóna je jedním z příkladů situace, kdy strategie *Maximální kapacita skladového místa* je lepší než strategie *Množství poptávky vlny*. Během hlavní sezóny se některé položky mohou prodávat ve velkém objemu. Proto možná budete chtít proaktivně co nejvíce doplňovat relevantní umístění pro vychystávání, abyste snížili počet ID práce, které jsou vytvořeny pro doplnění.

> [!IMPORTANT]
> Chcete-li plně využít výhod strategie *Maximální kapacita skladového místa*, musíte předefinovat limity skladování pro příslušná místa. Jinak tato strategie funguje stejně jako strategie *Množství poptávky vlny*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Zapněte funkci Doplnění na maximum na základě limitů skladování

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Doplnění na maximum na základě limitů skladování*

## <a name="set-up-replenishment-strategies"></a>Nastavení strategie doplňování

Pro přístup k šablonám přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**. V části **Přehled** vyberte nebo vytvořte šablonu doplňování poptávky vlny, kde pole **Typ doplňování** je nastaveno na *Poptávka vlny*. Poté nastavte řádky šablony doplňování v části **Podrobnosti šablony doplňování**. Pro každý řádek v poli **Strategie doplňování** vyberte strategii doplňování, kterou chcete použít.

![Stránka Šablony doplnění](media/ReplenTempWaveDmdMaxLocCap.png "Stránka Šablony doplnění")

Pokud se sloupec **Strategie doplňování** nezobrazí v mřížce v sekci **Podrobnosti šablony doplňování**, ujistěte se, že byla funkce zapnuta a že vybraná šablona doplňování má typ doplňování *Poptávka vlny*.

> [!NOTE]
> Strategie *Množství poptávky vlny* je výchozí strategie. Proto stačí aktualizovat řádky šablony doplňování tam, kde chcete použít místo toho strategii *Maximální kapacita skladového místa*.

## <a name="example-scenarios"></a>Ukázkové scénáře

### <a name="example-1"></a>Příklad 1

V tomto příkladu existuje pouze jedna šablona doplňování, která má pouze jeden řádek šablony doplňování.

Vytvoříte prodejní objednávku na 130 kusů (ks) položky A0001. Před uvolněním objednávky do skladu je sklad nastaven následujícím způsobem:

- Existuje pouze jedno hromadné umístění a má 500 ks dostupných zásob na skladě.
- Existují tři výdejová místa, z nichž každé má limit skladování 100 ks. (Pamatujte, že pro strategii *Maximální kapacita skladového místa* jsou povinné skladovací limity.)
- Místa vložení doplnění jsou stejná jako místa prodejního výdeje.
- Jednotka doplnění je krabice (1 krabice = 20 ks).

V době objednávky jsou v prodejních výdejových místech k dispozici následující zásoby:

- **Pick-001:** 20 ks (1 krabice)
- **Pick-002:** 0 ks
- **Pick-003:** 0 ks

Zpočátku je strategie doplňování nastavena na *Množství poptávky vlny*.

Po uvolnění prodejní objednávky do skladu a spuštění zpracování vln pro vlnu získáte následující práci doplnění:

- **Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.
- **Práce doplnění 2:** Vyberte 2 krabice z hromadného umístění a umístěte je do místa pick-002.

Získáte dvě ID práce doplňování, protože musíte doplnit dvě místa a vícenásobné vložení není podporováno.

Pokud nastavíte strategii doplňování místo toho na *Maximální kapacita skladového místa*, získáte následující práci doplnění:

- **Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.
- **Práce doplnění 2:** Vyberte 5 krabice z hromadného umístění a umístěte je do místa pick-002.

[![Příklad 1](media/ReplenTemp_example_1.png "Příklad 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Příklad 2

Tento příklad ukazuje, co se stane, když hromadné umístění nemá dostatek zásob k pokrytí extra množství. Používá stejný scénář jako v příkladu 1, ale hromadné umístění má 160 ks (8 krabic).

Strategie *Množství poptávky vlny* vytváří stejnou práci jako v příkladu 1.

Protože se však strategie *Maximální kapacita skladového místa* pokusí vytvořit ID práce, jako tomu bylo v příkladu 1, může selhat. V tomto okamžiku se systém pokusí o obnovení.

V závislosti na nastavení možnost **Povolit rozdělení** ve směrnicích skladového místa pro výdej doplňování jsou možné dva výsledky:

- Pokud je možnost **Povolit rozdělení** nastavena na *Ano*, je vytvořena následující práce doplnění:

    - **Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.
    - **Práce doplnění 2:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-002.

- Pokud je možnost **Povolit rozdělení** nastavena na *Ne*, je vytvořena následující práce doplnění:

    - **Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.
    - **Práce doplnění 2:** Vyberte 2 krabice z hromadného umístění a umístěte je do místa pick-002.

Výsledky se liší kvůli informacím, které jsou k dispozici při vytváření práce. Když je možnost **Povolit rozdělení** nastavena na *Ano* ve směrnicích skladového místa pro výdej doplňování víte, že se vám podařilo najít 160 ks. Proto pro toto množství můžete vytvořit práci. Když je však možnost **Povolit rozdělení** nastavena na *Ne*, nevíte o existenci 160 ks. Protože extra množství, které jste se rozhodli doplnit, byly 3 krabice, odečtete toto extra množství a zkusíte původní množství znovu.

[![Příklad 2](media/ReplenTemp_example_2.png "Příklad 2")](media/ReplenTemp_example_2_large.png)

Chcete-li tedy získat maximální množství na doplněná místa, měli byste nastavit možnost **Povolit rozdělení** na *Ano* na směrnicích skladového místa pro výdej doplňování.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
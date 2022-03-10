---
title: Výpočty modelu konfigurace produktu
description: Toto téma popisuje, jak vytvořit výpočty pro atributy v modelu konfigurace produktu.
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349fed3ca75b94db2f421a1ff3c3553c96c202c37d59857a3d973f3de8f995ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755244"
---
# <a name="product-configuration-model-calculations"></a>Výpočty modelu konfigurace produktu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit výpočty pro atributy v modelu konfigurace produktu.

## <a name="prerequisites"></a>Předpoklady

Výpočty se používají v modelu konfigurace produktu pro výpočet hodnot konfigurace produktu. Než začnete nastavovat výpočty, musí existovat model konfigurace souvisejícího produktu. Přehled procesu nastavení konfiguračních modelů a souvisejících úkolů najdete v části [Nastavení modelu konfigurace produktu](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Tvorba výpočtů

Výpočet se skládá z výrazu a cílového atributu. Další informace najdete v části [Výpočty pro modely konfigurace produktu - často kladené dotazy](calculate-product-configuration-models.md).

Chcete-li vytvořit výpočet pro existující model produktu, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Společné \> Modely konfigurace produktu**.
1. Otevřete model konfigurace produktu a zvolte **Upravit**.
1. Na záložce s náhledem **Výpočty** vyberte **Přidat**, chcete-li přidat výpočet, a poté pro něj nastavte následující pole:

    - **Název** - Zadejte název výpočtu.
    - **Popis** - Zadejte popis výpočtu.
    - **Cílový atribut** - Vyberte atribut, pro který provádíte výpočet.

1. Vyberte **Upravit výraz**.
1. V dialogovém okně **Zadat výpočet**, přidejte do výrazu požadované atributy, operátory a hodnoty. Další informace o tom, jak pracovat s těmito prvky, najdete v části [Omezení výrazu a omezení tabulky v modelech konfigurace produktu](expression-constraints-table-constraints-product-configuration-models.md).
1. Když je váš výraz připraven, vyberte **OK**.

## <a name="calculation-examples"></a>Příklady výpočtů

Tato část poskytuje několik příkladů, které ukazují, jak výpočty fungují.

### <a name="example-1"></a>Příklad 1

Atribut target má logickou hodnotu a výpočet používá následující podmíněný výraz:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Tento výraz vrací hodnotu *True* do cílového atributu, pokud je `decimalAttribute2` větší nebo rovno `decimalAttribute1`. V opačném případě vrátí hodnotu *False*.

### <a name="example-2"></a>Příklad 2

Tento příklad používá textový atribut `textFixedList` jako cílový atribut. Tento atribut obsahuje následující pevný seznam.

| Hodnota | Hodnota řešitele |
|---|---|
| A | 1a |
| mld. | 2b |
| K | 2c |

Následující snímek obrazovky ukazuje, jak by nastavení tohoto atributu mohlo vypadat ve vašem systému.

![Nastavení typu atributu pro příklad 2.](media/model-calculations-example2.png "Nastavení typu atributu pro příklad 2")

Atribut se používá v následujícím podmíněném příkazu:

`If[integerAttribute < 150, 0, 2]`

Pokud je `integerAttribute` menší než 150, tento příkaz vrátí textovou hodnotu prvního záznamu v pevném seznamu *A*. V opačném případě vrátí textovou hodnotu třetího záznamu v pevném seznamu *C*.

> [!NOTE]
> Pevný seznam je ekvivalentní výčtu založenému na nule (enum) a k jeho hodnotám se přistupuje příslušnou celočíselnou hodnotou. Proto první pevná hodnota seznamu (*A*) odpovídá *0*, druhá hodnota (*B*) odpovídá *1* a třetí hodnota (*C*) odpovídá *2*.

### <a name="example-3"></a>Příklad 3

Tento příklad používá cílový atribut `textFixedList` z předchozího příkladu. Používá také jiný textový atribut, `textAttribute`, který obsahuje následující pevný seznam.

| Hodnota | Hodnota řešitele |
|---|---|
| AA | 1aa |
| BB | 2bb |

Následující snímek obrazovky ukazuje, jak by nastavení tohoto atributu mohlo vypadat ve vašem systému.

![Nastavení typu atributu pro příklad 3.](media/model-calculations-example3.png "Nastavení typu atributu pro příklad 3")

Hodnota pro atribut `textFixedList` se počítá pomocí následujícího podmíněného příkazu:

`If[textAttribute == "1aa", 0, 2]`

Pokud hodnota `textAttribute` má hodnotu řešitele rovnající se *1aa*, tento výraz vrací textovou hodnotu prvního záznamu v pevném seznamu `textFixedList` *A*. V opačném případě vrátí textovou hodnotu třetího záznamu v pevném seznamu `textFixedList` *C*.

> [!NOTE]
> - Podmíněný příkaz musí používat hodnotu řešitele atributu.
> - Ve výpočtech lze použít pouze textové atributy pevného seznamu.

## <a name="see-also"></a>Viz také

- [Výpočty pro modely konfigurace produktu - často kladené dotazy](calculate-product-configuration-models.md)
- [Přidání omezení výrazu do modelu konfigurace produktu](tasks/add-expression-constraint-product-configuration-model.md)
- [Přehled modelů konfigurace produktu](product-configuration-models.md)

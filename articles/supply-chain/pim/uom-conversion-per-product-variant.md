---
title: Převod měrné jednotky pro variantu produktu
description: Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204486"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Převod měrné jednotky pro variantu produktu

[!include [banner](../includes/banner.md)]

Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu. Zahrnuje také příklad nastavení.

Tato funkce umožňuje společnostem definovat jiný převod jednotek mezi variantami stejného produktu. Následující příklad je použit v tomto tématu. Společnost prodává trička ve velikostech S, M, L a XL. Tričko je definováno jako produkt a jsou definovány různé velikosti variant produktu. Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři. Společnost chce sledovat různé varianty triček po **kusech**, nicméně trička prodává po **krabicích**. Převod mezi jednotkou zásob a prodejní jednotkou je 1 krabice = 5 kusů s výjimkou varianty XL, kde 1 krabice = 4 kusy.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Nastavení produktu pro převod jednotek pro variantu

Varianty produktu lze vytvořit pouze pro produkty **podtyp produktu**: **základní produkt**. Další informace naleznete v tématu [Vytvoření základního produktu](tasks/create-product-master.md).

Tato funkce není povolena pro produkty, které jsou nastaveny pro procesy skutečné hmotnosti. 

Po vytvoření základního produktu s variantami produktu lze nastavit převody jednotek pro varianty. Položku nabídky pro otevření stránky s převody naleznete v kontextu produktu nebo variantě produktu na následujících stránkách.

-   Strnka **Podrobnosti o produktu**
-   Strána **Zveřejněné informace o produktu**
-   Stránka **zveřejněné varianty produktu**

Otevřete-li stránku **Převod jednotek** v kontextu základního produktu nebo zveřejněné varianty produktu, můžete vybrat, jestli chcete nastavit převod jednotky pro produkt nebo variantu produktu. To lze provést výběrem buď **varianty produktu**, nebo **produktu** v poli **Tvorba převodu pro**.

### <a name="product-variant"></a>Varianta produktu

Vyberete-li **Varianta produktu**, můžete si vybrat, pro kterou variantu si přejete nastavit převod jednotek v poli **varianta produktu**.

### <a name="product"></a>Produkt

Vyberete-li **Produkt**, potom můžete nastavit převod jednotky pro základní produkt. Tento převod jednotek bude použit pro všechny varianty produktu bez definovaného převodu jednotek.

### <a name="example"></a>Příklad

Základní produkt, **tričko**, má čtyři varianty: S, M, L a XL. Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři.

Nejprve otevřete stránku **Převod jednotek** ze stránky podrobnosti o zveřejnění produktu pro **tričko.**

Na stránce **Převod jednotek** nastavte převod jednotky pro variantu produktu XL.

| **Pole**             | **Nastavení**             |
|-----------------------|-------------------------|
| Vytvoření převodu pro | Varianta produktu         |
| Varianta produktu       | Tričko : : XL : : |
| Z jednotky             | Krabice                   |
| Koeficient                | 4                       |
| Do jednotky               | Kusy                  |

Varianty zveřejněného produktu S, M a L mají stejný převod jednotek mezi jednotkou krabice a kusů, což znamená, že můžete definovat převod jednotky pro tyto varianty produktu pro základní produkt.

| **Pole**             | **Nastavení** |
|-----------------------|-------------|
| Vytvoření převodu pro | Produkt     |
| Produkt               | Tričko     |
| Z jednotky             | Krabice       |
| Koeficient                | 5           |
| Do jednotky               | Kusy      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Použití aplikace Excel pro aktualizaci převodů jednotek

Pokud má produkt mnoho variant s různými převody jednotek, je vhodné exportovat převody jednotek ze stránky **Převod jednotek** do tabulky aplikace Excel, aktualizovat převody a publikovat je zpět v aplikaci Supply Chain Mangement.

Možnost exportovat do aplikace Excel a publikovat úpravy zpět do aplikace Supply Chain Mangement je povolena z nabídky **Otevřít v aplikaci Microsoft office** v podokně Akce na stránce **Převod jednotek**.

---
title: Převod měrné jednotky pro variantu produktu
description: Toto téma popisuje nastavení způsobu převodu měrné jednotky pro varianty produktu. Zahrnuje také příklad nastavení.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5f327d1d0b38ad724da6a302cefc115262317812
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001692"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Převod měrné jednotky pro variantu produktu

[!include [banner](../includes/banner.md)]

Toto téma popisuje nastavení způsobu převodu měrné jednotky pro různé varianty produktu.

Místo vytváření více jednotlivých produktů, které je třeba udržovat, můžete pomocí variant produktu vytvořit variace jednoho produktu. Variantou produktu může být Například tričko dané velikosti a barvy.

Dříve bylo možné provádět jednotkové převody pouze na základním produktu. Proto měly všechny varianty produktu stejná pravidla pro převod jednotek. Nicméně, když je funkce *Převody měrných jednotek pro varianty produktů* zapnutá, pokud se vaše trička prodávají v krabicích a počet triček, které lze zabalit do krabice, závisí na velikosti trička, můžete nyní nastavit jednotkové převody mezi různými velikostmi triček a krabic, do kterých se trička zabalí.

## <a name="turn-on-the-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Pokud tuto funkci ve vašem systému ještě nevidíte, přejděte na [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Převody měrných jednotek pro varianty produktů*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Nastavení produktu pro převod jednotek pro variantu

Varianty produktu lze vytvořit pouze pro produkty, které jsou základními produkty. Další informace naleznete v tématu [Vytvoření základního produktu](tasks/create-product-master.md). funkce *Převody měrných jednotek pro varianty produktů* není k dispozici pro produkty, které jsou nastaveny pro procesy se skutečnou hmotnosti.

Chcete-li nakonfigurovat předlohu produktu tak, aby podporovala převod jednotky pro každou variantu, postupujte takto.

1. Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.
1. Vytvořte nebo otevřete hlavní produkt a přejděte na jeho stránku **Detaily produktu**.
1. Nastavte možnost **Povolit převody měrných jednotek** na *Ano*.
1. V podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Převody jednotek**.
1. Otevře se stránka **Převody jednotek**. Vyberte jeden z následujících karet:

    - **Převody uvnitř třídy** - Tuto kartu vyberte, chcete-li převádět jednotky, které patří do stejné třídy jednotek.
    - **Převody vně třídy** - Tuto kartu vyberte, chcete-li převádět jednotky, které nepatří do stejné třídy jednotek.

1. K přidání nového převodu jednotek klikněte na tlačítko **Nový**.
1. Nastavte pole **Vytvořit převod pro** na jednu z následujících hodnot:

    - **Produkt** - Vyberete-li tuto hodnotu, můžete nastavit převod jednotky pro základní produkt. Tento převod jednotek bude použit jako záložní pro všechny varianty produktů, pro které není definovaný žádný převod jednotek.
    - **Varianta produkt** - Vyberete-li tuto hodnotu, můžete nastavit převod jednotky pro určitou variantu produktu. Použijte pole **Varianta produktu** k výběru varianty.

    ![Přidání nového převodu jednotek](media/uom-new-conversion.png "Přidání nového převodu jednotek")

1. K nastavení převodu jednotek použijte další pole, která jsou k dispozici.
1. Vyberte **OK** k uložení nového převodu jednotek.

> [!TIP]
> Otevřete stránku **Převody jednotek** pro produkt nebo variantu produktu z kterékoli z následujících stránek:
> 
> - Podrobnosti produktu
> - Podrobnosti o uvolněných produktech
> - Uvolněné varianty produktu

## <a name="example-scenario"></a>Příklad

V tomto scénáři společnost prodává trička ve velikostech S, M, L a XL. Tričko je definováno jako produkt a jsou definovány různé velikosti variant produktu. Košile jsou baleny v krabicích. Pro S, M a L velikosti může být v každé krabici pět košil. Avšak pro velikost XL je v každé krabici místo pouze pro čtyři košile.

Společnost chce sledovat různé varianty triček podle *kusů*, ale prodávat je po *krabicích*. U S, M a L velikostí je převod mezi jednotkou zásob a prodejní jednotkou 1 krabice = 5 kusů. U XL velikosti je převod 1 krabice = 4 kusy.

1. Ze stránky **Podrobnosti o zveřejnění produktu** pro **tričko** otevřete stránku **Převod jednotek**.
1. Na stránce **Převod jednotek** nastavte převod jednotek pro variantu produktu **XL** takto.

    | Pole                 | Nastavení                 |
    |-----------------------|-------------------------|
    | Vytvoření převodu pro | Varianta produktu         |
    | Varianta produktu       | Tričko : : XL : : |
    | Z jednotky             | Krabice                   |
    | Koeficient                | 4                       |
    | Do jednotky               | Kusy                  |

1. Protože varianty zveřejněného produktu **S**, **M** a **L** mají stejný převod jednotek mezi jednotkou *krabice* a *kusů*, znamená to, že můžete definovat převod jednotky pro tyto varianty produktu pro základní produkt.

    | Pole                 | Nastavení |
    |-----------------------|---------|
    | Vytvoření převodu pro | Produkt |
    | Produkt               | Tričko |
    | Z jednotky             | Krabice   |
    | Koeficient                | 5       |
    | Do jednotky               | Kusy  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Použití aplikace Excel pro aktualizaci převodů jednotek

Pokud má produkt mnoho variant produktu, které mají různé jednotkové převody, je vhodné exportovat jednotkové převody do sešitu Microsoft Excel, aktualizovat je a poté je publikovat zpět do Dynamics 365 Supply Chain Management.

Chcete-li exportovat jednotkové převody do Excelu, na stránce **Převody jednotek** v podokně akcí vyberte **Otevřít v Microsoft Office**.

## <a name="additional-resources"></a>Další prostředky

[Správa měrných jednotek](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
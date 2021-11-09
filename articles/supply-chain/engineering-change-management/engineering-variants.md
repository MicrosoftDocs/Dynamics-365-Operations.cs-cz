---
title: Generování variant pro technické produkty
description: Toto téma popisuje, jak generovat varianty pro technické produkty
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e24bceac9457212ecaafda876d19ba62df049371
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2021
ms.locfileid: "7471829"
---
# <a name="generate-variants-for-engineering-products"></a>Generování variant pro technické produkty

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak generovat varianty pro technické produkty.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Zapnutí generování variant pro technické produkty

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Správa technických změn*
- **Název funkce:** *Zapnutí generování variant pro technické produkty*

> [!IMPORTANT]
> Funkce *Generování variant pro technické produkty* bude ve vašem systému viditelná až poté, co povolíte konfigurační klíč *Správa technických změn*. Pokyny naleznete v tématu [Přehled správy technických změn](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Generování jedné nebo více nových variant technického produktu

Můžete vytvořit jednu nebo více nových variant produktu a nekopírovat přitom informace z existujícího produktu. To je užitečné, když potřebujete vytvořit několik variant produktu současně.

Následující postup poskytuje příklad, jak vytvořit několik variant obsahujících barevnou dimenzi.

1. Otevřete stránku **Uvolněné produkty** (například přechodem do nabídky **Správa technických změn \> Běžné \> Uvolněné produkty**).
1. V podokně akcí otevřete kartu **Produkt** a ve skupině **Nový** zvolte **Technický produkt**.
1. Otevře se dialogové okno **Nový produkt** . Vyberte příslušnou **Technickou kategorii**.
1. Pokud zvolená technická kategorie obsahuje varianty dimenzí, můžete pro ně nyní nastavit hodnoty. Když má například kategorie dimenzi **Barva**, můžete ji nastavit na *Modrá*.
1. Podle potřeby proveďte další nastavení. Tlačítkem **OK** vytvořte produkt.
1. Vytvoří se produkt a modrá varianta V-1, a nový produkt se poté otevře.
1. Podle potřeby k variantě přidejte kusovník (BOM) a trasu.
1. V podokně akcí otevřete kartu **Produkt** a ve skupině **Základní produkt** zvolte **Dimenze produktu**.
1. Otevře se stránka **Dimenze produktu**. Tato stránka obsahuje kartu pro každou dostupnou dimenzi. Na každé kartě přidejte řádek pro každou hodnotu, kterou budete podporovat u každé relevantní dimenze. (V tomto případě můžete přidat řádky do karty **Barva** s hodnotami *Bílá*, *Žlutá*, a *Zelená*).
1. Zavřete stránku a vyberte **Vydané varianty produktu**. Všimněte si, že se objeví první varianta, kterou jste vytvořili (modrá V-1).
1. V podokně akcí na kartě **Varianta produktu** vyberte **Návrhy variant**.
1. V dialogovém okně **Návrhy variant** proveďte některý z těchto kroků:

    - V horní části dialogového okna je sekce pro každou dostupnou dimenzi. U každé dimenze zaškrtněte políčko u každé hodnoty, pro kterou chcete vygenerovat návrh varianty, a poté vyberte **Navrhnout** na panelu nástrojů. Příslušné návrhy jsou přidány do sekce **Navrhované varianty**.
    - Vyberte **Navrhnout vše** na panelu nástrojů, aby se generovaly návrhy variant pro všechny dostupné kombinace hodnot dimenze. Návrhy jsou přidány do sekce **Navrhované varianty**.

1. V sekci **Navrhované varianty** zaškrtněte políčko u každé varianty, kterou chcete vytvořit. Pak výběrem možnosti **Vytvořit** generujte a vydejte vybrané varianty pro technickou společnost. Platí následující podmínky:

    - Žádná z vytvořených variant nebude mít kusovník ani trasu.
    - Atributy pro tyto varianty budou mít výchozí hodnoty z technické kategorie a nebudou zkopírovány z předchozí varianty.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Generování varianty jako kopie jiné varianty produktu

Variantu produktu můžete vytvořit na základě jiné varianty produktu. Kusovník (BOM) a trasa ze zdrojové varianty produktu jsou zkopírovány do nové varianty. To může být užitečné u samostatných technických produktů, kde může být užitečné vytvořit kusovník na základě počátečního kusovníku a sledovat změny oproti předchozí variantě. Aby byla zachována sledovatelnost, systém zaznamenává, která varianta byla zkopírována, aby vytvořila novou kopii.

Následující postup poskytuje příklad, jak vytvořit novou variantu obsahující barevnou dimenzi vytvořením kopie stávající varianty

1. Otevřete stránku **Uvolněné produkty** (například přechodem do nabídky **Správa technických změn \> Běžné \> Uvolněné produkty**).
1. V podokně akcí otevřete kartu **Produkt** a ve skupině **Nový** zvolte **Technický produkt**.
1. Otevře se dialogové okno **Nový produkt** . Vyberte příslušnou **Technickou kategorii**.
1. Pokud zvolená technická kategorie obsahuje varianty dimenzí, můžete pro ně nyní nastavit hodnoty. Když má například kategorie dimenzi **Barva**, můžete ji nastavit na *Modrá*.
1. Podle potřeby proveďte další nastavení. Tlačítkem **OK** vytvořte produkt.
1. Vytvoří se produkt a modrá varianta V-1, a nový produkt se poté otevře.
1. Podle potřeby k variantě přidejte kusovník (BOM) a trasu.
1. Podle potřeby k variantě produktu přidejte atributy.
1. Přidejte do objednávky technických změn modrou variantu produktu V-1.
1. Nastavte **Dopad** na hodnotu *Nová varianta*.
1. Vyberte novou hodnotu barvy (např. *Bílá*). Platí následující podmínky: 
    - Nová varianta má kusovník a trasu, které byly zkopírovány z předchozí varianty.
    - Nová varianta má atributy zkopírované z předchozí varianty.
1. Schvalte změnový příkaz.
1. Zpracujte změnový příkaz. Po zpracování příkazu bude vytvořena nová varianta V-1 a uvolněna do technické společnosti.

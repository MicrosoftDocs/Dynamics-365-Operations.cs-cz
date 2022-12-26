---
title: Třídy menší než nákladní vůz (LTL)
description: Tento článek vysvětluje, co jsou třídy menší než nákladní vůz (LTL), a popisuje, jak je nastavit v Microsoft Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9c1c7233b637b84ec901d7f83ae00f8a04895edb
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838411"
---
# <a name="less-than-truckload-ltl-classes"></a>Třídy menší než nákladní vůz (LTL)

[!include [banner](../includes/banner.md)]

Třída méně než nákladní vůz (LTL) je třída nákladní dopravy, která se používá ke klasifikaci položek, které lze odeslat. Obecně platí, že každý typ produktu nebo komodity má kód národní klasifikace nákladní dopravy (NMFC), který odpovídá konkrétnímu číslu třídy nákladní dopravy pro zásilky LTL. Nákladní třídy LTL představují kategorie položek, zatímco kódy NMFC se vztahují ke konkrétním komoditám v každé z 18 nákladních tříd.

Tato funkce systému umožňuje provádět následující úlohy:

- Definovat třídy nákladní dopravy LTL, které se ve vaší společnosti používají.
- Přiřadit každou třídu LTL kódu NMFC na stránce **Kódy NMFC**. Další informace viz [Kódy Národní klasifikace nákladní dopravy (NMFC)](nmfc-codes.md).
- Přiřadit každému produktu kód NMFC (a tedy jeho přidružený kód LTL) na stránce **Produkty**.
- Přesně vyhodnotit třídu LTL každého produktu, kterému je přiřazen kód NMFC.
- Určit požadavky na balení pro každou třídu LTL kontrolou mezinárodních standardů LTL. Tímto způsobem zajistíte, že vaše výrobky budou dobře chráněny a bezpečně odeslány.
- Získejte přesné odhady dopravy na základě přepravní třídy LTL pro každý produkt.

Tento článek popisuje, jak vytvořit třídy LTL v řešení Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Vytvoření třídy LTL

Třídu LTL vytvoříte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Třídy LTL**.
    - Přejděte do nabídky **Správa přepravy \> Nastavení \> Přepravní normy \> Třídy LTL**.

2. V podokně Akce vyberte možnost **Nový** a vytvořte třídu LTL. Poté nastavte následující pole:

    - **Třída LTL** – Zadejte interní identifikátor (ID) třídy LTL vaší společnosti pro typ komodity. Většina společností používá mezinárodní standard. V takovém případě bude hodnota tohoto pole odpovídat hodnotě parametru pole **Třída**. Pokud však vaše společnost používá svůj vlastní standard, zadejte kód, který tomuto standardu vyhovuje.
    - **Název** – Zadejte popisný název, který vám a dalším uživatelům pomůže vybrat správnou třídu LTL pro každý kód NMFC.
    - **Třída** – Zadejte mezinárodní standardní ID třídy LTL pro typ komodity. Kód, který zde zadáte, musí odpovídat oficiálnímu standardu.

## <a name="example-set-up-ltl-classes"></a>Příklad: Nastavení tříd LTL

Následující příklad ukazuje, jak nastavit dva různé třídy LTL, které můžete použít s různými typy produktů.

1. Přejděte na **Správa skladu \> Nastavení \> Zásoby \> Třídy LTL** nebo **Správa přepravy \> Nastavení \> Standardy přepravy \> Třídy LTL**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Třída LTL:** *92.5*
    - **Název:** *Počítače, monitory, chladničky*
    - **Třída:** *92.5*

1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Třída LTL:** *125*
    - **Název:** *Malé domácí spotřebiče*
    - **Třída:** *125*

1. V podokně akcí vyberte **Uložit**.

## <a name="additional-resources"></a>Další prostředky

- [Kódy Motor Freight Classification (NMFC)](nmfc-codes.md)
- [Vytvoření přepravního dokladu](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

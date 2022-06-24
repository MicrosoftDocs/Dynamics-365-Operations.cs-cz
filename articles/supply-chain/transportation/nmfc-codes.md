---
title: Kódy Motor Freight Classification (NMFC)
description: Tento článek popisuje, jak pracovat s kódy National Motor Freight Classification (NMFC) v Microsoft Dynamics 365 Supply Chain Management
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 522e4d4e26b04b5ca1dd317e433c5a20ff3cb12e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893258"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Kódy Motor Freight Classification (NMFC)

[!include [banner](../includes/banner.md)]

Kódy National Motor Freight Classification (NMFC) vám pomohou klasifikovat položky, které lze odeslat. Kód NMFC je označení, které se používá ke seskupení komodit. Umožňuje přepravním společnostem vyhodnotit zboží k odeslání klasifikací položek na základě úvah, jako je vhodnost kamionu, problémy s nakládáním, problémy s manipulací a rychle se kazící zboží. Komodity jsou seskupeny do jedné z 18 nákladních tříd pomocí řady čísel od 50 do 500. Třída, do které je komodita seskupena, je založena na vyhodnocení čtyř přepravních charakteristik: hustoty, skladovatelnosti, manipulace a odpovědnosti. Společně tyto vlastnosti zajišťují přepravitelnost komodity.

Kód NMFC je přidružen ke každé přepravní položce menší než nákladní vozidlo (LTL). Například notebooku může být přiřazen NMFC, který je klasifikován na 2,5, zatímco elektrickým kabelům může být přiřazen NMFC, který je klasifikován na 65.

Tato funkce může pracovníkům pomoci použít kódy NMFC ke klasifikaci přepravních položek LTL. Několik příkladů:

- Pokud vaše společnost uvede na nákladním listu (BOL) popis nákladu, bude mít přepravce určitou představu o tom, co je náklad. Nákladní doprava je důležitá klasifikace, protože mnoho přepravních společností zakládá celý svůj obchodní model na typech nákladu, který přepravují.
- Tato klasifikace může být pro vaši společnost zásadní, protože se používá k určení nákladů na danou zátěž.
- Vaše společnost může identifikovat ziskovost logistické a přepravní společnosti LTL.

Tento článek popisuje, jak pracovat s k=ody NMFC v aplikaci Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Předpoklady

Před vytvořením kódů NMFC musíte nastavit všechny třídy nákladní dopravy LTL, které k nim musí být namapovány. Nákladní třídy LTL představují kategorie položek, zatímco kódy NMFC se vztahují ke konkrétním komoditám v každé z 18 nákladních tříd. Další informace o tom, jak pracovat s třídami LTL, najdete v části [Třídy menší než nákladní vůz (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Vytvoření kódu NMFC

Kód NMFC vytvoříte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Kódy NMFC**.
    - Přejděte do nabídky **Správa přepravy \> Nastavení \> Přepravní normy \> Kódy NMFC**.

1. Vyberte **Nový** pro vytvoření NMFC kódu. Poté nastavte následující pole:

    - **NMFC kód** - Zadejte kód NMFC pro typ komodity.
    - **Název** - Zadejte název NMFC kódu.
    - **Třída LTL** - Vyberte třídu LTL, která je přidružena k kódu NMFC.
    - **Manipulační jednotka BOL** - Definujte výchozí typ zpracování zásilky.

## <a name="example-set-up-nmfc-codes"></a>Příklad: Nastavení kódů NMFC

Následující příklad ukazuje, jak nastavit dva různé kódy NMFC, které lze použít s různými produkty.

1. Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Kódy NMFC**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **NMFC kód:** *92.5*
    - **Název:** *Počítače*
    - **Třída LTL:** *92.5*
    - **Manipulační jednotka BOL:** *Jednotka*

1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **NMFC kód:** *125*
    - **Název:** *Telefony*
    - **Třída LTL:** *125*
    - **Manipulační jednotka BOL:** *Jednotka*

1. V podokně akcí vyberte **Uložit**.

## <a name="additional-resources"></a>Další prostředky

- [Méně než třídy nákladu (LTL)](ltl-class.md)
- [Vytvoření přepravního dokladu](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Vratné poplatky jsou špatně vypočítány na základě vráceného množství
description: Tento článek poskytuje pokyny pro odstraňování problémů, které mohou pomoci, když pokladní vidí nesprávné vratné poplatky v pokladním místě (POS) za množství vrácených položek.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 7a84207f587a826b9acdfd818c64220c5327bde1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890236"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Vratné poplatky jsou špatně vypočítány na základě vráceného množství

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro odstraňování problémů, které mohou pomoci, když pokladní vidí nesprávné vratné poplatky v pokladním místě (POS) za množství vrácených položek.

## <a name="description"></a>Popis

Zákazník vrátí částečné množství položek, které byly zakoupeny v prodejní objednávce, která obsahuje vratné poplatky na úrovni řádku. Místo částečného vrácení peněz však POS zobrazuje všechny poplatky jako vratné.

Zákazník například zakoupí množství pěti položek s cenou 5 USD za položku a celkové náklady jsou 25 USD. Zákazník poté vrátí tři z pěti položek. Pokladníkovi se však na pokladně zobrazí vratný poplatek 25 USD namísto očekávaného vratného poplatku 15 USD za tři položky, které byly vráceny.

## <a name="resolution"></a>Řešení

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Zapnutí funkce Povolit vrácení poplatků na základě vráceného množství

Od verze Microsoft Dynamics 365 Commerce 10.0.26 funkce **Povolit vrácení poplatků na základě vráceného množství** umožňuje vypočítat vratné poplatky na úrovni řádku na základě množství vrácených položek.

Chcete-li povolit funkci **Povolit vrácení poplatků na základě vráceného množství** v ústředí Commerce, postupujte takto.

1. Otevřete pracovní prostor **Správa funkcí** (**Správce systému \> Pracovní prostory \> Správa funkcí**).
1. V seznamu dostupných funkcí vyhledejte a vyberte funkci **Povolit vrácení poplatků na základě vráceného množství**.
1. V pravém podokně vyberte **Povolit**.

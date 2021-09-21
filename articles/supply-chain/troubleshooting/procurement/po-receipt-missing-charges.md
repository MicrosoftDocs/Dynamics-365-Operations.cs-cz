---
title: Příjemka nákupní objednávky nezahrnuje všechny poplatky
description: Příjemka nákupní objednávky nezahrnuje všechny poplatky
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475754"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Příjemka nákupní objednávky nezahrnuje všechny poplatky

## <a name="symptoms"></a>Příznaky

Když obdržíte objednávku, ne všechny poplatky jsou zahrnuty v potvrzení.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Na stránce **Parametry modulu Zásobování a zdroje** na kartě **Dodávka** se ujistěte, že možnost **Generovat náklady na příjemce produktu** je nastavena na *Ano*.
1. Vytvořte nákupní objednávku, která obsahuje náklady.
1. Potvrďte nákupní objednávku.
1. Přijměte nákupní objednávku.
1. Podívejte se na celkový příjem a porovnejte jej s očekávaným součtem.
1. Všimněte si, že ne všechny poplatky jsou zahrnuty v příjemce nákupní objednávky.

## <a name="resolution"></a>Řešení

Řešení závisí na způsobu, jakým byly nastaveny vedlejší náklady. Informace o tom, jak nastavit vedlejší náklady podle vašich požadavků, najdete v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

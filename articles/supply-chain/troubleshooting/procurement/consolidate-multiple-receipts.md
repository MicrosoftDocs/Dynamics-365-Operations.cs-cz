---
title: Nemůžete konsolidovat více příjemek produktu do jedné nákupní objednávky
description: Nelze sloučit více příjemek produktu do jedné nákupní objednávky, pokud mají různé řádky příjemek produktu různá data zaúčtování.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475765"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Nemůžete konsolidovat více příjemek produktu do jedné nákupní objednávky

## <a name="symptoms"></a>Příznaky

Nelze sloučit více příjemek produktu do jedné nákupní objednávky, pokud mají různé řádky příjemek produktu různá data zaúčtování.

## <a name="resolution"></a>Řešení

V dřívějších verzích Dynamics 365 Supply Chain Management byla konsolidace v této situaci povolena. Tento postup je však náchylný k chybám. Datum zaúčtování na řádcích nákupní objednávky, které jsou vytvořeny, by se nemělo lišit od účetního data na řádcích příjemky produktu, ze kterých byly tyto řádky nákupní objednávky vytvořeny. (Datum účtování na řádcích nákupní objednávky odpovídá datu účtování v záhlaví nákupní objednávky.) Konsolidace více příjemek produktu do jedné nákupní objednávky proto již není povolena.

Datum účtování se používá například pro rozpočtové rezervace a břemeno. Proto by mělo být uchováno během přechodu z příjemky produktu na nákupní objednávku.

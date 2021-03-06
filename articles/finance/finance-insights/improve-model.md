---
title: Vylepšit model předpovědi (preview)
description: Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186635"
---
# <a name="improve-the-prediction-model-preview"></a>Vylepšit model předpovědi (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů. Model začnete vylepšovat v pracovním prostoru **Předpovědi plateb zákazníka** v Microsoft Dynamics 365 Finance. Kroky vylepšení jsou poté dokončeny v AI Builderu.

## <a name="select-historical-outcomes"></a>Vyberte historické výsledky

Nejprve vyberete jeden nebo více ze tří možných výsledků pro faktury: **Včas**, **Pozdě** a **Velmi pozdě**. Měly by být vybrány všechny tři výsledky. Pokud zrušíte výběr některého z výsledků, faktury se odfiltrují z procesu cvičení a přesnost predikce se sníží.

[![Potvrzování výsledků](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Pokud vaše organizace vyžaduje pouze dva výsledky, změňte prahové hodnoty **Pozdě** a **Velmi pozdě** na 0 (nula) dnů. Tímto způsobem efektivně sbalíte předpověď na binární stav **Včas** nebo **Pozdě**.

## <a name="select-fields"></a>Vybrat pole

Při výběru polí, která chcete zahrnout do modelu, mějte na paměti, že seznam obsahuje všechna dostupná pole v tabulce Microsoft Dataverse, která je mapována na data v datovém jezeře Azure. Některá z těchto polí by **neměla** být vybrána. Pole, která by neměla být vybrána, spadají do jedné ze tří kategorií:

- Pole je povinné pro tabulku Dataverse, ale v datovém jezeře pro ni neexistují žádná podpůrná data.
- Pole je ID, a proto nemá smysl pro funkci strojového učení.
- Pole představuje informace, které během predikce nebudou k dispozici.

V následujících částech jsou uvedena pole, která jsou k dispozici pro entity faktury a zákazníka, a seznam polí, která by **neměla** být vybrána pro cvičení. Kategorie, která je zadána pro každé z těchto polí, odkazuje na kategorie v předchozím seznamu.
 
### <a name="invoice-dataverse-table"></a>Tabulka faktury Dataverse

Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku faktury.

[![Dostupná pole pro tabulku faktury](./media/available-fields.png)](./media/available-fields.png)

Následující pole by pro cvičení neměla být vybrána:

- **Účet faktury** (kategorie 2)
- **Je zavřena** (kategorie 3) - Toto pole se používá k filtrování faktur ke cvičení (uzavřeno) a předpověď (neuzavřeno).
- **Název** (kategorie 1)
- **ID zdroje** (kategorie 2)
- **Záznam zdroje** (kategorie 2)
- **Zdrojová tabulka** (kategorie 2)

### <a name="customer-dataverse-table"></a>Tabulka zákazníka Dataverse

Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku zákazníka.

[![Dostupná pole pro tabulku zákazníka](./media/related-entities.png)](./media/related-entities.png)

Následující pole by pro cvičení nemělo být vybráno:

- **Unikátní klíč řádku** (kategorie 2)

## <a name="filters"></a>Filtry

Filtry aktuálně nepodporují scénář predikce plateb zákazníka. Proto vyberte **Přeskočit tento krok** a pokračujte na souhrnnou stránku.

[![Detailní model s filtry](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

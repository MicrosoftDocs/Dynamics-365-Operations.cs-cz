---
title: Kde byla položka použita
description: Tohle téma popisuje, jak získat přehled o tom, kde se používá položka v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918319"
---
# <a name="item-where-used"></a>Kde byla položka použita

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Můžete provést výpočet pro určitou položku, abyste získali přehled o tom, kde je použita položka v modulu Správa majetku. Ve výsledcích se zobrazuje kontext, ve kterém byla položka použita během její životnosti. Stránku **Kde byla položka použita** lze otevřít z hlavní nabídky modulu Správa majetku a lze ji také otevřít z následujících stránek:

[Kusovník majetku](../objects/object-BOM.md)

[Náhradní díly ve výchozích nastaveních typu majetku](../setup-for-objects/object-types.md)

[Prognóza položky v prognóze výchozích nastavení typu práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[Prognóza údržby pracovního příkazu](../work-orders/maintenance-forecasts.md)

[Nákupní žádanka pracovního příkazu](../work-orders/procurement.md)

[Nákup pracovního příkazu](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Provedení výpočtu místa použití položky

1. Klikněte na možnosti **Správa majetku** > **Dotazy** > **Kde byla položka použita** nebo vyberte tlačítko **Kde byla položka použita** na jedné z výše uvedených stránek.

2. V dialogovém okně **Kde byla položka použita** vyberte položku, pro kterou chcete provést výpočet v poli **Číslo položky**.

3. V poli **Úroveň** určete, jak detailní mají být řádky položky v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a struktura funkčního místa má více úrovní, všechny řádky položek pro funkční místo budou zobrazeny na nejvyšší úrovni. Proto mohou být vztah/množství na řádku přidány z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky položky na všech úrovních funkčních míst, ke kterým se vztahují.

4. V oddílu **Zahrnout** vyberte možnost „Ano“ u přepínacích tlačítek, která chcete zahrnout do výpočtu.

5. Výpočet zahájíte klepnutím na tlačítko **OK**.

6. Na kartě **Kde byla položka použita** > ve skupinách podokna akce **> Seskupit podle...** vyberte odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka podokna akcí jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

7. Chcete-li zobrazit dimenze související s danou položkou, klikněte na možnost **Zobrazit dimenze** a vyberte dimenze, které mají být zobrazeny.

Na níže uvedeném obrázku je zobrazen příklad výpočtu použitého pro položku s číslem položky „1000“.

![Obrázek č. 1](media/12-controlling-and-reporting.png)


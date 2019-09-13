---
title: Vypočítat vytížení kapacity
description: Toto téma vysvětluje, jak vypočítat vytížení kapacity v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886786"
---
# <a name="calculate-capacity-load"></a>Vypočítat vytížení kapacity

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ve správě majetku lze vypočítat vytížení kapacity na

- řádcích rozvrhu údržby  
- pracovních příkazech, které ještě nebyly naplánovány  
- naplánovaných pracovních příkazech

To je užitečné v případě, že chcete získat přehled očekávaného vytížení kapacity pro určité období. Výpočet vytížení kapacity lze provést u veškerého majetku nebo vybraného majetku. Můžete také provést výpočet pro aktivity prostojů údržby nebo fondu pracovních příkazů.

1. Klikněte na **Správa majetku** > **Dotazy** > **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** / **Aktivní skupiny pracovních příkazů** > zvolte skupinu pracovních příkazů v seznamu > tlačítko **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny Aktivity prostojů údržby** / **Aktivní Aktivity prostojů údržby** > zvolte aktivitu údržby v seznamu > tlačítko **Vytížení kapacity**.

2. V dialogovémokně **Vypočítat vytížení kapacity** vyberte období pro výpočet v polích **Počáteční datum/čas** a **Koncové datum a čas**.

3. Chcete-li do výpočtu zahrnout řádky rozvrhu údržby, vyberte Ano na přepínači **Zahrnout rozvrh údržby**.

4. Chcete-li do výpočtu zahrnout práce pracovního příkazu, vyberte Ano na přepínači **Zahrnout pracovní příkaz**.

5. V poli **Úroveň** určete, jak detailní mají být řádky vytížení kapacity v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby a pracovní příkazy pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby a všechny pracovní příkazy na všech úrovních funkčních míst, ke kterým se vztahují.

6. Výpočet zahájíte klepnutím na tlačítko **OK**.

7. Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka skupiny podokna akcí jsou zvýrazněna modrou barvou. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

Následující obrázek ukazuje příklad rozhraní.

![Obrázek č. 1](media/01-capacity-planning.png)

>[!NOTE]
>Chcete-li se zaměřit pouze na plánování kapacity týkající se plánovaných pracovních příkazů, nahlédněte do části [Výpočet vytížení kapacity na plánovaných pracovních příkazech](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).


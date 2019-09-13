---
title: Vypočítat prognózu položky
description: Toto téma vysvětluje, jak vypočítat prognózu položky v modulu Správa majetku.
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886763"
---
# <a name="calculate-item-forecast"></a>Vypočítat prognózu položky

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Stejně jako lze provádět výpočty vytížení kapacity, které jsou popsány v předchozím oddílu, můžete také provádět výpočty prognózy položek na

- Řádky rozvrhu údržby  
- pracovních příkazech, které ještě nebyly naplánovány  
- Naplánované pracovní příkazy

To je užitečné v případě, že chcete získat přehled o očekávané spotřebě položek (náhradní díly a další položky vyžadované pro dokončení pracovních příkazů) za určité období. Výpočet prognózy položek lze provést u veškerého majetku nebo vybraného majetku. Můžete také provést výpočet v aktivitě prostoje údržby (**Všechny aktivity prostoje údržby** nebo **Aktivní aktivity prostojů údržby**) nebo ve skupině pracovních příkazů (**Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**).

1. Klikněte na **Správa majetku** > **Dotazy** > **Prognóza položkyy**, nebo **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** / **Aktivní skupiny pracovních příkazů** > zvolte skupinu pracovních příkazů v seznamu > tlačítko **Prognóza položky**, nebo **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny Aktivity prostojů údržby** / **Aktivní Aktivity prostojů údržby** > zvolte aktivitu prostoje údržby v seznamu > tlačítko **Prognóza položky**.

2. V dialogovém okně **Vypočítat prognóza položky** vyberte období pro výpočet v polích **Počáteční datum/čas** a **Koncové datum a čas**.

3. Chcete-li do výpočtu prognózy zahrnout řádky rozvrhu údržby, vyberte Ano na přepínači **Zahrnout rozvrh údržby**.

4. Chcete-li do výpočtu prognózy zahrnout práce pracovního příkazu, vyberte Ano na přepínači **Zahrnout pracovní příkaz**.

5. V poli **Úroveň** určete, jak detailní mají být řádky prognózy položky v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby a pracovní příkazy pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby a všechny pracovní příkazy na všech úrovních funkčních míst, ke kterým se vztahují.

6. Výpočet zahájíte klepnutím na tlačítko **OK**.

7. Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka skupiny podokna akcí jsou zvýrazněna modrou barvou. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

8. Chcete-li zobrazit produkt, sklad nebo sledovací dimenze související s položkami, klikněte na tlačítko **Zobrazit dimenze**. Zvolte příslušná zaškrtávací políčka a klikněte na tlačítko **OK**.

Následující obrázek ukazuje snímek obrazovky rozhraní.

![Obrázek č. 1](media/02-capacity-planning.png)

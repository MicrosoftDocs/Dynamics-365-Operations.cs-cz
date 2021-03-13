---
title: Vypočítat vytížení kapacity
description: Toto téma vysvětluje, jak vypočítat vytížení kapacity v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3aa87f5594be079144142296cac977b0bfdd125e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022576"
---
# <a name="calculate-capacity-load"></a>Vypočítat vytížení kapacity

[!include [banner](../../includes/banner.md)]


Ve správě majetku lze vypočítat vytížení kapacity na:

- řádcích rozvrhu údržby  
- pracovních příkazech, které ještě nebyly naplánovány  
- naplánovaných pracovních příkazech

To je užitečné v případě, že chcete získat přehled očekávaného vytížení kapacity pro určité období. Výpočet vytížení kapacity lze provést u veškerého majetku nebo vybraného majetku. Můžete také provést výpočet pro aktivity prostojů údržby nebo fondu pracovních příkazů.

1. Klikněte na **Správa majetku** > **Dotazy** > **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** / **Aktivní skupiny pracovních příkazů** > zvolte skupinu pracovních příkazů v seznamu > tlačítko **Vytížení kapacity**, nebo **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny Aktivity prostojů údržby** / **Aktivní Aktivity prostojů údržby** > zvolte aktivitu údržby v seznamu > tlačítko **Vytížení kapacity**.

2. V dialogovémokně **Vypočítat vytížení kapacity** vyberte období pro výpočet v polích **Počáteční datum/čas** a **Koncové datum a čas**.

3. Chcete-li do výpočtu zahrnout řádky rozvrhu údržby, vyberte Ano na přepínači **Zahrnout rozvrh údržby**.

4. Chcete-li do výpočtu zahrnout práce pracovního příkazu, vyberte Ano na přepínači **Zahrnout pracovní příkaz**.

5. V poli **Úroveň** určete, jak detailní mají být řádky vytížení kapacity v případě funkčních míst. 

    Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby a pracovní příkazy pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. 
    
    Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby a všechny pracovní příkazy na všech úrovních funkčních míst, ke kterým se vztahují.

6. Výpočet zahájíte klepnutím na tlačítko **OK**.

7. Ve skupině **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Na snímku obrazovky níže jsou vybraná tlačítka **Seskupit podle** označena modře. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

    ![Obrázek č. 1](media/01-capacity-planning.png)

>[!NOTE]
>Chcete-li se zaměřit pouze na plánování kapacity týkající se plánovaných pracovních příkazů, nahlédněte do části [Výpočet vytížení kapacity na plánovaných pracovních příkazech](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).


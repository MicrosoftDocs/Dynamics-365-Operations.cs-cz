---
title: Výpočet vytížení kapacity na plánovaných pracovních příkazech
description: Tento článek vysvětluje, jak vypočítat vytížení kapacity na plánovaných pracovních příkazech v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857946"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Výpočet vytížení kapacity na plánovaných pracovních příkazech

[!include [banner](../../includes/banner.md)]

 

Chcete-li získat přehled o vytížení práce zdrojů pro určité období, můžete vypočítat vytížení kapacity na plánovaných pracovních příkazech. Výpočty lze provádět u následujících zdrojů: pracovníci údržby, skupiny pracovníků, nástroje a majetek.

1. Klikněte na **Správa majeku** > **Dotazy** > **Plán** > **Vytížení kapacity**.

2. V dialogovém okně **Vypočítat vytížení kapacity** > pole **Zobrazit** vyberte typ vytížení, který chcete vypočítat: **Kapacita**, **Rezervované** nebo **Zůstatek**.

3. Nechcete-li zobrazit výsledky obsahující nulu, vyberte možnost **Ano** na přepínacím tlačítku **Přeskočit nulu**.

4. Vyberte typy zdroje, pro které chcete vypočítat vytížení kapacity volbou **Ano** na příslušném přepínači: **Pracovník**, **Skupina pracovníků údržby**, **Nástroj** a **Majetek**.

5. V poli **Od data** vyberte počáteční datum výpočtu.

6. V poli **Typ intervalu** vyberte interval pro výpočet: **Den**, **Týden**, **Měsíc** nebo **Čtvrtletí**.

7. V poli **Frekvence období** zadejte počet intervalů, které chcete vypočítat. Pokud jste například jako typ intervalu vybrali možnost **den** a do pole zadáte číslo "5", bude proveden výpočet pěti dnů od počátečního data.

8. Výpočet zahájíte klepnutím na tlačítko **OK**.

Níže uvedený údaj ukazuje výsledek výpočtu, který pokrývá tři týdny pro typ vytížení **Rezervováno**.

![Obrázek č. 1.](media/08-work-order-scheduling.png)

[!NOTE]
Pokud pro výpočet vyberete typ vytížení **Kapacita** nebo **Zůstatek**, zobrazí se stejný výsledek v případě, že pro zdroje ve vybraném období nebyly provedeny žádné rezervace.

Informace o způsobu výpočtu vytížení kapacity na řádcích plánu údržby a neplánovaných pracovních příkazech naleznete v tématu [Výpočet vytížení kapacity](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
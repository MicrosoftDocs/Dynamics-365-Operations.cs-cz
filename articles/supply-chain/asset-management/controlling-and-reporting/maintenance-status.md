---
title: Stav údržby
description: Toto téma vysvětluje, jak vypočítat stav údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 138e2e72fbf761d209d288c2bd778c08519b9c69b0715f4466d4838255a2a31e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752002"
---
# <a name="maintenance-status"></a>Stav údržby

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete vytvořit výpočet přehledu nových, aktivních a dokončených požadavků na údržbu, pracovních příkazů a aktivit prostojů údržby za určité období. Můžete také zobrazit počet provedených odhadů podmínek pro stejné období. Pomocí tohoto výpočtu získáte přehled o pracovním vytížení, které se týká příchozích a dokončených požadavků na údržbu a pracovních příkazů.

## <a name="make-a-maintenance-status-calculation"></a>Výpočet stavu údržby

1. Klikněte na možnosti **Správa majetku** > **Dotazy** > **Stav údržby**.

2. V dialogovém okně **Stavvýpočtu** vyberte časový rozsah, pro který chcete provést výpočet v polích **Od data** a **Do data**.

3. V poli **Úroveň** určete, jak detailní mají být řádky údržby v případě funkčních míst. 

  Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky údržby pro funkční místo, a proto lze stav na řádku navýšit z funkčních míst na nižší úrovni. 
  
  Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky údržby na všech úrovních funkčních míst, ke kterým se vztahují.

4. Výpočet zahájíte klepnutím na tlačítko **OK**.

5. Ve skupině **Seskupit podle** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka **Seskupit podle** jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

6. Nezapomeňte tlačítkem **Aktualizovat** aktualizovat výpočet při každé změně aktivací nebo deaktivací tlačítek **Seskupit podle** nebo provedením výpočtu pro nové období.

7. Klikněte na možnost **Stav**, chcete-li vytvořit nový výpočet stavu údržby.

>[!NOTE]
>Výsledky zobrazené v sekci **Stav údržby** zahrnují pouze požadavky na údržbu a pracovní příkazy, které mají skutečný počáteční datum a čas. Pole koncového data a času mohou být prázdná.

## <a name="example-1"></a>Příklad 1

Na níže uvedeném snímku obrazovky jsou aktivována tlačítka **Rok** a **Měsíc**. Při vybraných těchto možnostech **Seskupit podle** získáte obecný přehled o měsíčním pracovním vytížení a propustnosti, které souvisejí s požadavky na údržbu a pracovními příkazy. 

![Příklad měsíčního pracovního vytížení.](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Příklad 2

Na níže uvedeném snímku obrazovky byly přidány informace o funkčních místech. Nyní je možné porovnat pracovní vytížení a propustnost mezi funkčními místy, která mohou představovat geografická umístění, továrny nebo pracovní oblasti. 

![Příklad měsíčního pracovního vytížení s funkčními místy.](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
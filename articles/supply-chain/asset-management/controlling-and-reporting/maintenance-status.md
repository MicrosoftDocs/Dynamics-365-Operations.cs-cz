---
title: Stav údržby
description: Toto téma vysvětluje, jak vypočítat stav údržby v modulu Správa majetku.
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918342"
---
# <a name="maintenance-status"></a>Stav údržby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V modulu Správa majetku můžete výpočtem získat přehled nových, aktivních a dokončených požadavků na údržbu, pracovních příkazů a aktivit prostojů údržby za určité období. Můžete také zobrazit počet provedených odhadů podmínek pro stejné období. Pomocí tohoto výpočtu získáte přehled o pracovním vytížení, které se týká příchozích a dokončených požadavků na údržbu a pracovních příkazů.

## <a name="make-a-maintenance-status-calculation"></a>Výpočet stavu údržby

1. Klikněte na možnosti **Správa majetku** > **Dotazy** > **Stav údržby**.

2. V dialogovém okně **Stavvýpočtu** vyberte období, pro které chcete provést výpočet v polích **Od data** a **Do data**.

3. V poli **Úroveň** určete, jak detailní mají být řádky údržby v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky údržby pro funkční místo, a proto lze stav na řádku navýšit z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky údržby na všech úrovních funkčních míst, ke kterým se vztahují.

4. Výpočet zahájíte klepnutím na tlačítko **OK**.

5. Ve skupině podoken akcí **Seskupit podle...** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka podokna akcí jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

6. Nezapomeňte tlačítkem **Aktualizovat** aktualizovat výpočet při každé změně aktivací nebo deaktivací tlačítek **Skupiny pole...** nebo provedením výpočtu pro nové období.

7. Klikněte na možnost **Stav**, chcete-li vytvořit nový výpočet stavu údržby.

>[!NOTE]
>Výsledky zobrazené v sekci **Stav údržby** zahrnují pouze požadavky na údržbu a pracovní příkazy, které mají skutečný počáteční datum a čas. Pole koncového data a času mohou být prázdná.

*Příklad 1:*

Na níže uvedeném obrázku jsou aktivovány tlačítka **Rok** a **Měsíc**. Zde získáte obecný přehled o měsíčním pracovním vytížení a propustnosti, které souvisejí s požadavky na údržbu a pracovními příkazy. 

![Obrázek č. 1](media/13-controlling-and-reporting.png)

*Příklad 2:*

Na níže uvedeném obrázku byly přidány informace o funkčních místech. Nyní je možné porovnat pracovní vytížení a propustnost mezi funkčními místy, která mohou představovat geografická umístění, továrny nebo pracovní oblasti. 

![Obrázek č. 2](media/14-controlling-and-reporting.png)


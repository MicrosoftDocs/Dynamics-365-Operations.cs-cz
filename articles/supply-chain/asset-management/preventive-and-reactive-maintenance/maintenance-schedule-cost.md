---
title: Náklady rozvrhu údržby
description: Toto téma popisuje náklady rozvrhu údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8feea75bb223bdbd013b11cdf3a63d504afb04f5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208195"
---
# <a name="maintenance-schedule-cost"></a>Náklady rozvrhu údržby

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku lze vypočítat rozpočtové náklady na řádcích rozvrhu údržby. To je užitečné v případě, že chcete získat přehled o očekávaných nákladech, například nákladech na plánované preventivní práce údržby pro další rok. Výpočty jsou založeny na stávajících řádcích rozvrhu údržby typu „Plány údržby“ a „Pořadí údržby“ a „Požadavky na údržbu“.

1. Klinkěte na položky **Správa majetku** > **Dotazy** > **Majetek** > **Náklady rozvrhu údržby**.

2. V dialogovém okně **Náklady rozvrhu údržby** můžete vybrat **sadu finančních dimenzí**, pokud chcete zobrazit náklady seskupené ve finančních dimenzích.

>[!NOTE]
>Sady finančních dimenzí se nastavují v části **Hlavní kniha** > **Účtová osnova** > **Dimenze** > **Sady finančních dimenzí**.

3. V poli **Úroveň** určete, jak detailní mají být řádky rozvrhu údržby v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky rozvrhu údržby pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky rozvrhu údržby na všech úrovních funkčních míst, ke kterým se vztahují.

4. Chcete-li provést výpočet pro určitý majetek, klikněte na položku **Filtr** na záložce s náhledem **Záznamy k zahrnutí** a vyberte příslušný majetek. Je-li to nutné, můžete také datum **Očekávané zahájení** pro výpočet nákladů nebo vybrat jiný **Stav** pro výpočet nákladů.

5. Výpočet nákladů zahájíte klepnutím na tlačítko **OK**.

6. Na kartě **Náklady rozvrhu údržby** ve skupinách podokna akce **Seskupit podle...** vyberte odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu nákladů. Vybraná tlačítka skupiny podokna akcí jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

7. Chcete-li provést nový výpočet nákladů, klikněte na tlačítko **Vypočítat náklady**.

Na následujícím obrázku jsou uvedeny výsledky výpočtu nákladů rozvrhu údržby.

![Obrázek č. 1](media/17-preventive-maintenance.png)


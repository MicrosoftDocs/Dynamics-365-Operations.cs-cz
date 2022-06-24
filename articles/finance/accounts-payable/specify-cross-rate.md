---
title: Stanovení křížového kurzu
description: Tento článek obsahuje obecné informace o křížených sazbách v aplikaci Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889954"
---
# <a name="specify-the-cross-rate"></a>Stanovení křížového kurzu

[!include [banner](../includes/banner.md)]

Tento článek popisuje účel křížového kurzu a zadání křížového kurzu při vyrovnání platby s fakturou. Křížový kurz použijte, pokud platí následující kritéria: 
-   Má být vyrovnána platba pro fakturu. 
-   Řádek platby a řádek faktury používají různé měny. 
-   Ani jedna měna není zúčtovací měna. 

Křížový kurz není použit pro výpočet pro převod měny transakce platby na zúčtovací měnu platby. Místo toho směnné kurzy z tabulky směnných kurzů jsou načteny pro výpočet hodnoty částky měny platební transakce platby a částky zúčtovací měny platby. 

Například zúčtovací měna je USD, měna faktury je CAD a měna platby je EUR. Křížový kurz umožňuje zadat směnný kurz pro převod přímo mezi CAD a EUR a není nutný převod prostřednictvím USD. Pokud vyberete fakturu a primární platbu, můžete pro řádek faktury zadat křížovou měnu. Termínem křížová měna se označuje směnný kurz mezi měnami pro transakce s ohledem na datum vyrovnání.

1.  Přejděte na jednu z následujících stránek:
- **Pohledávky> Společné > Odběratelé > Všichni odběratelé** 
- **Závazky> Společné > Dodavatelé > Všichni dodavatelé** 
- **Zásobování a zdroje > Společné > Dodavatelé > Všichni dodavatelé.**
2.  Vyberte odběratele nebo dodavatele, jejichž otevřené transakce mají být vyrovnány. 
3.  Pro odběratele na stránce se seznamem **Všichni odběratelé** přejděte na **Shromáždit > Vyrovnat otevřené transakce**. Pro dodavatele na stránce se seznamem **Všichni dodavatelé** přejděte na **Faktura > Vyrovnat otevřené transakce**. 
4.  Vyberte transakci, která je primární platbou, a klikněte na **Označit platbu**. Bude zaškrtnuto políčko ve sloupci **Označit** a ve sloupci **Primární platba** bude zobrazena ikona pro informace. 
5.  V poli **Křížový kurz** zadejte směnný kurz mezi měnou faktury a měnou platby, s ohledem na datum vyrovnání. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

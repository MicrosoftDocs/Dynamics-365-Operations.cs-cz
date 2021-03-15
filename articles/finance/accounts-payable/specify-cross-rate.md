---
title: Stanovení křížového kurzu
description: Toto téma obsahuje obecné informace o křížených sazbách v aplikaci Microsoft Dynamics 365 Finance.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 317cad877cec4d9f02f53762af65f0b226d0aad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979381"
---
# <a name="specify-the-cross-rate"></a>Stanovení křížového kurzu

[!include [banner](../includes/banner.md)]

Toto téma popisuje účel křížového kurzu a zadání křížového kurzu při vyrovnání platby s fakturou. Křížový kurz použijte, pokud platí následující kritéria: 
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
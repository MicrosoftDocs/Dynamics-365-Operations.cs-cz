---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o funkci uznání výnosů. Tato funkce poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů pro objednávky s více prvky.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458641"
---
# <a name="revenue-recognition-overview"></a>Přehled uznání výnosů

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funkci uznání výnosů nelze zapnout pomocí správy funkcí. Pro její zapnutí musíte momentálně použít konfigurační klíče.

Společnosti v průmyslových odvětvích, které prodávají více prvků, jako jsou produkty, služby, předplatné atd., musí být schopny rozdělit objednávky s více prvky, aby mohly být výnosy přiznány na základě souboru pokynů pro jednotlivé společnosti a pro jednotlivá odvětví.

Obecně lze proces přiznání výnosů použít k provedení těchto úloh:

* Přiřazení výnosů, abyste mohli zaručit, že příslušná výnosová cena bude uznána na základě hodnoty komponent na objednávkách s více prvky.
* Odložení výnosů na základě plánu výnosů, který představuje smluvní časový rámec a procenta pro uznání výnosů v čase.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Video [Způsob použití uznání výnosů v Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (zobrazené výše) je zahrnuto do [playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupného na YouTube.

Funkce uznání výnosů poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů.

Uvolněné produkty se používají pro podporu uznání výnosů v dokumentech prodejních objednávek. Uvolněné produkty obsahují nastavení, které je vyžadováno pro určení výnosové ceny a plánu výnosů. Prodejní objednávka může pocházet z projektu určeného časem a materiálem.

Společnosti mohou používat funkcionalitu plánu výnosů bez použití funkcionality výnosové ceny. Proto se cena na řádcích prodejní objednávky použije buď jako výnos nebo jako odložený výnos. Pokud na řádku prodejní objednávky existuje plán výnosů, cena na řádku prodejní objednávky se odloží. Pokud na řádku prodejní objednávky neexistuje plán výnosů, cena na řádku prodejní objednávky bude zaúčtována na účet výnosů v okamžik, kdy je fakturována.

Výnosová cena se vypočítá buď při potvrzení prodejní objednávky nebo při zaúčtování faktury. Chcete-li zobrazit náhled výnosové ceny před zaúčtováním faktury, musíte potvrdit prodejní objednávku.

Když je prodejní objednávka potvrzena, vytvoří se též plán očekávaných výnosů, pokud některý z řádků prodejní objednávky má plán výnosů. Když je prodejní objednávka vyfakturována, plán očekávaných výnosů je odstraněn a je nahrazen za plán uznání skutečných výnosů.

Podrobnosti plánu uznání výnosů se udržují pro každý řádek prodejní objednávky. Proto může manažer uznání výnosů zobrazit podrobnosti a uvolnit řádky do výnosů, když byl dokončen smluvní závazek. Na konci každého období může manažer uznání výnosů vytvořit deník výnosů, aby uvolnil všechny řádky plánu, které jsou splatné v den nebo před dnem, který určí. Tento deník výnosů není zaúčtován okamžitě. Proto může manažer uznání výnosů ověřit, že jsou z odložených výnosů do skutečných výnosů uvolňovány správné částky.

Pokud smluvní změna způsobí přidání nového řádku prodejní objednávky buď do existující prodejní objednávky nebo nové prodejní objednávky, lze spustit proces přidělení, aby se opravila výnosová cena napříč všemi řádky v prodejních objednávkách.

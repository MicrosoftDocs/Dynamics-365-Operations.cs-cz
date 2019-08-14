---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o funkci uznání výnosů. Tato funkce poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů pro objednávky s více prvky.
author: kweekley
manager: aolson
ms.date: 08/24/2018
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
ms.openlocfilehash: d52a9c7315cccf668a8b9bcf7ba5cad7039e186e
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863556"
---
# <a name="revenue-recognition-overview"></a>Přehled uznání výnosů

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Funkci uznání výnosů nelze ještě zapnout pomocí správy funkcí. Pro její zapnutí musíte momentálně použít konfigurační klíče.

Společnosti v průmyslových odvětvích, které prodávají více prvků, jako jsou produkty, služby, předplatné atd., musí být schopny rozdělit objednávky s více prvky, aby mohly být výnosy přiznány na základě souboru pokynů pro jednotlivé společnosti a pro jednotlivá odvětví.

Obecně lze proces přiznání výnosů použít k provedení těchto úloh:

* Přiřazení výnosů, abyste mohli zaručit, že příslušná výnosová cena bude uznána na základě hodnoty komponent na objednávkách s více prvky.
* Odložení výnosů na základě plánu výnosů, který představuje smluvní časový rámec a procenta pro uznání výnosů v čase.

Funkce uznání výnosů poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů.

Uvolněné produkty se používají pro podporu uznání výnosů v dokumentech prodejních objednávek. Uvolněné produkty obsahují nastavení, které je vyžadováno pro určení výnosové ceny a plánu výnosů. Prodejní objednávka může pocházet z projektu určeného časem a materiálem.

Společnosti mohou používat funkcionalitu plánu výnosů bez použití funkcionality výnosové ceny. Proto se cena na řádcích prodejní objednávky použije buď jako výnos nebo jako odložený výnos. Pokud na řádku prodejní objednávky existuje plán výnosů, cena na řádku prodejní objednávky se odloží. Pokud na řádku prodejní objednávky neexistuje plán výnosů, cena na řádku prodejní objednávky bude zaúčtována na účet výnosů v okamžik, kdy je fakturována.

Výnosová cena se vypočítá buď při potvrzení prodejní objednávky nebo při zaúčtování faktury. Chcete-li zobrazit náhled výnosové ceny před zaúčtováním faktury, musíte potvrdit prodejní objednávku.

Když je prodejní objednávka potvrzena, vytvoří se též plán očekávaných výnosů, pokud některý z řádků prodejní objednávky obsahuje plán výnosů. Když je prodejní objednávka vyfakturována, plán očekávaných výnosů je odstraněn a je nahrazen za plán uznání skutečných výnosů.

Podrobnosti plánu uznání výnosů se udržují pro každý řádek prodejní objednávky. Proto může manažer uznání výnosů zobrazit podrobnosti a uvolnit řádky do výnosů, když byl dokončen smluvní závazek. Na konci každého období může manažer uznání výnosů vytvořit deník výnosů, aby uvolnil všechny řádky plánu, které jsou splatné v den nebo před dnem, který určí. Tento deník výnosů není zaúčtován okamžitě. Proto může manažer uznání výnosů ověřit, že jsou z odložených výnosů do skutečných výnosů uvolňovány správné částky.

Pokud smluvní změna způsobí přidání nového řádku prodejní objednávky buď do existující prodejní objednávky nebo nové prodejní objednávky, lze spustit proces přidělení, aby se opravila výnosová cena napříč všemi řádky prodejních objednávek.

---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o funkci uznání výnosů. Tato funkce poskytuje flexibilní rámec, který vaší společnosti umožňuje definovat vlastní pravidla uznání výnosové ceny a plánu výnosů pro objednávky s více složkami.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ef59e6a3a0c553ad43db2ed35cb68b57c505f2ac7414592880e361fa3f5c4a12
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756266"
---
# <a name="revenue-recognition-overview"></a>Přehled uznání výnosů

[!include [banner](../includes/banner.md)]

Společnosti podnikající v oborech, kde se obchoduje s více složkami, jako jsou produkty, služby nebo předplatná, musí umět rozlišovat jednotlivé složky na objednávkách, takže jejich výnosy mohou být uznány na základě souboru pokynů pro jednotlivé společnosti a odvětví.

> [!NOTE]
> Funkci uznání výnosů nelze zapnout prostřednictvím správy funkcí. V současné době ji aktivujete pomocí konfiguračních klíčů.

> Uznání výnosů (včetně funkce sady) nelze použít v kanálech Commerce (elektronické obchodování, POS, kontaktní středisko). Položky konfigurované s uznáním výnosů nesmí být přidány na objednávky nebo do transakcí vytvořených v kanálech Commerce.

Obecně lze uznání výnosů použít k následujícím účelům:

* Přidělení výnosů, které pomáhá zaručit, že příslušná výnosová cena bude uznána na základě hodnoty komponent na objednávkách s více složkami.
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
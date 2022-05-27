---
title: Změna nebo odstranění původní mezipodnikové prodejní objednávky
description: Toto téma vysvětluje změnu a odstranění původní prodejní objednávky
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cfacd1710aa5812230395409f1dd7c2e882faa9f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673739"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Změna nebo odstranění původní mezipodnikové prodejní objednávky

[!include [banner](../../includes/banner.md)]

Když změníte prodejní objednávku, jsou změny automaticky synchronizovány s příslušnou mezipodnikovou nákupní objednávkou a s mezipodnikovou prodejní objednávkou.

> [!NOTE]
> Na nákupní objednávky pro externí dodavatele nemají provedené změny vliv, ani se řádky původní prodejní objednávky nepřipojí k řádkům nákupních objednávek pro externí dodavatele.

Následující tabulka sumarizuje změny, které můžete provést, a očekávané výsledky.

| Operace | Výsledek |
|---|---|
| Vymazání&nbsp;původní&nbsp;prodejní&nbsp;objednávky.&nbsp; | Odstraní se také související mezipodniková nákupní objednávka a mezipodniková prodejní objednávka. Je-li objednávka ve stavu **Výdejka** nebo následujícím stavu během zpracování, prodejní objednávku nelze odstranit. |
| Odstranění řádku v původní prodejní objednávce. | Odstraní se také související řádek v mezipodnikové nákupní objednávce a řádek v mezipodnikové prodejní objednávce. Je-li objednávka ve stavu **Výdejka** nebo následujícím stavu během zpracování, řádek prodejní objednávky nelze odstranit. |
| Přidání nového řádku prodeje do původní prodejní objednávky. | V mezipodnikové nákupní objednávce i v mezipodnikové prodejní objednávce se vytvoří nový řádek prodeje. |
| Změna množství na řádku původní prodejní objednávky. | Množství se synchronizuje s řádkem mezipodnikové nákupní objednávky a s řádkem mezipodnikové prodejní objednávky. Ve všech objednávkách se přepočítá čistá částka. |
| Zákaz přímé dodávky u původní prodejní objednávky. | Pole **Přímá dodávka** nemůžete v původní prodejní objednávce změnit, pokud mezipodniková prodejní objednávka dosáhla minimálního stavu **Výdejka**, **Výstupní objednávka** nebo **Deník výdejek**. Doručovací adresa v mezipodnikové nákupní objednávce se změní na standardní dodací adresu (standardní dodací adresa nákupní objednávky). Řádky mezipodnikové nákupní objednávky se také změní na standardní dodací adresu pro řádky. Oba údaje se synchronizují s mezipodnikovou prodejní objednávkou a s řádky. Typ dodání na všech řádcích v původní prodejní objednávce se změní na **Žádný** a pole se synchronizuje s řádky v mezipodnikové nákupní objednávce. Nákupní objednávky pro externí dodavatele nejsou ovlivněny, stejně jako původní řádky prodeje připojené k řádkům nákupní objednávky pro externí dodavatele. Bude aktualizováno datum dodání na mezipodnikové objednávce a řádcích – a také požadovaná data příjmu nebo expedice na mezipodnikové prodejní objednávce a řádcích. |
| Povolení přímé dodávky u původní prodejní objednávky. | Pokud mezipodniková prodejní objednávka dosáhla minimálního stavu **Výdejka**, **Výstupní objednávka** nebo **Deník výdejek**, nemůžete v původní prodejní objednávce změnit pole **Přímá dodávka**. Dodací adresa v mezipodnikové nákupní objednávce se změní na dodací adresu z původní prodejní objednávky a synchronizuje se s mezipodnikovou prodejní objednávkou. Typ dodání na všech řádcích v původní prodejní objednávce se změní na **Přímá dodávka** a pole se synchronizuje s řádky v mezipodnikové nákupní objednávce. Dodací adresa na jednotlivých řádcích původní prodejní objednávky se synchronizuje s řádky mezipodnikové nákupní objednávky i s řádky mezipodnikové prodejní objednávky. Bude aktualizováno datum dodání na mezipodnikové objednávce a řádcích – a také požadovaná data příjmu nebo expedice na mezipodnikové prodejní objednávce a řádcích. |
| Přidání poznámky do záhlaví původní prodejní objednávky a řádků. | Poznámka se zkopíruje do mezipodnikové nákupní objednávky a do mezipodnikové prodejní objednávky. |
| Změna nebo odstranění poznámky. | Jestliže poznámku změníte nebo odstraníte, změní se nebo odstraní i odpovídající poznámka v mezipodnikové nákupní objednávce a mezipodnikové prodejní objednávce. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

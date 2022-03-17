---
title: Povolení konzistentního zpracování způsobu doručení v kanálech elektronického obchodování
description: Toto téma popisuje, jak povolit konzistentní zpracování způsobu doručení, aby se vyřešily možné problémy související s toky poplatků v kanálech elektronického obchodování Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349941"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Povolení konzistentního zpracování způsobu doručení v kanálech elektronického obchodování 

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak povolit konzistentní zpracování způsobu doručení, aby se vyřešily možné problémy související s toky poplatků v kanálech elektronického obchodování Microsoft Dynamics 365 Commerce.

V Dynamics 365 Commerce se poplatky na úrovni záhlaví bez poměrného rozdělení ve výchozím nastavení v kanálech elektronického obchodu neuplatňují. Toto chování může v kanálech elektronického obchodování způsobit jeden nebo oba následující problémy:

- Poplatky na úrovni záhlaví bez poměrného rozdělení se nezobrazují.
- Poplatky za způsoby doručení nejsou konzistentní mezi výběrem způsobu doručení a souhrnem objednávky v pokladně.

Chcete-li tyto problémy vyřešit, musíte zapnout funkci **Povolit konzistentní zpracování způsobu doručení v kanálu**. Tato funkce zajišťuje, že se v kanálech elektronického obchodu objeví poplatky na úrovni záhlaví bez poměrného rozdělení, a že informace o doručení prodejní objednávky jsou zpracovávány konzistentně stejným pracovním postupem požadavků.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Zapnutí funkce Povolit konzistentní zpracování způsobu doručení v kanálu

Chcete-li zapnout funkci **Povolit konzistentní zpracování způsobu doručení v kanálu** v centrále Commerce, postupujte takto.

1. Otevřete pracovní prostor **Správa funkcí** (**Správa systému \> Pracovní prostory \> Správa funkcí**).
1. V seznamu dostupných funkcí vyhledejte a vyberte **Povolit konzistentní zpracování způsobu doručení v kanálu**.
1. V pravém podokně vyberte **Povolit**.

---
title: Povolení konzistentního zpracování způsobu doručení v kanálech elektronického obchodování
description: Tento článek popisuje, jak povolit konzistentní zpracování způsobu doručení, aby se vyřešily možné problémy související s toky poplatků v kanálech elektronického obchodování Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279643"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Povolení konzistentního zpracování způsobu doručení v kanálech elektronického obchodování 

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit konzistentní zpracování způsobu doručení, aby se vyřešily možné problémy související s toky poplatků v kanálech elektronického obchodování Microsoft Dynamics 365 Commerce.

V Dynamics 365 Commerce se poplatky na úrovni záhlaví bez poměrného rozdělení ve výchozím nastavení v kanálech elektronického obchodu neuplatňují. Toto chování může v kanálech elektronického obchodování způsobit jeden nebo oba následující problémy:

- Poplatky na úrovni záhlaví bez poměrného rozdělení se nezobrazují.
- Poplatky za způsoby doručení nejsou konzistentní mezi výběrem způsobu doručení a souhrnem objednávky v pokladně.

Chcete-li tyto problémy vyřešit, musíte zapnout funkci **Povolit konzistentní zpracování způsobu doručení v kanálu**. Tato funkce zajišťuje, že se v kanálech elektronického obchodu objeví poplatky na úrovni záhlaví bez poměrného rozdělení, a že informace o doručení prodejní objednávky jsou zpracovávány konzistentně stejným pracovním postupem požadavků.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Zapnutí funkce Povolit konzistentní zpracování způsobu doručení v kanálu

Chcete-li zapnout funkci **Povolit konzistentní zpracování způsobu doručení v kanálu** v centrále Commerce, postupujte takto.

1. Otevřete pracovní prostor **Správa funkcí** (**Správa systému \> Pracovní prostory \> Správa funkcí**).
1. V seznamu dostupných funkcí vyhledejte a vyberte **Povolit konzistentní zpracování způsobu doručení v kanálu**.
1. V pravém podokně vyberte **Povolit**.

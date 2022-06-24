---
title: Povolení konzistentního zpracování způsobu doručení v kanálech elektronického obchodování
description: Tento článek popisuje, jak povolit konzistentní zpracování způsobu doručení, aby se vyřešily možné problémy související s toky poplatků v kanálech elektronického obchodování Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885578"
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

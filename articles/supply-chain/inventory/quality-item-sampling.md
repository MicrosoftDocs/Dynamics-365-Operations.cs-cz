---
title: Vzorkování položek řízení kvality
description: Toto téma popisuje, jak nastavit vzorkování položek.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956572"
---
# <a name="quality-management-item-sampling"></a>Vzorkování položek řízení kvality

Vzorkování položek se používá jako součást přidružení kvality. Definuje množství aktuální fyzické zásoby, která musí být zkontrolována. Vzorkování může být založeno na pevném množství, procentuální hodnotě nebo celé licenční značky.

## <a name="set-up-item-sampling"></a>Nastavení vzorkování zboží

Pro nastavení vzorkování položek postupujte následujícím způsobem.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Vzorkování položek**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Vzorkování položky**.
1. V poli **Popis** zadejte hodnotu.
1. Zadejte číslo do pole **Hodnota**. Tato hodnota se vztahuje k určení množství, které je vybráno v přilehlém poli.
1. V oddílu **Zpracování** vyberte zaškrtávací políčko **Úplné blokování**, pokud má být zablokováno celé množství šarže nebo množství objednávky, pokud test selže. Pokud toto políčko není zaškrtnuto, budou v případě neúspěchu testu blokovány pouze položky v objednávce kvality.
1. Zvolte **Uložit**.
1. Zavřete stránku.

> [!NOTE]
> Funkce *Správa kvality pro procesy skladu* poskytuje dodatečné možnosti vzorkování zboží. Přidá koncepci *rozsahu vzorkování položek* a možnost definovat plnou registrační značku jako specifikaci množství. Pokud jste tuto funkci povolili, další informace naleznete v tématu [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Časté otázky k asynchronnímu režim vytváření zákazníka
description: V tomto článku jsou odpovědi na časté otázky týkající se režimu asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690195"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Časté otázky k asynchronnímu režim vytváření zákazníka

[!include [banner](includes/banner.md)]

V tomto článku jsou odpovědi na časté otázky týkající se režimu asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Proč nemohu aktivovat funkci „Povolit úpravy zákazníků v asynchronním režimu“?

Než aktivujete funkci **Povolit úpravy zákazníků v asynchronním režimu**, musíte aktivovat následující funkce:

- Vylepšení výkonu pro objednávky a transakce zákazníků
- Aktivovat vylepšené vytváření asynchronního zákazníka
- Povolit asynchronní vytváření pro adresy zákazníků

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Proč se po aktivaci funkce „Povolit úpravy zákazníků v asynchronním režimu“ stále zobrazují volání služeb v reálném čase do Commerce headquarters?

K tomuto problému dochází, když úlohy Commerce Data Exchange (CDX) nebyly spuštěny, aby bylo zajištěno, že stav funkce a další metadata kanálu jsou synchronizována s kanálem. Než scénář zopakujete, ujistěte se, že jsou v Commerce headquarters spuštěny následující úlohy CDX:

- 1110 (Globální konfigurace)
- 1010 (Zákazníci)
- 1070 (Konfigurace kanálu)

Data uložená v mezipaměti v Commerce Scale Unit (CSU) se nemusí po spuštění úloh CDX okamžitě projevit v Commerce headquarters.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Proč Commerce headquarters neukazuje vytvoření nebo aktualizace zákazníků z pokladního místa (POS) nebo kanálu elektronického obchodu?

Ujistěte se, že následující akce byly provedeny v pořadí, ve kterém jsou zde uvedeny.

1. Spusťte P-úlohu CDX v Commerce headquarters, abyste zajistili, že asynchronní zákaznická data jsou uložena v tabulkách **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** a **RETAILASYNCCUSTOMERATTRIBUTEV2**.
1. Spusťte dávkovou úlohu **Synchronizovat požadavky zákazníků a kanálů** v Commerce headquarters. Po úspěšném provedení dávkové úlohy budou mít všechny záznamy, které byly úspěšně zpracovány z výše uvedených tabulek, pole **OnlineOperationCompleted** nastaveno na **1**.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>Jak poznám, která správa zákazníků v asynchronním režimu selhala a jak mohu provést změny, pokud jsou vyžadovány?

Chcete-li zobrazit všechny operace v asynchronním režimu a stav jejich synchronizace, přejděte v Commerce headquarters na **Commerce a Retail \> Zákazníci \> Stav synchronizace zákazníka**. Chcete-li provést změny, upravit konkrétní operaci, aktualizovat pole, vyberte **Uložit** a poté vyberte **Synchronizovat** pro synchronizaci změn.


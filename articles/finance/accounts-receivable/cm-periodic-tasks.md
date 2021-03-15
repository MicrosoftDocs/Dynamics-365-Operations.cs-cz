---
title: Pravidelné úlohy správy úvěrů
description: V tomto tématu jsou popsány pravidelné úlohy, které jsou nezbytnou součástí procesu správy limitů úvěru u odběratelů.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b41b87cd3e2e80b87318c5c771d45a4d0e5d4b85
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971696"
---
# <a name="periodic-credit-management-tasks"></a>Periodické úkoly správy kreditu

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány pravidelné úlohy, které jsou nezbytnou součástí procesu správy limitů úvěru u odběratelů.

## <a name="update-risk-scores"></a>Aktualizovat skóre rizika

Během vývoje podniku a při změnách okolností se mohou měnit také úvěrová rizika u daného odběratele. Chcete-li pro odběratele zachovat odpovídající limity úvěru, je nutné pravidelně kontrolovat kritéria pro jednotlivá hodnocení rizik a aktualizovat hodnocení jednotlivých odběratelů. Následující hodnocení lze aktualizovat pomocí stránky **Aktualizace hodnocení rizik** (**Úvěr a inkasa \> Pravidelné úlohy \> Správa úvěru \> Aktualizace hodnocení rizik**). Jsou také zpracovány všechny výpočty definované uživatelem.

- **Průměrný počet dnů do zaplacení** – Toto hodnocení je průměrný počet dnů do zaplacení faktur odběratelem.
- **Odběratelem od** – Toto hodnocení představuje počet let, po který byl odběratel odběratelem vaší organizace.
- **Aktivní od** – Toto hodnocení představuje počet let, po které odběratel podniká. Používá hodnotu pole **Začátek podnikání** na stránce **Odběratelé**.
- **Počet dnů neuhrazeného prodeje** – Toto hodnocení je založeno na zůstatku pohledávek, prodejích, výnosech a počtu dnů za předchozí dvanáctiměsíční období.
- **Průměrný zůstatek** – Toto hodnocení je založeno na zůstatku pohledávek za předchozí dvanáctiměsíční období.
- **Skupina správy úvěru**, **Stav účtu** a **Země** – Tato hodnocení používají informace od odběratele.

## <a name="update-customer-balance-statistics"></a>Aktualizace statistiky zůstatku odběratele

Chcete-li aktualizovat výpočet statistiky zůstatku, která se zobrazuje na stránce **Dotaz statistiky zůstatku**, můžete spustit proces **Aktualizace statistiky zůstatku odběratele**, který aktualizuje výpočet statistiky zůstatku, jež se zobrazuje na stránce. Tyto informace se používají k výpočtu hodnocení rizik a hodnot, které se zobrazují v okně s fakty statistiky úvěru na stránce **Odběratel**.

Při spuštění tohoto procesu se aktualizují statistiky zůstatku odběratele u jednoho odběratele. Chcete-li nastavit dávkovou úlohu pro spuštění procesu u více odběratelů, můžete použít stránku **Výpočet statistiky zůstatku** (**Správa úvěru \> Pravidelné úlohy \> Výpočet statistiky zůstatku**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
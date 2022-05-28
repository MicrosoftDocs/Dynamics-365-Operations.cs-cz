---
title: Periodické úkoly správy kreditu
description: V tomto tématu jsou popsány pravidelné úlohy, které jsou součástí procesu správy limitů úvěru u odběratelů.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 53b7cd00b3287f18ba65391842ac259ab2434b86
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735429"
---
# <a name="periodic-credit-management-tasks"></a>Periodické úkoly správy kreditu

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány pravidelné úlohy, které jsou součástí procesu správy limitů úvěru u odběratelů.

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

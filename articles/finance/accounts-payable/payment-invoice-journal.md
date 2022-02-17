---
title: Použití plánu plateb na deník faktur
description: Toto téma popisuje, jak přidat platbu do deníku faktur dodavatele.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075570"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Použití plánu plateb na deník faktur

[!include [banner](../includes/preview-banner.md)]

V Microsoft Dynamics 365 Finance vydání 10.0.25 je nyní v deníku faktur dodavatele podporován plán plateb.

Chcete-li používat tuto funkci, musíte povolit funkci **Použít plán plateb na deník faktur** ve Správě funkcí.

Po aktivaci funkce je přidáno nové pole **Platební kalendář** na stránku **Deník faktur**. Když vytvoříte řádek deníku faktur, pokud jsou platební podmínky uchovávány u dodavatele a jsou vybrány v plánu plateb, pole **Platební kalendář** je na stránce **Deník faktur** aktualizováno.

Použitý rozvrh plateb můžete změnit podle vašich obchodních požadavků. Během účtování deníku faktur dodavatele budou vytvořeny otevřené transakce dodavatele podle plánu plateb.

Chcete-li zkontrolovat několik otevřených transakcí dodavatele, které byly vygenerovány z plánu plateb, přejděte na **Závazky \> Faktury \> Otevřené faktury dodavatele** a zadejte číslo faktury nebo účet dodavatele.

Chcete-li zkontrolovat nebo konfigurovat plán plateb, přejděte na **Závazky \> Nastavení platby \> Platební kalendář**.

Chcete-li konfigurovat platební podmínky a přiřadit plán plateb, přejděte na **Závazky \> Nastavení plateb \> Platební podmínky**.

Chcete-li zachovat platební podmínky u dodavatele, přejděte na **Závazky \> Všichni prodejci**, vyberte účet dodavatele a poté na kartě **Platba** nastavte pole **Platební podmínky**.

Funkce plánu plateb je také k dispozici v procesu **Registr faktur dodavatelů**. Pokud je v deníku registru faktur vybrán plán plateb, při zaúčtování registru faktur **ne** bude generováno více řádků plateb dodavatele. Řádky plateb dodavatele se vygenerují po schválení faktury.

## <a name="limitation"></a>Omezení

U nevyřízené faktury dodavatele – pokud je plán plateb v záhlaví faktury – existuje rozšířená stránka, která uživatelům umožňuje upravovat řádky plateb. (Uživatelé mohou například upravit datum splatnosti a hodnotu každého řádku plateb.) Řádky plateb, které jsou generovány z deníku faktur, budou mít hodnotu z plánu plateb.

Tato funkce bude v budoucí verzi k dispozici v deníku faktur dodavatele a u nevyřízených faktur.

---
title: Aplikace Viditelnost zásob
description: Toto téma popisuje, jak používat aplikaci Viditelnost zásob.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a60fc00642a77d3dc595a6222727637f0d7cd588
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475053"
---
# <a name="use-the-inventory-visibility-app"></a>Použití aplikace viditelnosti zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Toto téma popisuje, jak používat aplikaci Viditelnost zásob.

Viditelnost zásob poskytuje modelem řízenou aplikaci pro vizualizaci. Aplikace obsahuje tři stránky: **Konfigurace**, **Provozní viditelnost** a **Souhrn zásob**. Má následující funkce:

- Poskytuje uživatelské rozhraní (UI) pro konfiguraci množství na skladě a konfiguraci předběžných rezervací.
- Podporuje dotazy na zásoby v reálném čase,. zahrnující různé kombinace dimenzí.
- Poskytuje uživatelské rozhraní pro odesílání požadavků na rezervaci.
- Poskytuje přizpůsobený pohled na skladové zásoby produktů společně se všemi dimenzemi.

## <a name="prerequisites"></a>Předpoklady

Než začnete, nainstalujte a nastavte doplněk Viditelnost inventáře podle popisu v tématu [Instalace a nastavení doplňku Viditelnost zásob](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Otevření aplikace viditelnosti zásob

Chcete -li otevřít aplikaci Viditelnost zásob, přihlaste se k prostředí Power Apps a otevřete **Viditelnost zásob**.

## <a name="configuration"></a><a name="configuration"></a>Konfigurace

Stránka **Konfigurace** aplikace Viditelnost zásob vám pomůže nastavit konfiguraci množství na skladě a konfiguraci předběžných rezervací. Po instalaci doplňku obsahuje výchozí konfigurace výchozí nastavení pro Microsoft Dynamics 365 Supply Chain Management (zdroj dat `fno`). Výchozí nastavení můžete zkontrolovat. Odteď zde na základě vašich obchodních požadavků a požadavků na účtování zásob vašeho externího systému můžete upravit konfiguraci a standardizovat tak způsob, jakým mohou být změny v inventáři zaúčtovány, organizovány a dotazovány z různých systémů.

Úplné podrobnosti o konfiguraci řešení najdete v části [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Provozní viditelnost

Stránka **Provozní viditelnost** obsahuje výsledky dotazu na zásoby v reálném čase sestaveného na základě různých kombinací dimenzí. Když je zapnutá funkce *OnHandReservation*, můžete také odesílat požadavky na rezervaci ze stránky **Provozní viditelnost**.

### <a name="on-hand-query"></a>Dotaz na zásoby na skladě

Karta **Dotaz na zásoby na skladě** zobrazuje výsledky dotazu na zásoby v reálném čase.

Když vyberete kartu **Dotaz na zásoby na skladě**, systém požádá o vaše přihlašovací údaje, aby mohl získat nosný token, který je vyžadován pro dotaz do služby Viditelnost zásob. Nosný token můžete jednoduše vložit do pole **Nosný token** a pak zavřít dialogové okno. Poté můžete odeslat požadavek na zpracování dotazu.

Pokud nosný token není platný nebo pokud jeho platnost vypršela, musíte do pole **Nosný token** vložit nový token. Zadejte správné hodnoty v polích **ID klienta**, **ID tenanta**, **Tajný klíč klienta** a poté vyberte **Obnovit**. Systém automaticky získá nový, platný nosný token.

Chcete-li odeslat dotaz na skladové množství, zadejte dotaz do těla požadavku. Použijte vzor, který je popsán v části [Dotaz pomocí metody POST](inventory-visibility-api.md#query-with-post-method).

![Nastavení dotazu na zásoby na skladě](media/inventory-visibility-query-settings.png "Nastavení dotazu na zásoby na skladě")

### <a name="reservation-posting"></a>Odeslání rezervace

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

K odeslání požadavku na rezervaci použijte kartu **Odeslání rezervace**. Než budete moci odeslat požadavek na rezervaci, musíte zapnout funkci *OnHandReservation*. Další informace o této funkci naleznete v části [Rezervace Viditelnosti zásob](inventory-visibility-reservations.md).

Chcete-li odeslat požadavek na rezervaci, musíte do těla požadavku zadat hodnotu. Použijte vzor, který je popsán v části [Vytvoření jedné rezervační události](inventory-visibility-api.md#create-one-reservation-event). Pak vyberte **Odeslat**. Chcete-li zobrazit podrobnosti odpovědi na požadavek, vyberte **Zobrazit detaily**. Z podrobností odpovědi můžete také získat hodnotu `reservationId`.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Souhrn zásob

**Souhrn zásob** je přizpůsobené zobrazení pro entitu *součtu zásob na skladě*. Poskytuje souhrn zásob produktů společně se všemi dimenzemi. Souhrnná data zásob budou pravidelně synchronizována z aplikace Viditelnost zásob. Než uvidíte data na kartě **Souhrn zásob**, musíte zapnout funkci *OnHandMostSpecificBackgroundService* na kartě **Správa funkcí**.

Pomocí **rozšířeného filtru**, který Dataverse nabízí, můžete vytvořit osobní zobrazení ukazující řádky, které jsou pro vás důležité. Možnosti rozšířeného filtru vám umožní vytvořit širokou škálu zobrazení, od jednoduchých po složité. Také vám umožňují přidat do filtrů seskupené a vnořené podmínky. Chcete-li se dozvědět více o tom, jak používat **rozšířený filtr**, přečtěte si téma [´´Uprava nebo vytvoření osobních zobrazení pomocí rozšířených filtrů mřížky](/powerapps/user/grid-filters-advanced).

V horní části přizpůsobeného zobrazení jsou tři pole: **Výchozí dimenze**, **Vlastní dimenze** a **Míra**. Pomocí těchto polí můžete řídit, které sloupce jsou viditelné.

Můžete vybrat záhlaví sloupce a filtrovat nebo seřadit aktuální výsledek.

Ve spodní části přizpůsobeného zobrazení se zobrazují informace typu „50 záznamů (29 vybraných)“ nebo „50 záznamů“. Tyto informace se týkají aktuálně načtených záznamů z výsledku **Rozšířeného filtru**. Text „29 vybraných“ odkazuje na počet záznamů, které byly vybrány pomocí filtru záhlaví sloupců z načtených záznamů.

V dolní části pohledu je tlačítko **Načíst další**, kterým načtete další záznamy z Dataverse. Výchozí počet načtených záznamů je 50. Když použijete tlačítko **Načíst další**, do zobrazení se načte dalších 1 000 dostupných záznamů. Číslo na tlačítku **Načíst další** vyjadřuje aktuálně načtené záznamy a celkový počet záznamů ve výsledku **Rozšířeného filtru**.

![Souhrn zásob](media/inventory-visibility-onhand-list.png "Souhrn zásob")

---
title: Aplikace Viditelnost zásob
description: Tento článek popisuje, jak používat aplikaci Viditelnost zásob.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306166"
---
# <a name="use-the-inventory-visibility-app"></a>Použití aplikace Inventory Visibility

[!include [banner](../includes/banner.md)]


Tento článek popisuje, jak používat aplikaci Viditelnost zásob.

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

K odeslání požadavku na rezervaci použijte kartu **Odeslání rezervace**. Než budete moci odeslat požadavek na rezervaci, musíte zapnout funkci *OnHandReservation*. Další informace o této funkci naleznete v části [Rezervace Viditelnosti zásob](inventory-visibility-reservations.md).

Chcete-li odeslat požadavek na rezervaci, musíte do těla požadavku zadat hodnotu. Použijte vzor, který je popsán v části [Vytvoření jedné rezervační události](inventory-visibility-api.md#create-one-reservation-event). Pak vyberte **Odeslat**. Chcete-li zobrazit podrobnosti odpovědi na požadavek, vyberte **Zobrazit detaily**. Z podrobností odpovědi můžete také získat hodnotu `reservationId`.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Souhrn zásob

Stránka **Souhrn zásob** poskytuje souhrn zásob produktů společně se všemi dimenzemi. Jedná se o přizpůsobené zobrazení pro entitu *Součet zásob na skladě*. Data souhrnu zásob jsou pravidelně synchronizována z aplikace Viditelnost zásob.

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>Povolte souhrn zásob a nastavte frekvenci synchronizace

Chcete-li povolit stránku **Souhrn zásob** a nastavite frekvenci synchronizace, postupujte takto:

1. Otevřete stránku **Konfigurace**.
1. Otevřete kartu **Správa a nastavení funkcí**.
1. Nastavte přepínač pro funkci **OnHandMostSpecificBackgroundService** na *Ano*.
1. Když je funkce povolena, sekce **Konfigurace služby** se zpřístupní a obsahuje řádek pro konfiguraci funkce **OnHandMostSpecificBackgroundService**. Toto nastavení vám umožňuje zvolit frekvenci, s jakou se budou synchronizovat souhrnná data zásob. Použijte tlačítka **Nahoru** a **Dolů** ve sloupci **Hodnota** pro změnu doby mezi synchronizacemi (která může být až 5 minut). Pak vyberte **Uložit**.
1. Vyberte **Aktualizujte konfiguraci** pro uložení všech změn.

![Nastavení OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.PNG "Nastavení OnHandMostSpecificBackgroundService")

> [!NOTE]
> Funkce *OnHandMostSpecificBackgroundService* sleduje pouze změny produktu na skladě, ke kterým došlo po zapnutí funkce. Data pro produkty, které se od zapnutí této funkce nezměnily, nebudou synchronizovány z mezipaměti služby inventáře do prostředí Dataverse. Pokud stránka **Souhrn inventáře** nezobrazuje všechny dostupné informace, které očekáváte, přejděte na **Správa zásob > Pravidelné úkoly > Integrace doplňku Viditelnost zásob**, deaktivuje dávkovou úlohu a znovu ji aktivujte. Tím se provede počáteční odeslání a všechna data se synchronizují do entity *Součet zásob na skladě* během následujících 15 minut. Chcete-li tuto funkci používat, doporučujeme vám ji zapnout před vytvořením jakýchkoli změn zásob na skladě a aktivovat dávkovou úlohu **Integrace doplňku Viditelnost zásob**.

### <a name="work-with-the-inventory-summary"></a>Práce se souhrnem zásob

Pomocí **rozšířeného filtru**, který Dataverse nabízí, můžete vytvořit osobní zobrazení ukazující řádky, které jsou pro vás důležité. Možnosti rozšířeného filtru vám umožní vytvořit širokou škálu zobrazení, od jednoduchých po složité. Také vám umožňují přidat do filtrů seskupené a vnořené podmínky. Chcete-li se dozvědět více o tom, jak používat **rozšířený filtr**, přečtěte si téma [´´Uprava nebo vytvoření osobních zobrazení pomocí rozšířených filtrů mřížky](/powerapps/user/grid-filters-advanced).

V horní části přizpůsobeného zobrazení jsou tři pole: **Výchozí dimenze**, **Vlastní dimenze** a **Míra**. Pomocí těchto polí můžete řídit, které sloupce jsou viditelné.

Můžete vybrat záhlaví sloupce a filtrovat nebo seřadit aktuální výsledek.

Ve spodní části přizpůsobeného zobrazení se zobrazují informace typu „50 záznamů (29 vybraných)“ nebo „50 záznamů“. Tyto informace se týkají aktuálně načtených záznamů z výsledku **Rozšířeného filtru**. Text „29 vybraných“ odkazuje na počet záznamů, které byly vybrány pomocí filtru záhlaví sloupců z načtených záznamů.

V dolní části pohledu je tlačítko **Načíst další**, kterým načtete další záznamy z Dataverse. Výchozí počet načtených záznamů je 50. Když použijete tlačítko **Načíst další**, do zobrazení se načte dalších 1 000 dostupných záznamů. Číslo na tlačítku **Načíst další** vyjadřuje aktuálně načtené záznamy a celkový počet záznamů ve výsledku **Rozšířeného filtru**.

![Souhrn zásob](media/inventory-visibility-onhand-list.png "Souhrn zásob")

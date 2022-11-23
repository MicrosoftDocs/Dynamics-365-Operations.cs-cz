---
title: Aplikace Viditelnost zásob
description: Tento článek popisuje, jak používat aplikaci Viditelnost zásob.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762693"
---
# <a name="use-the-inventory-visibility-app"></a>Použití aplikace Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak používat aplikaci Viditelnost zásob.

Viditelnost zásob poskytuje modelem řízenou aplikaci pro vizualizaci. Aplikace obsahuje tři stránky: **Konfigurace**, **Provozní viditelnost** a **Souhrn zásob**. Má následující funkce:

- Poskytuje uživatelské rozhraní (UI) pro konfiguraci množství na skladě a konfiguraci předběžných rezervací.
- Podporuje dotazy na zásoby v reálném čase,. zahrnující různé kombinace dimenzí.
- Poskytuje uživatelské rozhraní pro odesílání požadavků na rezervaci.
- Poskytuje zobrazení zásob produktů na skladě společně se všemi dimenzemi.
- Poskytuje zobrazení seznamu zásob produktů na skladě společně s předdefinovanými dimenzemi. Zobrazení seznamu na skladě může být buď úplným souhrnem, nebo předem načteným výsledkem z dotazu na skladě.

## <a name="prerequisites"></a>Předpoklady

Než začnete, nainstalujte a nastavte doplněk Viditelnost inventáře podle popisu v tématu [Instalace a nastavení doplňku Viditelnost zásob](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>Otevřete a ověřte aplikaci Viditelnost zásob

Pro otevření a ověření aplikace Viditelnost zásob proveďte následující postup.

1. Přihlaste se k prostředí Power Apps.
1. Otevřete aplikaci **Viditelnosti zásob**.
1. Otevřete stránku **Provozní viditelnost** z levého panelu.
1. Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v horní části stránky.
1. V dialogovém okně **Nastavení** zadejte hodnoty **ID klienta**, **Id tenanta** a **Tajný klíč klienta**, které jste si poznamenali, když jste [instalovali a nastavovali Viditelnost zásob](inventory-visibility-setup.md).
1. Vyberte tlačítko **Obnovit** vedle pole **Nosný token**. Systém vygeneruje nový nosný token na základě informací, které jste zadali.

    ![Nastavení dotazu na zásoby na skladě.](media/inventory-visibility-query-settings.png "Nastavení dotazu na zásoby na skladě")

1. Když obdržíte platný nosný token, zavřete dialogové okno. Platnost nosného tokenu po nějaké době vyprší. Proto ho musíte občas aktualizovat, když potřebujete aktualizovat konfiguraci, zveřejňovat data nebo data dotazu.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurace aplikace Viditelnost zásob

Stránka **Konfigurace** aplikace Viditelnost zásob vám pomůže nastavit obecnou konfiguraci správy dat a konfiguraci funkce. Po instalaci doplňku obsahuje výchozí konfigurace výchozí nastavení pro Microsoft Dynamics 365 Supply Chain Management (zdroj dat `fno`). Výchozí nastavení můžete zkontrolovat. Poté zde na základě vašich obchodních požadavků a požadavků na účtování zásob vašeho externího systému můžete upravit konfiguraci a standardizovat tak způsob, jakým mohou být změny v inventáři zaúčtovány, organizovány a dotazovány z různých systémů.

Úplné podrobnosti o konfiguraci řešení najdete v části [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Provozní viditelnost

Stránka **Provozní viditelnost** obsahuje výsledky dotazu na zásoby, zaúčtování rezervace a přidělení v reálném čase sestaveného na základě různých kombinací dimenzí. Když je [zapnutá](inventory-visibility-configuration.md) funkce *OnHandReservation*, můžete také odesílat požadavky na rezervaci ze stránky **Provozní viditelnost**.

### <a name="on-hand-query"></a>Dotaz na zásoby na skladě

Karta **Dotaz na zásoby na skladě** na stránce **Provozní viditelnost** umožňuje dotazování na zásoby na skladě v reálném čase. Chcete-li nastavit a spustit dotaz, postupujte následujícím způsobem.

1. Otevřete aplikaci **Viditelnosti zásob**.
1. Otevřete stránku **Provozní viditelnost** z levého panelu.
1. Na kartě **Dotaz na zásoby na skladě** zadejte hodnoty **ID organizace**, **ID lokality** a **ID umístění**, na které se chcete dotazovat.
1. Do pole **ID produktu** zadejte jedno nebo více ID produktů, abyste získali přesnou shodu pro váš dotaz. Pokud necháte pole **ID produktu** prázdné, budou výsledky zahrnovat všechny produkty na zadaném místě a umístění.
1. Chcete-li získat podrobnější výsledek (například zobrazení podle hodnot dimenzí, jako je barva a velikost), vyberte dimenze seskupení podle pole **Seskupit výsledky podle**.
1. Chcete-li najít položky, které mají konkrétní hodnotu rozměru (například barva = červená), vyberte rozměr v poli **Filtrovat dimenze** pole a poté zadejte hodnotu dimenze.
1. Vyberte **Dotaz**. Obdržíte zprávu o úspěchu (zelená) nebo neúspěšnou (červená). Pokud dotaz selže, zkontrolujte kritéria dotazu a ujistěte se, že [nosný token](#open-authenticate) nevypršel.

Dalším způsobem, jak vytvořit dotaz na zásoby na skladě, jsou přímé požadavky na rozhraní API. Můžete použít `/api/environment/{environmentId}/onhand/indexquery` nebo `/api/environment/{environmentId}/onhand`. Další informace viz [Veřejná rozhraní API Viditelnosti zásob](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Odeslání rezervace

K odeslání požadavku na rezervaci použijte kartu **Odeslání rezervace** na stránce **Provozní viditelnost**. Než budete moci odeslat požadavek na rezervaci, musíte zapnout funkci *OnHandReservation*. Další informace o této funkci a jak ji zapnout naleznete v části [Rezervace viditelnosti zásob](inventory-visibility-reservations.md).

> [!NOTE]
> Schopnost provést předběžnou rezervaci prostřednictvím uživatelského rozhraní je určena k otestování funkce. Každý požadavek předběžné rezervace by měl být spojen se změnou řádku transakčního příkazu (vytvoření, úprava, odstranění atd.). Proto doporučujeme provádět pouze předběžné rezervace, které jsou propojeny s backendovou objednávkou. Další informace viz [Rezervace ve Viditelnosti zásob](inventory-visibility-reservations.md).

Chcete-li odeslat žádost o předběžnou rezervaci pomocí uživatelského rozhraní, postupujte podle těchto kroků.

1. Otevřete aplikaci **Viditelnosti zásob**.
1. Otevřete stránku **Provozní viditelnost** z levého panelu.
1. Na kartě **Zaúčtování rezervace** v poli **Množství** zadejte množství, které chcete zarezervovat.
1. Zrušte zaškrtnutí políčka **Povolit záporné zásoby pro podporu nadměrného prodeje**, abyste zabránili nadměrnému prodeji nebo nadměrným rezervacím.
1. V poli **Operátor** vyberte zdroj dat a fyzickou míru, které se vztahují na předběžně rezervované množství.
1. Zadejte hodnoty **ID organizace**, **ID lokality**, **ID umístění** a **ID produktu**, na které se chcete dotazovat.
1. Chcete-li získat podrobnější výsledek, vyberte zdroj dat, dimenze a hodnoty dimenzí.

Dalším způsobem, jak zaúčtovat předběžnou rezervaci, je zadávat přímé požadavky API. Použijte vzor, který je popsán v části [Vytvoření jedné rezervační události](inventory-visibility-api.md#create-one-reservation-event). Pak vyberte **Odeslat**. Chcete-li zobrazit podrobnosti odpovědi na požadavek, vyberte **Zobrazit detaily**. Z podrobností odpovědi můžete také získat hodnotu `reservationId`.

### <a name="allocation"></a>Přidělení

Informace o tom, jak spravovat přidělení z uživatelského rozhraní a rozhraní API, viz [Přidělení zásob Viditelnosti zásob](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Souhrn zásob

Stránka **Souhrn zásob** poskytuje souhrn zásob produktů společně se všemi dimenzemi. Jedná se o přizpůsobené zobrazení pro entitu *Součet zásob na skladě*. Data souhrnu zásob jsou pravidelně synchronizována z aplikace Viditelnost zásob.

Chcete-li povolit stránku **Souhrn zásob** a nastavite frekvenci synchronizace, postupujte takto:

1. Otevřete stránku **Konfigurace**.
1. Otevřete kartu **Správa a nastavení funkcí**.
1. Nastavte přepínač pro funkci **OnHandMostSpecificBackgroundService** na *Ano*.
1. Když je funkce povolena, sekce **Konfigurace služby** se zpřístupní a obsahuje řádek pro konfiguraci funkce **OnHandMostSpecificBackgroundService**. Toto nastavení vám umožňuje zvolit frekvenci, s jakou se budou synchronizovat souhrnná data zásob. Použijte tlačítka **Nahoru** a **Dolů** ve sloupci **Hodnota** pro změnu doby mezi synchronizacemi (která může být až 5 minut). Pak vyberte **Uložit**.

    ![Nastavení OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "Nastavení OnHandMostSpecificBackgroundService")

1. Vyberte **Aktualizujte konfiguraci** pro uložení všech změn.

> [!NOTE]
> Funkce *OnHandMostSpecificBackgroundService* sleduje pouze změny zásob na skladě, ke kterým došlo po zapnutí funkce. Data pro produkty, které se od zapnutí této funkce nezměnily, nebudou synchronizovány z mezipaměti služby inventáře do prostředí Dataverse. Pokud stránka **Souhrn inventáře** nezobrazuje všechny dostupné informace, které očekáváte, otevřete Supply Chain Management, přejděte na **Správa zásob > Pravidelné úkoly > Integrace doplňku Viditelnost zásob**, deaktivuje dávkovou úlohu a znovu ji aktivujte. Tím se provede počáteční odeslání a všechna data se synchronizují do entity *Součet zásob na skladě* během následujících 15 minut. Chcete-li používat funkci *OnHandMostSpecificBackgroundService*, doporučujeme vám ji zapnout před vytvořením jakýchkoli změn zásob na skladě a aktivovat dávkovou úlohu **Integrace doplňku Viditelnost zásob**.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Přednačtení přehlednějšího dotazu na zásoby na skladě

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management uchovává velké množství informací o vašich aktuálních zásobách na skladě a zpřístupňuje je pro širokou škálu účelů. Mnoho každodenních operací a integrací třetích stran však vyžaduje jen malou podmnožinu těchto podrobností a dotazování systému na všechny z nich může vést k velkým datovým sadám, jejichž sestavení a přenos zabírá čas. Služba viditelnosti zásob proto může periodicky načítat a ukládat zjednodušenou sadu dat aktuálních zásob na skladu, aby byly tyto optimalizované informace neustále dostupné. Uložené podrobnosti o zásobách na skladě jsou filtrovány na základě konfigurovatelných obchodních kritérií, aby bylo zajištěno, že budou zahrnuty pouze ty nejrelevantnější informace. Vzhledem k tomu, že filtrované seznamy zásob na skladě jsou uloženy místně ve službě viditelnosti zásob a jsou pravidelně aktualizovány, umožňují rychlý přístup, export dat na vyžádání a efektivní integraci s externími systémy.

Stránka **Předběžné načtení souhrnu viditelnosti zásob** obsahuje zobrazení entity *Výsledky předběžného načtení indexového dotazu na zásoby na skladě*. Na rozdíl od entity *Souhrn zásob* poskytuje entita *Výsledky předběžného načtení indexového dotazu na zásoby na skladě* seznam zásob produktů na skladě spolu s vybranými dimenzemi. Viditelnost zásob synchronizuje předem načtená souhrnná data každých 15 minut.

Chcete-li zobrazit data na kartě **Předběžné načtení souhrnu viditelnosti zásob**, musíte zapnout funkci *OnHandIndexQueryPreloadBackgroundService* na kartě **Správa funkcí** na stránce **Konfigurace** a poté vyberte **Aktualizovat konfiguraci** (viz také [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md)).

> [!NOTE]
> Stejně jako u funkce *OnhandMostSpecificBackgroudService* sleduje funkce *OnHandIndexQueryPreloadBackgroundService* pouze změny zásob na skladě, ke kterým došlo po jejím zapnutí. Data pro produkty, které se od zapnutí této funkce nezměnily, nebudou synchronizovány z mezipaměti služby inventáře do prostředí Dataverse. Pokud stránka **Souhrn inventáře** nezobrazuje všechny dostupné informace, které očekáváte, přejděte na **Správa zásob > Pravidelné úkoly > Integrace doplňku Viditelnost zásob**, deaktivuje dávkovou úlohu a znovu ji aktivujte. Tím se provede počáteční odeslání a všechna data se synchronizují do entity *Výsledky předběžného načtení indexového dotazu na zásoby na skladě* během následujících 15 minut. Chcete-li tuto funkci používat, doporučujeme vám ji zapnout před vytvořením jakýchkoli změn zásob na skladě a aktivovat dávkovou úlohu **Integrace doplňku Viditelnost zásob**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtrujte a procházejte souhrny zásob

Pomocí **rozšířeného filtru**, který Dataverse nabízí, můžete vytvořit osobní zobrazení ukazující řádky, které jsou pro vás důležité. Možnosti rozšířeného filtru vám umožní vytvořit širokou škálu zobrazení, od jednoduchých po složité. Také vám umožňují přidat do filtrů seskupené a vnořené podmínky. Chcete-li se dozvědět více o tom, jak používat rozšířený filtr, přečtěte si téma [Úprava nebo vytvoření osobních zobrazení pomocí rozšířených filtrů mřížky](/powerapps/user/grid-filters-advanced).

Stránka **Souhrn zásob** nabízí tři pole nad mřížkou (**Výchozí dimenze**, **Vlastní dimenze** a **Míra**), která můžete použít k určení, které sloupce jsou viditelné. Můžete také vybrat libovolné záhlaví sloupce a filtrovat nebo seřadit aktuální výsledek podle tohoto sloupce. Následující screenshot zvýrazňuje pole dimenze, filtrování, počtu výsledků a „načíst další“, která jsou k dispozici na stránce **Souhrn zásob**.

![Stránka Souhrn zásob.](media/inventory-visibility-onhand-list.png "Stránka Souhrn zásob")

Protože pro načítání souhrnných dat budete mít použity předem definované dimenze, na stránce **Předběžné načtení souhrnu viditelnosti zásob** jsou zobrazeny sloupce související s dimenzemi. *Dimenze nelze přizpůsobit – systém podporuje pouze dimenze pracoviště a místa pro předem načtené seznamy zásob na skladě.* Stránka **Předběžné načtení souhrnu viditelnosti zásob** obsahuje filtry, které jsou podobné těm na stránce **Souhrn zásob**, kromě již vybraných dimenzí. Následující screenshot zvýrazňuje pole filtrování, která jsou k dispozici na stránce **Předběžné načtení souhrnu viditelnosti zásob**.

![Stránka Předběžné načtení souhrnu viditelnosti zásob.](media/inventory-visibility-preload-onhand-list.png "Stránka Předběžné načtení souhrnu viditelnosti zásob")

Ve spodní části stránek **Předběžné načtení souhrnu viditelnosti zásob** a **Souhrn zásob**, najdete informace jako „50 záznamů (29 vybraných)“ nebo „50 záznamů“. Tyto informace se týkají aktuálně načtených záznamů z výsledku **Rozšířeného filtru**. Text „29 vybraných“ odkazuje na počet záznamů, které byly vybrány pomocí filtru záhlaví sloupců z načtených záznamů. Je zde také tlačítko **Načíst další**, kterým načtete další záznamy z Dataverse. Výchozí počet načtených záznamů je 50. Když použijete tlačítko **Načíst další**, do zobrazení se načte dalších 1 000 dostupných záznamů. Číslo na tlačítku **Načíst další** vyjadřuje aktuálně načtené záznamy a celkový počet záznamů ve výsledku **Rozšířeného filtru**.

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
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520845"
---
# <a name="use-the-inventory-visibility-app"></a>Použití aplikace Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak používat aplikaci Viditelnost zásob.

Viditelnost zásob poskytuje modelem řízenou aplikaci pro vizualizaci. Aplikace obsahuje tři stránky: **Konfigurace**, **Provozní viditelnost** a **Souhrn zásob**. Má následující funkce:

- Poskytuje uživatelské rozhraní (UI) pro konfiguraci množství na skladě a konfiguraci předběžných rezervací.
- Podporuje dotazy na zásoby v reálném čase,. zahrnující různé kombinace dimenzí.
- Poskytuje uživatelské rozhraní pro odesílání požadavků na rezervaci.
- Poskytuje zobrazení zásob produktů na skladě společně se všemi dimenzemi.
- Poskytuje zobrazení seznamu zásob produktů na skladě společně s předdefinovanými dimenzemi.


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

Když otevřete kartu **Dotaz na zásoby na skladě** na stránce **Provozní viditelnost**, systém požádá o vaše přihlašovací údaje, aby mohl získat nosný token, který je vyžadován pro dotaz na službu viditelnosti zásob. Nosný token můžete jednoduše vložit do pole **Nosný token** a pak zavřít dialogové okno. Poté můžete odeslat požadavek na zpracování dotazu.

Pokud nosný token není platný nebo pokud jeho platnost vypršela, musíte do pole **Nosný token** vložit nový token. Zadejte správné hodnoty v polích **ID klienta**, **ID tenanta**, **Tajný klíč klienta** a poté vyberte **Obnovit**. Systém automaticky získá nový, platný nosný token.

Chcete-li odeslat dotaz na skladové množství, zadejte dotaz do těla požadavku. Použijte vzor, který je popsán v části [Dotaz pomocí metody POST](inventory-visibility-api.md#query-with-post-method).

![Nastavení dotazu na zásoby na skladě](media/inventory-visibility-query-settings.png "Nastavení dotazu na zásoby na skladě")

### <a name="reservation-posting"></a>Odeslání rezervace

K odeslání požadavku na rezervaci použijte kartu **Odeslání rezervace** na stránce **Provozní viditelnost**. Než budete moci odeslat požadavek na rezervaci, musíte zapnout funkci *OnHandReservation*. Další informace o této funkci a jak ji zapnout naleznete v části [Rezervace viditelnosti zásob](inventory-visibility-reservations.md).

Chcete-li odeslat požadavek na rezervaci, musíte do těla požadavku zadat hodnotu. Použijte vzor, který je popsán v části [Vytvoření jedné rezervační události](inventory-visibility-api.md#create-one-reservation-event). Pak vyberte **Odeslat**. Chcete-li zobrazit podrobnosti odpovědi na požadavek, vyberte **Zobrazit detaily**. Z podrobností odpovědi můžete také získat hodnotu `reservationId`.

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

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Přednačtení přehlednějšího dotazu na zásoby na skladě

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management uchovává velké množství informací o vašich aktuálních zásobách na skladě a zpřístupňuje je pro širokou škálu účelů. Mnoho každodenních operací a integrací třetích stran však vyžaduje jen malou podmnožinu těchto podrobností a dotazování systému na všechny z nich může vést k velkým datovým sadám, jejichž sestavení a přenos zabírá čas. Služba viditelnosti zásob proto může periodicky načítat a ukládat zjednodušenou sadu dat aktuálních zásob na skladu, aby byly tyto optimalizované informace neustále dostupné. Uložené podrobnosti o zásobách na skladě jsou filtrovány na základě konfigurovatelných obchodních kritérií, aby bylo zajištěno, že budou zahrnuty pouze ty nejrelevantnější informace. Vzhledem k tomu, že filtrované seznamy zásob na skladě jsou uloženy místně ve službě viditelnosti zásob a jsou pravidelně aktualizovány, umožňují rychlý přístup, export dat na vyžádání a efektivní integraci s externími systémy.

> [!NOTE]
> Aktuální verze Preview této funkce může poskytovat pouze předem načtené výsledky, které zahrnují pracoviště a místo. Konečná verze funkce by vám měla umožnit výběr jiných dimenzí pro předběžné načtení výsledků.

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

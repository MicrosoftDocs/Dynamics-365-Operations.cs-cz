---
title: Sledování příchozích cest a cest přepravních kontejnerů
description: Tento článek vysvětluje, jak můžete pomocí stránky Sledování vstupu monitorovat průběh cest a cest přepravních kontejnerů.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 17874f984945b27e036eafda841ec1fd95d345be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854348"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Sledování příchozích cest a cest přepravních kontejnerů

[!include [banner](../../includes/banner.md)]

Stránka **Sledování vstupu** umožňuje monitorovat průběh cest a cest přepravních kontejnerů. Každá cesta a cesta kontejneru je rozdělena na části podle *aktivit*, z nichž každá má na stránce svůj vlastní řádek. Na této stránce můžete zobrazit a zadat odhadovaná a skutečná kalendářní data podle aktivity.

Obvykle, v závislosti na nastavení zadaném v [řídicím centru sledování](delivery-information-setup.md#tracking-control-center), tyto aktivity automaticky zobrazují odhadované datum dojetí do konečného cíle. V závislosti na nastavení také konečné datum obvykle aktualizuje datum dodání nebo potvrzené datum na řádcích nákupní objednávky. U řádků převodního příkazu můžete nastavit systém tak, aby aktualizoval datum přijetí.

Chcete-li otevřít stránku **Sledování vstupu** přejděte na uzel **Náklady za doručení \> Sledování \> Sledování vstupu**.

## <a name="filter-the-activities-list"></a>Filtrování seznamu aktivit

Pole **Cesta** a **Přepravní kontejner** v horní části stránky **Sledování vstupu** můžete použít k filtrování stránky tak, aby zobrazovala pouze aktivity, které jsou přidruženy k vybrané cestě anebo přepravnímu kontejneru.

## <a name="update-tracking-information"></a>Aktualizace informace o sledování

Chcete-li aktualizovat plán cesty nebo cesty kontejneru, zadejte datum zahájení první aktivity. Odhadované datum ukončení poslední aktivity se poté aktualizuje. Nastavení pro každý úsek a šablonu cesty v [řídicím centru sledování](delivery-information-setup.md#tracking-control-center) určuje odhadované doby realizace. Odhadovaná data ukončení využívají dobu realizace od data zahájení aktivity. Poté, když je zaznamenáno skutečné datum ukončení, je datum zahájení další aktivity aktualizováno na stejné datum jako skutečné datum ukončení předchozí aktivity. Skutečná doba realizace se aktualizuje, aby bylo možné provést srovnání a analýzu. Další poznámky lze zadat do pole **Poznámka**.

Pořadí aktivit v mřížce je určeno pořadím úseků v příslušné šabloně cesty. Pokud se změní pořadí úseků v připojené cestě, změní se také řízení sledování.

Data všech kontejnerů můžete aktualizovat výběrem příkazu **Aktualizovat datum zahájení** nebo **Aktualizovat skutečné datum ukončení** v podokně akcí. Alternativně můžete zadat kalendářní data pro každý kontejner v zásilce. Tento přístup umožňuje větší flexibilitu, protože kontejnery lze v prostředí s více cestami rozdělit.

## <a name="buttons-on-the-action-pane"></a>Tlačítka v podokně akcí

Tlačítka v podokně akcí na stránce **Sledování vstupu** můžete použít pro práci s příchozími cestami. V následující tabulce jsou popsána dostupná tlačítka.

| Tlačítko | popis |
|---|---|
| Úpravy | Upravte cestu nebo cestu přepravního kontejneru. |
| Nová | Vytvořte novou cestu nebo cestu přepravního kontejneru. |
| Odstranit | Odstraňte vybranou cestu nebo cestu přepravního kontejneru. |
| Počáteční datum aktualizace | Aktualizujte datum zahájení aktivity pro všechny kontejnery v cestě. Když se aktualizuje datum zahájení konkrétní aktivity nebo úsek cesty, aktualizují se následující odhadovaná data zahájení na základě zadané doby realizace. |
| Aktualizovat skutečné koncové datum | Aktualizujte datum ukončení aktivity pro všechny kontejnery v cestě. Když se aktualizuje datum ukončení konkrétní aktivity nebo úsek cesty, aktualizují se následující aktivity na základě zadané doby realizace. |
| Přidat aktivity | Přidejte aktivitu do cesty ručně. Můžete například přidat aktivitu dezinfekce. Přidání může způsobit změnu potvrzeného data dodání zboží na lodi nebo cestě. Když je do cesty přidána aktivita, odhadované dny se nezadají, dokud se neaktualizuje datum zahájení úseku cesty. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informace a nastavení na kartě Přehled

Karta **Přehled** zobrazuje seznam všech aktivit, které patří do cesty anebo přepravního kontejneru, který je vybrán v horní části stránky. V následující tabulce jsou popsána pole, která jsou k dispozici pro každou aktivitu.

| Pole | popis |
|---|---|
| Úsek | ID úseku pro aktivitu, jak je definován v šabloně cesty. |
| Způsob dodání | Předpokládaná metoda doručení pro aktivitu. |
| Aktivita | Toto pole obvykle identifikuje úlohu nebo úkol, který je spojen s aktivitou. Mezi typické příklady patří *Plavba lodí* a *Odbavení*. |
| popis | Delší popis aktivity. |
| Počáteční datum | Toto pole zpočátku zobrazuje odhadované datum zahájení aktivity. Po zadání skutečného data ukončení předchozí aktivity se však zobrazí skutečné datum zahájení. Toto pole se používá k určení odhadovaného data ukončení na základě doby realizace. |
| Odhadované datum ukončení | Hodnota tohoto pole se počítá na základě data zahájení a doby realizace. Obvykle nebudete hodnotu upravovat přímo. |
| Skutečné datum dokončení | Uživatel by měl toto pole aktualizovat co nejdříve po výskytu aktivity. Skutečná doba realizace se poté aktualizuje. |
| Odhadované dny | Odhadovaná doba (ve dnech) potřebná k dokončení aktivity. |
| Skutečné dny | Skutečná doba (ve dnech) potřebná k dokončení aktivity. |
| Poznámka | Toto pole použijte k přidání různých poznámek a podrobností o aktivitě. |

## <a name="information-and-settings-on-the-general-tab"></a>Informace a nastavení na kartě Obecné

Karta **Obecné** zobrazuje informace o úseku, který je vybrán na kartě **Přehled**. Ačkoli se tu opakují některé informace uvedené na kartě **Přehled**, obsahuje také další informace o vybraném úseku.

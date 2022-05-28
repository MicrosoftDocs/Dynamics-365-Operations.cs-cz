---
title: Aktualizace sledování pro zaskladnění
description: Toto téma popisuje, jak nastavit a spustit periodický úkol Aktualizovat sledování pro zaskladnění.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f02ba71b4eb32551cebc6cf160f0285eac8ae7ad
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673963"
---
# <a name="update-tracking-for-put-away"></a>Aktualizace sledování pro zaskladnění

[!include [banner](../includes/banner.md)]

Periodický úkol *Aktualizovat sledování pro zaskladnění* je navržen tak, aby byl spuštěn jako noční opakující se dávka. Identifikuje, které plavby obdržely všechny skladové transakce a které plavby nemají hodnotu pro skutečné datum ukončení. Potom podle potřeby nastaví skutečné datum ukončení na aktuální datum.

*Činnosti kontejneru* jsou vytvořeny pro každý *úsek* cesty každého *přepravního kontejneru*. Tyto hodnoty jsou definovány šablonou cesty, která je vybrána při vytváření plavby. U každého záznamu činností kontejneru lze nastavit hodnoty **Počáteční datum**, **Odhadované datum ukončení**, a **Skutečné datum ukončení**. Tato pole lze aktualizovat po obdržení potvrzení, že úsek začal nebo byl dokončen.

Informace související s potvrzenými kalendářními daty obvykle poskytuje třetí strana, například zasílatel, protože tyto akce jsou udržovány mimo aplikaci Microsoft Dynamics 365 Supply Chain Management. Informace třetí strany však nejsou nutné ke sledování příchodu zboží z přepravního úseku do skladu (jak je označeno zaskladněním zboží). Sledování lze tedy určit na základě informací zadaných v Dynamics 365 Supply Chain Management.

Chcete-li nastavit a spustit periodický úkol *Aktualizovat sledování pro zaskladnění*, postupujte takto.

1. Přejděte do nabídky **Náklady za doručení \> Periodické úkoly \> Aktualizovat sledování pro zaskladnění**.
1. V dialogovém okně **Aktualizovat sledování pro zaskladnění** v části **Parametry** nastavte následující pole:

    - **Úsek** – Vyberte jedinečný identifikační název/číslo pro část cesty, u které chcete aktualizovat sledování. Vybraná hodnota musí představovat příjezd plavby do skladu.
    - **Aktivita** – Vyberte aktivitu, která byla provedena během vybraného úseku. Tyto hodnoty jsou přiřazeny podle řádku šablony cesty v řídicím centru sledování.

1. Chcete-li omezit sadu záznamů, které mají být zahrnuty do aktualizace, vyberte tlačítko **Filtr** na záložce **Záznamy, které mají být zahrnuty**. Zobrazí se standardní dialogové okno dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Supply Chain Management. Pole zde jsou jen pro čtení a zobrazují hodnoty, které se vztahují k vašemu dotazu.
1. Na kartě s náhledem **Spustit na pozadí** nastavte dávkové a plánovací možnosti, jak požadujete, stejně jako u jiných typů úloh v Supply Chain Management.
1. Výběrem **OK** použijte vaše nastavení a spusťte nebo naplánujte aktualizaci.

---
title: Přecenění leasingových splátek vázaných na indexovou sazbu
description: Toto téma popisuje úpravu provedenou za účelem pronájmu závazku k aktivu s právem na užívání (ROU), když se variabilní leasingové platby změní z důvodu změny indexové sazby.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5abd1f5d265c6e8b53903e6df5c52a06b3468880
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968045"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Přecenění leasingových splátek vázaných na indexovou sazbu

[!include [banner](../includes/banner.md)]

Toto téma popisuje úpravu provedenou za účelem pronájmu závazku k aktivu s právem na užívání (ROU), když se variabilní leasingové platby změní z důvodu změny indexové sazby. Leasingový závazek a používaný majetek budou upraveny tak, aby zohledňovaly částky platby. V rámci tématu Kodifikace účetních standardů 842 (ASC 842), což je standard v Obecně přijímaných účetních zásadách v USA (US GAAP), se mění pouze variabilní platby, když se platby zvyšují nebo snižují z důvodu změny indexové sazby, pokud neexistují další změny peněžních toků. Tyto další změny mohou zahrnovat změnu podmínek leasingu, která souvisí s úrokovými sazbami. Další informace viz ASC 842-10-55-225 a odstavec 42 (b) Mezinárodního standardu účetního výkaznictví 16 (IFRS 16).

## <a name="adjust-lease-payments"></a>Úprava leasingových splátek

Podle těchto kroků proveďte přecenění leasingových splátek vázaných na indexovou sazbu.

1. Chcete-li spustit proces přecenění indexu leasingu, přejděte na **Majetkový leasing \> Periodické \> Přehodnocení indexové sazby**.

    Zobrazí se stránka **Přehodnocení indexové sazby**, která zobrazuje všechny předchozí procesy přecenění indexu pronájmu, které byly spuštěny. Informace na této stránce zahrnují ID procesu, které bylo vygenerováno z nastavení číselných řad, právnickou osobu, počet leasingových knih, které byly upraveny, celkovou úpravu závazků u leasingů IFRS 16 a celkové variabilní platby, které byly upraveny pro leasingy ASC 842.

2. Chcete-li spustit přecenění, v podokně akcí vyberte **Přecenění indexu leasingu**.

    Zobrazí se dialogové okno **Parametry přecenění indexu**. Zde můžete filtrovat a vybrat, které leasingy, skupiny leasingu nebo jiná kritéria se mají použít, když vyberete leasingy, které chcete přehodnotit. Na kartě **Spustit na pozadí** můžete nastavit proces přecenění indexu tak, aby běžel dávkově.

4. Vyberte filtry pro výběr leasingů, které by měly být zahrnuty do zpracování na pozadí, a poté vyberte **OK**.

    Objeví se dialogové okno **Náhled přehodnocení indexu** s nájemními smlouvami, které budou přeceněny. Ukazuje také úpravy aktiv a pasiv nebo úpravy variabilních plateb.

5. Chcete-li zabránit přeceňování leasingů, vyberte leasingy, které **by měly** být přeceněny. Pokud nevyberete žádné leasingy, budou všechny leasingy přeceněny. Po dokončení vyberte **OK** k přecenění leasingových splátek.
6. Chcete-li zobrazit transakce, které byly vytvořeny pro konkrétní proces přecenění indexu, vyberte ID procesu a poté vyberte **Transakce**.

    Zobrazí se dialogové okno s podrobnostmi o transakcích, které byly vytvořeny během zpracování.

> [!NOTE]
> Přeceňovat lze pouze leasingy, jejichž datum přecenění je systémové datum nebo dřívější. Systém automaticky ignoruje všechny leasingy, jejichž datum přecenění je pozdější než systémové datum.

## <a name="asc-842-leases--index-revaluation"></a>Leasingy ASC 842 - přecenění indexu

Chcete-li zobrazit účinky procesu přecenění leasingu na leasingy ASC 842, otevřete plán plateb pro leasing. Stránka zobrazuje pouze proměnné platby, které byly provedeny ke dni nebo po změně data přecenění z důvodu přecenění indexu. Amortizační a odpisové plány zůstávají nezměněny. Když vytvoříte fakturu s variabilní platbou, bude variabilní platba odepsána z účtu účtování variabilní platby. Také variabilní částka platby je přidána k položce kreditu, která je zaúčtována přímo prodejci nebo zaúčtována na splatný účet Notes, v závislosti na nastavení knihy pronájmu.

Řádky platebního plánu na stránce s podrobnostmi o pronájmu jsou automaticky aktualizovány o nový řádek, který označuje novou sazbu indexu. Sloupec dále ukazuje, zda byl řádek vytvořen ručně nebo prostřednictvím procesu přecenění indexu.

## <a name="ifrs-16-leases--index-revaluation"></a>Leasingy IFRS 16 - přecenění indexu

Chcete-li zobrazit účinky procesu přecenění leasingu na leasingy IFRS 16, otevřete podrobnosti o leasingu pro upravený leasing. Pole **doba trvání leasingu** a **očekávaná doba použitelnosti majetku** byla aktualizována, aby odrážela plynutí času od data zahájení nebo data úpravy do data přecenění. Řádky platebního plánu byly navíc aktualizovány tak, aby odrážely nové platby na leasing, novou indexovou sazbu a způsob, jakým byl řádek vytvořen.

Můžete si prohlédnout nově vygenerovaný plán plateb, který začíná datem přecenění, a zobrazit celkovou aktualizovanou částku platby. Byl také vytvořen nový plán amortizace závazků z leasingu a plán odpisů aktiv, aby odrážely upravený splátkový kalendář.

Položka deníku automaticky zaúčtovala položku deníku úprav na účet kvůli změnám v leasingových splátkách, které souvisejí s přeceněním indexu.

> [!NOTE]
> Pokud je možnost **Částka splátky** aktivní na pevné záložce **Všeobecné** stránky **Údaje leasingu** a související kniha je IFRS 16, proces přecenění indexu automaticky přidá záznam do dialogového okna **Rozdělení částky platby**. Částka bude odrážet změnu, která byla provedena v platbě z důvodu přecenění indexu. Záznam bude označen jako **Používá se pro přecenění indexu IRFS 16**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

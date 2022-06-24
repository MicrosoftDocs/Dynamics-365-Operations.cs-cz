---
title: Plán dodávek
description: Tento článek obsahuje informace o stránce Plán dodávek a jejích funkcích.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851732"
---
# <a name="supply-schedule"></a>Plán dodávek

[!include [banner](../includes/banner.md)]

Stránka **Plán dodávek** zobrazuje komplexní přehled nabídky a poptávky pro určitý produkt nebo produktovou řadu. Informace jsou filtrovány podle umístění, hlavního plánu a období. Na stránce můžete také vytvářet nové objednávky, upravovat stávající plánované objednávky a spouštět hlavní plánování.

## <a name="open-the-supply-schedule-page"></a>Otevření stránky Plán dodávek

Stránku **Plán dodávek** můžete otevřít některým z následujících způsobů:

- Přejděte na **Hlavní plánování \> Hlavní plánování \> Plán dodávek**. V dialogovém okně **Upravit filtr** zadejte plán a produkt, který hledáte, zadáním hodnot filtru do příslušných polí. (Ve zbytku tohoto článku je kolekce hodnot filtrů, které zadáte, označována jako „filtr“ nebo „aktuální filtr“.) Až budete hotovi, vyberte **OK**.
- Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**. Vyberte nebo otevřete produkt. Poté v podokně akcí na kartě **Plán** ve skupině **Zobrazit** zvolte **Plán dodávek**.
- Přejděte do uzlu **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Alokační klíče pro položky**. Vyberte alokační klíč položky, který se používá jako produktová řada. Poté v podokně akcí vyberte možnost **Plán dodávek**.
- Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**. Vyberte nebo otevřete plánovanou objednávku. Poté v podokně akcí na kartě **Zobrazit** ve skupině **Zobrazit** zvolte **Plán dodávek**.

> [!NOTE]
> Když otevřete stránku **Plán dodávek** z produktu, produktové řady nebo plánované objednávky, nemusíte zadávat hodnoty filtrů. Systém použije výchozí šablonu období.

## <a name="use-the-supply-schedule-page"></a>Používání stránky Plán dodávek

Stránka **Plán dodávek** se skládá z horní části, záložky **Konečné zásoby období**, další záložky, která se stane viditelnou na základě čáry vybrané v horní části, a podokna Okno s fakty. (Chcete-li otevřít podokno Okno s fakty a zobrazit okno s fakty, vyberte na pravém okraji stránky **Související informace**.)

### <a name="upper-section"></a>Horní část

Horní část stránky **Plán dodávek** obsahuje mřížku, která ukazuje následující data pro produkt nebo produktovou řadu. Tato data jsou rozdělena podle období definovaných hodnotou **Šablona období** z filtru.

- **Počáteční zásoby období** – Tento řádek ukazuje očekávaný stav zásob na začátku období, pokud dojde k realizaci všech objednávek v systému.
- **Konečné zásoby období** – Tento řádek ukazuje očekávaný stav zásob na konci období, pokud dojde k realizaci všech objednávek v systému.
- **Doložené konečné zásoby období** – Tento řádek ukazuje množství zásob na konci období, které jsou doloženy vůči budoucí poptávce.
- **Čisté dodávky období** – Tento řádek ukazuje rozdíl mezi nabídkou a poptávkou v daném období.
- **Minimální zásoby** – Tento uzel ukazuje pojistnou zásobu pro produkt nebo produktovou řadu. Chcete-li tento uzel rozbalit nebo sbalit, vyberte jej a poté vyberte **Rozbalit** nebo **Sbalit** na panelu nástrojů. Tento uzel se zobrazí pouze v případě, že pro produkt nebo produktovou řadu existuje pojistná zásoba.
- **Poptávka** - Tento uzel ukazuje poptávku po produktu nebo produktové řadě. Poptávka je seskupena podle typu transakce. Chcete-li tento uzel rozbalit nebo sbalit, vyberte jej a poté vyberte **Rozbalit** nebo **Sbalit** na panelu nástrojů. Mezi typy transakcí poptávky patří deníky prodejů, převodů a zásob. Tento uzel se zobrazí pouze v případě, kdy existuje poptávka po produktu nebo produktové řadě.
- **Dodávka** - Tento uzel ukazuje dodávku produktu nebo produktové řady. Dodávka je seskupena podle typu transakce. Chcete-li tento uzel rozbalit nebo sbalit, vyberte jej a poté vyberte **Rozbalit** nebo **Sbalit** na panelu nástrojů. Typy dodavatelských transakcí zahrnují výrobu, nákup a převody. Tento uzel se zobrazí pouze v případě, kdy existuje dodávka produktu nebo produktové řady.

Mnoho dostupných tlačítek na panelu nástrojů, okna s fakty a záložky se zobrazují podle vašeho výběru možností v horní části. Typ transakce obvykle zvolíte výběrem jednoho z řádků pod uzlem **Dodávka** nebo **Poptávka**. Poté zvolíte období výběrem konkrétního sloupce pro vybraný řádek.

Panel nástrojů nad mřížkou v horní části stránky **Plán dodávek** obsahuje následující tlačítka:

- **Rozbalit/Sbalit** – Rozbalte nebo sbalte vybraný uzel, například **Poptávka**, **Dodávka** nebo jejich podřízené uzly. (Uzly ukazují předponu **\[+\]** nebo **\[-\]** jako indikátor, zda jsou aktuálně sbalené nebo rozbalené.)
- **Nový** – Otevřete nabídku, kde každý příkaz zase otevře dialogové okno nebo stránku, která vám umožní přidat konkrétní typ položky pro výběr. Mezi dostupné příkazy patří **Prognóza dodávky**, **Plánovaná objednávka**, **Plánovaný kanban**, **Nová výrobní zakázka**, **Nákupní objednávka** a **Převodní příkaz**.
- **Hlavní plánování** – Spusťte hlavní plánování. Zobrazí se dialogové okno, kde můžete určit plán, který se má spustit. Ve výchozím nastavení je pole **Hlavní plán** nastaveno tak, aby odpovídalo aktuálnímu filtru.
- **Maximální dokončená výroba** – Otevře stránku **Maximální dokončená výroba** pro produkt, který je definován v aktuálním filtru.
- **Aktualizovat plánované objednávky** – Otevře stránku **Plánované objednávky**, která zobrazuje plánované objednávky pro produkt nebo produktovou řadu, která je definována v aktuálním filtru.
- **Úroveň** – Rozšíří plánované objednávky podle nastavení z dialogového okna, které se objeví.
- **Zásady materiálového plánu závislé na umístění** – Otevře stránku **Disponibilita položky** pro produkt definovaný v aktuálním filtru.
- **Kanbanové pravidlo** – Otevře stránku **Kanbanová pravidla** pro produkt, který je definován v aktuálním filtru.

### <a name="fasttabs"></a>Záložky

Stránka **Plán dodávek** může obsahovat následující záložky:

- **Konečné zásoby období** – Tato záložka zobrazuje konečné zásoby období v grafickém formátu.
- **Profil dodávky** – Tato záložka zobrazuje data o dodávce v grafickém formátu. Zobrazí se, když vyberete uzel **Dodávka** uzel nebo řádek pod ním v horní části.
- **Souhrn** – Tato záložka zobrazuje souhrnné podrobnosti související s typem transakce, který jste vybrali v horní části. Pokud například vyberete **Prodeje** pod uzlem **Poptávka**, záložka zobrazuje pole související s prodejními objednávkami, například **Požadované řádky prodejních objednávek** nebo **Celková částka**. Pokud zvolíte **Výrobní zakázky** pod uzlem **Výroba** uzlu **Dodávka**, tato záložka zobrazuje pole, která souvisejí s výrobními zakázkami, jako například **Plánované výrobní zakázky** nebo **Celkem naplánováno**. Hodnoty polí závisí na období, které jste vybrali v horní části. 
- **\[Typ transakce\] - \[Období\]** – Tato záložka zobrazuje objednávky pro typ transakce a období, které jste vybrali v horní části. V názvu záložky se odrážejí tyto výběry. Může se jmenovat například **Prodejní objednávky – Nevyřízené položky** nebo **Výrobní zakázky – týden 37**.

### <a name="action-pane"></a>Podokno akcí

V podokně akcí jsou k dispozici následující tlačítka:

- **Upravit filtr** – Otevře dialog **Upravit filtr**, ve kterém můžete aktualizovat hodnoty filtrů a poté znovu otevřít stránku **Plán dodávek**, která odráží aktualizované nastavení filtru.
- **Zobrazit zpoždění** – Zvýrazní příslušné řádky v horní části, pokud existuje zpožděná objednávka daného typu transakce.

### <a name="factbox-pane"></a>Podokno Okno s fakty

Chcete-li otevřít podokno Okno s fakty a zobrazit okno s fakty, vyberte na pravém okraji stránky **Související informace**. Na stránce **Plán dodávek** jsou k dispozici následující okna s fakty:

- **Podrobnosti zboží** – Toto okno s fakty zobrazuje základní informace o produktu, který je definován v aktuálním filtru. Je prázdné, pokud jste ve filtru definovali produktovou řadu.
- **Akce** – Toto okno s fakty zobrazuje akce pro objednávky s typem transakce, který jste vybrali v horní části.
- **Zpoždění** – Toto okno s fakty zobrazuje zpoždění pro objednávky s typem transakce, který jste vybrali v horní části.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

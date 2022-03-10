---
title: Nastavení dceřiné právnické osoby pro konsolidaci
description: Toto téma vysvětluje, jak pracovat s účtovými osnovami pro konsolidační společnosti.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: fbec5ad8fa5e17b75859c07ee64a66c9568c97d3d18b6a7616a64303d3a33f10
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727952"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Nastavení dceřiné právnické osoby pro konsolidaci

[!include [banner](../includes/banner.md)]

Metoda, která slouží k přípravě účtů dceřiné společnosti pro konsolidaci, zčásti závisí na rozsahu účtové osnovy účtů ve dceřiné právnické osobě, jež odráží strukturu účtové osnovy v konsolidované právnické osobě.

Před zahájením konsolidace jako součásti uzávěrky určitého období proveďte přípravné operace pro uzávěrku období, avšak neuzavírejte účty dceřiné společnosti, dokud nebude konsolidace dokončena. Další informace o uzávěrce na konci období naleznete v tématu [Uzavření hlavní knihy na konci období](close-general-ledger-at-period-end.md) a [Uzavření fiskálního roku](tasks/close-fiscal-year.md).

> [!NOTE]
>  Doporučujeme použít Management Reporter pro Microsoft Dynamics 365 Finance, chcete-li kombinovat finanční výsledky pro více právnických osob v konsolidovaném formátu. Management Reporter vám umožňuje vytvářet konsolidované finanční výkazy napříč právnickými osobami, používat Excel k importu konsolidačních dat z jiných zdrojů a převádět částky do libovolného počtu měn vykazování, aniž byste museli spouštět proces konsolidace v Dynamics 365 Finance.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Mapování hlavních účtu dceřiné společnosti na konsolidované hlavní účty

Pokud účtová osnova ve dceřiné právnické osobě nedodržuje účtovou osnovu konsolidované právnické osoby, můžete mapovat hlavní účty v dceřiné společnosti na hlavní účty konsolidované právnické osoby.

1. V *dceřiné právnické osobě* přejděte na **Hlavní kniha \> Založit** \> **Účtová osoba \> Účtová osoba**.
2. Vyberte účtovou osnovu. Na pevné záložce **Hlavní účty** vyberte hlavní účet a poté vyberte **Upravit**.
3. Vyberte jednotlivé hlavní účty dceřiné společnosti, které je třeba mapovat na hlavní účet konsolidované společnosti. Na pevné záložce **Obecné** v poli **Konsolidační účet** zadejte účet v konsolidované právnické osobě, na který mají být převedeny transakce či zůstatek vybraného hlavního účtu dceřiné společnosti. Pro některé účty dceřiné společnosti můžete zadat stejný konsolidovaný hlavní účet.

    > [!NOTE]
    > Pokud se typy hlavních účtů mapovaných vedlejší účtů liší od typů hlavního účtu pro účty v konsolidované právnické osobě, hodnoty účtů, které mají typ hlavního účtu **Celkem** jsou přepsány během konsolidace.

4. Připravte sestavy a finanční výkazy pro konsolidovanou právnickou osobu, které jsou založeny na finančních dimenzích. Pomocí těchto kroků můžete namapovat finanční dimenze, které se používají na účtech dceřiné společnosti, na finanční dimenze v konsolidované právnické osobě:

    1. V *Dceřiné právnické osobě* přejděte na **Hlavní kniha \> Nastavení \> Finanční dimenze \> Finanční dimenze**, vyberte finanční dimenzi a poté vyberte **Hodnoty finanční dimenze**.
    2. Vyberte hodnotu finanční dimenze pro mapování na jinou hodnotu finanční dimenze v konsolidované právnické osobě.
    3. Na záložce s náhledem **Obecné** zadejte v poli **Skupinová dimenze** finanční dimenzi v konsolidované právnické osobě. Během konsolidace bude přiřazena tato finanční dimenze transakcím a zůstatkům, které používají vybrané finanční dimenze v dceřiné právnické osobě. Finanční dimenze, které sem zde zadáte, musí být používány v konsolidované právnické osobě. Můžete přiřadit finanční dimenzi, která slouží jako finanční dimenze skupiny, několika finančním dimenzím dceřiné společnosti.

5. Pokud provádíte online konsolidaci, postupujte podle těchto kroků, abyste zajistili, že k převodům dojde podle vašich představ:

    1. V *konsolidované právnické osobě* přejděte na **Hlavní kniha \> Periodické \> Konsolidovat \> Konsolidovat \[Exportovat do\]**, chcete-li otevřít stránku **Konsolidovat\[ Online\]**.
    2. Na kartě **Kritéria** zaškrtněte políčko **Použít konsolidační účet**.
    3. Na kartě **Finanční dimenze** vyberte příslušné finanční dimenze.
    4. Pro každou vybranou finanční dimenzi můžete zadat číslo v poli **Pořadí segmentů** a označit tak pořadí, ve kterém mají být dimenze zobrazeny.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Uchovejte stejnou účtovou osnovu v dceřiné společnosti i konsolidované právnické osobě

Hlavní účty v dceřiné právnické osobě mohou mít stejná čísla účtů a stejnou strukturu účtové osnovy jako hlavní účty konsolidované právnické osoby. V tomto případě není nutné ručně mapovat hlavní účty v dceřiné společnosti na hlavní účty v konsolidované právnické osobě.

Před zahájením konsolidace postupujte podle těchto kroků.

1. V *konsolidované právnické osobě* přejděte na **Hlavní kniha \> Periodické \> Konsolidovat \> Konsolidovat \[Exportovat do\]**, chcete-li otevřít stránku **Konsolidovat\[ Online\]**.
2. Zaškrtněte políčko **Použít konsolidační účet**. Během konsolidace budou transakce a zůstatky automaticky převedeny na správné účty.

> [!NOTE]
> Pokud si účty vzájemně neodpovídají, konsolidace bude zastavena a bude zobrazena zpráva.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Vytvoření účtovou osnovu pro konsolidovanou právnickou osobu založenou na existující účtové osnově

Konsolidaci je možné provést i v případě, že dosud nebyla vytvořena účtová osnova konsolidované právnické osoby.

- Pokud jste naplánovali účtovou osnovu, kterou chcete použít v konsolidované právnické osobě, můžete na tuto osnovu namapovat účty dceřiné společnosti.
- Pokud nenamapujete žádné účty dceřiné společnosti, budou při přenosu dat dceřiné společnosti do konsolidované společnosti automaticky vytvořeny účty konsolidované právnické osoby. Tyto účty jsou založeny na hlavním účtu. Následující data se shromažďují v účtech v konsolidované právnické osobě, které mají stejné číslo účtu jako účty dceřiné společnosti.

Bez ohledu na to, zda jsou namapovány účty, zrušte zaškrtnutí políčka **Použít konsolidační účet** na stránce **Konsolidovat** v konsolidované právnické osobě před spuštěním tohoto typu konsolidace.

> [!NOTE]
> Pomocí této metody lze vytvořit účtovou osnovu v konsolidované právnické osobě na základě účtové osnovy některé z dceřiných právnických osob. (Další informace viz [Skupiny konsolidačních účtů a další konsolidační účty](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Poté každému konsolidovanému hlavnímu účtu přiřaďte vhodný princip převodu konsolidace a spusťte konsolidaci pro všechny dceřiné právnické osoby.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
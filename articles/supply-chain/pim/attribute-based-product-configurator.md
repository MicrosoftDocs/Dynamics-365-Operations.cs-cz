---
title: Prodejní ceny podle atributů pro konfiguraci produktu založeného na omezeních
description: Toto téma popisuje, jak vytvářet modely prodejních cen s prodejními cenami podle komponent a atributů než podle fyzického kusovníku a trasy (postupu).
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65ab96c71fa44d6acad0bcb5cd7a65321109b93d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221960"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Prodejní ceny podle atributů pro konfiguraci produktu založeného na omezeních

Toto téma popisuje, jak vytvářet modely prodejních cen s prodejními cenami podle komponent a atributů než podle fyzického kusovníku a trasy (postupu). Pro každý model konfigurace produktu můžete vytvořit několik modelů prodejních cen.

## <a name="set-relevant-product-information-management-parameters"></a>Nastavení relevantních parametrů modulu Řízení informací o produktu

Než začnete vytvářet cenové modely, musíte definovat výchozí měnu, která se použije při vytváření modelů prodejních cen. Můžete také zvolit, zda chcete připojit soubor aplikace Microsoft Excel s rozpisem cen pro všechny řádky objednávky nebo nabídky. Rozpis cen vám umožní sdílet se zákazníky podrobnosti o tom, jak jste dosáhli konkrétní prodejní ceny nakonfigurovaného produktu.

Nastavení výchozí měny:

1. Přejděte do oddílu **Správa informací o produktu \> Nastavení \> Parametry modulu řízení informací o produktu**.
1. Otevřete kartu **Modely konfigurace produktů založených na omezeních**.
1. Otevřete rozevírací seznam **Výchozí měna** a vyberte měnu.

    ![Nastavení výchozí měny pro konfiguraci produktu založeného na omezeních](media/prod-config-currency.png "Nastavení výchozí měny pro konfiguraci produktu založeného na omezeních")

1. Pokud chcete připojit excelovýc soubor s rozpisem cen pro všechny řádky objednávky nebo nabídky, pak v oddílu **Cenový model** nastavte možnost **Připojit** na *Ano*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Sestavení modelů prodejních cen

Sestavení modelu prodejních cen:

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyberte cílový model konfigurace produktu.
1. V podokně akcí otevřete kartu **Model** a ve skupině **Nastavení** vyberte **Cenové modely**.
1. Otevře se stránka **Cenové modely**.
1. Vyberte cenový model nebo do mřížky přidejte nový.
1. Vyberte **Upravit**, aby se otevřela stránka úprav pro vybraný model, která poskytuje následující funkce:
    - Záhlaví formuláře zobrazuje výchozí měnu a umožňuje vám přidat nové měny pro nastavení ceny.
    - V levém podokně jsou zobrazeny všechny komponenty a uživatelské požadavky modelu produktu. Každý uzel ve stromu modelu produktu může mít jeden výraz základní ceny a volitelný počet pravidel výrazu. Pravidlo výrazu se skládá z podmínky a výrazu a každé pravidlo výrazu pokrývá možnost produktu, která pomáhá řídit cenu produktu.
    - Když vytváříte podmínky a výrazy, máte k dispozici stejné operátory jako pro výpočty v modelu produktu. Editor výrazů také podporuje podmínky i výrazy.
1. Vyberte uzel v levém sloupci a poté pomocí funkcí popsaných v předchozím kroku pro něj vytvořte cenová pravidla (viz také příklad poskytnutý po tomto postupu). Podle potřeby tento krok opakujte pro každý uzel.

Následující příklad ukazuje základní cenu statického čísla 899,95 EUR, kterou lze upravit jedním nebo více z následujících pěti pravidel výrazu, v závislosti na konfiguraci vybrané zákazníkem:

- Za bílou povrchovou úpravu skříně odečtěte 59,95 EUR.
- Za ochranu rohů připočítejte 35,95 EUR.
- Za kovovou přední mřížku připočítejte 89,95 EUR.
- Za povrchovou úpravu skříně z růžového dřeva připočítejte 119,95 EUR.
- Připočítejte 12,95 EUR za každou jednotku výšky reproduktoru.

![Příklad cenového modelu](media/prod-config-rules-example.png "Příklad cenového modelu")

## <a name="add-support-for-multiple-currencies"></a>Přidání podpory pro více měn

Při prodeji konfigurovatelného produktu systém zkontroluje, zda byly ceny nastaveny výslovně v měně zákazníka. Pokud ano, použijí se explicitní hodnoty. Pokud ne, systém použije směnné kurzy měn stanovené pro prodejní společnost k převodu hodnoty výchozí měny na měnu zákazníka.

Postup přidání explicitních cen v další měně:

1. Otevřete stránku úprav svého cenového modelu, jak je popsáno v oddíle [Sestavení modelů prodejních cen](#build-price-model).
1. Vybert tlačítko **Přidat** v záhlaví cenového modelu a otevřete rozevírací dialogové okno **Měny** se seznamem dostupných měn.
1. Vyberte měnu, kterou chcete přidat, v rozevíracím dialogovém okně **Měny**, a poté vyberte **OK**.
1. Rozevírací seznam **Aktuální měna** nyní obsahuje měnu, kterou jste právě přidali, a k tomu všechny ostatní měny, které mohly být přidány dříve. Vyberte novou měnu a všimněte si, že mřížka v oddíle **Pravidla výrazů** nyní obsahuje dvě pole výrazu:
    - **Výraz** – Zobrazuje výraz (nebo konstantní hodnotu) pro nalezení ceny pomocí aktuálně vybrané měny pro pole **Aktuální měna**.
    - **Výchozí výrazy** – Zobrazuje výraz (nebo konstantní hodnotu) pro nalezení ceny pomocí výchozí měny (zobrazené v poli **Výchozí měna**).

    > [!NOTE]
    > Pole **Podmínka** pro pravidla výrazu je „vlastněno“ výchozí měnou, což znamená, že nemůžete upravit podmínku pro jiné měny. Nemůžete ani přidat nová pravidla výrazu, pokud je jako **Aktuální měna** vybrána jiná než výchozí měna.
1. Upravte hodnoty ve sloupci **Výraz** podle potřeby pro aktuální měnu.

V níže uvedeném příkladu je výchozí měna _EUR_ a měna _USD_ byla přidána jako další měna.

![Příklad modelu s více měnami](media/prod-config-rules-currency-example.png "Příklad modelu s více měnami")

> [!NOTE]
> Nelze přidat pravidla výrazu, která jsou jedinečná pro jinou než výchozí měnu. Chcete-li vytvořit pravidla výrazu, která by byla relevantní pouze pro jinou měnu než výchozí měnu, nastavte výraz ceny pro výchozí měnu na nulu. Poté nastavte odpovídající výraz pro jinou než výchozí měnu.

## <a name="test-your-price-model"></a>Otestování cenového modelu

Chcete-li otestovat, jak prodejní ceny fungují v konfigurační relaci, otevřete stránku úprav svého cenového modelu, jak je popsáno v oddíle [Sestavení modelů prodejních cen](#build-price-model), a poté v podokně akcí vyberte **Test**. Otevře se dialogové okno **Testovací model produktu**, kde můžete provést následující akce:

- Pomocí zde nabízeného nastavení konfigurace vyberte možnosti produktu a poté zjistěte, jak ovlivňují zobrazenou hodnotu **Cena a datum expedice**.
- Výběrem **Zobrazit rozúčtování ceny** si stáhnete excelový dokument, který zobrazuje veškeré podrobnosti o tom, jak byla cena vypočítána.

![Otestování modelu produktu](media/prod-config-test.png "Otestování modelu produktu")

Stažená tabulka zobrazuje absolutní hodnotu i příspěvek jako procento pro každý element aktivní ceny. Pokud jste na stránce **Parametry modulu řízení informací o produktu** nastavili možnost cenového modelu **Připojit**, připojí se tato excelová stránka k řádku objednávky nebo nabídky.

![Excelová tabulka zobrazující rozpis cen](media/prod-config-excel-example.png "Excelová tabulka zobrazující rozpis cen")

## <a name="set-up-selection-criteria-for-price-models"></a>Nastavení kritérií výběru pro cenové modely

Když jsou vaše cenové modely na místě, musíte stanovit alespoň jedno výběrové kritérium, které vybere cenový model, když nakonfigurujete nabídku nebo objednávku. Uděláte to nastavením jednoho nebo více dotazů. V kombinaci s odpovídajícími modely prodejních cen poskytují dotazy velkou flexibilitu při cílení prodejních cen na konkrétní zákazníky, regiony, období a další kritéria.

Nastavení kritérií výběru pro cenové modely:

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyberte cílový model konfigurace produktu.
1. V podokně akcí otevřete kartu **Model** a ve skupině **Nastavení** vyberte **Kritéria cenového modelu**. Otevře se stránka **Kritéria cenového modelu**.
1. Pokud řádek dotazu, který potřebujete, dosud neexistuje, vyberte **Nový** v podokně akcí, přidejte do mřížky nový řádek a proveďte pro něj následující nastavení:
    - **Název** – Zadejte název tohoto řádku.
    - **Popis** – Stručně popište dotaz a k čemu slouží.
    - **Cenový model** – Vyberte [cenový model](#build-price-model) (z aktuálního modelu konfigurace), který dotaz použije při spuštění.
    - **Typ objednávky** – Vyberte typ objednávky, na kterou se bude dotaz vztahovat.
    - **Platné od** – Určete první den, kdy se dotaz použije.
    - **Ukončit platnost k datu** – Určete poslední datum, kdy se dotaz použije.

    ![Kritéria cenového modelu](media/prod-config-price-model-criteria.png "Kritéria cenového modelu")

1. Vyberte řádek pro dotaz, který chcete definovat, a poté v **Podoknu akcí** vyberte **Upravit**. Otevře se dialogové okno návrháře dotazů. Funguje jako většina návrhářů dotazů v aplikaci Supply Chain Management. Slouží k definování podmínek, za kterých by měl být použit cenový model pro vybraný řádek.

1. Opakujte kroky 4 až 5 pro každý požadovaný dotaz.
    > [!TIP]
    > Můžete ušetřit čas zkopírováním existujícího řádku, který je již podobný novému, který potřebujete přidat. Chcete-li to provést, vyberte cílový řádek a poté v podokně akcí vyberte **Duplikát**.

1. Po dokončení nastavení kritérií je uspořádejte do správného pořadí v seznamu **Kritéria cenového modelu**. Chcete-li přemístit řádek, vyberte řádek a poté v podokně akcí vyberte **Nahoru** nebo **Dolů**.

    > [!IMPORTANT]
    > V době konfigurace začne systém hledat od začátku seznamu a použije první dotaz, který odpovídá datům v nabídce nebo na řádku objednávky. Proto musíte své nejspecifičtější dotazy umístit nahoru. Pokud do horní části seznamu umístíte obecný dotaz, bude použit právě tento, i když níže v seznamu může být dotaz, který cílí na přesného zákazníka nebo potenciálního zákazníka z konfigurace.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Nastavení prodejních cen založených na atributech pro verzi modelu produktu

Posledním krokem je určení prodejních cen založených na atributech pro verzi modelu produktu. Postup je následující:

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyberte cílový model konfigurace produktu.
1. V podokně akcí otevřete kartu **Model** a ve skupině **Podrobnosti modelu produktu** vyberte **Verze**.
1. Otevře se stránka **Verze**. Ujistěte se, že **Metoda cenových kalkulací** je nastavená na **Na základě atributů**.
    ![Nastavení metody cenových kalkulací podle atributů](media/prod-config-versions.png "Nastavení metody cenových kalkulací podle atributů")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Finanční konsolidace a převod měny"
description: "Toto téma popisuje finanční konsolidace a převod měny v hlavní knize."
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.translationtype: HT
ms.sourcegitcommit: ce9c24a0a89dd4e6a0f3f2c7789b4f553d88d412
ms.openlocfilehash: 8427d53bac3216d362b2bf8983a847f069351b3b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/13/2018

---

# <a name="financial-consolidations-and-currency-translation"></a>Finanční konsolidace a převod měny

[!include [banner](../includes/banner.md)]

Toto téma vás provede přístupem, který používají aplikace Microsoft Dynamics 365 for Finance and Operations a finanční výkaznictví ke konsolidaci. Popisuje scénáře, které zahrnují výkaznictví několika společností, agregace, eliminaci a minoritní podíl. Také vysvětluje, jak postupovat v určitých situacích, jako jsou například scénáře, kdy mají právnické osoby jiná fiskálního období nebo jiné účtové osnovy.

Toto téma bylo napsáno pro uživatele a funkční konzultanty a předpokládá, že čtenáři mají obecné znalosti aplikace Finance and Operations a finančního výkaznictví. Základní nastavení není zmíněno.

> [!NOTE]
> Termín *právnická osoba* se používá v aplikaci Finance and Operations a termín *společnost* se používá ve finančním výkaznictví. V tomto tématu se používají oba termíny. Pro účely tohoto tématu je však jejich význam stejný.

## <a name="audience"></a>Cílová skupina
Toto téma je určeno pro uživatele financí a účetnictví a aplikační konzultanty, kteří chtějí použít Finance and Operations a finanční výkaznictví pro konsolidaci více společností a dat více měn.

## <a name="approach"></a>Přístup
Finance and Operations používá ke zpracování konsolidace samostatnou právnickou osobu. Umožňuje konsolidace s jednou instancí, ale umožňuje přenést data z jiných zdrojů. Proces konsolidace musí být spuštěn pokaždé, když jsou ve zdrojových právnických osobách provedeny změny.

Finanční výkaznictví může konsolidovat více společností při generování sestavy. Ačkoliv jsou data uložena v datovém tržišti, jsou verzována a lze je exportovat, každá zdrojová společnost je vlastníkem a kontejnerem dat. Sestavu lze spouštět kdykoliv, i každou minutu (například). To poskytuje mnoho dalších výhod, například možnost přechodu na podrobnosti všech společností a dimenzí.

Uživatelé mohou použít konsolidaci online, finanční výkaznictví nebo kombinaci obou. Jejich volba závisí na potřebách jejich společnosti a preferencích jejich auditorů.

## <a name="consolidations"></a>Konsolidace
Modul **Konsolidace** zahrnuje možnosti pro konsolidaci více právnických osob během procesu konsolidace a pro import nebo export zůstatku společnosti. Lze také nastavit eliminace a zaúčtovat deníky eliminací.

## <a name="benefits-of-using-consolidate-online"></a>Výhody používání konsolidace online
Zákazníci, kteří používají modul **Konsolidace** získají různé výhody:

- **Hloubka dat** – Můžete vytvářet konsolidované sestavy, které spojí skutečná a rozpočtová data na úrovni účtu a na úrovni dimenzí.
- **Dynamické konsolidace** – Konsolidace lze zpracovat více než jednou.
- **Možnosti auditu** – Dimenze a účty jsou evidovány pro analýzy a audit, a zůstatky jsou vytvářeny podle data.
- **Převod měny** – Můžete nastavit rozsahy účtů a kurzů pro převod ze zúčtovací měny zdrojové společnosti na zúčtovací měnu konsolidační společnosti.
- **Zpracování eliminací v konsolidované společnosti nebo společnosti eliminace** – Můžete zpracovat a zaúčtovat eliminace jako samostatný proces během konsolidace. Případně můžete spustit návrh samostatně.

## <a name="supported-consolidation-scenarios"></a>Podporované scénáře konsolidace
Zde jsou uvedeny některé scénáře konsolidace, které podporuje konsolidace online:

- Jednoúrovňová konsolidace mezi právnickými osobami
- Konsolidace zahrnující eliminace
- Minoritní podíl (v tomto scénáři je třeba použít ruční výpočet a zadání do společnosti.)
- Více účtových osnov mezi právnickými osobami
- Různé fiskální kalendáře mezi více právnickými osobami
- Konsolidace, které obsahují více měn vykazování

## <a name="legal-entity-setup"></a>Nastavení právnické osoby
Před zpracováním konsolidace je nutné nakonfigurovat právnickou osobu. Konsolidaci lze spustit tolikrát, kolikrát budete potřebovat, a všechna data budou převedena z měny účetnictví zdrojové společnosti na měnu, která je definována pro konsolidační společnost. Proto pro následující organizační strukturu, pokud musíte převést všechny severoamerické společnosti nejprve na americké dolary (USD) a poté na eura (EUR), měnu mateřské společnosti, musíte mít alespoň dvě konsolidační společnosti.

![Organizační struktura](./media/organizational-structure.png "Organizační struktura")

V předchozí organizační struktuře musíte mít pro konsolidaci v Severní Americe právnickou osobu, protože konsolidace vždy konsolidují z účetní měny zdrojové společnosti na měnu konsolidační společnosti. V příkladu, pokud jsou všechny společnosti zahrnuty do jediné konsolidace, bude mexická dceřiná společnost převedena z mexických pesos (MXN) na EUR, nikoliv z MXN na USD na EUR.

Když vytvoříte právnickou osobu, můžete specifikovat, zda je společnost použita jak pro konsolidační proces, tak pro proces eliminace, nebo pouze pro jeden z těchto procesů. Na následujícím obrázku se společnost používá pro oba tyto procesy. Všimněte si, že nelze zaúčtovat denní deníky v konsolidované společnosti, ale lze je zaúčtovat ve společnosti eliminace. Proto můžete chtít samostatnou společnost eliminace.

![Právnická osoba, která je použita pro konsolidaci a eliminaci](./media/sep-elimination-company.png "Právnická osoba, která je použita pro konsolidaci a eliminaci")

## <a name="main-accounts-and-consolidation-account-groups"></a>Hlavní účty a skupiny konsolidačních účtů
Jednu volbu, kterou musíte provést, je to, jak chcete konsolidovat svou účtovou osnovu. Během procesu konsolidace existují tři možnosti pro konsolidaci hlavních účtů.

První možností je použití hlavních účtů ze zdrojové společnosti. V takovém případě bude konsolidován každý účet ze všech společností. Například pokud je účet 100000 ve společnosti USMF a účet 1100 ve společnosti DEMF, konsolidační společnost bude zahrnovat oba účty. Jednotlivé účty mají odpovídající zůstatek.

Druhou možností je zadat výchozí konsolidační účet na stránce **Hlavní účty**. Účet bude poté namapován na konsolidační účet. Tato možnost může být užitečná, pokud máte různé účtové osnovy nebo musíte mapovat na osnovu, která je definována ústředím.

![Výchozí konsolidační účet zadaný na stránce Hlavní účty](./media/main-accounts.png "Výchozí konsolidační účet zadaný na stránce Hlavní účty")

Třetí možností je použití skupiny konsolidačních účtů. Můžete definovat tolik skupin konsolidačních účtů, kolik potřebujete. Poté na stránce **Další konsolidační účty** jen namapujete hlavní účet z účetní osnovy na účet, který pro tuto skupinu vyžadujete.

![Mapování na stránce Další konsolidační účty](./media/additional-consolidation-accounts.png "Mapování na stránce Další konsolidační účty")

## <a name="consolidating-online"></a>Online konsolidace
Chcete-li získat informace o zadání podrobností online konsolidace, přečtěte si téma [Konsolidace online](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Správa konsolidačních transakcí
Chcete-li zobrazit výsledky konsolidace, máte několik možností:

- Vygenerujte finanční sestavu proti konsolidační společnosti.
- Zkontrolujte stránku se seznamem **Předvaha** v konsolidační společnosti.
- V seznamu transakcí konsolidace na stránce **Konsolidace** zobrazte zůstatky vytvořené podle data pro každou zdrojovou společnost pro každé období.

    ![Konsolidační transakce na stránce Konsolidace](./media/managing-consolidation-transactions.png "Konsolidační transakce na stránce Konsolidace")

Pokud chcete spustit konsolidaci znovu, můžete zpracovat pouze konsolidaci. Případně vyberte nejprve **Odebrat transakce** na stránce **Konsolidace**.

## <a name="consolidate-with-import"></a>Konsolidovat s importem
Konsolidace pomocí funkce importu pracuje stejně jako funkce konsolidace online. Když vyberete právnické osoby, budete procházet zdrojový soubor, který obsahuje data.

## <a name="export-company-balances"></a>Export zůstatků společnosti
Funkce exportu zůstatků společnosti pracuje též stejně jako funkce konsolidace online. Když vyberete právnické osoby, nastavíte cestu k souboru pro výstup.

## <a name="elimination-rules"></a>Pravidla eliminace
Chcete-li eliminovat mezipodnikové transakce, můžete vytvořit pravidlo eliminace. Případně můžete provést ruční zadání eliminace ve společnosti, která je stanovena jako společnost eliminace. Pokud vytvoříte pravidlo eliminace, máte k dispozici dvě možnosti pro metodu eliminace: **Čistá změna** a **Pevná**.

### <a name="set-up-elimination-rules"></a>Nastavení pravidel eliminace
Při nastavování pravidel eliminace v aplikaci Finance and Operations můžete vytvořit finanční dimenzi konkrétně pro účely eliminace. Většina zákazníků nazývá tuto finanční dimenzi **Obchodní partner** nebo podobně. Pokud se rozhodnete nepoužít finanční dimenzi, pak je nutné mít hlavní účty, které jsou použity pro pouze mezipodnikové transakce.

Nastavení pro eliminace naleznete v části **Nastavení** modulu **Konsolidace**. Jakmile zadáte popis pravidla, je třeba vybrat společnost, do které bude deník eliminace zaúčtován. Vybraná společnost by měla mít vybranou volbu **Použít pro proces finanční eliminace** v nastavení právnické osoby.

Můžete podle potřeby nastavit datum, kdy pravidlo eliminace nabude platnosti, a datum jeho vypršení. Musíte nastavit volbu **Aktivní** na **Ano**, pokud chcete, aby bylo pravidlo eliminace k dispozici v procesu návrhu eliminace. Vyberte název deníku typu **Eliminace**.

![Základní vlastnosti pravidla eliminace](./media/ledger-elimination-rule-journal.png "Základní vlastnosti pravidla eliminace")

Po definování základních vlastností zvolte **Řádky** pro definování skutečných pravidel zpracování. Existují dvě možnosti pro eliminace: eliminace změny čisté částky nebo určení pevné částky.

Vyberte zdrojové účty. Jako zástupný znak můžete použít hvězdičku (\*). Například hodnota **1\*** zvolí jako zdroj dat pro přidělení všechny účty začínající číslem **1**.

Po výběru zdrojových účtů použijte pole **Specifikace účtu** pro určení účtu, který se používá z cílové společnosti. Vyberte **Zdroj**, pokud chcete použít stejný hlavní účet definovaný ve zdrojovém účtu. Vyberete-li možnost **Definováno uživatelem**, je nutné zadat cílový účet.

![Stránka s řádkem pravidla eliminace hlavní knihy](./media/ledger-elimination-rule-line.png "Stránka s řádkem pravidla eliminace hlavní knihy")

Pole **Specifikace dimenze** funguje jako pole **Specifikace účtu**. Vyberte **Zdroj** pro použití stejné dimenze v cílové společnosti a ve zdrojové společnosti. Vyberete-li **Definováno uživatelem**, je třeba určit dimenze v cílové společnosti volbou **Cílové dimenze**. Pak vyberte zdrojové dimenze, finanční dimenze a hodnoty, které slouží jako zdroj eliminace.

### <a name="process-elimination-transactions"></a>Zpracování eliminační transakce
Existují dva způsoby ke zpracování transakcí eliminací. Transakci lze zpracovat během procesu online konsolidace nebo můžete vytvořit deník eliminace a spustit proces návrhu eliminace. Tato část se zaměřuje na druhou možnost.

Ve společnosti určené jako společnost eliminace vyberte možnost **Deník eliminace** v modulu **Konsolidace**. Po vybrání názvu deníku zvolte **Řádky**. Chcete-li spustit návrh, zvolte **Návrhy** \> **Návrh eliminace**.

Vyberte společnost, která je zdrojem konsolidovaných dat, a pak vyberte pravidlo pro zpracování. Zadejte počáteční a koncové datum pro definování rozsahu dat, ve kterém se vyhledávají částky eliminace. Pole **Datum zaúčtování do hlavní knihy** určuje datum použité pro zaúčtování deníku do hlavní knihy. Po zvolení **OK** můžete zkontrolovat částky a zaúčtovat deník.

> [!NOTE]
> Deník eliminace zobrazuje částky pro hodnoty účtu v měně původních transakcí, nikoliv v zúčtovací měně. Při kontrole částek v deníku eliminace může být toto chování matoucí.

Další informace a příklady naleznete v tématu [Pravidla eliminace](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Přecenění měny v konsolidační společnosti
Při konsolidaci dat z jedné zúčtovací měny na jinou musíte spustit přecenění měny, pokud dojde ke změně směnných kurzů, aby byly správně přehodnoceny zůstatky účtů. Při původní konsolidaci data použijte kartu **Převod měny** k výběru počátečních směnných kurzů, které mají být použity pro převod při procesu konsolidace. Po zadání nového směnného kurzu (např. v dalším měsíci) je nutné přecenění zůstatků účtů. Nerealizované zisky nebo ztráty jsou pak aktualizovány na základě nového směnného kurzu a data.

Další informace o přecenění měny v konsolidační společnosti naleznete v tématu [Přecenění měny v konsolidační společnosti](currency-revaluation-consolidation-company.md).

Další informace o tom, jak funguje přecenění měny v modulu **Hlavní kniha** naleznete v tématu [Přecenění cizí měny pro hlavní knihu](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Doplňkové informace
- Při zpracování konsolidace budou konsolidovány všechny účtovací vrstvy.
- Deníky eliminace lze zaúčtovat pouze na aktuální vrstvě.
- Pouze provozní zůstatky jsou konsolidovány. Z toho vyplývá, že chcete-li zobrazit počáteční zůstatky, musíte stále spustit uzávěrku na konci roku v konsolidační společnosti.
- Můžete zaúčtovat denní deník ve společnosti eliminace, ale nikoliv v konsolidační společnosti.

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Výhody používání finančního výkaznictví pro finanční konsolidace a převod měny, nebo pro doplnění online konsolidace pro konsolidované vykazování
Zákazníci, kteří používají finanční výkaznictví pro finanční konsolidace a převod měny, nebo pro doplnění online konsolidace pro konsolidované vykazování, získají různé výhody:

- **Hloubka dat** – Můžete vytvářet konsolidované sestavy, které spojí skutečná a rozpočtová data na úrovni účtu a na úrovni dimenzí. Pro Finance and Operations tato data zahrnují data z kontroly rozpočtu a plánování rozpočtu.
- **Dynamické konsolidace** – Konsolidace lze provést kdykoli a na kterékoli úrovni v hierarchii organizace.
- **Dokončit možnosti auditu** – Všechny dimenze, účty a podrobnosti transakce jsou evidovány pro analýzy a audit. Kromě toho finanční výkaznictví poskytuje úplný přechod zpět k původní transakci v každé právnické osobě, která je konsolidována.
- **Efektivní převod měny** – Po minimální nastavení v aplikaci Finance and Operations můžete převést všechny sestavy finančního výkaznictví na jakoukoli měnu vykazování, která byla nastavena. Kromě toho můžete nastavit neomezený počet měn vykazování.
- **Zaúčtování eliminací u zdroje** –Lze vytvořit a vytisknout sestavu eliminace pro ověření transakcí eliminace. Potom můžete zaúčtovat všechny nové eliminace jako standardní mezipodnikové transakce. Můžete také použít právnickou osobu eliminace pro jakoukoliv transakci, kterou ve svých právnických osobách nechcete.

## <a name="supported-consolidation-scenarios"></a>Podporované scénáře konsolidace
Zde jsou uvedeny některé scénáře konsolidace, které podporuje finanční výkaznictví:

- Jednoúrovňové a mnohoúrovňové konsolidace mezi právnickými osobami
- Konsolidace, které používají organizační struktury vytvořené právnických osob
- Konsolidace zahrnující eliminace
- Minoritní podíl
- Více účtových osnov mezi právnickými osobami
- Různé fiskální kalendáře mezi více právnickými osobami
- Konsolidace, které obsahují více měn vykazování
- Konsolidace obchodní jednotky

## <a name="generating-consolidated-financial-statements"></a>Generování konsolidovaných finančních výkazů
Další informace o scénářích, kde můžete vygenerovat konsolidační finanční výkazy naleznete v tématu [Generování konsolidovaných finančních výkazů](./generating-consolidated-financial-statements.md).


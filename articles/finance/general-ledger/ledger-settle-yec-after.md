---
title: Funkce Sledování mezi vyrovnáním hlavní knihy po uzávěrce na konci roku
description: Tento článek vysvětluje, jak používat funkci Sledování mezi vyrovnáním hlavní knihy po spuštění procesu uzávěrky hlavní knihy na konci roku.
author: kweekley
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832162"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Funkce Sledování mezi vyrovnáním hlavní knihy po uzávěrce na konci roku

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Příprava funkce Sledování sloužící k vyrovnání hlavní knihy po roční uzávěrce

Hlavní změna funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** (funkce **Sledování**) je, že vyrovnání hlavní knihy nelze provést napříč fiskálními roky. Toto meziroční omezení je relevantní pouze pro vyrovnání hlavní knihy, nikoli pro vyrovnání pohledávek nebo závazků.

Než povolíte funkci **Sledování** , fiskální rok, který projde uzávěrkou na konci roku, nesmí obsahovat žádné transakce hlavní knihy, které jsou vyrovnány napříč fiskálními roky. Přesněji řečeno, všechny transakce, které byly zaúčtovány do fiskálního roku, pro který spouštíte uzávěrku na konci roku, nesmí být vyrovnány s transakcemi, které byly zaúčtovány do jiného fiskálního roku. Transakce mohou být poté znovu vyrovnány s transakcemi v rámci stejného fiskálního roku.

Tento článek popisuje kroky, které jsou nutné k identifikaci, zrušení vyrovnání a opětovnému vyrovnání transakcí, které jsou vyrovnány napříč fiskálními roky. V uvedeném příkladu byl fiskální rok 2022 uzavřen. Důraz je kladen na přípravu transakcí pro vyrovnání hlavní knihy s předstihem před uzávěrkou na konci roku 2023.

## <a name="example-setup"></a>Příklad nastavení

Následující obrázek znázorňuje transakce, které byly zaúčtovány pro hlavní účet 110190. Transakce hlavní knihy v zelené barvě byly vyrovnány ve stejném fiskálním roce a nemusí se měnit. Transakce označené červeně jsou vyrovnány v hlavní knize, ale mají data transakcí v různých fiskálních letech. Tyto transakce musí být identifikovány a možná bude nutné zrušit vyrovnání hlavní knihy.

![Transakce hlavní knihy.](./media/afterYEC1.png)

## <a name="example"></a>Příklad

Pokud chce vaše organizace použít funkci **Sledování** po spuštění uzavření fiskálního roku 2022, postupujte podle těchto kroků.

> [!NOTE]
> Uzávěrka roku 2022 a dřívější fiskální roky se musí opakovat, pouze pokud jsou nové transakce zaúčtovány do fiskálního roku 2022 nebo dříve. Po dokončení následujícího postupu by do roku 2022 neměly být zaúčtovány žádné nové transakce. Proces roční uzávěrky nemusí být znovu spuštěn.
>
> Transakce hlavní knihy, které jsou vyrovnány v průběhu fiskálních let, mohou zůstat vyrovnány hlavní knihou, pokud nejsou vyrovnány s transakcí, která byla zaúčtována do roku 2023 nebo později. Pokud jste například vyrovnali transakce v letech 2019 a 2020, mohou zůstat vyrovnány.

1. Dokončete uzávěrku roku 2022 bez aktivované funkce **Sledování**.
2. Volitelné: Po dokončení uzávěrky na konci roku 2022 povolte funkci **Sledování**. Uzávěrka na konci roku se považuje za dokončenou, když jsou zaúčtovány všechny úpravy a proces uzávěrky na konci roku není znovu spuštěn.

    > [!IMPORTANT]
    > Funkce **Sledování** nesmí být povolena, pokud bude znovu spuštěna uzávěrka za rok 2022. Výhodou aktivace této funkce nyní je, že zabráníte uživatelům vyrovnat transakce hlavní knihy, které byly zaúčtovány do různých fiskálních let.

    Pokud uzávěrka na konci roku není dokončena, stále můžete provést další kroky, aniž byste povolili funkci **Sledování**. Funkci povolíte v pozdějším kroku, jak je uvedeno.

3. Na stránce **Vyrovnání hlavní knihy** identifikujte součet všech transakcí, které jsou vyrovnány za fiskální roky 2022 a 2023. Upozorňujeme, že transakce z roku 2021, které jsou vyrovnány s transakcemi za rok 2022, nejsou relevantní, protože rok 2022 již byl uzavřen. Tyto transakce mohou zůstat vyrovnané.

    1. Zadejte rozsah dat pro celý fiskální rok 2022. Pokud jako fiskální rok používáte kalendářní rok, zadejte například od 1. ledna 2022 do 31. prosince 2022.
    2. V poli **Stav** vyberte možnost **Vyrovnáno**.
    3. Filtrujte vždy pouze jeden hlavní účet.

        - Tyto kroky budete muset opakovat pro každý účet hlavní knihy, u kterého dochází k vyrovnání.
        - Pokud pro vyrovnání hlavní knihy již nejsou nastaveny jiné účty hlavní knihy, možná je budete muset dočasně přidat zpět do nastavení vyrovnání hlavní knihy. Poté proveďte tyto kroky, pokud tyto účty hlavní knihy obsahují transakce v roce 2023, které jsou vyrovnány s transakcemi v roce 2022 nebo dříve.

    4. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Stav** a pak vyberte seskupení podle tohoto sloupce.
    5. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Částka v měně transakce** a pak vyberte celkový součet tohoto sloupce.

        - Pokud jste transakce vyrovnali až v roce 2022, součet bude 0 (nula).
        - Pokud máte transakce, které byly vyrovnány v průběhu fiskálních let, součet nebude 0 (nula).

    6. Zjistěte, které transakce byly vyrovnány mezi lety 2022 a 2023, filtrováním podle hodnoty **Datum vyrovnání**. Pokud filtrujete podle data vyrovnání od 1. ledna 2023 do 31. prosince 2023, získáte celkem 700 USD, což je součet transakcí, které byly vyrovnány v hlavní knize v letech 2022 a 2023.

    ![Celková částka transakcí za rok 2022.](./media/afterYEC2.png)

4. Opakujte krok 3 pro fiskální rok 2023. Celková částka by měla odpovídat 700 USD z roku 2022, protože nebyly vyrovnány žádné transakce z roku 2023 s transakcemi z roku 2024.

    ![Celková částka transakcí za rok 2023.](./media/afterYEC3.png)

5. Pokud jste v kroku 2 povolili funkci **Sledování**, deaktivujte ji, než přejdete ke kroku 6. V dalších krocích stornujete vyrovnání hlavní knihy, které překročilo fiskální roky. Pokud je povolena funkce **Sledování**, nelze vyrovnání hlavní knihy pro fiskální rok 2022 stornovat. Proto musíte před pokračováním tuto funkci vypnout.
6. Po deaktivaci funkce **Sledování** použijte stejné filtry na stránce **Vyrovnání hlavní knihy** ke stornování vyrovnání hlavní knihy podrobných transakcí.

    1. Vraťte se na stránku **Vyrovnání hlavní knihy** a filtrujte data transakcí pro rok 2023. Poté vyhledejte podrobné transakce, které tvoří celkem 700 USD. Filtrování těchto informací nemusí být snadné. Možná budete muset odeslat data do Microsoft Excel , abyste je mohli vyhodnotit.
    2. Až budete mít seznam transakcí, vyberte transakce hlavní knihy na stránce **Vyrovnání hlavní knihy** a vyberte možnost **Označit vybrané**. Nemusíte vidět obě strany transakcí hlavní knihy, které byly vyrovnány. Pokud označíte buď debet, nebo kredit, vše, co má stejnou hodnotu **ID vyrovnání**, bude stornováno, i když hodnota **Označená částka** není **0** (nula).
    3. Výběrem volby **Stornovat označené transakce** stornujete vyrovnání transakcí.

    ![Stornování transakcí.](./media/afterYEC4.png)

7. Zaúčtujte opravu hlavního deníku, abyste rozdělili počáteční zůstatek za rok 2023 na dvě částky: částku, která byla vyrovnána v rámci transakce za fiskální rok 2022 a částka, která ještě nebyla vyrovnána za rok 2023.

    - **Část počátečního zůstatku, která byla vyrovnána za předchozí rok:** První částka je 700 USD na základě součtů, které byly nalezeny a vyrovnány v letech 2022 a 2023.
    - **Část počátečního zůstatku, která nebyla vyrovnána za předchozí rok:** Druhá částka je rozdíl mezi počátečním zůstatkem a první částkou 525 USD. Zbývající částka je 1700 USD − 700 USD = 1000 USD.

    Tímto způsobem můžete vyrovnat transakce z roku 2023 o částku 700 USD, která byla původně vyrovnána s transakcí z roku 2022. Tento krok je povinný, protože vyrovnání hlavní knihy neumožňuje částečné vyrovnání.

    1. Přejděte do hlavního deníku a zaúčtujte úpravu. Vaše organizace se bude muset rozhodnout, jaké datum transakce použije, na základě otevřených období v roce 2023.
    2. Možná budete muset dočasně vypnout parametr **Nepovolit ruční zadávání** na stránce **Hlavní účet**. Tato úprava nebude zaúčtována, pokud hlavní účet neumožňuje ruční zadání.

    ![Nezaúčtovaná úprava.](./media/afterYEC5.png)

8. Nyní můžete znovu vyrovnat nevyrovnané transakce. Vraťte se na stránku **Vyrovnání hlavní knihy** a omezte rozsah dat od 1. ledna 2022 do 31. prosince 2022. Následující obrázek znázorňuje nevyrovnané transakce, které nyní existují:

    ![Nevyrovnané transakce.](./media/afterYEC6.png)

    - Počáteční zůstatek 1700 USD lze vyrovnat úpravou -1700 USD.
    - Podrobné transakce, které nebyly vyrovnány, za -700 USD, lze vyrovnat úpravou 700 USD.

9. Opět povolte funkci **Sledování**.
10. Po povolení funkce **Sledování** nelze provést vyrovnání hlavní knihy napříč fiskálními roky. Možná budete muset zbývající zůstatek 1000 USD dále rozdělit na menší částky, než budete moci vyrovnat nové transakce v roce 2023. Někteří zákazníci se mohou rozhodnou zveřejnit tento detail během kroku 8, kde se 1000 USD dále dělí tak, aby představoval nevyrovnané transakce z roku 2022. Tento přístup v podstatě napodobuje to, co funkce **Sledování** dělá pouze pro aktuální rok. Příští rok to bude automaticky provedeno pomocí nastavení **Zachovat podrobnosti** v nastavení vyrovnání hlavní knihy.

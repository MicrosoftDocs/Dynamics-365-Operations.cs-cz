---
title: Funkce Sledování mezi vyrovnáním hlavní knihy před roční uzávěrkou
description: Tento článek vysvětluje, jak používat funkci Sledování mezi vyrovnáními hlavní knihy před spuštěním procesu uzávěrky hlavní knihy na konci roku.
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
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832155"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Funkce Sledování mezi vyrovnáním hlavní knihy před uzávěrkou na konci roku

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Příprava funkce Sledování sloužící k vyrovnání hlavní knihy před roční uzávěrkou

Hlavní změna funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** (funkce **Sledování**) je, že vyrovnání hlavní knihy nelze provést napříč fiskálními roky. Toto meziroční omezení je relevantní pouze pro vyrovnání hlavní knihy, nikoli pro vyrovnání pohledávek nebo závazků.

Než povolíte funkci **Sledování** , fiskální rok, který projde uzávěrkou na konci roku, nesmí obsahovat žádné transakce hlavní knihy, které jsou vyrovnány napříč fiskálními roky. Přesněji řečeno, všechny transakce, které byly zaúčtovány do fiskálního roku, pro který spouštíte uzávěrku na konci roku, nesmí být vyrovnány s transakcemi, které byly zaúčtovány do jiného fiskálního roku. Transakce mohou být poté znovu vyrovnány s transakcemi v rámci stejného fiskálního roku.

Tento článek popisuje kroky, které jsou nutné k identifikaci, zrušení vyrovnání a opětovnému vyrovnání transakcí, které jsou vyrovnány napříč fiskálními roky. V uvedeném příkladu byl fiskální rok 2021 uzavřen a vy se připravujete na uzávěrku pro fiskální rok 2022.

## <a name="example-setup"></a>Příklad nastavení

Následující obrázek znázorňuje transakce, které byly zaúčtovány pro hlavní účet 110190. Transakce hlavní knihy v zelené barvě byly vyrovnány ve stejném fiskálním roce a nemusí se měnit. Transakce označené červeně jsou vyrovnány v hlavní knize, ale mají data transakcí v různých fiskálních letech. Tyto transakce musí být identifikovány a možná bude nutné zrušit vyrovnání hlavní knihy.

![Transakce hlavní knihy.](./media/YEC1.png)

## <a name="example"></a>Příklad

Pokud chce vaše organizace použít funkci **Sledování** před spuštěním uzavření fiskálního roku 2022, postupujte podle těchto kroků.

> [!NOTE]
> Uzávěrka roku 2021 a dřívější fiskální roky se musí opakovat, pouze pokud jsou nové transakce zaúčtovány do fiskálního roku 2021 nebo dříve. Po dokončení následujícího postupu nebudou do roku 2021 zaúčtovány žádné nové transakce. Proces roční uzávěrky nemusí být znovu spuštěn.
>
> Transakce hlavní knihy, které jsou vyrovnány v průběhu fiskálních let, mohou zůstat vyrovnány hlavní knihou, pokud nejsou vyrovnány s transakcí, která byla zaúčtována do roku 2022 nebo později. Pokud jste například vyrovnali transakce v letech 2019 a 2020, mohou zůstat vyrovnány.

1. Volitelné: Dočasně povolte funkci **Sledování**.

    - Pokud se rozhodnete funkci povolit, budete ji muset deaktivovat v pozdějších krocích, jak je dále uvedeno. Výhodou aktivace této funkce nyní je, že dočasně zabráníte uživatelům vyrovnat transakce hlavní knihy, které byly zaúčtovány do různých fiskálních let.
    - Pokud se rozhodnete funkci nepovolit, doporučujeme požádat svůj tým, aby nevyrovnával transakce napříč fiskálními roky. Pokud dojde k meziročnímu vyrovnání po dokončení následujících kroků, budete muset kroky zopakovat, abyste identifikovali a zrušili vyrovnání těchto transakcí hlavní knihy.

2. Na stránce **Vyrovnání hlavní knihy** identifikujte součet všech transakcí, které jsou vyrovnány za fiskální roky 2021 a 2022.

    1. Zadejte rozsah dat pro celý fiskální rok 2021. Pokud jako fiskální rok používáte kalendářní rok, zadejte například od 1. ledna 2021 do 31. prosince 2021.

        Pokud je povolena funkce **Sledování**, zobrazí se upozornění, že transakce nelze vyrovnat nebo zrušit jejich vyrovnání pro uzavřený fiskální rok. Upozornění není relevantní, protože v tomto kroku nedochází k žádnému vyrovnání ani zrušení vyrovnání.

    2. V poli **Stav** vyberte možnost **Vyrovnáno**.
    3. Filtrujte vždy pouze jeden hlavní účet.

        - Tyto kroky budete muset opakovat pro každý účet hlavní knihy, u kterého dochází k vyrovnání.
        - Pokud pro vyrovnání hlavní knihy již nejsou nastaveny jiné účty hlavní knihy, možná je budete muset dočasně přidat zpět do nastavení vyrovnání hlavní knihy. Poté proveďte tyto kroky, pokud tyto účty hlavní knihy obsahují transakce v roce 2022, které jsou vyrovnány s transakcemi v jiném fiskálním roce.

    4. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Stav** a pak vyberte seskupení podle tohoto sloupce.
    5. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Částka v měně transakce** a pak vyberte celkový součet tohoto sloupce.

        - Pokud jste transakce vyrovnali až v roce 2021, součet bude 0 (nula).
        - Pokud máte transakce, které byly vyrovnány v průběhu fiskálních let, součet nebude 0 (nula).

        Na následujícím obrázku je zůstatek 525 USD. Tento zůstatek je součtem transakcí, které byly vyrovnány s transakcemi v jiném fiskálním roce. Váš součet může zahrnovat transakce, které byly vyrovnány mezi lety 2021 a 2022, a transakce, které byly vyrovnány mezi lety 2022 a 2023.

        ![Transakce hlavní knihy za roky 2021–2022.](./media/YEC2.png)

    6. Zjistěte, které transakce byly vyrovnány mezi lety 2020 a 2021, dalším filtrováním podle hodnoty **Datum vyrovnání**. Zadejte filtr časového období od 1. ledna 2021 do 31. prosince 2021. Nejsou zobrazeny žádné transakce, protože nebyly vyrovnány žádné transakce za rok 2020 s transakcemi zaúčtovanými do roku 2021.
    7. Zjistěte, které transakce byly vyrovnány mezi lety 2021 a 2022 změnou filtru data hodnoty **Datum vyrovnání**. Zadejte filtr časového období od 1. ledna 2022 do 31. prosince 2022. Transakce se znovu zobrazí a součet je 525 USD, protože všechny transakce byly vyrovnány v letech 2021 až 2022.

3. Na stránce **Vyrovnání hlavní knihy** identifikujte součet všech transakcí, které jsou vyrovnány za fiskální roky 2021 a 2022.

    1. Zadejte rozsah dat pro celý fiskální rok 2022. Pokud jako fiskální rok používáte kalendářní rok, zadejte například od 1. ledna 2022 do 31. prosince 2022.
    2. V poli **Stav** vyberte možnost **Vyrovnáno**.
    3. Filtrujte vždy pouze jeden hlavní účet.
    4. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Stav** a pak vyberte seskupení podle tohoto sloupce.
    5. Vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Částka v měně transakce** a pak vyberte celkový součet tohoto sloupce.

        ![Celkové částky transakce hlavní knihy.](./media/YEC3.png)

    6. Přidejte další filtr na hodnotu **Datum vyrovnání**. Zadejte filtr časového období od 1. ledna 2022 do 31. prosince 2022. Je zobrazen stejný součet 525 USD. Tento výsledek potvrzuje, že celkový počet transakcí vyrovnaných v letech 2021 a 2022 je 525 USD.

        ![Transakce hlavní knihy pro data vyrovnání v letech 2022 a 2023.](./media/YEC4.png)

    7. Změňte další filtr na hodnotě **Datum vyrovnání**. Zadejte filtr časového období od 1. ledna 2023 do 31. prosince 2023. Je zobrazen nový součet 700 USD. Tento součet představuje celkovou částku transakcí, které byly vyrovnány v letech 2022 a 2023.
 
4. Opakujte krok 3 pro fiskální rok 2023. Celková částka by měla odpovídat 700 USD z roku 2022, protože nebyly vyrovnány žádné transakce z roku 2023 s transakcemi z roku 2024.
5. Pokud jste v kroku 1 povolili funkci **Sledování**, deaktivujte ji, než přejdete ke kroku 6. V dalších krocích stornujete vyrovnání hlavní knihy, které překročilo fiskální roky. Pokud je povolena funkce **Sledování**, nelze vyrovnání hlavní knihy pro fiskální rok 2021 stornovat. Proto musíte před pokračováním tuto funkci vypnout.
6. Po deaktivaci funkce **Sledování** použijte stejné filtry na stránce **Vyrovnání hlavní knihy** ke stornování vyrovnání hlavní knihy podrobných transakcí.

    1. Vraťte se na stránku **Vyrovnání hlavní knihy** a filtrujte data transakcí pro rok 2021. Přidejte další filtr na hodnotu **Datum vyrovnání**. Zadejte filtr časového období od 1. ledna 2022 do 31. prosince 2022. Poté vyhledejte podrobné transakce, které tvoří celkem 525 USD. Filtrování těchto informací nemusí být snadné. Možná budete muset odeslat data do Microsoft Excel , abyste je mohli vyhodnotit.
    2. Až budete mít seznam transakcí, vyberte transakce hlavní knihy na stránce **Vyrovnání hlavní knihy** a vyberte možnost **Označit vybrané**. Nemusíte vidět obě strany transakcí hlavní knihy, které byly vyrovnány. Pokud označíte buď debet, nebo kredit, vše, co má stejnou hodnotu **ID vyrovnání**, bude stornováno, i když hodnota **Označená částka** není **0** (nula).
    3. Výběrem volby **Stornovat označené transakce** stornujete vyrovnání transakcí.

    ![Storno označených transakcí.](./media/YEC5.png)

7. Opakujte krok 6 pro storno vyrovnání transakcí, které byly vyrovnány v letech 2022 a 2023.

    ![Storno transakcí hlavní knihy.](./media/YEC6.png)

8. Zaúčtujte opravu hlavního deníku, abyste rozdělili počáteční zůstatek za rok 2022 na dvě částky: částku, která byla vyrovnána v rámci transakce za fiskální rok 2021 a částka, která ještě nebyla vyrovnána za rok 2022.

    - **Část počátečního zůstatku, která byla vyrovnána za předchozí rok:** První částka je 525 USD na základě součtů, které byly nalezeny a vyrovnány v letech 2021 a 2022.
    - **Část počátečního zůstatku, která nebyla vyrovnána za předchozí rok:** Druhá částka je rozdíl mezi počátečním zůstatkem a vyrovnanou částkou 525 USD. Zbývající částka je 1025 USD − 525 USD = 500 USD.

    Tímto způsobem můžete vyrovnat transakce z roku 2022 o částku 525 USD, která byla původně vyrovnána s transakcí z roku 2021. Tento krok je povinný, protože vyrovnání hlavní knihy neumožňuje částečné vyrovnání.

    1. Přejděte do hlavního deníku a zaúčtujte úpravu. Vaše organizace se bude muset rozhodnout, jaké datum transakce použije, na základě otevřených období. Tyto transakce mohly být vyrovnány s použitím data vyrovnání v lednu nebo únoru 2022, ale pokud je to jediné otevřené období, úprava může být zaúčtována do prosince.
    2. Možná budete muset dočasně vypnout parametr **Nepovolit ruční zadávání** na stránce **Hlavní účet**. Tato úprava nebude zaúčtována, pokud hlavní účet neumožňuje ruční zadání.

    ![Nezaúčtovaná úprava.](./media/YEC7.png)

9. Nyní můžete znovu vyrovnat nevyrovnané transakce. Vraťte se na stránku **Vyrovnání hlavní knihy** a omezte rozsah dat od 1. ledna 2022 do 31. prosince 2022. Následující obrázek znázorňuje nevyrovnané transakce, které nyní existují:

    ![Nevyrovnané transakce.](./media/YEC8.png)

    - Počáteční zůstatek 1025 USD lze vyrovnat úpravou -1 025 USD.
    - Podrobné transakce, které nebyly vyrovnány, za -400 USD, -50 USD a -75 USD, lze vyrovnat úpravou 525 USD.

    ![Podrobné transakce.](./media/YEC9.png)

10. Povolte funkci **Sledování**. Nyní jste připraveni na spuštění roční uzávěrku.

    - Než spustíte roční uzávěrku, zvažte výběr možnosti **Zachovat podrobnosti** pro všechny rozvahové účty v nastavení vyrovnání hlavní knihy. Další informace o výhodách provedení tohoto kroku naleznete v dokumentu Sledování.
    - Když zahájíte uzávěrku za rok 2022 a stále budou nalezeny transakce vyrovnané napříč fiskálními roky, proces roční uzávěrky vás okamžitě upozorní.
    - Pokud jsou transakce z roku 2021 a 2022 stále vyrovnány, budete muset znovu deaktivovat funkci **Sledování** a zopakovat předchozí kroky, abyste zrušili vyrovnání těchto transakcí. Tento přístup je nutný, protože rok 2021 je uzavřen a u transakcí v uzavřeném fiskálním roce nelze zrušit vyrovnání.
    - Pokud jsou transakce z roku 2022 a 2023 stále vyrovnány, **nemusíte** deaktivovat funkci **Sledování**. Vzhledem k tomu, že rok 2022 ani 2023 není uzavřen, můžete použít předchozí kroky k zrušení vyrovnání transakcí.

Po úspěšném spuštění uzávěrky za rok 2022 můžete od této chvíle ponechat funkci **Sledování** povolenu.

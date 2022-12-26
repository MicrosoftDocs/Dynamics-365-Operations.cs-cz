---
title: Sledování mezi funkcí vyrovnání hlavní knihy po roční uzávěrce pomocí stránky s dotazem
description: Tento článek vysvětluje, jak používat funkci Sledování mezi vyrovnáním hlavní knihy pomocí nové stránky s dotazy po spuštění uzávěrky hlavní knihy na konci roku.
author: kweekley
ms.date: 12/15/2022
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853120"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Sledování mezi funkcí vyrovnání hlavní knihy po roční uzávěrce pomocí stránky s dotazem

Jedna primární změna funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** (funkce **Sledování**) je, že vyrovnání hlavní knihy nelze provést napříč fiskálními roky. Toto meziroční omezení je relevantní pouze pro vyrovnání hlavní knihy, nikoli pro vyrovnání pohledávek nebo závazků.

Než povolíte funkci **Sledování** , fiskální rok, který projde uzávěrkou na konci roku, nesmí obsahovat žádné transakce hlavní knihy, které jsou vyrovnány napříč fiskálními roky. Přesněji řečeno, všechny transakce, které byly zaúčtovány do fiskálního roku, pro který spouštíte uzávěrku na konci roku, nesmí být vyrovnány s transakcemi, které byly zaúčtovány do jiného fiskálního roku. Transakce mohou být poté znovu vyrovnány s transakcemi v rámci stejného fiskálního roku.

Tento článek popisuje kroky, které jsou nutné k identifikaci, zrušení vyrovnání a opětovného vyrovnání transakcí, které jsou vyrovnány napříč roky. V uvedeném příkladu byl fiskální rok 2022 uzavřen. Důraz je kladen na přípravu transakcí pro vyrovnání hlavní knihy před uzávěrkou na konci roku 2023.

Od verze Microsoft Dynamics 365 Finance 10.0.29 můžete identifikovat, zrušit a znovu vyrovnat transakce hlavní knihy pomocí nové stránky s dotazy, která je k dispozici. Pokud aktuálně nepoužíváte Microsoft Dynamics 365 Finance vydání 10.0.29 nebo novější, můžete najít kroky pro identifikaci, zrušení vyrovnání a opětovné vyrovnání transakcí hlavní knihy v následujících článcích:

- [Funkce Sledování mezi vyrovnáním hlavní knihy před uzávěrkou na konci roku](ledger-settle-yec.md)
- [Funkce Sledování mezi vyrovnáním hlavní knihy po uzávěrce na konci roku](ledger-settle-yec-after.md)

Další informace o novém okně dotazu naleznete v části [Dotaz na vyrovnání hlavní knihy](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Příklad nastavení

Následující obrázek znázorňuje transakce, které byly zaúčtovány pro hlavní účet 110200. Transakce v zelené barvě byly vyrovnány ve stejném fiskálním roce a nemusí se měnit. Transakce označené červeně byly vyrovnány v hlavní knize, ale mají data transakcí v různých fiskálních letech. Tyto transakce musí být identifikovány a možná bude nutné zrušit vyrovnání hlavní knihy.

![Zaúčtované transakce hlavní knihy.](./media/excel.png)

## <a name="example"></a>Příklad

Pokud chce vaše organizace použít funkci **Sledování** po spuštění uzavření fiskálního roku 2022, postupujte podle těchto kroků.

> [!NOTE]
> Uzávěrka roku 2022 a dřívější fiskální roky se musí opakovat, pouze pokud jsou nové transakce zaúčtovány do fiskálního roku 2022 nebo dříve. Po dokončení následujícího postupu nebudou do roku 2022 zaúčtovány žádné nové transakce. Proces roční uzávěrky nemusí být znovu spuštěn.
>
> Transakce hlavní knihy, které jsou vyrovnány v průběhu fiskálních let, mohou zůstat vyrovnány hlavní knihou, pokud nejsou vyrovnány s transakcí, která byla zaúčtována do roku 2022 nebo později. Pokud jste například vyrovnali transakce v letech 2019 a 2020, mohou zůstat vyrovnány.

1. Dokončete uzávěrku roku 2022 bez aktivované funkce **Sledování**.
2. Identifikujte všechny transakce, které byly zaúčtovány do jiných fiskálních let, ale byly vyrovnány s transakcemi, které byly zaúčtovány do roku 2023 (následující fiskální rok, který bude uzavřen).

    > [!NOTE]
    > Transakce z roku 2021, které byly vyrovnány s transakcemi za rok 2022, nejsou relevantní, protože tento rok již byl uzavřen za rok 2022. Tyto transakce mohou zůstat vyrovnané.

    1. Na stránce **Vyrovnání hlavní knihy** vyberte **Kontrola meziročních vyrovnání**.
    2. Vyberte fiskální rok 2023, což je následující rok, pro který chcete spustit proces roční uzávěrky.
    3. Výběrem hodnoty v poli **Sada finančních dimenzí** zobrazíte finanční dimenze, které chcete zobrazit pro účet hlavní knihy. Hlavní účet je zobrazen vždy, i když vybraná sada dimenzí neobsahuje hlavní účet.
    4. Vyberte **Zobrazit transakce**.

    Stránka s dotazy zobrazí všechny transakce z ostatních fiskálních let, které jsou vyrovnány s transakcemi, které byly zaúčtovány v roce 2023.

    ![Meziroční vyrovnání k roku 2023.](./media/2023-cross-settlement.png)

3. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Exportovat všechny řádky**. Tyto řádky jsou všechny transakce, jejichž vyrovnání musí být zrušeno pro rok 2022, než bude možné spustit uzávěrku na konci roku pro následující rok (2023). Chcete záznam těchto transakcí.

    Po exportu všech podrobných transakcí z let 2022 do Excelu jste připraveni zrušit vyrovnání transakcí pomocí stránky s dotazy.

4. Vyberte všechny záznamy v mřížce a poté vyberte **Zrušit vyrovnání označených záznamů**. U všech vybraných transakcí v mřížce bude zrušeno vyrovnání.

    Jsou zobrazeny dvě varovné zprávy, aby bylo zajištěno, že podrobnosti transakce budou exportovány do aplikace Excel předtím, než dojde k vyrovnání transakcí. Pokud omylem zrušíte vyrovnání transakcí hlavní knihy před odesláním podrobností do Excelu, neexistuje způsob, jak zrušení vyrovnání zvrátit.

    ![Zrušení meziročních vyrovnání.](./media/revert-settlement.png)

5. Použijte data Excelu k nalezení celkové částky transakcí v roce 2022, které byly vyrovnány s transakcemi v roce 2023. V tomto příkladu to jsou transakce v roce 2023 ve výši 700 USD.
6. Zaúčtujte opravu hlavního deníku, abyste rozdělili počáteční zůstatek za rok 2022 na dvě částky: částku, která byla vyrovnána s transakcemi za fiskální rok 2022 a částka, která ještě nebyla vyrovnána za rok 2023.

    - **Část počátečního zůstatku, která byla vyrovnána za předchozí rok:** První částka je 700 USD na základě součtů, které byly nalezeny a vyrovnány v letech 2021 a 2022.
    - **Část počátečního zůstatku, která nebyla vyrovnána za předchozí rok:** Druhá částka je rozdíl mezi počátečním zůstatkem a vyrovnanou částkou 700 USD. Zbývající částka je 1700 USD − 700 USD = 1000 USD.

    Tímto způsobem můžete vyrovnat transakce z roku 2023 o částku 700 USD, která byla původně vyrovnána s transakcí z roku 2022. Tento krok je povinný, protože vyrovnání hlavní knihy neumožňuje částečné vyrovnání.

    1. Přejděte do hlavního deníku a zaúčtujte úpravu. Vaše organizace se bude muset rozhodnout, jaké datum transakce použije, na základě otevřených období v roce 2023.
    2. Možná budete muset dočasně vypnout parametr **Nepovolit ruční zadávání** na stránce **Hlavní účet**. Tato úprava nebude zaúčtována, pokud hlavní účet neumožňuje ruční zadání.

    ![Zaúčtování opravy hlavního deníku.](./media/no-manual4.png)

7. Nyní můžete znovu vyrovnat nevyrovnané transakce. Vraťte se na stránku **Vyrovnání hlavní knihy** a omezte rozsah dat od 1. ledna do 31. prosince 2023. Poté pomocí podrobných transakcí, které jste exportovali do Excelu, vyhledejte konkrétní transakce, které je třeba znovu vyrovnat. Následující obrázek znázorňuje nevyrovnané transakce, které nyní existují:

    ![Nevyrovnané transakce za rok 2023.](./media/2023-unsettled5.png)

    - Počáteční zůstatek 1700 USD lze vyrovnat úpravou -1700 USD.
    - Podrobné transakce, které nebyly vyrovnány, za -700 USD, lze vyrovnat úpravou 700 USD.

8. Povolte funkci **Sledování**. Nyní jste připraveni na spuštění roční uzávěrku.

    - Než spustíte roční uzávěrku pro rok 2023, zvažte výběr možnosti **Zachovat podrobnosti** pro všechny rozvahové účty v nastavení vyrovnání hlavní knihy. Další informace viz [Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku](awareness-between-ledger-settlement-year-end-close.md).
    - Když zahájíte uzávěrku za rok 2023 a stále budou nalezeny transakce vyrovnané napříč fiskálními roky, proces roční uzávěrky vás okamžitě upozorní. K této situaci může dojít, pokud uživatelé vyrovnali transakce v průběhu fiskálních let před aktivací funkce **Sledování**.
    - Pokud jsou transakce z roku 2022 a 2023 stále vyrovnány, budete muset znovu deaktivovat funkci **Sledování** a poté zopakovat předchozí kroky, abyste zrušili vyrovnání těchto transakcí. Tento přístup je nutný, protože rok 2022 je uzavřen a u transakcí v uzavřeném fiskálním roce nelze zrušit vyrovnání.

Po úspěšném spuštění uzávěrky za rok 2022 můžete od této chvíle ponechat funkci **Sledování** povolenu.

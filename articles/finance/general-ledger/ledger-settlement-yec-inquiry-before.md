---
title: Funkce Sledování mezi vyrovnáním hlavní knihy před uzávěrkou na konci roku pomocí stránky s dotazy
description: Tento článek vysvětluje, jak používat funkci Sledování mezi vyrovnáním hlavní knihy pomocí nové stránky s dotazy před spuštěním uzávěrky hlavní knihy na konci roku.
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
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853123"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Funkce Sledování mezi vyrovnáním hlavní knihy před uzávěrkou na konci roku pomocí stránky s dotazy

Jedna primární změna funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** (funkce **Sledování**) je, že vyrovnání hlavní knihy nelze provést napříč fiskálními roky. Toto meziroční omezení je relevantní pouze pro vyrovnání hlavní knihy, nikoli pro vyrovnání pohledávek nebo závazků.

Než povolíte funkci **Sledování** , fiskální rok, který projde uzávěrkou na konci roku, nesmí obsahovat žádné transakce hlavní knihy, které jsou vyrovnány napříč fiskálními roky. Přesněji řečeno, všechny transakce, které byly zaúčtovány do fiskálního roku, pro který spouštíte uzávěrku na konci roku, nesmí být vyrovnány s transakcemi, které byly zaúčtovány do jiného fiskálního roku. Transakce mohou být poté znovu vyrovnány s transakcemi v rámci stejného fiskálního roku.

Tento článek popisuje kroky, které jsou nutné k identifikaci, zrušení vyrovnání a opětovného vyrovnání transakcí, které jsou vyrovnány napříč fiskálními roky. V uvedeném příkladu byl fiskální rok 2021 uzavřen a vy se připravujete na uzávěrku pro fiskální rok 2022.

Od verze Microsoft Dynamics 365 Finance 10.0.29 můžete identifikovat, zrušit a znovu vyrovnat transakce hlavní knihy pomocí nové stránky s dotazy, která je k dispozici. Pokud aktuálně nepoužíváte Finance vydání 10.0.29 nebo novější, můžete najít kroky pro identifikaci, zrušení vyrovnání a opětovné vyrovnání transakcí hlavní knihy v následujících článcích:

- [Funkce Sledování mezi vyrovnáním hlavní knihy před uzávěrkou na konci roku](ledger-settle-yec.md)
- [Funkce Sledování mezi vyrovnáním hlavní knihy po uzávěrce na konci roku](ledger-settle-yec-after.md)

Další informace o novém okně dotazu naleznete v části [Dotaz na vyrovnání hlavní knihy](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Příklad nastavení

Následující obrázek znázorňuje transakce, které byly zaúčtovány pro hlavní účet 110200. Transakce v zelené barvě byly vyrovnány ve stejném fiskálním roce a nemusí se měnit. Transakce označené červeně byly vyrovnány v hlavní knize, ale mají data transakcí v různých fiskálních letech. Tyto transakce musí být identifikovány a možná bude nutné zrušit vyrovnání hlavní knihy.

![Zaúčtované transakce hlavní knihy.](./media/ledgersettlement.png)

## <a name="example"></a>Příklad

Pokud chce vaše organizace použít funkci **Sledování** před uzavřením fiskálního roku 2022, postupujte podle těchto kroků.

> [!NOTE]
> Uzávěrka roku 2021 a dřívější fiskální roky se musí opakovat, pouze pokud jsou nové transakce zaúčtovány do fiskálního roku 2021 nebo dříve. Po dokončení následujícího postupu nebudou do roku 2021 zaúčtovány žádné nové transakce. Proces roční uzávěrky nemusí být znovu spuštěn.
>
> Transakce hlavní knihy, které jsou vyrovnány v průběhu fiskálních let, mohou zůstat vyrovnány hlavní knihou, pokud nejsou vyrovnány s transakcí, která byla zaúčtována do roku 2022 (rok, který se uzavírá) nebo později. Pokud jste například vyrovnali transakce v letech 2019 a 2020, mohou zůstat vyrovnány.

1. **Neaktivujte** funkci **Sledování**.
2. Na stránce **Vyrovnání hlavní knihy** vyberte **Kontrola meziročních vyrovnání**.
3. Identifikujte všechny transakce, které byly zaúčtovány do jiných fiskálních let, ale byly vyrovnány s transakcemi, které byly zaúčtovány do roku 2022.

    1. Vyberte fiskální rok 2022, pro který chcete spustit proces roční uzávěrky.
    2. Výběrem hodnoty v poli **Sada finančních dimenzí** zobrazíte finanční dimenze, které chcete zobrazit pro účet hlavní knihy. Hlavní účet je zobrazen vždy, i když vybraná sada dimenzí neobsahuje hlavní účet.
    3. Vyberte **Zobrazit transakce**.

    Stránka s dotazy zobrazí všechny transakce pro všechny účty hlavní knihy (i když již nejsou v nastavení vyrovnání hlavní knihy) ze všech ostatních fiskálních let, které jsou vyrovnány s transakcemi zaúčtovanými do roku 2022. Jsou zobrazeny tři různé účty hlavní knihy.

    ![Meziroční vyrovnání k roku 2022.](./media/review-cross-year.png)

3. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Exportovat všechny řádky**. Tyto řádky jsou všechny transakce, jejichž vyrovnání musí být zrušeno pro rok 2022, než bude možné spustit uzávěrku na konci roku. Tento podrobný seznam transakcí je potřeba, abyste mohli později správně vyrovnat transakce.
4. Všimněte si fiskálních let, pro které byly tyto transakce zaúčtovány. V tomto příkladu to jsou transakce v letech 2021 a 2023.
5. Na stránce s dotazy změňte fiskální rok na 2021, první fiskální rok, který obsahuje transakce, které byly vyrovnány s transakcemi z roku 2022.
6. Použijte filtr ve sloupci **Datum transakce**, aby byly zahrnuty pouze transakce, které byly zaúčtovány do roku 2022. Tyto transakce jsou podrobné transakce z roku 2022, které byly vyrovnány s transakcemi v roce 2021.
7. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Exportovat všechny řádky**.

    > [!IMPORTANT]
    > V následujících krocích bude vyrovnání těchto transakcí zrušeno a poté budou opětovně vyrovnány jako transakce v roce 2022. Je nezbytné, abyste tento detail zachovali v Excelu.

    ![Meziroční vyrovnání k roku 2021.](./media/review-cross-year.png)

8. Na stránce s dotazy změňte fiskální rok na 2023, další fiskální rok, který obsahuje transakce, které byly vyrovnány s transakcemi z roku 2022. 
9. Použijte filtr ve sloupci **Datum transakce**, aby byly zahrnuty pouze transakce, které byly zaúčtovány do roku 2022. Tyto transakce jsou podrobné transakce z roku 2023, které byly vyrovnány s transakcemi v roce 2022. 
10. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Exportovat všechny řádky**.

    > [!IMPORTANT]
    > V následujících krocích bude vyrovnání těchto transakcí zrušeno a poté budou opětovně vyrovnány jako transakce v roce 2022. Je nezbytné, abyste tento detail zachovali v Excelu.

    ![Meziroční vyrovnání k roku 2023.](./media/filter-transactions.png)

11. Opakujte předchozí kroky pro každý fiskální rok, který obsahuje transakce, které byly vyrovnány s transakcemi v roce 2022. Vždy exportujte podrobné transakce do Excelu.

    Po exportu všech podrobných transakcí z let 2021 a 2023 do Excelu jste připraveni zrušit vyrovnání transakcí pomocí nové stránky s dotazy.

12. Změňte fiskální rok na 2022.
13. Vyberte všechny záznamy v mřížce a poté vyberte **Zrušit vyrovnání označených záznamů**. U všech vybraných transakcí v mřížce bude zrušeno vyrovnání.

    Jsou zobrazeny dvě varovné zprávy, aby bylo zajištěno, že podrobnosti transakce budou exportovány do aplikace Excel předtím, než dojde k vyrovnání transakcí. Pokud omylem zrušíte vyrovnání transakcí hlavní knihy před odesláním podrobností do Excelu, neexistuje způsob, jak zrušení vyrovnání zvrátit.

    ![Zrušení vyrovnání křížově vyrovnaných transakcí.](./media/revert-unsettle.png)

14. Použijte data Excelu k nalezení celkové částky transakcí v roce 2021 a 2023, které byly vyrovnány s transakcemi v roce 2022. V tomto příkladu jsou transakce za rok 2021 celkem za 525 USD a transakce za rok 2023 za celkem 700 USD.
15. Zaúčtujte opravu hlavního deníku, abyste rozdělili počáteční zůstatek za rok 2022 na dvě částky: částku, která byla vyrovnána, do fiskálního roku 2021 a částka, která ještě nebyla vyrovnána, do roku 2022.

    - **Část počátečního zůstatku, která byla vyrovnána za předchozí rok:** První částka je 525 USD na základě součtů, které byly nalezeny a vyrovnány v letech 2021 a 2022.
    - **Část počátečního zůstatku, která nebyla vyrovnána za předchozí rok:** Druhá částka je rozdíl mezi počátečním zůstatkem a vyrovnanou částkou 525 USD. Zbývající částka je 1025 USD − 525 USD = 500 USD.

    Tímto způsobem můžete vyrovnat transakce z roku 2022 o částku 525 USD, která byla původně vyrovnána s transakcí z roku 2021. Tento krok je povinný, protože vyrovnání hlavní knihy neumožňuje částečné vyrovnání.

    1. Přejděte do hlavního deníku a zaúčtujte úpravu. Vaše organizace se bude muset rozhodnout, jaké datum transakce použije, na základě otevřených období. Tyto transakce mohly být vyrovnány s použitím data vyrovnání v lednu nebo únoru 2022, ale pokud je to jediné otevřené období, úprava může být zaúčtována do prosince.
    2. Možná budete muset dočasně vypnout parametr **Nepovolit ruční zadávání** pro účet 110200 na stránce **Hlavní účet**. Tato úprava nebude zaúčtována, pokud hlavní účet neumožňuje ruční zadání.

    ![Zaúčtování opravy hlavního deníku.](./media/not-post.png)

16. Nyní můžete znovu vyrovnat nevyrovnané transakce. Vraťte se na stránku **Vyrovnání hlavní knihy**, zadejte časové období od 1. ledna do 31. prosince 2022 a vyfiltrujte hlavní účet 110200. Poté pomocí podrobných transakcí, které jste exportovali do Excelu, vyhledejte konkrétní transakce, které je třeba znovu vyrovnat. Následující obrázek znázorňuje nevyrovnané transakce, které nyní existují:

    ![Nevyrovnané transakce.](./media/updated-unsettled.png)

    - Počáteční zůstatek 1025 USD lze vyrovnat úpravou -1 025 USD.
    - Podrobné transakce, které nebyly vyrovnány, za -400 USD, -50 USD a -75 USD, lze vyrovnat úpravou 25 USD.

17. Povolte funkci **Sledování**. Nyní jste připraveni na spuštění roční uzávěrku.

    - Než spustíte roční uzávěrku, zvažte výběr možnosti **Zachovat podrobnosti** pro všechny rozvahové účty v nastavení vyrovnání hlavní knihy. Další informace viz [Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku](awareness-between-ledger-settlement-year-end-close.md).
    - Když zahájíte uzávěrku za rok 2022 a stále budou nalezeny transakce vyrovnané napříč fiskálními roky, proces roční uzávěrky vás okamžitě upozorní. Tato situace může nastat, pokud uživatelé vyrovnali transakce napříč fiskálními roky poté, co jste dokončili předchozí kroky.
    - Pokud jsou transakce z roku 2021 a 2022 stále vyrovnány, budete muset znovu deaktivovat funkci **Sledování** a poté zopakovat předchozí kroky, abyste zrušili vyrovnání těchto transakcí. Tento přístup je nutný, protože rok 2021 je uzavřen a u transakcí v uzavřeném fiskálním roce nelze zrušit vyrovnání.
    - Pokud jsou transakce z roku 2022 a 2023 stále vyrovnány, nemusíte deaktivovat funkci **Sledování**. Vzhledem k tomu, že rok 2022 ani 2023 není uzavřen, můžete použít předchozí kroky k zrušení vyrovnání transakcí.

18. Transakci 700 USD z roku 2023 můžete vyrovnat s podrobnými transakcemi, které byly převedeny jako počáteční zůstatky v roce 2023. Tato transakce nebude vyrovnána s původní transakcí v roce 2022.

Po úspěšném spuštění uzávěrky za rok 2022 můžete od této chvíle ponechat funkci **Sledování** povolenu.

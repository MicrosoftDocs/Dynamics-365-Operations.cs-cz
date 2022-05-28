---
title: Sestavy nákladů za doručení
description: Toto téma popisuje, jak vyhledat a použít různé typy sestav, které jsou k dispozici pro modul Náklady za doručení.
author: Weijiesa
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2ffe3f6b3bf43cca066a1ecd14947bd111adaad6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690325"
---
# <a name="landed-cost-reports"></a>Sestavy nákladů za doručení

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Neuhrazené faktury

Sestava nevyřízených faktur obsahuje seznam všech nevyřízených faktur různých úrovní nákladů, které jsou spojeny s každou cestou. Používá se k pravidelnému odsouhlasení cesty a nákladů na cestu spolu se seznamem transakcí hlavní knihy. Poté, co byly režijní náklady fakturovány, budou odstraněny ze sestavy.

Chcete-li vygenerovat sestavu nevyřízených faktur, postupujte následujícím způsobem.

1. Přejděte na **Náklady za doručení \> Sestavy \> Sledování \> Nevyřízené faktury**.
1. V dialogovém okně **Nevyřízené faktury** zadejte v poli **Ke dni** datum. Jakákoli faktura, která nebyla k uvedenému datu nebo před tímto datem vyřízena, bude zahrnuta do výstupu.
1. V části **Zobrazit** vyberte jednu z následujících možností:

    - **Nefakturované náklady** – Zahrnout náklady na fakturované zásilky, které mají odhadovanou hodnotu nákladů, ale žádné skutečné náklady.
    - **Nefakturovaný sklad** – Zahrnout náklady, které byly fakturovány, ale pro které ještě nebyla přijata nákupní objednávka.
    - **Vše nefakturované** – Zahrňte výsledky obou možností **Nefakturované náklady** a **Nefakturovaný sklad**.

1. Nastavte možnost **Zahrnout nové náklady** na *Ano*, když chcete zahrnout náklady, které ještě nemají skutečné náklady a pro který nebyl přijat inventář. Pokud ji nastavíte na *Ne*, sestava bude obsahovat pouze náklady, které byly fakturovány.
1. V části **Zobrazit** povolte všechny typy podrobností, které chcete zahrnout do sestavy.
1. Stejně jako u jiných typů sestav v Microsoftu Dynamics 365 Supply Chain Management použijte záložku **Cíl** k výběru výstupního formátu sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Záznamy k zahrnutí** k dalšímu omezení záznamů, které budou zahrnuty do sestavy.
1. Klepnutím na tlačítko **OK** sestavu vygenerujte.

## <a name="activityprovider-analysis-reports"></a>Sestavy analýzy aktivity/poskytovatele

Sestavy analýzy aktivity/poskytovatele vám umožňují zkontrolovat přesnost vašich časových odhadů pro každého poskytovatele.

Chcete-li vygenerovat sestavu analýzy aktivity/poskytovatele, postupujte následujícím způsobem.

1. V závislosti na typu sestavy, kterou chcete vytvořit, proveďte jeden z těchto kroků:

    - Přejděte na **Náklady za doručení \> Sestavy \> Analýza aktivity/poskytovatele podle aktivity**. V tomto případě budou časové odhady seskupeny podle aktivity.
    - Přejděte na **Náklady za doručení \> Sestavy \> Analýza aktivity/poskytovatele podle poskytovatele**. V tomto případě budou časové odhady seskupeny podle poskytovatele.

    Zobrazí se buď dialogové okno **Analýza aktivity/poskytovatele podle aktivity** nebo **Analýza aktivity/poskytovatele podle poskytovatele**. V obou dialogových oknech jsou stejné možnosti.

1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Cíl** k výběru výstupního formátu sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Záznamy k zahrnutí** k dalšímu omezení záznamů, které budou zahrnuty do sestavy.
1. Klepnutím na tlačítko **OK** sestavu vygenerujte.

## <a name="voyage-costing-reports"></a>Sestavy výpočtu nákladů cesty

Sestavy výpočtu nákladů na cestu zobrazují náklady na položky a importní náklady na folio, přepravní kontejner nebo cestu, v závislosti na možnostech, které vyberete při generování sestavy. Každá sestava výpočtu nákladů na cestu vám umožňuje zobrazit odhadované náklady na cestu ve srovnání se skutečnými náklady a lze ji rozčlenit podle několika identifikačních faktorů.

Chcete-li vygenerovat sestavu výpočtu nákladů na cestu, postupujte následujícím způsobem.

1. V závislosti na typu sestavy, kterou chcete vytvořit, proveďte jeden z těchto kroků:

    - Přejděte na **Náklady za doručení \> Sestavy \> Výpočet nákladů \> Výpočet nákladů cesty podle jednotlivých nákladů**. V takovém případě se u možnosti jednotlivých nákladů zobrazí importní náklady podle oblasti nákladů a podle kódu typu nákladů.
    - Přejděte na **Náklady za doručení \> Sestavy \> Výpočet nákladů \> Výpočet nákladů cesty podle kategorie vykazování**. V takovém případě budou importní náklady rozčleněny do různých kategorií vykazování. Typy nákladů jsou seskupeny podle kategorií vykazování.

    Zobrazí se buď dialogové okno **Výpočet nákladů cesty podle jednotlivých nákladů**, nebo **Výpočet nákladů cesty podle kategorie vykazování** . Tato dialogová okna vypadají podobně. Veškeré rozdíly jsou zmíněny ve zbytku tohoto postupu.

1. Pokud jste otevřeli dialogové okno **Výpočet nákladů cesty podle kategorie vykazování**, vyberte v poli **Náklady** jednu z následujících hodnot:

    - **Hodnota nákladů** – Hodnota se vypočítá buď pomocí automatických nákladů, nebo se vytvoří ručně v oblasti nákladů.
    - **Odhadované** – Po přijetí zboží jsou nastaveny odhadované náklady.
    - **Aktuální** - Po fakturaci objednávky jsou skutečné náklady nastaveny na fakturované náklady.
    - **Nejlepší** – Systém použije kteroukoli z předchozích tří možností, která je nejpřesnější. (Doporučujeme vybrat tuto možnost.)

1. Nastavte možnost **Za položku** na *Ano*, chcete-li zobrazit cenu každé položky. Nastavte ji na *Ne*, když chcete zobrazit náklady na celou cestu.
1. V části **Zobrazení** vyberte kategorie, podle kterých rozepíšete náklady.
1. V části **Dimenze** vyberte dimenze, které chcete zahrnout do sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Cíl** k výběru výstupního formátu sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Záznamy k zahrnutí** k dalšímu omezení záznamů, které budou zahrnuty do sestavy.
1. Klepnutím na tlačítko **OK** sestavu vygenerujte.

## <a name="shipping-container-receipts-list"></a>Seznam příjemek přepravního kontejneru

Seznam příjmů přepravního kontejneru obsahuje všechna nepřijatá množství, jejichž termín je v očekávaném datu nebo před ním. Pracovníci skladu mohou pomocí této sestavy identifikovat očekávané zboží na přepravním kontejneru. Lze jej také použít k ručnímu ověření zboží při jeho přijetí do přepravního kontejneru.

Chcete-li vygenerovat seznam příjmů přepravního kontejneru, postupujte takto.

1. Přejděte na **Náklady za doručení \> Sestavy \> Sledování \> Seznam příjmů přepravního kontejneru**.
1. V dialogovém okně **Seznam příjmů přepravního kontejneru** zadejte datum v poli **Očekávané datum**. Jakékoli množství, která nebylo k uvedenému datu nebo před tímto datem přijato, bude zahrnuto do výstupu.
1. V části **Dimenze** vyberte dimenze, které chcete zahrnout do sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Cíl** k výběru výstupního formátu sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Záznamy k zahrnutí** k dalšímu omezení záznamů, které budou zahrnuty do sestavy.
1. Klepnutím na tlačítko **OK** sestavu vygenerujte.

## <a name="expected-delivery-report"></a>Sestava očekávaného dodání

Sestava očekávaného dodání obsahuje základní informace o cestě, přepravním kontejneru, foliu, položkách a očekávaném datu dodání.

Chcete-li vygenerovat sestavu očekávaného dodání, postupujte následujícím způsobem.

1. Přejděte na **Náklady za doručení \> Sestavy \> Sledování \> Očekávané dodání**.
1. V dialogovém okně **Očekávané dodání** vyberte v poli **Očekávané datum** to datum, kdy se očekává dodání zboží do konečného cílového skladu. Do výstupu bude zahrnut jakýkoli řádek cesty, který má očekávané datum k tomuto datu nebo před tímto datem a který ještě nebyl přijat.
1. Volitelné: V poli **Účet dodavatele** vyberte účet dodavatele a zahrňte do sestavy pouze dodávky od konkrétního dodavatele.
1. V části **Dimenze** vyberte dimenze, které chcete zahrnout do sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Cíl** k výběru výstupního formátu sestavy.
1. Stejně jako u jiných typů sestav v Supply Chain Management použijte záložku **Záznamy k zahrnutí** k dalšímu omezení záznamů, které budou zahrnuty do sestavy.
1. Klepnutím na tlačítko **OK** sestavu vygenerujte.

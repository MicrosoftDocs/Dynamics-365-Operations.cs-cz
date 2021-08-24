---
title: Konfigurace ručních rozhodnutí ve workflow
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí.
author: ChrisGarty
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bfe14dc96c2e20f06594808bc45a82699465bb2ab61328b1b22b663db49d98f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754923"
---
# <a name="configure-manual-decisions-in-a-workflow"></a>Konfigurace ručních rozhodnutí ve workflow

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního rozhodnutí.

Pokud budete chtít nakonfigurovat ruční rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Následně nakonfigurujte vlastnosti dílčího workflowu pomocí ručního rozhodnutí.

## <a name="name-the-decision"></a>Název rozhodnutí

Pomocí následujících kroků zadejte název ručního rozhodnutí.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Název** zadejte jedinečný název ručního rozhodnutí.

## <a name="enter-a-subject-line-and-instructions"></a>Zadání řádku předmětu a pokynů

Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k tomuto ručnímu rozhodnutí. Například pokud konfigurujete rozhodnutí pro nákupní požadavky, uživatel, který je k rozhodnutí přiřazeno, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**. Řádek předmětu se zobrazí na panelu zpráv na stránce. Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny. K zadání řádku předmětu a pokynů použijte následující postup.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Na kartě **Pokyny** v poli **Předmět pracovní položky** zadejte řádek předmětu.
3. Řádek předmětu můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:

    1. V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2. Klikněte na **Vložit zástupný text**.
    3. V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4. Klepněte na tlačítko **Vložit**.

4. Chcete-li přidat překlady řádku předmětu, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.
    6. Klepněte na tlačítko **Zavřít**.

5. V poli **Pokyny pracovní položky** zadejte pokyny.
6. Pokyny můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:

    1. V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2. Klikněte na **Vložit zástupný text**.
    3. V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4. Klepněte na tlačítko **Vložit**.

7. Chcete-li přidat překlady pokynů, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.
    6. Klepněte na tlačítko **Zavřít**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Určete možné výsledky rozhodnutí

obvykle pokud je dokument přiřazen pracovníkovi s rozhodovací pravomocí, je tomuto pracovníkovi kladena otázka. Na tuto otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**. Podle následujících kroků můžete určit možné výsledky ručního rozhodnutí.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Na kartě **Výsledky** v poli **Výsledek 1** zadejte název výsledku nebo možnost.
3. Chcete-li přidat překlady výsledků, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Klepněte na tlačítko **Zavřít**.

4. V poli **Výsledek 2** zadejte název výsledku nebo možnost.
5. Chcete-li přidat překlady výsledků, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Klepněte na tlačítko **Zavřít**.

## <a name="specify-when-notifications-are-sent"></a>Zadejte, kdy se mají odesílat oznámení.

Můžete odeslat oznámení uživatelům, jakmile bude rozhodnutí provedeno, delegováno nebo eskalováno. Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.

1. V levém podokně klikněte na **Oznámení**.
2. Označte pole vedle událostí, při kterých se oznámení odešle:

    - **\[Volba 1\]** – přiřazený uživatel vybral možnost **\[Volba 1\]**.
    - **\[Volba 2\]** – přiřazený uživatel vybral možnost **\[Volba 2\]**.
    - **Delegovat** – přiřazený uživatel přiřadil rozhodnutí jinému uživateli.
    - **Eskalovat** – přiřazený uživatel neučinil rozhodnutí v přiděleném čase.

3. Vyberte řádek pro událost, kterou jste vybrali v kroku 2.
4. Na kartě **Text oznámení** zadejte v textovém poli text oznámení.
5. Oznámení můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:

    1. V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2. Klikněte na **Vložit zástupný text**.
    3. V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4. Klepněte na tlačítko **Vložit**.

6. Chcete-li přidat překlady oznámení, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.
    6. Klepněte na tlačítko **Zavřít**.

7. Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána. Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Příjemce oznámení</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu, které chcete oznámení odeslat.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td>
    <ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Uživatel</td>
    <td>Konkrétní uživatelé</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele. Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.

## <a name="assign-a-decision"></a>Přiřazení rozhodnutí

Pomocí následujícího postupu určíte, komu má být ruční rozhodnutí přiřazeno.

1. V levém podokně klikněte na **Přiřazení**.
2. Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Uživatelé, kterým je rozhodnutí přiřazeno</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete rozhodnutí přiřadit.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete rozhodnutí přiřadit.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, které chcete rozhodnutí přiřadit.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, kterým může být rozhodnutí přiřazen. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol>
    </li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, kterým by měl být rozhodnutí přiřazeno: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí bude přiřazeno všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude přiřazeno pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není přiřazeno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td>
    <ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Uživatel</td>
    <td>Konkrétní uživatelé</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele. Vyberte uživatele, kterým chcete rozhodnutí přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí. Vyberte některou z následujících možností:

    - **Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Dny** – zadejte počet dnů, které má uživatel na rozhodnutí. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.
    - **Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout. Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.
    - **Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout. Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.

    Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení. Rozhodnutí v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Určení akce prováděné při zpoždění rozhodnutí

Pokud uživatel v přiděleném čase rozhodnutí neučiní, rozhodnutí bude v prodlení. Rozhodnutí, které je v prodlení, může být eskalováno nebo automaticky přiřazeno jinému uživateli. Pro eskalování rozhodnutí v prodlení postupujte následovně.

1. V levém podokně klikněte na **Eskalování**.
2. Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu. Systém automaticky přiřadí dané rozhodnutí uživatelům uvedeným v cestě eskalace. Například v následující tabulce naleznete příklad eskalační cesty.

    | Pořadí | Eskalační cesta            |
    |----------|----------------------------|
    | 1        | Přiřadit k: Donna           |
    | 2        | Přiřadit k: Erin            |
    | 3        | Konečná akce: \[Volba 1\] |

    V tomto příkladu systém přiřadí zpožděné rozhodnutí Donně. Pokud Donna v určeném čase rozhodnutí neučiní, systém přiřadí rozhodnutí Erin. Pokud Erin v určeném čase rozhodnutí neučiní, systém jako rozhodnutí vybere možnost **\[Volba 1\]**.

3. Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**. Vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Uživatelé, kterým je rozhodnutí eskalováno</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které rozhodnutí eskalovat.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, ke kterým může být rozhodnutí eskalováno. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol>
    </li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být rozhodnutí eskalováno: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – rozhodnutí dokument bude eskalováno všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – rozhodnutí bude eskalováno pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – rozhodnutí není eskalováno žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td>
    <ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Uživatel</td>
    <td>Konkrétní uživatelé</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele. Vyberte uživatele, ke kterým chcete rozhodnutí eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na rozhodnutí. Vyberte některou z následujících možností:

    - **Hodiny** – zadejte počet hodin, které má uživatel na rozhodnutí. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Dny** – zadejte počet dnů, které má uživatel na rozhodnutí. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Týdny** – zadejte počet týdnů, které má uživatel na rozhodnutí.
    - **Měsíce** – vyberte den a týden, do kdy se musí uživatel rozhodnout. Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v daném měsíci.
    - **Roky** – vyberte den, týden a měsíc, do kdy se musí uživatel rozhodnout. Můžete například požadovat, aby uživatel učinil rozhodnutí do třetího pátku v prosinci.

5. Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty. Pořadí uživatelů lze změnit.
6. Pokud uživatelé v eskalační cestě v určeném čase rozhodnutí neučiní, systém sám provede rozhodnutí. Možnost, kterou systém vybere, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte možnost.

## <a name="set-a-time-limit"></a>Nastavení časového limitu

Tento postup použijte, pokud je rozhodnutí nutné učinit v určitém čase.

> [!NOTE]
> Možnosti, které vyberete v rámci této procedury, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** na stránce.

1. V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2. Označte pole **Nastavit časový limit pro prvek workflowu**.
3. V poli **Trvání** upřesněte, kdy má být rozhodnutí učiněno. Vyberte některou z následujících možností:

    - **Hodiny** – zadejte počet hodin Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Dny** – zadejte počet dnů Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Týdny** – zadejte počet týdnů.
    - **Měsíce** – vyberte den a týden, do kdy má být rozhodnutí učiněno. Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v daném měsíci.
    - **Roky** – vyberte den, týden a měsíc, do kdy má být rozhodnutí učiněno. Můžete například požadovat, aby bylo rozhodnutí učiněno do třetího pátku v prosinci.

4. Dojde-li k překročení časového limitu, systém učiní rozhodnutí. V seznamu **Akce** vyberte možnost, která má být vybrána.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
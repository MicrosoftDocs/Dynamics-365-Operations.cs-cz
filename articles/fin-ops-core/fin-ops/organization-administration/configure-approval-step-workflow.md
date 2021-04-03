---
title: Konfigurace schvalovacích kroků ve workflowu
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti schvalovacího kroku.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5442b7db0a1ccd2a2e07faf8635ac12ff06c560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565727"
---
# <a name="configure-approval-steps-in-a-workflow"></a>Konfigurace schvalovacích kroků ve workflowu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat vlastnosti schvalovacího kroku.

Pokud budete chtít nakonfigurovat schvalovací krok v editoru workflowu, klikněte pravým tlačítkem myši na krok schválení a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Následně nakonfigurujte vlastnosti dílčího workflowu pomocí schvalovacího kroku.

## <a name="name-the-step"></a>Pojmenování kroku
Pomocí následujících kroků zadejte název schvalovacího kroku.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Do pole **Název** zadejte jedinečný název schvalovacího kroku.

## <a name="enter-a-subject-line-and-instructions"></a>Zadání řádku předmětu a pokynů

Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k tomuto schvalovacímu kroku. Například pokud konfigurujete schvalovací krok pro nákupní požadavky, uživatel, který je ke kroku přiřazen, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**. Řádek předmětu se zobrazí na panelu zpráv na stránce. Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny. K zadání řádku předmětu a pokynů použijte následující postup.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Předmět pracovní položky** zadejte řádek předmětu.
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

## <a name="assign-the-approval-step"></a>Přiřazení schvalovacího kroku

Pomocí následujícího postupu určíte, komu má být schvalovací krok přiřazen.

1. V levém podokně klikněte na **Přiřazení**.
2. Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Uživatelé, kterým je schvalovací krok přiřazen</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, ke které chcete krok přiřadit.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, ke které chcete krok přiřadit.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete krok přiřadit.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, ke kterým může být krok přiřazen. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol>
    </li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být krok přiřazen: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – krok bude přiřazen všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – krok bude přiřazen pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – krok není přiřazen žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
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
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele systému. Vyberte uživatele, ke kterým chcete krok přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel pro provedení akce nebo reakce na dokumenty, které dosáhly schvalovacího kroku. Vyberte některou z následujících možností:

    - **Hodiny** – zadejte počet hodin, které má uživatel reagovat. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Dny** – zadejte počet dnů, které má uživatel reagovat. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Týdny** – zadejte počet týdnů, které má uživatel reagovat.
    - **Měsíce** – vyberte den a týden, do kdy musí uživatel reagovat. Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v měsíci.
    - **Roky** – vyberte den, týden a měsíc, do kdy musí uživatel reagovat. Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v prosinci.

    Pokud uživatel u dokumentu neprovede akci v přiděleném čase, dokument bude v prodlení. Dokument v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.

4. Jestliže přiřadíte schvalovací krok více uživatelům nebo skupině uživatelů na kartě **Zásada dokončení**, vyberte jednu z následujících možností:

    - **Jednotlivý schvalovatel** – akce použitá pro dokument je určena první reagující osobou. Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD. Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill. Pokud je Sue první osobou reagující na dokument, je akce, kterou provede, použita pro dokument. Jestliže ho Sue odmítne, je dokument zamítnut a odeslán zpět Samovi. Jakmile Sue dokument schválí, je odeslán Anně ke schválení.

        ![Workflow se schvalovacím procesem](./media/workflow_multipleusersinstep.gif)

    - **Většina schvalovatelů** – akce použitá pro dokument je určena, když reaguje většina schvalujících. Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD. Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill. Akci použitou pro dokument určují první dva schvalující, kteří reagují, tedy Sue a Jo.

        - Jestliže Sue dokument schválí a Jo ho zamítne, je dokument zamítnut a odeslán zpět Samovi.
        - Jestliže Sue i Jo dokument schválí, je dokument odeslán Anně ke schválení.

    - **Procentuální počet schvalovatelů** – akce použitá pro dokument je určena, když reaguje konkrétní procento schvalujících. Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD. Vyúčtování výdajů je momentálně přiřazeno Sue, Jo a Billovi a vy zadáte pro procento hodnotu **50**. Jestliže Sue a Jo jsou prvními dvěma schvalující, kteří reagují, akce, kterou provedou, je použitá v dokumentu vzhledem k tomu, že splňují požadavky 50 procent schvalovatelů.

        - Jestliže Sue dokument schválí a Jo ho zamítne, je dokument zamítnut a odeslán zpět Samovi.
        - Jestliže Sue i Jo dokument schválí, je dokument odeslán Anně ke schválení.

    - **Všichni schvalovatelé** – dokument musí schválit všichni schvalovatelé. V opačném případě se ve workflowu nedá pokračovat. Například Sam odeslal vyúčtování výdajů ve výši 15 000 USD. Vyúčtování výdajů je aktuálně přiřazeno uživatelům Sue, Jo a Bill. Jestliže Sue a Jo dokument schválí a Bill ho zamítne, je dokument zamítnut a odeslán zpět Stanislavovi. Jestliže Sue, Jo a Bill dokument schválí, je dokument odeslán Anně ke schválení.

## <a name="specify-when-the-approval-step-is-required"></a>Určete, kdy je schvalovací krok vyžadován.

Můžete určit, kdy je schvalovací krok vyžadován. Schvalovací krok může být vždy vyžadován, nebo může být vyžadován pouze v případě splnění určitých podmínek.

### <a name="the-approval-step-is-always-required"></a>Schvalovací krok je vyžadován vždy

Pokud je schvalovací krok vyžadován vždy, postupujte následovně.

1. V levém podokně klikněte na **Podmínka**.
2. Vyberte možnost **Vždy spustit tento krok**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Schvalovací krok je vyžadován za určitých podmínek

Schvalovací krok, který konfigurujete, může být vyžadován pouze po splnění určitých podmínek. Například pokud konfigurujete schvalovací krok pro workflow nákupního požadavku můžete chtít, aby ke schvalovacímu kroku docházelo pouze v případě, že je nákupní požadavek je vyšší než 10 000 USD. Pomocí následujícího postupu určete, kdy je schvalovací krok vyžadován.

1. V levém podokně klikněte na **Podmínka**.
2. Vyberte možnost **Provést tento krok pouze v případě, že je splněna následující podmínka**.
3. Zadání podmínky
4. Zadejte všechny další podmínky, které jsou požadovány.
5. Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:

    1. Klepněte na možnost **Test**.
    2. Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.
    3. Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.
    4. Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Co by se mělo stát, je-li dokument zpožděný

Pokud uživatel u dokumentu neprovede akci v přiděleném čase, dokument bude v prodlení. Dokument, který je v prodlení, může být eskalován nebo automaticky přiřazen ke schválení jinému uživateli. Pro eskalování dokumentu v prodlení postupujte následovně.

1. V levém podokně klikněte na **Eskalování**.
2. Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu. Systém automaticky přiřadí daný dokument uživatelům uvedeným v cestě eskalace. Například v následující tabulce naleznete příklad eskalační cesty.

    | Pořadí | Eskalační cesta      |
    |----------|----------------------|
    | 1        | Přiřadit k: Donna     |
    | 2        | Přiřadit k: Erin      |
    | 3        | Finální akce: odmítnutí |

    V tomto příkladu systém přiřadí zpožděný dokument Donně. Pokud Donna v přiděleném čase nereaguje, systém přiřadí dokument Erin. Pokud Erin v přiděleném čase nereaguje, systém dokument zamítne.

3. Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**. Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Uživatelé, kterým je dokument eskalován</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které dokument eskalovat.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, ke kterým může být dokument eskalován. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol>
    </li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být dokument eskalován: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – dokument bude eskalován všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – dokument bude eskalován pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – dokument není eskalován žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
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
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele. Vyberte uživatele, ke kterým chcete dokument eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel pro provedení akce nebo reakce na dokumenty. Vyberte některou z následujících možností:

    - **Hodiny** – zadejte počet hodin, které má uživatel reagovat. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Dny** – zadejte počet dnů, které má uživatel reagovat. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    - **Týdny** – zadejte počet týdnů, které má uživatel reagovat.
    - **Měsíce** – vyberte den a týden, do kdy musí uživatel reagovat. Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v měsíci.
    - **Roky** – vyberte den, týden a měsíc, do kdy musí uživatel reagovat. Můžete například požadovat, aby uživatel odpověděl do pátku třetího týdne v prosinci.

5. Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty. Pořadí uživatelů lze změnit.
6. Pokud uživatelé v eskalační cestě nereagují v určeném čase, systém automaticky provede akci vhodnou pro daný dokument. Akci, kterou systém provede, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte akci.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
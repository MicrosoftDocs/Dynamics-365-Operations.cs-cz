---
title: "Konfigurace ruční úlohy ve workflowu"
description: "Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního úkolu."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 09bd86ff7a4aa8ae64cfa4a38fba643f9117d6eb
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a>Konfigurace ruční úlohy ve workflowu

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nakonfigurovat vlastnosti ručního úkolu.

Pokud budete chtít nakonfigurovat ruční úkol v editoru workflowu, klikněte pravým tlačítkem myši na úkol a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Následně nakonfigurujte vlastnosti dílčího workflowu pomocí ručního úkolu.

## <a name="name-the-task"></a>Pojmenování úlohy
Pomocí následujících kroků zadejte název ručního úkolu.

1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  Do pole **Název** zadejte jedinečný název úlohy.

## <a name="enter-a-subject-line-and-instructions"></a>Zadání řádku předmětu a pokynů
Musíte zadat řádek předmětu a pokyny pro uživatele přiřazené k dané úkolu. Například pokud konfigurujete úkol pro nákupní požadavky, uživatel, který je k úkolu přiřazen, uvidí řádek s předmětem a pokyny na stránce **Nákupní žádanky**. Řádek předmětu se zobrazí na panelu zpráv na stránce. Uživatel poté může kliknutím na ikonu na panelu zpráv zobrazit pokyny. K zadání řádku předmětu a pokynů použijte následující postup.

1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  V poli **Předmět pracovní položky** zadejte řádek předmětu.
3.  Řádek předmětu můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení řádku předmětu uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:
    1.  V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2.  Klikněte na **Vložit zástupný text**.
    3.  V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4.  Klepněte na tlačítko **Vložit**.

4.  Chcete-li přidat překlady řádku předmětu, postupujte takto:
    1.  Klikněte na **Překlady**.
    2.  Na nově otevřené stránce klikněte na **Přidat**.
    3.  V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4.  V poli **Přeložený text** zadejte text.
    5.  Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 3.
    6.  Klepněte na tlačítko **Zavřít**.

5.  V poli **Pokyny pracovní položky** zadejte pokyny.
6.  Pokyny můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:
    1.  V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2.  Klikněte na **Vložit zástupný text**.
    3.  V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4.  Klepněte na tlačítko **Vložit**.

7.  Chcete-li přidat překlady pokynů, postupujte takto:
    1.  Klikněte na **Překlady**.
    2.  Na nově otevřené stránce klikněte na **Přidat**.
    3.  V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4.  V poli **Přeložený text** zadejte text.
    5.  Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 6.
    6.  Klepněte na tlačítko **Zavřít**.

## <a name="assign-the-task"></a>Přiřazení úlohy
Pomocí následujícího postupu určíte, komu má být ruční úkol přiřazen.

1.  V levém podokně klikněte na **Přiřazení**.
2.  Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 3 postupujte podle dalších kroků pro tuto možnost.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Možnost</th>
    <th>Uživatelé, ke kterým je úkol přiřazen</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, ke které chcete úkol přiřadit.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, ke které chcete úkol přiřadit.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete úkol přiřadit.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, ke kterým může být úkol přiřazen. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol></li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být úkol přiřazen: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – úkol bude přiřazen všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – úkol bude přiřazen pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – úkol není přiřazen žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td><ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Uživatel</td>
    <td>Konkrétní uživatelé aplikace Microsoft Dynamics 365 for Finance and Operations</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations. Vyberte uživatele, ke kterým chcete úkol přiřadit, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Fronta</td>
    <td>Fronta pracovních položek</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Fronta</strong> klepněte na kartu <strong>Založeno na frontě</strong>.</li>
    <li>Chcete-li přiřadit úkol konkrétní frontě, postupujte následujícím způsobem: <ol>
    <li>V seznamu <strong>Typ fronty</strong> vyberte <strong>Fronty pracovních položek</strong>.</li>
    <li>V seznamu <strong>Název fronty</strong> vyberte frontu.</li>
    </ol></li>
    <li>Pokud by konkrétní podmínka měla určit frontu, ke které bude úkol přiřazen, postupujte takto: <ol>
    <li>V seznamu <strong>Typ fronty</strong> vyberte <strong>Podmíněné fronty pracovních položek</strong>.</li>
    <li>V seznamu <strong>Název fronty</strong> vyberte <strong>Podmíněná fronta</strong>.</li>
    </ol></li>
    </ol>
    <strong>Poznámka:</strong> tato možnost se používá pouze u několika workflowů, jako je například správa případů.</td>
    </tr>
    </tbody>
    </table>

3.  Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na dokončení úkolu. Vyberte některou z následujících možností:
    -   **Hodiny** – zadejte počet hodin, které má uživatel na dokončení úkolu. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Dny** – zadejte počet dnů, které má uživatel na dokončení úkolu. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Týdny** – zadejte počet týdnů, které má uživatel na dokončení úkolu.
    -   **Měsíce** – vyberte den a týden, do kdy musí uživatel dokončit úkol. Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v daném měsíci.
    -   **Roky** – vyberte den, týden a měsíc, do kdy musí uživatel dokončit úkol. Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v prosinci.

    Pokud uživatel v přiděleném čase úkol nedokončí, úkol bude v prodlení. Úkol v prodlení je eskalován na základě možností vybraných v oblasti stránky **Eskalace**.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Určení akce prováděné při zpoždění úlohy
Pokud uživatel v přiděleném čase ruční úkol nedokončí, úkol bude v prodlení. Úkol, který je v prodlení, může být eskalován nebo automaticky přiřazen jinému uživateli. Pro eskalování úkolu v prodlení postupujte následovně.

1.  V levém podokně klikněte na **Eskalování**.
2.  Označte pole **Použít eskalační cestu** a vytvořte tak eskalační cestu. Systém automaticky přiřadí daný úkol uživatelům uvedeným v cestě eskalace. Například v následující tabulce naleznete příklad eskalační cesty.

    | Pořadí | Eskalační cesta      |
    |----------|----------------------|
    | 1        | Přiřadit k: Donna     |
    | 2        | Přiřadit k: Erin      |
    | 3        | Finální akce: odmítnutí |

    V tomto příkladu systém přiřadí zpožděný úkol Donně. Pokud ji Donna v určeném čase úkol nedokončí, systém přiřadí úkol Erin. Pokud Erin v přiděleném čase úkol nedokončí, systému dokument odeslaný ke zpracování zamítne.
3.  Pokud chcete přidat uživatele do eskalační cesty, klepněte na tlačítko **Přidat eskalaci**. Na kartě **Typ přiřazení** vyberte jednu z možností v následující tabulce a před přechodem na krok 4 postupujte podle dalších kroků pro tuto možnost.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Možnost</th>
    <th>Uživatelé, ke kterým je úkol eskalován</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarchie</td>
    <td>Uživatelé v určité organizační hierarchii</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Hierarchie</strong> na kartě <strong>Výběr hierarchie</strong> v seznamu <strong>Typ hierarchie</strong> vyberte typ hierarchie, ke které chcete úkol eskalovat.</li>
    <li>Systém musí z hierarchie načíst rozsah jmen uživatelů. Tato jména představují uživatele, ke kterým může být úkol eskalován. Podle těchto kroků určete počáteční a koncový bod rozsahu uživatelských jmen, které systém obdrží: <ol>
    <li>Chcete-li zadat počáteční bod, vyberte osobu v seznamu <strong>Začátek od</strong>.</li>
    <li>Chcete-li zadat koncový bod, klepněte na možnost <strong>Přidat podmínku</strong>. Poté zadáním podmínky označte, kde v hierarchii má systém přestat načítat jména.</li>
    </ol></li>
    <li>Na kartě <strong>Možnosti hierarchie</strong> zadejte uživatele v rozsahu, ke kterým by měl být úkol eskalován: <ul>
    <li><strong>Přiřadit všechny načtené uživatele</strong> – úkol bude eskalován všem uživatelům v rozsahu.</li>
    <li><strong>Přiřadit pouze poslednímu načtenému uživateli</strong> – úkol bude eskalován pouze poslednímu uživateli v rozsahu.</li>
    <li><strong>Vyloučit uživatele splňující následující podmínku</strong> – úkol není eskalován žádnému uživateli v rozsahu, který odpovídá konkrétní podmínce. Po klepnutí na volbu <strong>Přidat podmínku</strong> určete požadovanou podmínku.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td><ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Uživatel</td>
    <td>Konkrétní uživatelé aplikace Finance and Operations</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations. Vyberte uživatele, kterým chcete úkol eskalovat, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Na kartě **Časový limit** v poli **Trvání** určete, kolik času má uživatel na dokončení úkolu. Vyberte některou z následujících možností:
    -   **Hodiny** – zadejte počet hodin, které má uživatel na dokončení úkolu. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Dny** – zadejte počet dnů, které má uživatel na dokončení úkolu. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Týdny** – zadejte počet týdnů, které má uživatel na dokončení úkolu.
    -   **Měsíce** – vyberte den a týden, do kdy musí uživatel dokončit úkol. Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v daném měsíci.
    -   **Roky** – vyberte den, týden a měsíc, do kdy musí uživatel dokončit úkol. Můžete například požadovat, aby uživatel úlohu dokončil do třetího pátku v prosinci.

5.  Zopakujte kroky 3 a 4 u každého uživatele, který má být přidán do eskalační cesty. Pořadí uživatelů lze změnit.
6.  Pokud uživatelé v eskalační cestě v určeném čase úkol nedokončí, systém sám provede u úkolu vhodnou akci. Akci, kterou systém provede, můžete vybrat výběrem řádku **Akce** a na kartě **Konečná akce** vyberte akci.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Určení podmínky, podle které systém automaticky provede akci u úkolu
Systém lze nastavit tak, aby při splnění určitých podmínek prováděl akce u ručních úkolů. Například úkol bude vyžadovat, aby člen oddělení pro vyúčtování výdajů zkontrolovat příjmové doklady, které byly odeslány společně s vyúčtováním výdajů. Podle zásad společnosti musí být tento úkol proveden v případě, že celková částka vyúčtování výdajů bude větší než 100 USD. V tomto scénáři lze systém nastavit tak, aby automaticky označil úkol za **Dokončený** v situaci, kdy je celková částka nižší než 100. Pomocí tohoto postupu určete podmínky, za kterých má systém zpracovávat ruční úkol.

1.  V levém podokně klepněte na tlačítko **Automatické akce**.
2.  Označte pole **Povolit automatické akce**.
3.  Klepněte na možnost **Přidat podmínku**.
4.  Zadání podmínky
5.  Zadejte všechny další podmínky, které jsou požadovány.
6.  Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:
    1.  Klepněte na možnost **Test**.
    2.  Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.
    3.  Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.
    4.  Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.

7.  V seznamu **Akce automatického dokončení** vyberte akci, která má být u úkolu provedena.

## <a name="specify-when-notifications-are-sent"></a>Zadejte, kdy se mají odesílat oznámení.
Při delegování, eskalování, dokončení nebo zamítnutí ruční úlohy a při zadání požadavku na změnu můžete zaslat oznámení určeným osobám. Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.

1.  V levém podokně klikněte na **Oznámení**.
2.  Označte pole vedle událostí, při kterých se oznámení odešle:
    -   **Delegovat** – úkol byl přiřazen jinému uživateli.
    -   **Eskalovat** – přiřazený uživatel nedokončil úkol v přiděleném čase.
    -   **Dokončit** – přiřazený uživatel dokončil úkol.
    -   **Odmítnout** – přiřazený uživatel odmítl dokument, který byl odeslán.
    -   **Žádost o změnu** – přiřazený uživatel požádal o změnu dokumentu, který byl odeslán.

3.  Vyberte řádek pro událost, kterou jste vybrali v kroku 2.
4.  Na kartě **Text oznámení** zadejte v textovém poli text oznámení.
5.  Oznámení můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími informacemi. Při vkládání zástupného textu postupujte takto:
    1.  V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.
    2.  Klikněte na **Vložit zástupný text**.
    3.  V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4.  Klepněte na tlačítko **Vložit**.

6.  Chcete-li přidat překlady oznámení, postupujte takto:
    1.  Klikněte na **Překlady**.
    2.  Na nově otevřené stránce klikněte na **Přidat**.
    3.  V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4.  V poli **Přeložený text** zadejte text.
    5.  Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.
    6.  Klepněte na tlačítko **Zavřít**.

7.  Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána. Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Možnost</th>
    <th>Příjemce oznámení</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Uživatel workflowu</td>
    <td>Uživatelé v aktuálním workflowu</td>
    <td><ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Uživatel</td>
    <td>Konkrétní uživatelé aplikace Finance and Operations</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations. Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.

## <a name="set-a-time-limit"></a>Nastavení časového limitu
Tento postup použijte, pokud je ruční úkol nutné dokončit v určitém čase. 

**Poznámka:** možnosti, které vyberete v rámci této procedury, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** na stránce.

1.  V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2.  Označte pole **Nastavit časový limit pro prvek workflowu**.
3.  V poli **Trvání** upřesněte, kdy má být úloha dokončena. Vyberte některou z následujících možností:
    -   **Hodiny** – zadejte počet hodin, během kterých má být úkol dokončen. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Dny** – zadejte počet dnů, během kterých má být úkol dokončen. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Týdny** – zadejte počet týdnů, během kterých má být úkol dokončen.
    -   **Měsíce** – vyberte den a týden, do kdy má být úkol dokončen. Můžete například požadovat, aby byl úkol dokončen do třetího pátku v daném měsíci.
    -   **Roky** – vyberte den, týden a měsíc, do kdy má být úkol dokončen. Můžete například požadovat, aby byl úkol dokončen do třetího pátku v prosinci.

4.  Dojde-li k překročení časového limitu, systém u úlohy provede akci. V seznamu **Akce** vyberte akci, která má být provedena.

## <a name="specify-which-actions-are-available-to-the-user"></a>Určení dostupných akcí pro uživatele
Po přiřazení ruční úlohy uživateli musí uživatel danou úlohu zpracovat. Pomocí tohoto postupu určete akce, které může uživatel u úkolu provádět. **Poznámka:** Dostupné akce se budou lišit v závislosti na tom, jak byl úkol navržen.

1.  V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2.  Chcete-li uživateli umožnit, aby úkol označil jako **Dokončený**, označte pole **Dokončený**.
3.  Chcete-li uživateli umožnit označení odeslaného dokumentu jako zamítnutého, označte pole **Zamítnout**.
4.  Chcete-li uživateli umožnit vyžádání změn v odeslaném dokumentu, zaškrtněte políčko **Požadavek na změnu**.
5.  Chcete-li uživateli umožnit, aby úlohu postoupil jinému uživateli, zaškrtněte políčko **Delegovat**.
6.  Chcete-li uživateli umožnit, aby úlohu přeřadil jinému uživateli ve frontě pracovních položek, označte pole **Znovu přiřadit**.
7.  Chcete-li uživateli umožnit, aby úlohu přeřadil do fronty pracovních položek, označte pole **Uvolnit**. Jiný uživatel pak může úkol dokončit.






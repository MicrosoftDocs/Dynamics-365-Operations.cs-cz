---
title: "Konfigurace schvalovacího procesu ve workflowu"
description: "Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf3523b2768b197b3c75b9a8490f621eced91a7a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-approval-process-in-a-workflow"></a>Konfigurace schvalovacího procesu ve workflowu

[!INCLUDE [banner](../includes/banner.md)]

Pomocí následujícího postupu nakonfigurujte vlastnosti schvalovacího procesu.

Pokud budete chtít nakonfigurovat schvalovací proces, v editoru workflowu klikněte pravým tlačítkem myši na prvek schválení a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.
Pojmenování schvalovacího procesu
-------------------------

Pomocí následujících kroků zadejte název schvalovacího procesu.
1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  V poli **Název** zadejte jedinečný název schvalovacího procesu.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Určení podmínky, podle které systém automaticky provede akci u dokumentu
Můžete nakonfigurovat systém tak, aby automaticky zpracoval dokument, pokud jsou splněny určité podmínky. Systém může například schvalovat vyúčtování výdajů, která mají celkové částky nižší než 100 USD. Pomocí tohoto postupu určete podmínky, za kterých má systém u dokumentu provést akci.
1.  V levém podokně klepněte na tlačítko **Automatické akce**.
2.  Označte pole **Povolit automatické akce**.
3.  Klikněte na možnost **Přidat podmínku**.
4.  Zadání podmínky
5.  V případě potřeby zadejte další podmínky.
6.  Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:
    1.  Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.
    2.  Vyberte v oblasti **Ověřit podmínku** formuláře záznam.
    3.  Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.
    4.  Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.

7.  V seznamu **Akce automatického dokončení** vyberte akci, která má být u dokumentu provedena.

## <a name="specify-when-notifications-are-sent"></a>Zadejte, kdy se mají odesílat oznámení.
Při schválení, zamítnutí, delegování nebo eskalování dokumentu nebo při zadání požadavku na změnu můžete zaslat oznámení určeným osobám. Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.
1.  V levém podokně klikněte na **Oznámení**.
2.  Označte pole vedle událostí, při kterých se oznámení odešle:
    -   **Delegování** – přiřazení dokumentu jinému uživateli ke schválení.
    -   **Eskalace** – přiřazený uživatel nereagoval na dokument v přiděleném čase.
    -   **Schválení** – schválení dokumentu.
    -   **Zamítnutí** – zamítnutí dokumentu.
    -   **Požadavek na změnu** – přidělený uživatel požaduje změnu odeslaného dokumentu.

3.  Vyberte řádek pro událost, kterou jste vybrali v kroku 2.
4.  Klepněte na kartu **Text oznámení**.
5.  Do textového pole zadejte název oznámení.
6.  Text můžete přizpůsobit vložením zástupného textu, který bude při zobrazení uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:
    1.  Klepněte do textového pole do umístění, kde se má zástupný text zobrazit.
    2.  Klikněte na **Vložit zástupný text**.
    3.  V seznamu, který se zobrazí, vyberte vkládaný zástupný text.
    4.  Klepněte na tlačítko **Vložit**.

7.  Chcete-li přidat překlady oznámení, klikněte na **Překlady**. Ve formuláři, který se zobrazí, postupujte takto:
    1.  Klikněte na tlačítko **Přidat**.
    2.  V otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    3.  V textovém poli **Přeložený text** zadejte text.
    4.  Text můžete přizpůsobit vložením zástupného textu.
    5.  Klepněte na tlačítko **Zavřít**.

8.  Klikněte na kartu **Příjemce**.
9.  Zadejte, komu se mají odesílat oznámení. Vyberte jednu z možností v následující tabulce a před přechodem na krok 10 postupujte podle dalších kroků pro tuto možnost.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Parametr</th>
    <th>Příjemce oznámení</th>
    <th>Další kroky</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Účastník</strong></td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Účastník</strong> klepněte na kartu <strong>Založeno na roli</strong>.</li>
    <li>V seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Uživatel workflowu</strong></td>
    <td>Uživatelé zúčastnění v aktuálním workflowu</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> klepněte na kartu <strong>Uživatel workflowu</strong>.</li>
    <li>V seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se účastní workflowu.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>Uživatel</strong></td>
    <td>Konkrétní uživatelé aplikace Microsoft Dynamics 365 for Finance and Operations</td>
    <td><ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong>: obsahuje všechny uživatele aplikace Microsoft Dynamics 365 for Finance and Operations. Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>:.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Opakujte kroky 3 až 9 pro každou událost, kterou jste vybrali v kroku 2.

## <a name="specify-a-final-approver"></a> Určení konečného schvalovatele
Můžete určit konečného schvalovatele scénářů, kde je schvalujícím osoba, která odeslala dokument ke schválení. Chcete-li určit konečného schvalovatele, postupujte takto.
1.  V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2.  Zaškrtněte políčko **Použít konečného schvalovatele**.
3.  V seznamu vyberte uživatele, který bude konečným schvalovatelem.

## <a name="set-a-time-limit"></a>Nastavení časového limitu
Tento postup použijte, pokud je proces schvalování nutné dokončit v určitém čase.

| **Poznámka**                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Možnosti, které v těchto krocích vyberete, přepíší možnosti vybrané v oblasti **Přiřazení** a **Eskalace** jednotlivých schvalovacích kroků. |

1.  V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2.  Zaškrtněte políčko **Nastavit časový limit pro prvek** **workflowu**.
3.  V poli **Trvání** upřesněte, kdy má být schvalovací proces dokončen. Vyberte některou z následujících možností:
    -   **Hodiny** – zadejte počet hodin, dokdy musí být schvalovací proces dokončen. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Dny** – zadejte počet dní, dokdy musí být schvalovací proces dokončen. Pak vyberte kalendář, který vaše organizace používá, a zadejte informace o pracovním týdnu vaší organizace.
    -   **Týdny** – zadejte počet týdnů, dokdy musí být schvalovací proces dokončen.
    -   **Měsíce** – vyberte den a týden, do kdy má být schvalovací proces dokončen. Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v daném měsíci.
    -   **Roky** – vyberte den, týden a měsíc, do kdy má být schvalovací proces dokončen. Můžete například požadovat, aby byl schvalovací proces dokončen do třetího pátku v prosinci.

4.  Dojde-li k překročení časového limitu, systém u dokumentu provede akci. V seznamu **Akce** vyberte akci, která má být provedena.

## <a name="specify-which-actions-are-available-to-the-user"></a>Určení dostupných akcí pro uživatele
Po přidělení dokumentu uživateli ke schválení musí uživatel daný dokument zpracovat. Pomocí tohoto postupu určete akce, které může uživatel u odeslaného dokumentu provádět.
1.  V levém podokně klepněte na tlačítko **Pokročilá nastavení**.
2.  Chcete-li uživatelům umožnit schválení dokumentu, zaškrtněte políčko **Schválit**.
3.  Chcete-li uživatelům zamítnout schválení dokumentu, zaškrtněte políčko **Zamítnout**.
4.  Chcete-li uživatelům umožnit vyžádání změn v dokumentu, zaškrtněte políčko **Požadavek na změnu**.
5.  Chcete-li uživateli umožnit, aby úlohu postoupil jinému uživateli ke schválení, zaškrtněte políčko **Delegovat**.

**Poznámka**: Políčko **Povolit akce z pracovního seznamu v podnikovém portálu** se již nepoužívá.

## <a name="configure-the-approval-steps"></a> Konfigurace kroků schválení
Schvalovací proces se skládá z kroků schválení. Pomocí následujícího postupu přidáte do schvalovacího procesu kroky a nakonfigurujete je.
1.  V editoru workflowu poklepejte na schvalovací proces. V editoru workflowu se zobrazí kroky schvalovacího procesu.
2.  Chcete-li přidat schvalovací krok, přetáhněte krok z oblasti **Prvky workflowu** na plátno.
3.  Chcete-li nakonfigurovat schvalovací krok, získáte informace v části [Konfigurace schvalovacího kroku](configure-approval-step-workflow.md).







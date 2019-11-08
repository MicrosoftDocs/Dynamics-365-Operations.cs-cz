---
title: Konfigurace vlastností workflow
description: Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190113"
---
# <a name="configure-workflow-properties"></a>Konfigurace vlastností workflow

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat různé vlastnosti workflowu.

Pokud chcete konfigurovat vlastnosti workflowu, otevřete workflow v editoru workflowu. Klikněte na plátno editoru workflowu a klepněte na tlačítko **Vlastnosti** k otevření stránky **Vlastnosti**. Pro konfiguraci vlastností workflowu můžete použít následující kroky.

## <a name="name-the-workflow"></a>Pojmenování workflowu

Pomocí následujících kroků zadejte název workflowu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Název** zadejte jedinečný název workflowu. Předpokládejme například, že vytváříte workflowy nákupních požadavků pro každou zemi nebo oblast, ve které působíte. Pro workflow nákupního požadavku můžete například zadat název **Nákupní požadavky – Dánsko** nebo **Nákupní požadavky – Španělsko**.

## <a name="specify-the-workflow-owner"></a>Zadání vlastníka workflowu

Vlastník workflowu je osoba, která bude spravovat workflow. Vlastníka workflowu můžete zadat provedením následujícího postupu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V seznamu **Vlastník** vyberte jméno osoby, který bude spravovat tento workflow.

## <a name="select-an-email-template"></a>Výběr šablony e-mailu

Podle těchto kroků vyberte šablonu e-mailu, která se používá k vytvoření oznámení o workflowu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V seznamu **Šablona e-mailu k oznámení pro workflow** vyberte šablonu.

## <a name="enter-instructions-for-users"></a>Zadání pokynů pro uživatele

Můžete zadat pokyny pro uživatele, kteří budou odesílat dokumenty ke zpracování a schválení. Tito uživatelé jsou označovány jako *původci*. Budeme například předpokládat, že vytváříte workflow nákupní žádanky, a že jste zadali pokyny. Tyto pokyny mohou zobrazit uživatelé zadáním nákupního požadavku na stránce **Nákupní požadavky**. Původce může zobrazit pokyny klepnutím na příslušnou ikonu na panelu zpráv pro workflow. Pokyny pro uživatele můžete zadat provedením následujícího postupu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Pokyny pro odeslání** zadejte pokyny.
3. Pokyny můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení pokynů uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:

    1. Klepnutím v poli **Pokyny pro odeslání** zadejte, kde se má zástupný text zobrazit.
    2. Klikněte na **Vložit zástupný text**.
    3. V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4. Klepněte na tlačítko **Vložit**.

4. Chcete-li přidat překlady pokynů, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Text můžete přizpůsobit vložením zástupného textu. Pokyny, jak zadat zástupný text, naleznete v kroku 3.
    6. Klepněte na tlačítko **Zavřít**.

## <a name="specify-when-this-workflow-is-used"></a>Určete, kdy se má použít tento workflow.

Můžete vytvořit více workflowů založených na stejném typu. Můžete například vytvořit workflow nákupních požadavků, pro každou zemi nebo oblast, ve které působíte, například Nákupní požadavky – Dánsko a Nákupní požadavky – Španělsko. Pokud máte více workflowů založených na stejném typu, je nutné zadat, kdy má být který workflow použit. U předchozího příkladu zadáte následující podmínky:

- Nákupní požadavky – Dánsko se má používat v případě, že země či oblast = DK
- Nákupní požadavky – Španělsko se má používat v případě, že země či oblast = ES

Pomocí následujících kroků zadejte, kdy se má použít workflow, který konfigurujete.

1. V levém podokně klikněte na **Aktivace**.
2. Označte pole **Nastavit podmínky pro spuštění tohoto workflowu**.
3. Klepněte na možnost **Přidat podmínku**.
4. Zadání podmínky
5. Zadejte všechny další podmínky, které jsou požadovány.
6. Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:

    1. Klepněte na možnost **Test**.
    2. Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam.
    3. Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám. Například pokud vytváříte workflow nákupního požadavku pro Španělsko, oblast **Ověřit podmínku** na stránce bude obsahovat seznam nákupních žádanek. Po klepnutí na možnost **Test** systém vyhodnotí vybraný nákupní požadavek, aby zjistil, zda země či oblast = ES.
    4. Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.

## <a name="specify-when-notifications-are-sent"></a>Zadejte, kdy se mají odesílat oznámení.

Když je dokument odeslán ke zpracování, je vytvořena instance workflowu. Uživatelům lze odeslat oznámení v případech, kdy jsou instance workflowu (na základě tohoto workflowu) spuštěny, dokončeny, zrušeny nebo zastaveny z důvodu chyby. Pomocí následujících kroků můžete zadat, kdy mají být odeslána oznámení.

1. V levém podokně klikněte na **Oznámení**.
2. Označte pole u každé události, která má spustit oznámení:

    - **Zahájeno** – odesílat oznámení při zahájení instance workflowu.
    - **Zastaveno** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu chyby.
    - **Dokončeno** – odesílat oznámení při dokončení instance workflowu.
    - **Bez možnosti obnovy** – odesílat oznámení v případě, že je instance workflowu zastavena z důvodu neobnovitelné chyby.
    - **Ukončeno** – odesílat oznámení při ukončení instance workflowu.

3. Vyberte řádek pro událost, kterou jste vybrali v kroku 2.
4. Na kartě **Text oznámení** zadejte text oznámení.
5. Text můžete přizpůsobit vložením zástupného textu. Zástupný text bude při zobrazení textu uživatelům nahrazen odpovídacími daty. Při vkládání zástupného textu postupujte takto:

    1. Klepnutím do pole zadejte, kde se má zástupný text zobrazit.
    2. Klikněte na **Vložit zástupný text**.
    3. V nově otevřeném seznamu vyberte vkládaný zástupný text.
    4. Klepněte na tlačítko **Vložit**.
    5. Běžný zástupce za **Text oznámení**, který má být zahrnut, je "Poslední poznámky: %Workflow.Last note%", který zobrazuje všechny komentáře z předchozího kroku.

6. Chcete-li přidat překlady textu, postupujte takto:

    1. Klikněte na **Překlady**.
    2. Na nově otevřené stránce klikněte na **Přidat**.
    3. V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.
    4. V poli **Přeložený text** zadejte text.
    5. Text můžete přizpůsobit vložením zástupného textu. Pokyny, jak zadat zástupný text, naleznete v kroku 5.
    6. Klepněte na tlačítko **Zavřít**.

7. Na kartě **Příjemce** použijte následující možnosti k určení příjemce oznámení.

    <table>
    <thead>
    <tr>
    <th>Možnost</th>
    <th>Oznámení bude odesláno těmto uživatelům</th>
    <th>Při odesílání oznámení postupujte takto</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Účastník</td>
    <td>Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</td>
    <td>
    <ol>
    <li>Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Účastník</strong>.</li>
    <li>Na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</li>
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel workflowu</td>
    <td>Uživatelé, kteří jsou účastníci tohoto workflowu</td>
    <td>
    <ol>
    <li>Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel workflowu</strong>.</li>
    <li>Na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte účastníka tohoto workflowu.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel</td>
    <td>Konkrétní uživatelé</td>
    <td>
    <ol>
    <li>Na kartě <strong>Příjemce</strong> klepněte na možnost <strong>Uživatel</strong>.</li>
    <li>Na kartě <strong>Uživatel</strong> obsahuje seznam <strong>Dostupní uživatelé</strong> všechny uživatele. Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Zadejte komentáře ke změnám provedeným v daném workflowu

Chcete-li zadat komentáře ke změnám provedeným u tohoto workflowu, proveďte následující kroky.

1. V levém podokně klikněte na **Poznámky**.
2. V poli **Zadat komentáře k workflowu** zadejte své poznámky.
3. Zkontrolujte své komentáře. Po přidání komentáře je již nelze upravit.
4. Kliknutím na **Přidat** přidáte komentáře do oblasti **Historie poznámek**.
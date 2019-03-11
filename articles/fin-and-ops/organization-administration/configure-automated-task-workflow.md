---
title: Konfigurace automatizovaných úloh ve workflowu
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a9f37228beedafa085987668d5c89b06c6c9d61
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "365102"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Konfigurace automatizovaných úloh ve workflowu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu.

Pokud budete chtít nakonfigurovat automatizovaný úkol v editoru workflowu, klikněte pravým tlačítkem myši na úkol a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Následně nakonfigurujte vlastnosti dílčího workflowu pomocí automatizovaného úkolu.

## <a name="name-the-task"></a>Pojmenování úlohy

Pomocí následujících kroků zadejte název automatizovaného úkolu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Do pole **Název** zadejte jedinečný název úlohy.

## <a name="specify-when-notifications-are-sent"></a>Zadejte, kdy se mají odesílat oznámení.

Lze odeslat oznámení uživatelům, kteří automatizovanou úlohu spustili nebo zrušili. Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.

1. V levém podokně klikněte na **Oznámení**.
2. Označte pole vedle událostí, při kterých se oznámení odešle:

    - **Spuštění** – oznámení jsou odeslána při spuštění úkolu.
    - **Zrušení** – oznámení jsou odeslána při zrušení úkolu.

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
    <li>V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Uživatel workflowu</td>
    <td>Uživatelé zúčastnění v aktuálním workflowu</td>
    <td>
    <ul>
    <li>Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Uživatel</td>
    <td>Konkrétní uživatelé Microsoft Dynamics 365 for Finance and Operations</td>
    <td>
    <ol>
    <li>Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</li>
    <li>Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations. Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.

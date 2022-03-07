---
title: Konfigurace workflow položky řádku
description: Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6d9dcb99e00d4ce3f99e525a72421cb12af178
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070114"
---
# <a name="configure-line-item-workflows"></a>Konfigurace workflow položky řádku

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku.

Pokud budete chtít nakonfigurovat prvek workflow položky řádku v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Pro konfiguraci vlastností prvku workflowu položky řádky můžete použít následující kroky.

## <a name="name-the-line-item-workflow-element"></a>Pojmenování prvku workflowu položky řádku

Pomocí následujících kroků zadejte název prvku workflowu položky řádky.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Název** zadejte jedinečný název prvku workflowu položky řádky.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Určení, zda se jeden workflow používá ke zpracování všech položek řádku

Tento postup slouží k určení, zda stejný workflow slouží ke zpracování všech položek řádku v dokumentu.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Pokud by měl stejný workflow zpracovávat všechny položky řádku v dokumentu, klepněte na tlačítko **Vyvolat jediný workflow pro všechny položky řádku**. Potom vyberte workflow, který slouží ke zpracování položek řádku.
3. Pokud má konkrétní workflow zpracovávat položky řádku, které splňují konkrétní sadu podmínek, klepněte na **Vyvolat workflow pro každou položku řádku**. Podle následujícího postupu určete sadu podmínek:

    1. Klepněte na možnost **Přidat**.
    2. V tabulce vyberte podmínku.
    3. Na kartě **Název podmínky** zadejte název sady podmínek, které definujete.
    4. Klepněte na volbu **Přidat podmínku** a zadejte podmínku.
    5. Zadejte všechny další podmínky, které jsou požadovány.
    6. Chcete-li ověřit, zda je zadaná sada podmínek nakonfigurována správně, klepněte na možnost **Testovací podmínka**. Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam a klikněte na **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám. Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.

    Na kartě **Workflow** vyberte workflow, který slouží ke zpracování položek řádků, které vyhovují sadě podmínek, které jste definovali.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
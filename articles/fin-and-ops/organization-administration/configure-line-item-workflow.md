---
title: "Konfigurace workflowu položky řádku"
description: "Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d30d6aeda6be7bc81763c0b3f20c568d3fc81526
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-line-item-workflow"></a>Konfigurace workflowu položky řádku

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku.

Pokud budete chtít nakonfigurovat prvek workflow položky řádku v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**. Pro konfiguraci vlastností prvku workflowu položky řádky můžete použít následující kroky.

## <a name="name-the-line-item-workflow-element"></a>Pojmenování prvku workflowu položky řádku
Pomocí následujících kroků zadejte název prvku workflowu položky řádky.

1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  V poli **Název** zadejte jedinečný název prvku workflowu položky řádky.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Určení, zda se jeden workflow používá ke zpracování všech položek řádku
Tento postup slouží k určení, zda stejný workflow slouží ke zpracování všech položek řádku v dokumentu.

1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  Pokud by měl stejný workflow zpracovávat všechny položky řádku v dokumentu, klepněte na tlačítko **Vyvolat jediný workflow pro všechny položky řádku**. Potom vyberte workflow, který slouží ke zpracování položek řádku.
3.  Pokud má konkrétní workflow zpracovávat položky řádku, které splňují konkrétní sadu podmínek, klepněte na **Vyvolat workflow pro každou položku řádku**. Podle následujícího postupu určete sadu podmínek:
    1.  Klepněte na možnost **Přidat**.
    2.  V tabulce vyberte podmínku.
    3.  Na kartě **Název podmínky** zadejte název sady podmínek, které definujete.
    4.  Klepněte na volbu **Přidat podmínku** a zadejte podmínku.
    5.  Zadejte všechny další podmínky, které jsou požadovány.
    6.  Chcete-li ověřit, zda je zadaná sada podmínek nakonfigurována správně, klepněte na možnost **Testovací podmínka**. Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam a klikněte na **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám. Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.

    Na kartě **Workflow** vyberte workflow, který slouží ke zpracování položek řádků, které vyhovují sadě podmínek, které jste definovali.






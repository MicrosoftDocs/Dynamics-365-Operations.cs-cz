---
title: Podrobení vrácených položek kontrole
description: Podrobení vrácených položek kontrole
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985784"
---
# <a name="take-returned-items-through-inspection"></a>Podrobení vrácených položek kontrole 

[!include [banner](../includes/banner.md)]


1.  Klikněte na **Řízení zásob** \> **Periodicky** \> **Správa kvality** \> **Karanténní příkazy** .

2.  Vyhledejte řádek objednávky, který odpovídá kontrolované vrácené položce.

    > [!NOTE]
    > <P>Karanténní příkaz lze přidružit pouze jednomu číslu zboží. Při vrácení 10 položek s různými čísly zboží v rámci jedné dodávky a při jejich odeslání do karantény dojde k vytvoření 10 samostatných karanténních příkazů.</P>

3.  Po prověření položky určete pomocí výběru v poli **Dispoziční kód** akci, která má být pro danou položku provedena, a způsob zpracování souvisejících finančních transakcí. Mezi příklady patří vrácení položky na sklad a refundace odběratele, vyřazení položky a odeslání náhradní položky odběrateli nebo vrácení položky odběrateli bez náhrady.
    
    > [!NOTE]
    > <P>V případě, že více položkám vráceným v rámci jedné dávky čísel položek nelze přiřadit stejný dispoziční kód, je nutné rozdělit karanténní příkaz (<STRONG>Funkce</STRONG> &gt; <STRONG>Rozdělit</STRONG>), aby bylo možné přiřadit jednotlivým dílčím dávkám různé dispoziční kódy.</P>


4.  Po dokončení kontroly můžete klepnutím na položku **Vykázat jako dokončené** vydat vrácené položky a vytvořit záznam deníku doručení položky. Osoba nebo oddělení, které zboží obdržely, poté deník zpracují, aby došlo k vrácení daného zboží do skladových zásob.
    
    - nebo -
    
    Ukončete karanténní příkaz a přesuňte položky zpět přímo na sklad pomocí jedné z funkcí tlačítka **Zásoby** .

5.  Uložte změny zavřením formuláře.

## <a name="see-also"></a>Viz také

[Určení způsobu nakládání s vrácenými položkami](specify-how-to-dispose-of-returned-items.md)

  



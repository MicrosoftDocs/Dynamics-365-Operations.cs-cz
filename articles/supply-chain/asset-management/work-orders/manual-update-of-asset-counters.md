---
title: Ruční aktualizace čítačů majetku
description: Toto téma popisuje manuální aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875548"
---
# <a name="manual-update-of-asset-counters"></a>Ruční aktualizace čítačů majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Čítače slouží k vytváření registrací položek majetku, které se týkají například počtu hodin v provozu nebo vyrobeného množství.

Pokud je vybraný typ čítače nastaven na hodnotu zdědit hodnoty čítačů (pevná záložka **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače** > **Obecné** > přepínací tlačítko **zdědit hodnoty čítačů majetku** nastavené na hodnotu Ano), po vytvoření nového řádku čítače tohoto typu bude každý podřízený majetek, který používá stejný typ čítače, automaticky aktualizován.

V položce **Všechen majetek** vytváříte hodiny nebo registrace čítačů množství na majetku na základě vašich hodnot majetku.

1. Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.

2. Vyberte majetek v seznamu a klikněte na možnost **Čítače**. Ve formuláři **Čítače majetku** se zobrazí seznam všech předchozích registrací čítačů vybraného majetku.

3. Kliknutím na tlačítko **Nový** vytvořte novou registraci. ID majetku je vloženo automaticky.

4. V poli **Čítač** vyberte relevantní čítač. K dispozici jsou pouze čítače související s typem majetku vybraným pro majetek. Související jednotka je automaticky vložena do pole **Jednotka**.

5. Vyberte datum a čas pro registraci čítače.

6. Do pole **Hodnota** zadejte číslo od poslední registrace čítače, nebo v poli **Agregovaná hodnota** zadejte celkové číslo.

- Pokud fyzicky instalujete do majetku nový čítač, je nutné provést registraci v položce majetku v **Čítačích majetku**. Dále je nutné vytvořit dva řádky registrace s identickými časovými razítky a na řádku, který se týká nového čítače, zaškrtněte tlačítko **Vynulovat čítač**. Po vytvoření dvou řádků registrace musí být první řádek pro čítač, který nahrazujete. V poli **Celkem** je celkové číslo součtem čítače všech registrovaných hodnot tohoto typu čítače.  
- Pokud je u majetku zaškrtnuto políčko **Vynulovat čítač** s použitím plánu údržby s typem intervalu "jednou z..." nebo "po dosažení...", čítač je v novém řádku čítače stále aktivní, protože vytváříte oddělený řádek čítače a začínáte znovu s novým čítačem.

![Obrázek č. 1](media/11-work-orders.png)


Chcete-li provést registrace čítačů u několika majetků, lze to provést v **Správa majetku** > **Dotazy** > **Majetek** > **Čítače majetku**.

>[!NOTE]
>Můžete nastavit rozsah pro definování odchylek ručních registrací čítačů a typ zprávy, která se má zobrazit, pokud se registrace nacházejí mimo definovaný rozsah. Informace o nastavení čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).

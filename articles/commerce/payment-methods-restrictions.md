---
title: Omezení platebních metod pro vrácení bez příjemky
description: Toto téma popisuje, jak lze určité typy plateb omezit pro refundaci, pokud jsou vrácení provedená bez příjemky.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: dd07c9c95639c8e69e1013fd7da283cf51b60ed0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804520"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Omezení platebních metod pro vrácení bez příjemky


[!include [banner](includes/banner.md)]

Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému. Toto téma popisuje, jak lze určité typy plateb omezit pro refundaci, pokud jsou vrácení provedená bez příjemky.

## <a name="set-up-payment-methods"></a>Nastavení metod platby

K nastavení způsobů platby je třeba dokončit následující úlohy.
1. Vytvořte metody platby, které jsou přijímány v rámci celé organizace.
2. Vytvoření celoorganizačních typů karet a čísel karet. Budou-li přijímány kreditní nebo debetní karty, je třeba vytvořit jeden typ úhrady pro karty a poté vytvořit celoorganizační typy karet a čísla karet.
3. Nastavte platební metody obchodu. Přiřaďte způsoby plateb ke každému obchodu a poté zadejte konkrétní nastavení pro každý způsob platby.
4. Nastavte karetní platební metody pro obchody. Pro jakékoli metody platby kartou, které obchod přijímá, dokončete nastavení karty.

![Nastavení obchodu](media/NoReceiptReturns1.png "Nastavení maloobchodu") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Omezení platebních metod pro vrácení bez příjemky

Pro každý způsob platby obchodu nastavte na stránce **Řízení obchodu** pod položkou **Bez vratky** možnost **Omezit pro refundace bez příjemky** na **Ano**. 

Výchozí hodnota přepínače je **Ne**, což zaručuje, že metoda platby pro refundaci je povolena. 

Když je možnost **Omezit pro refundace bez příjemky** nastavena na **Ano**, zvolená metoda platby nebude pro refundace povolena. 

![Způsob platby obchodu](media/NoReceiptReturns3.png "Způsob platby v maloobchodu") 

> [!NOTE]
> Pokud pokladník vybere způsob platby, který je omezen pro refundaci bez příjemky, zobrazí se zpráva pro ověření přijatelných způsobů platby.

![Přijatelné způsoby platby](media/NoReceiptReturns4.png "Přijatelné způsoby platby") 

Pokud má transakce vrácení s příjemkou i bez příjemky, podmínky omezení nebudou vynuceny, protože transakce bude workflow vrácení s příjemkou. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
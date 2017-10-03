--- 
title: "Zaznamenání příjmu zboží na nákupní objednávce"
description: "Tento postup popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 01fbf4964dfcecab272204db9c3f5068ca1879cb
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Zaznamenání příjmu zboží na nákupní objednávce

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce. Dále je možné zaregistrovat příjemku produktu ve skladu a poté později ji zaznamenat na nákupní objednávce. Tato úloha je provedena obvykle nákupčím nebo koordinátorem závazků. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Příklad obsahuje kroky k vytvoření jednoduché nákupní objednávky tak, že umístíte postup jako průvodce úkolem. Pokud jste použili postup na vlastních datech, můžete spustit dílčí úkol Záznam příjmu zboží.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Příprava nové nákupní objednávky pro příjem zboží
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu US-101 do pole Účet dodavatele.
4. Klikněte na tlačítko OK.
5. V poli Číslo zboží zadejte 'M0001'.
6. Zadejte číslo 5 do pole Množství.
7. V podokně akcí klikněte na položku Nákup.
8. Klikněte na tlačítko Potvrdit.

## <a name="record-receipt-of-goods"></a>Záznam příjmu zboží
1. V podokně akcí klikněte na položku Přijmout.
2. Klikněte na položku Příjemka produktu.
    * Pole Množství umožňuje nastavit různé možnosti pro množství, které chcete obdržet. Pokud již bylo množství zaregistrováno ve skladu, můžete vybrat Registrované množství.  Pro tuto hodnotu použijte hodnotu Objednané množství.   
3. Zadejte libovolnou hodnotu do pole Příjemka produktu.
    * Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.  
4. Rozbalte sekci Řádky.
5. Nastavte množství na hodnotu 4.
    * Zde je možné ručně zadat množství přijaté pro každý řádek objednávky.  
6. Sbalte oddíl Řádky.
7. Klikněte na tlačítko OK.
    * Zboží bylo zaznamenáno jako obdržené v nákupní objednávce a deník příjemek produktů byl vytvořen jako dokument, který tuto akci odráží. Akci Příjemka produktu můžete použít ke kontrole deníků vytvořených s nákupní objednávkou a zobrazit tak, co bylo přijato, a kdy.  



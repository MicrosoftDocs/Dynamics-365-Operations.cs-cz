---
title: Zaznamenání příjmu zboží na nákupní objednávce
description: Tento článek popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882453"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Zaznamenání příjmu zboží na nákupní objednávce

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak pořídit záznam příjmu zboží přímo na nákupní objednávce. Dále je možné zaregistrovat příjemku produktu ve skladu a poté později ji zaznamenat na nákupní objednávce. Tato úloha je provedena obvykle nákupčím nebo koordinátorem závazků. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Příklad obsahuje kroky k vytvoření jednoduché nákupní objednávky tak, že umístíte postup jako průvodce úkolem. Pokud jste použili postup na vlastních datech, můžete spustit dílčí úkol **Záznam příjmu zboží**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Příprava nové nákupní objednávky pro příjem zboží
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**.
2. Zvolte **Nové**.
3. Do pole **Účet dodavatele** zadejte `US-101`.
4. Vyberte **OK**.
5. Do pole **Číslo položky** zadejte `M0001`.
6. Do pole **Množství** zadejte `5`.
7. V podokně akcí klikněte na možnost **Zakoupit**.
8. Vyberte **Potvrdit**.

## <a name="record-receipt-of-goods"></a>Záznam příjmu zboží
1. V podokně akcí klikněte na možnost **Přijmout**.
2. Vyberte **Příjemka produktu**. Pole **Množství** umožňuje nastavit různé možnosti pro množství, které chcete obdržet. Pokud již bylo množství zaregistrováno ve skladu, můžete vybrat **Registrované množství**. Pro tuto hodnotu použijte hodnotu **Objednané množství**.
3. Rozbalte sekci **Přehled**.
4. Do pole **Příjemka produktu** zadejte libovolnou hodnotu. Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.  
5. Rozbalte sekci **Řádky**.
6. Nastavte **Množství** na hodnotu 4. Zde je možné ručně zadat množství přijaté pro každý řádek objednávky.  
7. Vyberte **OK**. Zboží bylo zaznamenáno jako obdržené v nákupní objednávce a deník příjemek produktů byl vytvořen jako dokument, který tuto akci odráží. Akci Příjemka produktu můžete použít ke kontrole deníků vytvořených s nákupní objednávkou a zobrazit tak, co bylo přijato, a kdy.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
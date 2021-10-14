---
title: Nastavení intervalů servisu
description: Toto téma popisuje, jak nastavit intervaly servisu. Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.
author: kamaybac
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0aeaef9fcf0c909638a9452633a321121e20814
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567840"
---
# <a name="set-up-service-intervals"></a>Nastavení intervalů servisu  

[!include [banner](../includes/banner.md)]

Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.

1. Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Intervaly servisu**.
2. Vytvořte nový interval servisu.
3. Zadejte ID a popis intervalu servisu.
4. Rozsah vyberte v poli **Rozsah**.
5. Do pole **Frekvence** zadejte frekvenci. Četnost je koeficient, kterým je nutné vynásobit rozsah, abyste získali interval servisní smlouvy.
6. Stiskem kláves **Alt+S** interval servisu uložte.

## <a name="example"></a>Příklad

Chcete například vytvořit interval servisu o délce 10 dní.

**Vytvoření intervalu servisu o délce 10 dní**

1. Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Intervaly servisu**.
2. Vytvořte nový interval servisu.
3. Zadejte ID a popis intervalu servisu.
4. V poli **Rozsah** vyberte **Denně**.
5. Do pole **Četnost** zadejte hodnotu 10.
6. Stiskem kláves **Alt+S** interval servisu uložte.

## <a name="related-topics"></a>Související témata

[Intervaly servisu](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Nastavení intervalů servisu
description: Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: aee440226c4bda40f9f14b3b6b1edc2cc495574d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242462"
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
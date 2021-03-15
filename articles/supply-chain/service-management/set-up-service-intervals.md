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
ms.openlocfilehash: 815da6b24de401ad11febb0b0564738ce6967a9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991658"
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
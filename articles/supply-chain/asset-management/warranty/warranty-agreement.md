---
title: Záruční smlouvy
description: Toto téma popisuje záruční smlouvy v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021497"
---
# <a name="warranty-agreements"></a>Záruční smlouvy

[!include [banner](../../includes/banner.md)]

 


V modulu Správa majetku můžete nastavit záruční podmínky, které mohou být spojeny s majetkem nebo typem majetku. Jsou vytvořeny záruční podmínky pro určité období. Záruku lze nastavit tak, aby poskytovala úplné pokrytí nebo částečné pokrytí, a můžete nastavit podmínky, které souvisejí s hodinami, výdaji a položkami.

Prvním krokem je vytvoření libovolných záručních smluv dodavatele, které máte pro své vybavení. Poté připojíte záruční smlouvy k majetku nebo typům majetku. Záruční smlouvy dodavatele se používají pouze pro informativní účely. Pokud je u majetku nastavena záruka dodavatele, můžete zobrazit období krytí záruky majetku.

## <a name="create-a-warranty-agreement"></a>Vytvoření záruční smlouvy

Záruční smlouva může zahrnovat několik řádků smlouvy, které pokryjí záruku za pracovní dobu, výdaje a položky.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Záruka**.
2. Zvolte **Nový** pro vytvoření produktu.
3. V poli **Záruka** zadejte ID záruky. 
4. Do pole **Název** zadejte popis.

    Na pevné záložce **Podrobnosti** pole **Majetek** zobrazuje množství aktivního majetku, který používá záruční smlouvu.

5. Na pevné záložce **Řádky záruky** postupujte podle těchto kroků a přidejte řádky, které by měly být součástí záruční smlouvy:

    1. Zvolte **Přidat řádek** a přidejte k záruce novou podmínku. Do pole **Řádek** se automaticky zadá pořadové číslo řádku.
    2. V poli **Období** vyberte typ období záruky.
    3. V poli **Interval** zadejte požadované číslo. Toto pole definuje počet období, pro která má být záruka platná.
    4. V poli **Procento** zadejte procento disponibility pro řádek záruky. Procentuální hodnota označuje, kolik je kryto vaší společností.

![Stránka Záruka](media/01-warranty.png)

---
title: Záruční smlouvy
description: Toto téma popisuje záruční smlouvy v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874686"
---
# <a name="warranty-agreements"></a>Záruční smlouvy

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


V modulu Správa majetku můžete nastavit záruční podmínky, které mohou být spojeny s majetkem nebo typem majetku. Jsou vytvořeny záruční podmínky pro určité období. Záruku lze nastavit tak, aby poskytovala úplné pokrytí nebo částečné pokrytí, a můžete nastavit podmínky, které souvisejí s hodinami, výdaji a položkami.

Prvním krokem je vytvoření libovolných záručních smluv dodavatele, které máte pro své vybavení. Poté připojíte záruční smlouvy k majetku nebo typům majetku. Záruční smlouvy dodavatele se používají pouze pro informativní účely. Pokud je u majetku nastavena záruka dodavatele, můžete zobrazit období krytí záruky majetku.

## <a name="create-a-warranty-agreement"></a>Vytvoření záruční smlouvy

Záruční smlouva může zahrnovat několik řádků smlouvy, které pokryjí záruku za pracovní dobu, výdaje a položky.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Záruka**.
2. Zvolte **Nový** pro vytvoření produktu.
3. V poli **Záruka** zadejte ID záruky.
4. Do pole **Název** zadejte popis.

    Na pevné záložce **Podrobnosti** pole **Majetek** zobrazuje množství aktivního majetku, který používá záruční smlouvu.

5. Na pevných záložkách **Hodinová záruka** a **Položková záruka** přidejte řádky, které mají být zahrnuty do záruční smlouvy týkající se hodin nebo položek, pomocí následujících kroků:

    1. Zvolte **Přidat řádek** a přidejte k záruce novou podmínku. Do pole **Řádek** se automaticky zadá pořadové číslo řádku.
    2. V poli **Období** vyberte typ období záruky.
    3. V poli **Interval** zadejte požadované číslo. Toto pole definuje počet období, pro která má být záruka platná.
    4. V poli **Procento** zadejte procento disponibility pro řádek záruky. Procentuální hodnota označuje, kolik je kryto vaší společností.

![Obrázek č. 1](media/01-warranty.png)

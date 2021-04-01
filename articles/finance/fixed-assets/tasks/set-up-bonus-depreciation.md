---
title: Nastavení počátečního mimořádného odpisu
description: Tento postup popisuje vytvoření nové náhrady za zvláštní odpisy a její přiřazení ke knize dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6627e7fa9a1eb1a9131ec7e2c3cc823b49b286cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257554"
---
# <a name="set-up-bonus-depreciation"></a>Nastavení počátečního mimořádného odpisu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje vytvoření nové náhrady za zvláštní odpisy a její přiřazení ke knize dlouhodobého majetku. Využívá účetní role a ukázková data pro právnické osoby USMF.


## <a name="create-a-special-depreciation-allowance"></a>Vytvoření náhrady za zvláštní odpisy
1. Přejděte do části Dlouhodobý majetek > Nastavení > Náhrada za zvláštní odpisy.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Náhrada za zvláštní odpisy.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Procento zadejte požadované číslo.
    * Pokud nebylo určeno procento, nastavte částku.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Přiřazení náhrady za zvláštní odpisy ke knize pro skupinu dlouhodobého majetku
1. Přejděte do části Dlouhodobý majetek > Nastavení > Skupiny dlouhodobého majetku.
2. V seznamu vyberte skupinu dlouhodobého majetku, která je přiřazena k náhradě za zvláštní odpisy.
3. Klepněte na Knihy.
4. V seznamu vyberte knihu, která je přiřazena k náhradě za zvláštní odpisy.
5. Klikněte na Náhrada za zvláštní odpisy.
6. Klikněte na položku Nová.
7. V poli Náhrada za zvláštní odpisy zadejte nebo vyberte hodnotu.
    * Výchozí hodnota pro procento nebo částku je převzatá z nastavení náhrady za zvláštní odpisy.  
8. V poli Priorita zadejte číslo.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
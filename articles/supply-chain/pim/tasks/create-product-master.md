---
title: Vytvoření základního produktu
description: Vytvořte základní produkt pro předem definované varianty.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e76c367d4aa6c08332371374a26dd6fdbbdb4eb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577329"
---
# <a name="create-a-product-master"></a>Vytvoření základního produktu

[!include [banner](../../includes/banner.md)]

Vytvořte základní produkt pro předem definované varianty. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro návrháře produktu.


## <a name="create-a-new-product-master"></a>Vytvoření základního produktu
1. Přejděte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Základní produkty**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Číslo produktu**. Číslo musí být jedinečné. Číselnou řadu lze nastavit pro pole **Číslo produktu**. V tomto případě uživatel nemusí zadat hodnotu.
4. Do pole **Název produktu** zadejte hodnotu. Zadejte popisný název produktu. Vyhledávací název je výchozí hodnota, ale lze ji uživatelem změnit.
5. V poli **Skupina dimenzí produktů** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. Skupina dimenzí produktu určuje, které čtyři dimenze produktu lze použít k vytvoření variant produktu. V tomto příkladu se používá skupina s barvou a velikostí.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu. Výchozí **Technologie konfigurace** je ‚předem definovaná varianta‘. Bude použita v tomto příkladu.
8. Klikněte na tlačítko **OK**.

## <a name="select-product-dimension-groups"></a>Volba skupin dimenzí produktů
1. V poli **Skupina barev** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V poli **Skupina velikostí** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
6. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="add-dimension-groups"></a>Přidání skupin dimenzí
1. V **podokně akcí** klikněte na **Produkt**.
2. Kliknutím na možnost **Skupiny dimenzí** otevřete dialog Zanechat.
3. V poli **Skupina dimenze úložiště** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. Dimenze uskladnění řídí způsob uložení položek ve skladu a jejich vydávání. Dimenze uskladnění mohou například zahrnovat pracoviště a sklad.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli **Skupina sledovací dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. Skupina sledovacích dimenzí určuje sledovací dimenze, které je možné přidat k produktu. Například číslo dávky a sériové číslo slouží ke sledování skladových položek.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klikněte na tlačítko **OK**.
10. Klikněte na možnost **Uložit**.
11. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
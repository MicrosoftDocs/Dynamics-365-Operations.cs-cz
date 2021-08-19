---
title: Aktualizace rozpočtů údržby
description: Toto téma vysvětluje, jak aktualizovat rozpočet údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c054cb96d56e40e35ee44142396f59d61395263ff41232423f6c7911478b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724933"
---
# <a name="update-maintenance-budgets"></a>Aktualizace rozpočtů údržby

[!include [banner](../../includes/banner.md)]

 

Na stránce **Řádky rozpočtu údržby** jsou zobrazeny všechny řádky rozpočtu, které byly vytvořeny pro rozpočet vybraný na stránce **Rozpočty údržby**. (Další informace naleznete v tématu [Vytvoření rozpočtů údržby](create-maintenance-budget.md).) Řádky rozpočtu údržby lze přepočítat a upravit, dokud není schválen rozpočet údržby. Po uplynutí rozpočtového období a zaúčtování nákladů do Správy majetku lze také aktualizovat řádky rozpočtu skutečnými náklady.

## <a name="recalculate-a-maintenance-budget"></a>Přepočítání rozpočtu údržby

Rozpočet údržby lze přepočítat na stránce **Řádky údržby rozpočtu**. Při přepočtu rozpočtu údržby budou stávající řádky rozpočtu odstraněny a bude proveden nový výpočet.

1. Na stránce **Řádky údržby rozpočtu** vyberte možnost **Přepočítat**.
2. V dialogovém okně **Přepočítat rozpočet** proveďte požadované změny nového výpočtu a poté klepněte na tlačítko **OK**.

Nové řádky rozpočtu jsou vytvořeny podle hodnot, které jste nastavili.

## <a name="adjust-budget-lines"></a>Upravit řádky rozpočtu

Namísto přepočítání celého rozpočtu údržby můžete upravit vybrané řádky, které se vztahují k rozpočtovým nákladům.

1. Na stránce **Řádků rozpočtu údržby** vyberte řádky, pro které chcete aktualizovat rozpočtové náklady.
2. Vyberte možnost **Upravit**.
3. Chcete-li přidat částku do vybraných řádků, zaškrtněte políčko **Přidat náklady** a poté zadejte hodnotu do pole **Přidat hodnotu**.
4. Chcete-li vynásobit rozpočtové náklady na vybraných řádcích rozpočtu podle koeficientu, zaškrtněte políčko **Vynásobit náklady** a zadejte koeficient do pole **Hodnota násobku**.

    Zadáte-li například **1,2** do pole **Hodnota násobku**, budou rozpočtové náklady na vybraných řádcích zvýšeny o 20 procent. Zadáte-li **0,7**, snížíte rozpočtové náklady na vybrané řádky o 30 procent.

5. Vyberte **OK**.

Vybrané řádky rozpočtu se aktualizují podle hodnot, které jste nastavili v kroku 3 nebo 4.

## <a name="update-actual-costs"></a>Aktualizovat skutečné náklady

Po uplynutí dat v řádcích rozpočtu a zaúčtování skutečných nákladů do Správy majetku lze také aktualizovat rozpočet údržby skutečnými náklady.

1. Na stránce **Řádky údržby rozpočtu** vyberte možnost **Aktualizovat náklady**.
2. V dialogovém okně **Vypočítat skutečné náklady** vyberte **OK**.

Pole **Skutečné náklady** v řádcích rozpočtu se aktualizují v případě, že byly zaúčtovány skutečné náklady. Nové řádky rozpočtu mohou být generovány, pokud byly vytvořeny nové typy majetku od vytvoření rozpočtu a pokud byly tyto typy majetku použity pro majetek, pro který byly vytvořeny pracovní příkazy a pro které byly zaúčtovány související náklady. Nové řádky rozpočtu zobrazují pouze skutečné náklady, protože pro ně nebyly vypočítány žádné rozpočtové náklady.

> [!NOTE]
> Chcete-li zobrazit přehled skutečných nákladů rozdělených na preventivní, opravné a investiční náklady, můžete provést výpočet pro stejné období na stránce **Řízení nákladů majetku**. 

## <a name="manually-add-budget-lines"></a>Přidat řádky rozpočtu ručně

Na stránce **Řádky údržby rozpočtu** můžete ručně přidat nový řádek rozpočtu výběrem možnosti **Nový** a výběrem možnosti na řádku. Zde je několik příkladů situací, kdy může být tento přístup užitečný:

- Víte, že renovace některého majetku je aktuálně ve fázi plánování, ale související úlohy ještě nebyly vytvořeny ve správě majetku. Chcete však, aby byly rozpočtové náklady pro tyto úlohy zahrnuty do rozpočtu údržby.
- Od tvorby rozpočtu údržby byl vytvořen nový majetek nebo nové typy majetku, ale plány údržby dosud nebyly nastaveny pro tento majetek nebo typy majetku. Chcete však, aby byly rozpočtové náklady pro tyto typy majetku zahrnuty do rozpočtu údržby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
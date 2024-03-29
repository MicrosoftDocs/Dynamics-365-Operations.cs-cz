---
title: Vytvoření rozpočtů údržby
description: Tento článek vysvětluje, jak vytvořit rozpočet údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858033"
---
# <a name="create-maintenance-budgets"></a>Vytvoření rozpočtů údržby

[!include [banner](../../includes/banner.md)]

 



Rozpočty údržby se používají k poskytnutí přehledu o očekávaných nákladech pro preventivní údržbu. Řádky rozpočtu jsou vypočítány na základě řádků plánu údržby, které mají očekávané počáteční datum během rozpočtového období.

Rozpočty údržby jsou založeny na typech nákladů, které se používají ve správě majetku: **Preventivní** **Opravný** a **Investice**. Rozpočtové náklady na údržbu investic jsou zahrnuty pro aktivní majetek, který má datum náhrady během rozpočtového období a související náhradní hodnotu. Rozpočtové náklady na opravnou údržbu jsou zahrnuty v případě, že do výpočtu rozpočtu bude zahrnuto dřívější opravné datum. V takovém případě se opravné náklady z předchozího období vypočítávají pro stejné budoucí období, pro které počítáte rozpočet údržby.

## <a name="create-a-maintenance-budget"></a>Vytvoření rozpočtu údržby

1. Vyberte **Správa majetku** \> **Dotazy** \> **Rozpočet údržby** \> **Rozpočet**.
2. Zvolte **Vytvořit rozpočet**.
3. Do pole **Rozpočet údržby** zadejte ID rozpočtu.
4. Zadejte popis do pole **Popis**.
4. Na záložce s náhledem **Období** zadejte do polí **Od data** a **Do data** počáteční a koncová data rozpočtového období.
5. Chcete-li zahrnout opravné rozpočtové náklady, které jsou vypočteny na základě skutečných nákladů z předchozího období, zadejte do pole **Opravné od data** počáteční datum období, ze kterého by tyto náklady měly být zahrnuty.
6. V závislosti na úrovni podrobností, které jsou v rozpočtu požadovány, nastavte na pěti záložkách s náhledem **Seskupit podle** příslušné možnosti.
7. Vyberte **OK**.
8. Vyberte **Řádky rozpočtu** pro otevření stránky **Řádky rozpočtu údržby**, kde můžete zobrazit všechny řádky rozpočtu, které byly vytvořeny pro dané období.
9. Chcete-li rozpočet schválit, vyberte jej na stránce **Rozpočty údržby** a poté vyberte **Schválit**. Poté v dialogovém okně **Schválit rozpočet** vyberte možnost **OK**. Vaše jméno je zadáno v poli **Schválil/a** na stránce **Rozpočty údržby**.

    > [!NOTE]
    > Po schválení rozpočtu údržby nelze přepočítat nebo upravit související řádky na stránce **Řádky rozpočtu údržby**, pokud jste nejprve neodebrali schválení. Chcete-li odstranit schválení rozpočtu údržby, vyberte jej na stránce **Rozpočty údržby** a poté vyberte **Schválit**. Poté v dialogovém okně **Schválit rozpočet** vyberte možnost **OK**.

![Rozpočty údržby.](media/01-maintenance-budgets.png)

Nový rozpočet údržby můžete také vytvořit zkopírováním existujícího rozpočtu. Na stránce **Rozpočty údržby** vyberte rozpočet, který chcete kopírovat, a poté vyberte **Kopírovat**. Tento přístup je užitečný, pokud jste například vytvořili rozpočet na jeden měsíc a chcete jej zkopírovat do dalších měsíců.

> [!NOTE]
> Rozpočet údržby vypočítá pouze rozpočtové náklady založené na řádcích rozvrhu údržby. Chcete-li vypočítat skutečné náklady pro stejné období, můžete provést výpočet na stránce **Kontrola nákladů majetku**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
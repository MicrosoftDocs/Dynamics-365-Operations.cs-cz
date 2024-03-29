---
title: Rozdělení dlouhodobého majetku
description: Tento článek vysvětluje, jak rozdělit procento jedné knihy majetku na novou knihu majetku.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880781"
---
# <a name="split-a-fixed-asset"></a>Rozdělení dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak rozdělit procento jedné knihy majetku na novou knihu majetku. 

## <a name="create-a-new-fixed-asset"></a>Vytvořit nový dlouhodobý majetek

1. V navigačním podokně přejděte na **Moduly \> Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
2. Zvolte **Nové**.
3. Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**. Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.
4. Zadejte hodnotu do pole **Název**.
5. Zavřete formulář.

## <a name="split-a-fixed-asset"></a>Rozdělení dlouhodobého majetku

Před rozdělením plně odepsaného majetku je třeba ručně změnit stav rezervace majetku ze **Zavřeno** na **Otevřeno**. Tento krok je nutný, protože stav rezervace musí být **Otevřeno**, pokud musíte pro majetek zaúčtovat transakce (například při odprodeji po vyřazení). Musíte také zapnout parametr **Povolit více transakcí v rámci jednoho dokladu** na kartě **Obecné** stránky **Obecné parametry hlavní knihy**. Po změně stavu knihy aktiv a povolení více transakcí v rámci jednoho dokladu proveďte následující kroky k rozdělení majetku.

1. V seznamu najděte a vyberte odkaz na dlouhodobý majetek, který chcete rozdělit.
2. Vyberte **Knihy**. Vyberte knihu určenou pro rozdělení na nový majetek.
3. Vyberte **Funkce**.
4. Vyberte **Rozdělit dlouhodobý majetek**.
5. Zadejte nebo vyberte hodnotu v poli **Do dlouhodobého majetku**.
6. V poli **Do knihy** vyberte tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Zadejte datum do pole **Datum transakce**.
8. Zadejte číslo do pole **Procento**.
9. V poli **Název deníku** zadejte nebo vyberte hodnotu.
10. Vyberte **OK**.

## <a name="post-the-journal-transaction"></a>Zaúčtování transakce deníku

1. V navigačním podokně přejděte na **Moduly \> Dlouhodobý majetek \> Položky deníku \> Deník dlouhodobého majetku**.
2. V seznamu vyberte deník vytvořený pomocí procesu rozdělení.
3. Vybrat **řádky**.

    - Ověřte, že byly vytvořeny řádky deníku.
    - Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.
    - Je vytvořena transakce pořízení pro nový majetek na stejnou částku.

4. Zvolte **Zaúčtovat**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

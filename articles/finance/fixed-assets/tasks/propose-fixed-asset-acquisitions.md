---
title: Nabídka pořízení dlouhodobého majetku
description: Tento článek popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.
author: moaamer
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35d2171dc828cb0227f310e81be1d3e3359f41c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909062"
---
# <a name="propose-fixed-asset-acquisitions"></a>Nabídka pořízení dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Tento článek popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku. Využívá účetní role a ukázková data pro právnické osoby USMF. Chcete-li získat dlouhodobý majetek prostřednictvím deníku návrhu dlouhodobého majetku, musíte nejprve vytvořit záznam dlouhodobého majetku a poté definovat pořizovací cenu v majetkové knize.

## <a name="create-an-asset-acquisition-proposal"></a>Vytvoření návrhu na pořízení majetku

Chcete-li vytvořit návrh na pořízení majetku, proveďte následující kroky. 

1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.
2. Zvolte **Nové**.
3. V poli **Název** zadejte nebo vyberte hodnotu.
4. V podokně akcí zvolte **Řádky**.
5. Vyberte **Návrhy**.
6. Vyberte **Návrh pořízení**.
7. Vyberte **Filtr**. Kliknutím na tlačítko **Vynulovat** vymažete předchozí hodnoty.
8. Vyberte řádek **Číslo dlouhodobého majetku**.
9. V poli **Kritéria** zadejte nebo vyberte hodnotu. Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.  
10. Chcete-li ukončit podokno, klepněte dvakrát na tlačítko **OK**.
- Ověřte, že byly vytvořeny řádky transakce.  
- V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.  
11. Na stránce vyberte kartu **Knihy**.
12. Zvolte **Zaúčtovat**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Zahrnutí výchozích finančních dimenzí do návrhu pořízení majetku

Transakci pořízení majetku lze vytvořit pomocí doplňků aplikace Excel v části **Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**. Vytvořte nový deník a přejděte do sekce **Řádky** na stránce. Vyberte ikonu Excelu a poté vyberte řádek deníku dlouhodobého majetku. Systém vytvoří a otevře šablonu aplikace Excel představující řádky deníku. Můžete přidat data pro řádky deníku, které přidáváte do šablony, a poté tyto informace publikovat zpět do systému. 

Pokud byly nastaveny výchozí dimenze pro vybranou knihu majetku a odpovídající dlouhodobý majetek, který byl zadán v šabloně aplikace Excel, budou výchozí finanční dimenze volány z hlavních dat knihy majetku, když je deník publikován z aplikace Excel do systému. Chcete-li finanční dimenze do knihy majetku zahrnout automaticky při publikování deníku dlouhodobého majetku z doplňku Excelu, je třeba předem nastavit výchozí dimenze.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]

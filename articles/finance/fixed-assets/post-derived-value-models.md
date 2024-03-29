---
title: Zaúčtování pomocí odvozených knih
description: Tento článek popisuje, jak lze používat odvozené knihy.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682850"
---
# <a name="post-with-derived-books"></a>Zaúčtování pomocí odvozených knih

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak lze používat odvozené knihy.

Jestliže zaúčtujete transakce pro oceňovací model obsahující odvozené knihy, zaúčtují se transakce odvozených knih automaticky z deníků, nákupních objednávek či volných faktur. Když ale připravíte transakce primární knihy v deníku dlouhodobého majetku, můžete zobrazit a změnit částky odvozených transakcí před jejich zaúčtováním.
-   Některé účty, například účet DPH a účty odběratelů nebo dodavatelů, se aktualizují pouze jednou zaúčtováním primární knihy. Transakce odvozené knihy jsou zaúčtovány na účtech, které byly definovány pro odvozenou knihu na stránce Účetní profily dlouhodobého majetku.
-   Jako možnost Typ transakce pro odvozené knihy se často používá možnost Pořízení. Tuto možnost použijte v případě, že se má kniha a odvozená kniha použít pro dlouhodobý majetek od doby jeho akvizice.
-   Pro typ transakce lze také použít jiné hodnoty. Když mají například primární kniha a odvozené knihy stejné intervaly s ohledem na prodej nebo likvidaci, jsou pro nastavení odvozené knihy odpisů k dispozici všechny typy transakcí dlouhodobého majetku.

> [!WARNING]
> Odpisy zaúčtované v odvozené knize odpisů budou na stejnou částku, která byla zaúčtována v primární knize. Pokud se metody odpisu u jednotlivých knih liší, neměly by být vytvářeny transakce odpisů pomocí odvozeného procesu. 

## <a name="example"></a>Příklad 
Níže naleznete informace popisující nastavení transakcí pořízení s funkcí odvozené knihy.

1.  Vytvořte knihy na stránce Knihy.
    -   Kniha pro účetnictví: OM 1, aktuální účtovací vrstva
    -   Kniha pro daňové účely: OM 2, účtovací vrstva pro daně

2.  Na virtuálním počítači 1 klikněte na kartu Odvozené knihy. Zvolte virtuální počítač 2 v poli Kniha a Pořízení v poli Typ transakce.

Knihy lze potom připojit k určitému dlouhodobému majetku. 

Když je zaúčtováno pořízení pro dlouhodobý majetek s knihou OM 1, pořízení se nezaúčtuje pouze v modelu OM 1, ale také v odvozené knize OM 2. Stav obou knih dlouhodobého majetku je aktualizován na Otevřeno.

> [!NOTE]                                                                                                         
> Pokud nepoužíváte odvozené knihy, je nutné zaúčtovat pořízení dlouhodobého majetku pro knihu OM 1 i knihu OM 2.

Další informace naleznete v tématu [Odvozené knihy](derived-books.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Přehled časově rozlišených položek
description: V tomto článku jsou popsána časová rozlišení a jsou zde také informace o způsobu jejich nastavení a vytvoření transakcí.
author: aprilolson
ms.date: 01/11/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14131"
- intro-internal
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e10842929ba58b845a1df949ecb7c776ae077e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904694"
---
# <a name="accruals-overview"></a>Přehled časově rozlišených položek

[!include [banner](../includes/banner.md)]

V tomto článku jsou popsána časová rozlišení a jsou zde také informace o způsobu jejich nastavení a vytvoření transakcí.

Časové rozlišené položky se používají v účtování časového rozlišení ke sledování výnosu, který je uznán v období, kdy je získán – nikoli při přijetí platby, a ke sledování výdajů (náklady), které jsou uznány, když k nim dojde – nikoli při provedení platby.

## <a name="accrual-schemes"></a>Schémata časového rozlišení
Schémata časově rozlišených položek se používají k nastavení odložených výnosů a nákladů a stejné schéma časového rozlišení lze použít pro výnosy a náklady. Časová rozlišení hlavní knihy přerozdělují náklady nebo výnosy řádku deníku, takže náklady a výnosy se rozpoznají v příslušných obdobích. Na stránce **Schémat časového rozlišení** zadáte debetní a kreditní účty, které budou použity po nasazení schématu časového rozlišení.

-   **Má dáti** – hlavní účet, který definujete, nahradí hlavní účet má dáti na řádku dokladu deníku. Tento účet se také použije ke stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.
-   **Dal** – hlavní účet, který definujete, nahradí hlavní účet dal na řádku dokladu deníku. Tento účet se také použije ke stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.

Po určení účtů, které chcete použít, můžete určit, jak se číslo dokladu vytváří při vytvoření transakcí časového rozlišení. Můžete také určit, jak často k transakcím dochází, kolikrát se transakce vytváří a kdy se transakce zaúčtovávají. Po vytvoření schématu časového rozlišení ho můžete použít v některých denících pomocí funkce časového rozlišení hlavní knihy.

## <a name="ledger-accruals"></a>Časové rozlišení hlavní knihy
Jakmile vstoupíte do deníku, můžete kliknout na volbu **Časové rozlišení hlavní knihy** v nabídce **Funkce**. Až poté vyberte schéma časového rozlišení, se zobrazí základní částka v deníku, která se rozloží v období podle určení schématu časového rozlišení. Například pokud provádíte platbu pojištění pro zaměstnance na celý rok v lednu a částka je na 12 000, je nutné rozpoznat tyto náklady každý měsíce. Můžete vybrat počáteční datum. Můžete také určit, zda je částka, která je časově rozlišená, založená na účtu nebo protiúčtu. Po provedení výběru klikněte na možnost **Transakce** pro zobrazení všech transakcí, které byly vytvořeny na základě schématu časového rozlišení. Například pokud rozložíte 12 000 ve výdajích pojištění na rok, zobrazí se 1 000 pro každý měsíc. Po zaúčtování deníku můžete zobrazit transakce použitím stránky dotazu **Transakce dokladu**. Pokud schéma časového rozlišení nelze použít (například když se jedná o fakturu prodejní objednávky nebo fakturu nákupní objednávky), můžete připsat předplacenou částku a odepsat částku výdajů. Můžete vybrat **Protiúčet**, když nasazujete schéma časového rozlišení.


Další informace naleznete v tématu [Vytvoření schémat časového rozlišení](tasks/create-accrual-schemes.md) a [Vytvoření transakcí časového rozlišení hlavní knihy](tasks/create-ledger-accrual-transactions.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

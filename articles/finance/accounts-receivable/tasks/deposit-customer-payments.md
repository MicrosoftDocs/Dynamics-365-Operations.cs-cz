---
title: Vklad platby odběratele
description: Vložení platby odběratele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176831"
---
# <a name="deposit-customer-payments"></a>Vklad platby odběratele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vložení platby odběratele. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte na **Podokno navigace Moduly > Pohledávky > Platby > Deník plateb**.
2. Zvolte **Nové**.
3. V poli **Název** vyberte **CustPay** v rozevírací nabídce.
4. Vybrat **řádky**.
5. V poli **Účet** vyberte odběratele, od kterého jste platbu zaznamenali.
6. V poli **Kredit** zadejte částku platby. Můžete určit, že chcete částku ponechat prázdnou a nechat systém vypočítat ji pomocí výběru faktur, které byly zaplaceny.  
7. Zadejte hodnotu do pole **Odkaz na platbu**. Platební odkaz může být číslo šeku pro platbu, kterou zadáváte. Platební reference je vyžadována, pokud označíte zahrnutí platby na vkladové složence.  
8. Zaškrtněte pole Použít vklad. složenku. Má-li být platba zahrnuta do zálohy, toto nastavení změňte na hodnotu Ano.  
9. Zvolte **Nové**.
10. V poli **Účet** vyberte odběratele pro další platbu.
11. Do pole **Kredit** zadejte výši úhrady.
12. Zadejte hodnotu do pole **Odkaz na platbu**.
13. Zaškrtněte pole **Použít vklad. složenku**.
14. Zvolte **Zaúčtovat**. Předtím, než lze generovat vkladové složenky, musí být zaúčtována platba. Tím je zajištěno, že platby se nezmění po vygenerování vkladové složenky.  
15. Vyberte **Funkce**.
16. Zvolte **Vkladová složenka**.
17. Vyberte **OK**. První stránka slouží k vytvoření vkladové složenky.  
18. Vyberte **OK**. Druhý krok je tisk vkladové složenky, ale tento krok není nutný.  

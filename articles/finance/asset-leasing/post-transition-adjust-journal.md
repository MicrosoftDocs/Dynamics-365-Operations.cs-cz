---
title: Položky deníku úprav po přechodu v leasingu majetku
description: Toto téma popisuje funkce, které vám umožní přechod portfolia leasingu na nové účetní standardy leasingu, téma Kodifikace účetních standardů 842 (ASC 842) a mezinárodní standard pro finanční výkaznictví 16 (IFRS 16).
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819763"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Položky deníku úprav po přechodu v leasingu majetku

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které vám umožňují přechod portfolia leasingu na nové účetní standardy leasingu: téma Kodifikace účetních standardů 842 (ASC 842), což je standard v Obecně přijímaných účetních zásadách v USA (US GAAP) a Mezinárodní finanční výkaznictví Standard 16 (IFRS 16).

Informace o tom, jak nastavit knihu pro přechod na nové standardy, viz [Nastavit knihy leasingu](set-up-lease-books.md).

Když vytvoříte položku deníku úpravy přechodu, vygeneruje se položka deníku. Tato položka odráží dopad rozvahy na záznam leasingu podle nových standardů k uvedenému datu. Příslušný účet aktiv je debetován zůstatkovou hodnotou k danému dni a účet pasiv je kreditován. Rozdíl se odečte nebo připíše k pozdrženým příjmům.

Chcete-li zaúčtovat vyrovnání přechodu v souladu s novými účetními standardy, postupujte takto.

1. Na stránce **Shrnutí leasingu** vyberte leasing a poté vyberte **Knihy**.
2. V knize vyberte **Splátkový kalendář**.
3. V dialogovém okně **Splátkový kalendář** vyberte **Potvrdit**. Pak zavřete dialogové okno.
4. Vyberte **Vyrovnání přechodu**.

    > [!NOTE]
    > Vyrovnání přechodu lze vytvořit pouze pro knihy leasingu, které jsou přiřazeny ke knize, kde je pole **Kniha přechodů** k dispozici. Pokud je hodnota v poli **Zahájení leasingu** pozdější než datum přechodu, hodnota v poli **Vyrovnání přechodu** nebude aktualizována.

5. Chcete-li zobrazit položku deníku, vyberte **Deníky leasingu majetku**.
6. Vyberte nový deník a pak vyberte **Zaúčtovat**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
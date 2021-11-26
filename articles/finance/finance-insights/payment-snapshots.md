---
title: Přehled snímků
description: Toto téma popisuje funkci snímků, která vám umožní uložit předpověď peněžních toků pro pozdější analýzu nebo srovnání se skutečností. Když generujete prognózu peněžních toků, můžete tuto prognózu uložit jako „snímek“. Tyto snímky pak můžete použít k úpravě účtů, které byly zahrnuty do prognózy, nebo k porovnání prognózy ve snímku se skutečnými údaji.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a91300ac17b36d890840e6c0c3104fad5fce68f0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752750"
---
# <a name="snapshots-overview"></a>Přehled snímků

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Snímky umožňují organizacím upravovat a ukládat informace o jejich peněžní pozici a prognózách hotovosti v určitém okamžiku. Můžete porovnat snímek se skutečnými finančními prostředky, prozkoumat rozptyl a použít tyto informace ke zlepšení prognóz peněžních toků v průběhu času. Chceme-li být konkrétnější, snímky lze používat následujícími způsoby:

- Sledování pozice hotovosti a prognózy hotovosti v čase.
- Filtrování dat pro zobrazení podmnožiny právnických osob, pro které byl snímek vytvořen.
- Upravování pozice hotovosti a prognózy hotovosti, které byly vygenerovány systémem.
- Provádění analýzy „what-if“ a zaujímání optimistického, pesimistického a nejpravděpodobnějšího pohledu na peněžní tok.
- Porovnání skutečné finanční výkonnosti s prognózou uloženou ve snímku.

Snímek můžete vytvořit výběrem **Nový snímek** buď na kartě **Hotovostní pozice** nebo **Předpověď hotovosti** v pracovním prostoru **Prognózy peněžních toků**. Po vytvoření snímku lze přírůstky a úbytky v něm upravit a uložit. Všechny uložené snímky jsou k dispozici na kartě **Snímky**. Chcete-li otevřít snímek, vyberte jeho název.

Přírůstky a úbytky hotovosti ve snímcích lze kdykoli upravit. Když je upravena částka přírůstku nebo částka úbytku, aktualizovaná částka je poměrně rozdělena na účty likvidity, které vytvářely původní zůstatek. Po dokončení úprav snímku vyberte **Uložit** pro uložení vašich změn.

Chcete-li porovnat skutečné finanční výsledky s prognózou, která byla uložena jako snímek, vyberte **Porovnat se skutečností**. Stránka **Porovnat se skutečností** zobrazí srovnání skutečných částek a prognózy. Graf v horní části stránky ukazuje srovnání přírůstků, úbytků a zůstatků v bance v překrývajících se obdobích mezi dvěma snímky. Mřížka v dolní části zobrazuje podrobné srovnání skutečných zůstatků v období a prognózu zůstatku pro každou částku likvidity. Sloupec **Rozptyl** v mřížce ukazuje rozdíl mezi skutečným zůstatkem v období a prognózou zůstatku.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

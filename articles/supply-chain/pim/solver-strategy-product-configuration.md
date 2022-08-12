---
title: Strategie řešitele pro konfiguraci produktů
description: Tento článek popisuje, jak můžete použít strategii řešitele ke zlepšení výkonu konfigurace produktu.
author: t-benebo
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b0b53da17bd106be60966d856d29d81a1e57f91
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065510"
---
# <a name="solver-strategy-for-product-configuration"></a>Strategie řešitele pro konfiguraci produktů

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak můžete použít strategii řešitele ke zlepšení výkonu konfigurace produktu.

Koncept strategie řešitele byl poprvé představen v aktualizaci Cumulative update 7 (CU7) pro Microsoft Dynamics AX 2012 R2. Byl rozšířen v kumulativní aktualizaci 8 (CU8) pro Microsoft Dynamics AX 2012 R3 a finanční a provozní aplikace, Enterprise Edition 7.3.

Koncept strategie řešitele se nyní skládá z následujících strategií:

- Výchozí
- Minimální domény jako první
- Shora dolů
- Z3

## <a name="solver-strategy"></a>Strategie řešitele 

Model konfigurace výrobku může být formulován jako [problém omezení spokojenosti](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) nabízí dva typy strategie řešitele k vyřešení problémů omezení spokojenosti, které lze používat z modelů konfigurace produktu. Tyto strategie řešitele využívají [heuristiky](https://techterms.com/definition/heuristic), která se používá k určení pořadí, ve kterém se proměnné problémů omezení spokojenosti zvažují při řešení problémů. Heuristika může významně ovlivnit výkon při řešení problému nebo třídy problémů.

Strategie řešitele pro modely konfigurace produktu určuje řešitele, který se používá s heuristikou. Strategie **Výchozí**, **Minimální domény jako první** a **Shora dolů** používají dva řešitele z MSF, zatímco strategie **Z3** používá Z3 řešitele. 

Reálné studie implementace odběratele ukázaly, že změna strategii řešitele pro model konfigurace produktu může zkrátit čas odezvy z minut na milisekundy. Je proto vhodné se pokusit o jinou strategii řešitele k nalezení nejúčinnější strategie pro konfiguraci modelu produktu.

## <a name="change-the-settings-for-the-solver-strategy"></a>Změna nastavení strategie řešitele

Chcete-li změnit strategii řešitele, na stránce **Modely konfigurace produktu** v podokně akcí zaškzvoltee **Vlastnosti modelu**. V dialogovém okně **Upravit podrobnosti modelu** vyberte strategii řešitele.

[![Změna strategie řešitele.](./media/solver-strategy.png)](./media/solver-strategy.png)

V současné době neexistuje žádná logiká, která automaticky detekuje, jaká strategie řešitele bude nejúčinnější strategií pro konfigurace produktu na základě omezení. Proto musíte vyzkoušet strategie řešitele po jedné.

Následující tabulka poskytuje doporučení o strategii řešitele k použití různých scénářů.

| Strategie řešitele      | Použití strategie v tomto scénáři |
|----------------------|-----------------------------------|
| Výchozí              | Strategie **Výchozí** byla optimalizována pro řešení modelů, které závisí na omezení tabulky. Studie implementace odběratele ukázaly, že tato strategie je nejúčinnější strategií v situacích, kdy jsou omezení tabulky často používány. |
| Minimální domény jako první | Strategie **Minimální doména jako první** a **Shora dolů** spolu blízce souvisí. Studie implementace odběratele ukázaly, že strategie **Shora dolů** překonává strategii **Minimální doména jako první**. Avšak strategie jako **Minimální doména jako první** se uchová v produktu pro zpětnou kompatibilitu. Obě tyto strategie řešitele se ukázaly být jako efektivnější při řešení modelů, které obsahují několik aritmetických výrazů, kde se nepoužívají žádná omezení tabulky. V některých případech však strategie **Výchozí** překonává výkonem tyto dvě strategie. Nezapomeňte vyzkoušet všechny strategie. |
| Shora dolů             | Strategie **Minimální doména jako první** a **Shora dolů** spolu blízce souvisí. Studie implementace odběratele ukázaly, že strategie **Shora dolů** překonává strategii **Minimální doména jako první**. Avšak strategie jako **Minimální doména jako první** se uchová v produktu pro zpětnou kompatibilitu. Obě tyto strategie řešitele se ukázaly být jako efektivnější při řešení modelů, které obsahují několik aritmetických výrazů, kde se nepoužívají žádná omezení tabulky. V některých případech však strategie **Výchozí** překonává výkonem tyto dvě strategie. Nezapomeňte vyzkoušet všechny strategie. |
| Z3                   | Doporučujeme používat strategii **Z3** jako výchozí strategii řešitele. Pokud máte obavy o výkon a škálovatelnost, můžete vyhodnotit další strategie. |

## <a name="additional-resources"></a>Další zdroje

[Přehled konfigurace produktu](build-product-configuration-model.md)

[Heuristika](https://techterms.com/definition/heuristic)

[Problém omezení spokojenosti](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

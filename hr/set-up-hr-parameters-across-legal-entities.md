---
title: "Nastavení parametrů lidských zdrojů mezi právnickými osobami"
description: "Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f93d548adc4ae81eb89ac7c01cdae79d20b763aa
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Nastavení parametrů lidských zdrojů mezi právnickými osobami

[!include[banner](includes/banner.md)]


Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.

Některé typy záznamů jako jsou například Záznamy pozice, jsou sdíleny mezi společnostmi. Pro tyto záznamy musíte nastavit sdílené parametry. Můžete například použít stránku **Sdílené parametry lidských zdrojů** k nastavení parametrů lidských zdrojů mezi právnickými osobami. 

Na stránce **Sdílené parametry lidských zdrojů** jsou seskupeny parametry do skupin podle jejich funkce. 

Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce. Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích. Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**. Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Lidské zdroje** &gt; **Nastavení** &gt; **Typy identifikace**. Můžete zadat jednoduchý kód a popis. 

Na kartě **Číselné řady** můžete vybrat číselné řady, které se používají pro následující záznamy: osobní číslo, pozice, ID požadavku uživatele, dokument I-9, uchazeč, diskuse, ID výhody a akce personálu (je-li povolen tento typ záznamu). Pro správu číselné řady odkazů a kódů, použijte stránky seznamu **Číselné řady**. Použijte funkci vyhledávání stránky, chcete-li tuto stránku najít. 

Na kartě **Pozice** určete, zda jsou k dispozici nové pozice pro přiřazení ve výchozím nastavení:

-   **Nikdy** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Při vytváření pozic se čas a datum položky **K dispozici pro přiřazení** na kartě **Obecné** stránky **Pozice** automaticky nastavuje na datum a čas vytvoření.
-   **Niky** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Pokud vyberete tuto možnost, je třeba otevřít stránku **Pozice** pro každou novou pozici, jakmile je k dispozici, a pak na kartě **Obecné** zadat datum položky **K dispozici pro přiřazení**, aby bylo aktivováno přiřazení pracovníka.


<a name="see-also"></a>Viz také
--------

[Nastavení parametrů lidských zdrojů pro konkrétní společnost](set-up-company-specific-hr-parameters.md)





---
title: Konfigurace sdílených parametrů
description: Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7b399e0e8972a15837648d7ae6ec0eaacb5196b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130416"
---
# <a name="configure-shared-parameters"></a>Konfigurace sdílených parametrů

Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.

Některé typy záznamů jako jsou například Záznamy pozice, jsou sdíleny mezi společnostmi. Pro tyto záznamy musíte nastavit sdílené parametry. Můžete například použít stránku **Sdílené parametry lidských zdrojů** k nastavení parametrů lidských zdrojů mezi právnickými osobami. 

Na stránce **Sdílené parametry lidských zdrojů** jsou seskupeny parametry do skupin podle jejich funkce. 

### <a name="previously-released-functionality"></a>Dříve vydané funkce
Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce. Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích. Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**. Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Správa personálu** &gt; **Karta Odkazy** &gt; **Nastavení** &gt; **Typy identifikace**. Můžete zadat jednoduchý kód a popis. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Pokud používáte Dynamics 365 Human Resources
Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce. Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích. Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**. Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Lidské zdroje** &gt; **Nastavení** &gt; **Typy identifikace**. Můžete zadat jednoduchý kód a popis. 

Na kartě **Číselné řady** můžete vybrat číselné řady, které se používají pro následující záznamy: osobní číslo, pozice, ID požadavku uživatele, dokument I-9, uchazeč, diskuse, ID výhody a akce personálu (je-li povolen tento typ záznamu). Pro správu číselné řady odkazů a kódů, použijte stránky seznamu **Číselné řady**. Použijte funkci vyhledávání stránky, chcete-li tuto stránku najít. 

Na kartě **Pozice** určete, zda jsou k dispozici nové pozice pro přiřazení ve výchozím nastavení:

-   **Nikdy** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Při vytváření pozic se čas a datum položky **K dispozici pro přiřazení** na kartě **Obecné** stránky **Pozice** automaticky nastavuje na datum a čas vytvoření.
-   **Niky** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Pokud vyberete tuto možnost, je třeba otevřít stránku **Pozice** pro každou novou pozici, jakmile je k dispozici, a pak na kartě **Obecné** zadat datum položky **K dispozici pro přiřazení**, aby bylo aktivováno přiřazení pracovníka.

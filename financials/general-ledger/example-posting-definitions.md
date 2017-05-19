---
title: "Definice účtování"
description: "Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 06d789d83b623e76c67a6ec4c9fc1fea673d3294
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="posting-definition-examples"></a>Příklady definice účtování

[!include[banner](../includes/banner.md)]


Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu.

než si přečtete obsah tohoto tématu, měli byste se seznámit s účtovacími definicemi a definicemi účtování transakcí. Informace naleznete v tématu [Definice účtování](posting-definitions.md). Následující příklady lze nastavit na stránce **Definice účtování**. Každý příklad obsahuje tyto oddíly:

-   Definice účtování – kritéria shody
-   Definice účtování – generované položky
-   Transakce s účty, hodnoty dimenzí a částky
-   Položky hlavní knihy generované z definice účtování

Když dojde ke shodě mezi účty a hodnotami dimenze v podokně **Kritéria shody** pro definici účtování a účty a hodnoty dimenze v transakci, záznamy v hlavní knize jsou generovány na základě podokna **Vytvořené položky** pro definice účtování. 
> [!NOTE]
> Pokud chcete přidružit definice účtování ke konkrétnímu typu transakce, použijte stránku **Definice účtování transakcí**. Po přidružení definice účtování k typu transakce a výběru možnost **Použít definice účtování** na stránce **Parametry hlavní knihy** musí všechny transakce vybraného typu používat definice účtování.

## <a name="example-purchase-order-encumbrances"></a>Příklad: břemeno nákupní objednávky
Jestliže povolíte zpracování břemene výběrem možnosti **Povolit proces břemena** na stránce **Parametry hlavní knihy**, definice účtování musí být použity pro záznam břemen do hlavní knihy pro všechny účty, které budou rezervovány. Ve většině případů jsou rezervovány všechny účty nákladů v rozvaze. 

Definice účtování pro břemena jsou nastaveny pro modul **Nakupování** na stránce **Definice účtování**. Poté v oblasti **Nakupování** na stránce **Definice účtování transakcí** můžete vybrat typ transakce **Nákupní objednávka** a přiřadit tak definici účtování k nákupní objednávce. 

Všechny transakce dokladu pro břemeno nákupní objednávky musí mít zůstatek (debet se musí rovnat kreditům) v každé jedinečné dimenzi na dokladu.

### <a name="posting-definition--match-criteria"></a>Definice účtování – kritéria shody

| Účetní struktura       | Číslo účtu shody | Priorita |
|-------------------------|----------------------|----------|
| Účetní struktura – zisky a ztráty | \*                   | 1        |

* Prázdná hodnota v poli **Číslo účtu shody** znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.

### <a name="posting-definition--generated-entries"></a>Definice účtování – generované položky

| Účetní struktura | Generované číslo účtu                    | Generované hodnoty Má dáti/Dal |
|-------------------|---------------------------------------------|------------------------|
| Zůstatek           | 300143 - -(účet pro břemeno)             | Stejné                   |
| Zůstatek           | 300144 - -(rezerva pro účet pro břemeno) | Vyvažující              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transakce s účty, hodnoty dimenzí a částky

Hodnoty pro účty a dimenze pochází z rozúčtování zadaného pro řádek nákupní objednávky nebo z účtů a dimenzí, které jsou generovány automaticky na základě výchozího nastavení pro dodavatele, položky, kategorie a šablony dimenze.

| Účet + dimenze           | Má Dáti  | Kreditní | Komentář |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Training | 250.00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Položky hlavní knihy generované z definice účtování

Generované položky hlavní knihy se vytvářejí pro záznam břemen.

| Účet + dimenze           | Má Dáti  | Kreditní | Komentář |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Training | 250.00 |        |         |
| 300144-OU\_1-OU\_3566-Training |        | 250.00 |         |

V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování. Z toho vyplývá, při vyhodnocení 606500-OU\_1-OU\_3566-Training jsou generované položky vytvořeny pro účty, které jsou definovány v podokně **Generované položky** pro definici účtování.

## <a name="example-budget-appropriations"></a>Příklad: rozdělení rozpočtu
Když povolíte rozdělení rozpočtu výběrem možnosti **Povolit rozdělení rozpočtu** na stránce **Parametry hlavní knihy**, je nutné použít definice účtování pro záznam položek registru rozpočtu do hlavní knihy. Když je konfigurace kontroly rozpočtu aktivní a zapnutá, definice účtování a definice účtování transakcí lze použít k podpoře záznamu položek pro odhady, revize, převody, projekty, dlouhodobý majetek a prognózy nabídky a poptávky v hlavní knize. 

Pro nastavení definice účtování pro položky registru rozpočtu s typem rozpočtu **Původní rozpočet**, když není povoleno rozdělení příjmů, vyberte modul **Rozpočet** na stránce **Definice účtování**. Potom můžete v oblasti **Rozpočet** na stránce **Definice účtování transakcí** použít kódy rozpočtu a přidružit tak definice účtování k položkám registru rozpočtu, které mají typ rozpočtu **Původní rozpočet**. 

Pokud jsou povoleny rozdělení příjmů rozpočtu a definice účtování, položky registru rozpočtu jsou zaznamenány pro kontrolu rozpočtu v hlavní knize.

### <a name="posting-definition--match-criteria"></a>Definice účtování – kritéria shody

| Účetní struktura       | Číslo účtu shody | Priorita |
|-------------------------|----------------------|----------|
| Účetní struktura – zisky a ztráty | \*                   | 1        |

* Prázdná hodnota v poli **Číslo účtu shody** znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.

### <a name="posting-definition--generated-entries"></a>Definice účtování – generované položky

| Účetní struktura | Generované číslo účtu              | Generované hodnoty Má dáti/Dal |
|-------------------|---------------------------------------|------------------------|
| Účetní struktura | 300145 - -(účet pro odhadované výnosy) | Stejné                   |
| Účetní struktura | 300146 - -(účet pro rozdělení)     | Vyvažující              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transakce s účty, hodnoty dimenzí a částky

Účty, hodnoty dimenzí a částky pro účetní položku rozpočtu zadáváte na stránce **Položka registru rozpočtu**.

| Účet + dimenze           | Má Dáti | Kreditní | Komentář |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Training |       | 250.00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Položky hlavní knihy generované z definice účtování

Generované položky v hlavní knize se vytvoří pro záznam původního rozpočtu v jednotlivých dimenzích.

| Účet + dimenze           | Má Dáti  | Kreditní | Komentář |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Training |        | 250.00 |         |
| 300146-OU\_1-OU\_3566-Training | 250.00 |        |         |

V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování. Z toho vyplývá při vyhodnocení 606400-OU\_1-OU\_3566-Training se vytvoří generované položky hlavní knihy.







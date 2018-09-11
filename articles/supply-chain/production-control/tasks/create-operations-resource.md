--- 
title: "Vytvoření provozního prostředku"
description: "Provozní prostředek provádí aktivity projektu nebo výrobního procesu."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e05eb5df2d29e90ed24fb13ed16543ad470dfe6b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-operations-resource"></a>Vytvoření provozního prostředku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Provozní prostředek provádí aktivity projektu nebo výrobního procesu. Tento postup popisuje postup definice provozního prostředku. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.

1. Přejděte na Prostředky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Prostředek.
4. Zadejte nějakou hodnotu do pole Popis.

## <a name="define-capacity-and-consumption-parameters"></a>Definování parametrů kapacity a spotřeby
1. Rozbalte sekci Operace.
2. V poli Podíl odpadu zadejte číslo.
3. V poli Kategorie nastavení zadejte nebo vyberte hodnotu.
    * Určete nákladovou kategorii, která určuje, jak nakládat s účtem pro náklady spojené s nastavením.  
4. V Kategorie operačního času zadejte nebo vyberte hodnotu.
    * Určete nákladovou kategorii, která určuje, jak nakládat s účtem pro náklady spojené s provozem.  
5. V Kategorie množství zadejte nebo vyberte hodnotu.
    * Určete nákladovou kategorii definující způsob nakládání s účtem pro náklady spojené s prostředky na základě výstupního množství.  
6. V poli Jednotka kapacity vyberte možnost.
    * Zadejte jednotku, ve které se má vyjádřit kapacita provozních prostředků.  
7. V poli Kapacita zadejte číslo.
8. V poli Procento účinnosti je třeba zadat číslo.
    * Určete účinnost, kterou očekáváte od provozních prostředků. Procenta účinnosti upraví propustnosti provozních prostředků a má vliv na dobu rezervovanou pro prostředek.  
9. V poli Procento plánování operací zadejte číslo.
    * Zadejte maximální procento kapacity provozního prostředku, kterou chcete použít při plánování operací.  
10. Vyberte Ano v poli Omezená kapacita.
    * Nastavte možnost Ano v případě, že provozní prostředek má být naplánován podle skutečné dostupné kapacitě, a pokud by se měly zvážit existující rezervace kapacity. Je-li tato možnost je nastavena na hodnotu Ne, u provozního prostředku se předpokládá, že je nastavena neomezená kapacita, a zdroj může být přeplněn.  
11. Vyberte možnost Ano v poli Kritický prostředek.

## <a name="define-working-times"></a>Definování pracovní doby
1. Rozbalte sekci Kalendáře.
2. Klepněte na možnost Přidat.
3. V poli Kalendář zadejte nebo vyberte hodnotu.
    * Určete kalendář pracovní doby, který definuje kapacitu prostředků (v hodinách).  
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="define-resource-capabilities"></a>Definování schopností prostředku
1. Rozbalte sekci Schopnosti.
2. Klepněte na možnost Přidat.
    * Schopnost je možnost provozních prostředků provádět určitou aktivitu. Plánovací modul přidělí prostředky spárováním provozních prostředků jednotlivých aktivit s možnostmi dostupných provozních prostředků.  
3. V poli Schopnost zadejte nebo vyberte hodnotu.
4. Do pole Úroveň zadejte číslo.
    * Určete úroveň způsobilosti, podle které prostředek zpracuje schopnost.  
5. V poli Priorita zadejte číslo.
    * Určete prioritu provozního prostředku s ohledem na schopnost. Při plánování podle priority nejprve vyberte provozní prostředky s nejvyšší prioritou (nejnižší číslo).  

## <a name="assign-resource-to-resource-group"></a>Přiřazení prostředku ke skupině prostředků
1. Rozbalte sekci Skupiny prostředků.
2. Klepněte na možnost Přidat.
    * Skupina prostředků definuje pracoviště, výrobní jednotku a kontext skladu pro provozní prostředek. Provozní prostředek může být naplánován pouze pokud byl přiřazen ke skupině prostředků, a pouze na pracoviště, kde je umístěna skupina prostředků.  
3. V poli Skupina prostředků zadejte nebo vyberte hodnotu.
4. V poli Vstupní místo zadejte nebo vyberte hodnotu.
    * Zadejte umístění ve skladu, ze kterého provozní prostředek spotřebovává materiál.  



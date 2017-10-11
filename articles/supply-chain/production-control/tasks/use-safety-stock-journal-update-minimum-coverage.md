--- 
title: "Použití deníku pojistných zásob pro aktualizaci minimální disponibility"
description: "Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72b873faaee7bc86bd98f90ca2fb12a216d2f06b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# Použití deníku pojistných zásob pro aktualizaci minimální disponibility

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů. To se provádí pomocí deníku pojistných zásob. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tato úloha je určena pro plánovače výroby k zachování minimální disponibility.


## Vytvoření názvu nového deníku pojistných zásob
1. Přejděte na Názvy deníku pojistných zásob.
2. Klikněte na položku Nová.
3. Do pole Název zadejte „Materiál“.
4. V poli Popis uveďte text „Materiál“.
5. Zavřete stránku.

## Vytvoření deníku pojistných zásob
1. Přejděte na Výpočet pojistných zásob.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
    * Vyberte vámi vytvořený názvu deníku pojistných zásob, jako například Materiál.  
4. Klikněte na Vytvořit řádky.
5. Zadejte datum do pole Od data.
    * Nastavte datum na '2015-01-02'.  
6. Do pole Do data zadejte datum.
    * Nastavte datum na '2015-12-30'.  
7. Klikněte na tlačítko OK.
    * Dojde tak k vytvoření řádků pro dimenze, pro něž existují skladové transakce.  

## Vypočítat návrh
1. Klikněte na Vypočítat návrh.
2. Vyberte možnost Použít průměrný výdej během doby realizace.
3. Nastavte Koeficient násobení na 10.
    * Koeficient pro násobení slouží k úpravě návrhu. Vzhledem k tomu, že ukázková data mají pouze několik transakcí, musíte nastavit koeficient k získání reálných návrhu.  
4. Klikněte na tlačítko OK.
    * Přejděte dolů a vyhledejte M0002 a M0003. Otevřete sloupec Vypočítané minimální množství.   

## Aktualizace minimálního množství
1. V poli Nové minimální množství zadejte číslo.
    * Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství. Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu. Například můžete zadat Vypočítané minimální množství v tomto poli pro M0002, pro které je přiřazen sklad 12.  
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Můžete například vybrat M0002 se skladem 12.  
3. V poli Nové minimální množství zadejte číslo.
    * Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství. Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.  

## Zaúčtování nového minimálního množství a ověření výsledku
1. Klikněte na položku Zaúčtovat.
2. Klikněte na tlačítko OK.
3. Kliknutím přejdete na odkaz v poli Číslo položky.
4. Kliknutím přejdete na odkaz v poli Číslo položky.
5. V podokně akcí klikněte na položku Plán.
6. Klikněte na Disponibilita položky.
    * Všimněte si, že bylo aktualizováno minimální množství s novým minimálním množstvím z deníku pojistných zásob.  


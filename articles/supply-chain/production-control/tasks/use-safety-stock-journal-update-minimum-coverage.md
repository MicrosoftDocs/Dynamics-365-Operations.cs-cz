--- 
title: "Použití deníku pojistných zásob pro aktualizaci minimální disponibility"
description: "Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Použití deníku pojistných zásob pro aktualizaci minimální disponibility

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů. To se provádí pomocí deníku pojistných zásob. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tato úloha je určena pro plánovače výroby k zachování minimální disponibility.


## <a name="create-a-new-safety-stock-journal-name"></a>Vytvoření názvu nového deníku pojistných zásob
1. Přejděte na Názvy deníku pojistných zásob.
2. Klikněte na položku Nová.
3. Do pole Název zadejte „Materiál“.
4. V poli Popis uveďte text „Materiál“.
5. Zavřete stránku.

## <a name="create-a-safety-stock-journal"></a>Vytvoření deníku pojistných zásob
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

## <a name="calculate-proposal"></a>Vypočítat návrh
1. Klikněte na Vypočítat návrh.
2. Vyberte možnost Použít průměrný výdej během doby realizace.
3. Nastavte Koeficient násobení na 10.
    * Koeficient pro násobení slouží k úpravě návrhu. Vzhledem k tomu, že ukázková data mají pouze několik transakcí, musíte nastavit koeficient k získání reálných návrhu.  
4. Klikněte na tlačítko OK.
    * Přejděte dolů a vyhledejte M0002 a M0003. Otevřete sloupec Vypočítané minimální množství.   

## <a name="update-minimum-quantity"></a>Aktualizace minimálního množství
1. V poli Nové minimální množství zadejte číslo.
    * Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství. Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu. Například můžete zadat Vypočítané minimální množství v tomto poli pro M0002, pro které je přiřazen sklad 12.  
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Můžete například vybrat M0002 se skladem 12.  
3. V poli Nové minimální množství zadejte číslo.
    * Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství. Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Zaúčtování nového minimálního množství a ověření výsledku
1. Klikněte na položku Zaúčtovat.
2. Klikněte na tlačítko OK.
3. Kliknutím přejdete na odkaz v poli Číslo položky.
4. Kliknutím přejdete na odkaz v poli Číslo položky.
5. V podokně akcí klikněte na položku Plán.
6. Klikněte na Disponibilita položky.
    * Všimněte si, že bylo aktualizováno minimální množství s novým minimálním množstvím z deníku pojistných zásob.  



--- 
title: "Vytvořit volnou fakturu"
description: "Tento průvodce úkolem ukazuje vytvoření volné faktury."
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: cs-cz
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a>Vytvořit volnou fakturu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem ukazuje vytvoření volné faktury. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte na Pohledávky > Faktury > Všechny volné faktury.
2. Klikněte na položku Nová.
3. V poli Účet odběratele vyberte hodnotu.
    * Jako výchozí účet faktury bude nastaven stejný účet, jaký byl použit pro účet odběratele.   
    * Pokud nebyla faktura zaúčtována, počátečním účetním stavem je Zpracovává se.   
    * Číslo faktury bude přiřazeno při zaúčtování faktury.  
    * Pokud používáte zmocnění SEPA, ve zmocnění k přímému debetu bude při výběru účtu zákazníka automaticky vyplněno zmocnění.  
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Hlavní účet zadejte číslo účtu bez dimenze.
    * Můžete také zadat jeden nebo více znaků pro hlavní účet a vyhledat účet pomocí vyhledávání. Dimenze zadáte později v této příručce.  
6. Rozbalte pevnou záložku Podrobnosti řádku, aby bylo možné přidat dimenze do hlavního účtu.
7. Klikněte na záložku Řádek finančních dimenzí.
    * Dimenze jsou pouze pro vybraný řádek.    
    * Skupina prodejní daně je vyplněna z údajů odběratele. Pokud odběratel nemá skupinu DPH, použije se skupina DPH z hlavního účtu.  
    * Skupina DPH položek je vyplněna z hlavního účtu. Pokud hlavní účet nemá skupinu DPH položky, použije se skupina DPH položky z parametrů DPH hlavní knihy.    
8. Zadejte číslo do pole Množství.
    * Množství je volitelné.  
9. Zadejte číslo do pole Jednotková cena.
    * Jednotková cena je volitelná.  
    * Částka se počítá jako součin množství a jednotkové ceny. Výpočet však lze přepsat a zadat vlastní částku.  
10. Kliknutím na položku DPH si můžete zobrazit částku DPH, která byla pro fakturu vypočtena.
    * Částky DPH si můžete prohlédnout na této stránce nebo je přepsat na záložce Úprava.  
11. Klikněte na tlačítko OK.
12. Klepněte na tlačítko Náklady, pokud chcete přidat náklady pro fakturu. 
13. Zadejte hodnotu do pole Kód nákladů.
14. Zadejte číslo do pole Hodnota nákladů.
15. Zavřete stránku.
16. Kliknutím na položku Součty si můžete zobrazit podrobnosti a celkové částky souhrnné faktury.
17. Klikněte na tlačítko Zavřít.
18. Kliknutím na položku Zaúčtovat fakturu zaúčtujte. Před zaúčtováním je možné akci zrušit.
    * Pokud chcete změnit časování tisku faktur: Vyberte možnost Aktuální pro tisk jednotlivých faktur při jejich aktualizaci, nebo vyberte Po pro tisk po aktualizaci všech faktur.  
    * Pokud chcete změnit způsob, jak chcete kontrolovat úvěrový limit odběratele před zaúčtováním, můžete změnit typ limitu úvěru.  
    * Pokud chcete vytisknout fakturu, vyberte možnost Ano.  
    * Pokud chcete zaúčtovat fakturu, vyberte možnost Ano. Fakturu můžete vytisknout bez zaúčtování.  
19. Klikněte na tlačítko OK.



---
title: Vytvoření šablony volné faktury
description: Tento postup ukazuje, jak vytvořit šablonu volné faktury.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182502"
---
# <a name="create-a-free-text-invoice-template"></a>Vytvoření šablony volné faktury

[!include [banner](../includes/banner.md)]

Pro tuto ukázku použijte ukázkovou společnost USMF. Tento postup je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.

## <a name="create-a-template"></a>Vytvořit šablonu

1. Přejděte na **Pohledávky > Faktury > Opakované faktury > Šablony volných faktur**.
    * Tato stránka slouží k vytvoření šablon volné faktury, které mohou zahrnovat řádky faktury, náklady, šablony rozúčtování a informace o účtu hlavní knihy.  
2. Klepnutím na položku **Nová** vytvořte novou volnou šablonu.
3. Zadejte hodnotu do pole **Název šablony**.
    * Název šablony jednoznačně identifikuje šablonu volné faktury. Žádné dvě šablony nemohou mít stejný šablony název.  
4. Do pole **Popis** zadejte popis šablony.
5. Rozbalte kartu **Řádky faktury**.
6. Do pole **Popis** zadejte popis řádku faktury.
7. V poli **Hlavní účet** vyberte účet výnosů.
    * Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce **Účetní profily odběratelů**.  
8. V poli **Skupina prodejní daně** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.  
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. V poli **Skupina daně položky** vyberte skupinu daně DPH položky pro aktuální řádek faktury.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. V poli **Jednotka ceny** zadejte nebo zobrazte cenu za jednotku pro řádek faktury
    * Toto množství je násobeno hodnotou v poli **Množství** pro určení částky na řádku faktury.  
13. Přidejte nový řádek do šablony volné faktury.
14. Do pole **Popis** zadejte popis řádku faktury.
15. V poli **Hlavní účet** vyberte účet výnosů.
    * Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce **Účetní profily odběratelů**.  
16. V poli **Skupina prodejní daně** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.  
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. V poli **Skupina DPH zboží** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Skupina DPH zboží pro aktuální řádek faktury.  
19. Klikněte na odkaz na vybraném řádku v seznamu.
20. Zadejte nebo zobrazte počet jednotek pro řádek faktury.
    * Toto číslo je násobeno hodnotou v poli Jednotková cena pro určení částky na řádku faktury.  
21. Zadání nebo zobrazení ceny za jednotku pro řádek faktury. 
    * Toto množství je násobeno hodnotou v poli **Množství** pro určení částky na řádku faktury.  
22. Zobrazte a upravte rozúčtování pro každý řádek a jakékoli podřízené řádky.
    * Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách.  
23. Aktualizujte rozúčtování pro vybraný řádek faktury.
24. Klepněte na tlačítko **Zavřít**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Uložení volné faktury jako šablony
Můžete také uložit existující volnou fakturu jako šablonu. Když zvolíte na kartě **Faktura** možnost **Uložit jako šablonu**, zadejte název a popis šablony. Když šablona s názvem již existuje, zobrazí se upozornění, že šablona s tímto názvem již existuje. Můžete ji stále nahradit kliknutím na **OK**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

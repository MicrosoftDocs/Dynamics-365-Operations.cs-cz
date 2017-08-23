--- 
title: "Vytváření a úpravy prodejních nabídek"
description: "Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5dcf7d2b5e5d5397c51c51223abe95f9d4911b4f
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-edit-sales-quotations"></a>Vytváření a úpravy prodejních nabídek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="create-a-sales-quotation"></a>Vytvoření prodejní nabídky
1. Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.
2. Klikněte na položku Nová.
3. V poli Typ účtu vyberte „Potenciální zákazník“.
4. V poli Potenciální zákazník zadejte nebo vyberte hodnotu.
5. Rozbalte sekci Obecné.
    * Vzhledem k tomu, že jste zvolili vytvoření nabídky z oblasti prodeje a marketingu, je typ nastaven automaticky na prodejní nabídku. K vytvoření nabídky pro projekt k ní musíte mít přístup z modulu Řízení a účetnictví projektů.   
6. Klikněte na tlačítko OK.
    * Pole a akce pro řádky nabídky se velmi podobají položkám na řádcích prodejní objednávky.   Stejně jako prodejní objednávky lze nabídky vytvářet pro konkrétní zboží nebo pro neznámé či neexistující číslo zboží, které v době vytvoření nabídky není k dispozici, nabídky lze vytvářet pro kategorii prodeje.  
7. V poli Zboží zadejte nebo vyberte hodnotu.
8. Zadejte hodnotu do pole Zboží.
9. Zavřete stránku.
10. Zadejte číslo do pole Množství.
    * Pokud existují platné obchodní smlouvy pro vybrané zboží v řádku, použití cena a slevy se automaticky zkopírují řádku nabídky. Ujistěte se, že pole Jednotková cena obsahuje hodnotu a chcete-li můžete také zadat hodnotu slevy.  
11. Klikněte na položku Uložit.
12. V podokně akcí klikněte na položku Prodejní nabídka.
13. Klikněte na položku Součty.
14. Klikněte na tlačítko OK.
15. Klikněte na položku Řádek prodejní nabídky.
16. Klikněte na položku Ceny.
    * Na stránce Spustit simulaci ceny můžete vyzkoušet úpravami očekávané výnosy nebo ziskovost vaší nabídky na základě požadované jednotkové ceny, částku slevy, procento slevy, celkovou částku, marži nebo příspěvkový poměr.   Pokud jste spokojeni s cílovými hodnotami, lze návrh použít pro daný řádek nabídky a její pole související s cenami bude odpovídajícím způsobem aktualizováno.  
    * Simulací cen můžete vytvářet, kolik chcete. Klepnete-li na Nový, cenové podmínky z aktuálního řádku nabídky se zkopírují na stránku. Můžete pak upravit hodnoty v jakémkoli poli souvisejícím s cenami do cílových hodnot. Změny v jednom z polí spustí přepočet ve všech ostatních polích. Aby systém vypočítal prodejní marže a příspěvkový poměr, musí znát pořizovací cenu produktu. Použijte kartu Simulované ceny pro podrobné zobrazení původních cen, navržených změn a jejich vlivu na celkové hodnoty nabídky.   Obecně platí, že když simulace určuje nové množství pro daný řádek nabídky, systém přepočítá a zadá novou hodnotu v poli Jednotková cena. Pokud simulace vychází z nové marže nebo nového příspěvkového poměru, je aktualizováno pouze pole Čistá částka a pole Jednotková cena je prázdné. V obou případech budou odstraněny všechny slevy, které byly na řádku nabídky před simulací.  
17. Zavřete stránku.
18. V podokně akcí klikněte na položku Nabídka.
19. Klikněte na položku Odeslat nabídku.
20. Vyberte možnost Ano v poli Tisk nabídky.
21. Klikněte na tlačítko OK.
    * Generování sestavy může trvat několik minut. Dokud proces nebude dokončen, stránku nezavírejte.  
22. Zavřete stránku.

## <a name="update-a-sales-quotation"></a>Aktualizace prodejní nabídky
1. V podokně akcí klikněte na položku Zpracovat.
2. Klepněte na Převést na odběratele.
3. V poli Účet odběratele zadejte hodnotu.
4. Klepněte na možnost Kontrola.
    * Ujistěte se, že se zobrazí zpráva, že číslo účtu, které jste zadali, lze volně použít.  
5. Klikněte na tlačítko OK.
    * Systém právě vytvořil účet nového odběratele pro potenciálního zákazníka z nabídky.  
6. Zavřete stránku.
7. V podokně akcí klikněte na položku Zpracovat.
8. Klikněte na tlačítko Potvrdit.
9. V poli Důvod zadejte nebo vyberte hodnotu.
10. Klikněte na tlačítko OK.
11. V podokně akcí klikněte na položku Obecné.
12. Klikněte na položku Prodejní objednávky.
13. Zavřete stránku.



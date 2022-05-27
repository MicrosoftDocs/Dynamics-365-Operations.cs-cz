---
title: Uzavření fiskálního roku
description: Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eb36cb856d191d64561060e7de4a1f9fd947882
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717467"
---
# <a name="close-the-fiscal-year"></a>Uzavření fiskálního roku

[!include [banner](../../includes/banner.md)]

Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku.


## <a name="validate-year-end-close-parameters"></a>Ověření parametrů roční uzávěrky
1. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**.
2. Rozbalte oddíl **Uzávěrka fiskálního roku**.
3. Vyberte **Ano** nebo **Ne** pro možnost **Odstranit transakce roční uzávěrky během převodu**.
    
Pokud již byl uzavřen fiskální rok a znovu spuštěna roční uzávěrka, je toto nastavení důležité. Pokud je nastavená na hodnotu **Ano**, bude odstraněn doklad pro předchozího roční uzávěrku a bude vytvořen nový doklad pro všechny počáteční zůstatky účtů. Pokud je nastavena na hodnotu **Ne**, předchozí doklad zůstane a nový doklad bude vytvořen pouze pro opravné položky, které byly zaúčtovány po poslední roční uzávěrce.

4. Vyberte **Ano** nebo **Ne** pro možnost **Vytvořit uzávěrkové transakce při převodu**.

Pokud je nastavena na hodnotu **Ano**, budou vytvořeny dvě transakce. Jeden doklad byl vytvořen v uzavíraném fiskálním roce, aby byly vynulovány zůstatky všech účtů hlavní knihy a druhý je vytvořen v dalším fiskálním roce pro počáteční zůstatky. Pokud je nastavena hodnota **Ne**, je vytvořen jediný doklad pro počáteční zůstatky dalšího fiskálního roku.  

5. Vyberte **Ano** nebo **Ne** jako odpověď na dotaz, zda **nastavit stav fiskálního roku na trvale uzavřený**.

Pokud je nastavena hodnota **Ano**, stav fiskálního roku bude nastaven na Trvale uzavřeno. Vzhledem k tomu, že trvale uzavřený rok nelze znovu otevřít, je nejvhodnější nastavit tuto možnost na hodnotu **Ne**.  

6. Vyberte **Ano** nebo **Ne** pro možnost **Číslo dokladu musí být vyplněno během roční uzávěrky**.

Pokud bude nastavena hodnota **Ano**, číslo dokladu musí být zadáno ručně během procesu roční uzávěrky. Číselná řada není použita k vygenerování tohoto čísla dokladu. Je doporučeno nastavit ji na hodnotu **Ano**.  

7. Zavřete stránku.
8. Přejděte na **Hlavní kniha > Uzávěrka období > Roční uzávěrka**.
9. Kliknutím na tlačítko **Nový** vytvořte šablonu roční uzávěrky.

Šablonu lze vytvořit skupinu právnických osob, pro které se má spustit roční uzávěrka. Tuto šablonu můžete znovu používat každý rok.  

10. Do pole **Název skupiny** zadejte název šablony roční uzávěrky.
11. V poli **Fiskální kalendář** vyberte fiskální rok, pro který bude šablona vytvořena.

Pouze právnické osoby, které používají stejný fiskální rok, mohou být seskupeny do šablony roční uzávěrky. Důvodem je, že roční uzávěrka se provádí výběrem fiskálního roku, nikoli data.  

12. V **podokně akcí** klikněte na možnost **Uložit**.
13. V části **právnické osoby** klikněte na tlačítko **přidat** a vyberte právnické osoby pro tuto šablonu.
    
Právnické osoby lze přidat výběrem právnické osoby nebo výběrem organizační hierarchie. Budou přidány pouze právnické osoby s organizační hierarchií se stejným vybraným fiskálním kalendářem.  

14. Vyberte právnické osoby nebo organizační hierarchii.
15. Klikněte na tlačítko **OK**.
16. Vyberte **Ano** nebo **Ne** pro možnost **Převést dimenze rozvahy**.

U rozvahových účtů je nejvhodnější nastavit tuto možnost na hodnotu **Ano**. To bude udržovat finanční dimenze v zaúčtovaných transakcích při vytváření počátečních zůstatků rozvahových účtů. Pro účty zisků a ztrát můžete vybrat možnost zachování finančních dimenzí (**Zavřít všechny**), když jsou zůstatky přesunuty do Zachovaných zisků, nebo můžete vybrat nahrazení finančních dimenzí hodnotou jiné dimenze (**Zavřít jednu**). Pokud zvolíte **Zavřít jednu**, můžete definovat konkrétní hodnotu dimenze pro každou dimenzi nebo toto pole nechat prázdné.  

17. Klikněte na možnost **Uložit**.
18. Spusťte roční uzávěrku výběrem příkazu **Spustit fiskální uzávěrku** v **podokně akcí**. Pro vybranou šablonu se spustí roční uzávěrka.  
19. Vyberte všechny právnické osoby nebo jejich podmnožinu ze šablony, pro kterou chcete roční uzávěrku spustit.

Při prvním spuštění konci roku zavřít, chcete-li získat počáteční zůstatek, které většina organizací mohou zvolit spuštění Uzávěrka pro všechny právnické osoby v rámci šablony. Pokud jsou potom provedeny úpravy položky, můžete spustit roční uzávěrku pouze pro právnické osoby, které mají úpravy.  

20. Klikněte na tlačítko **OK**.
21. Vyberte fiskální rok, pro který chcete spustit roční uzávěrku.
22. Zadejte hodnotu do pole **Typ dokladu**. Platí pravidlo doporučeného postupu zahrnout do čísla dokladu fiskální rok k usnadnění vyhledání dokladu roční uzávěrky, který je vytvořen.  
23. Roční uzávěrka se nastaví na výchozí dávková spouštění. Pro dlouhodobé procesy platí pravidlo doporučeného postupu spouštět je v dávkovém režimu. To je obvykle jeden z těchto procesů, což je důvod pro použití v dávkovém režimu ve výchozím nastavení.  
24. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

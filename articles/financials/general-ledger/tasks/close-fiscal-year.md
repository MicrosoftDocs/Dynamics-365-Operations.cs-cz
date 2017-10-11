--- 
title: "Uzavření fiskálního roku"
description: "Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 83ea19e11596374c3e3ceb051db0b483f4b58583
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="close-the-fiscal-year"></a>Uzavření fiskálního roku

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku.


## <a name="validate-year-end-close-parameters"></a>Ověření parametrů roční uzávěrky
1. Přejděte do Hlavní knihy > Nastavení hlavní knihy > Parametry hlavní knihy.
2. Rozbalte oddíl uzávěrky fiskálního roku.
3. Vyberte Ano nebo ne pro možnost Odstranit transakce roční uzávěrky během převodu.
    * Pokud již byl uzavřen fiskální rok a znovu spuštěna roční uzávěrka, je toto nastavení důležité. Pokud je nastavená na hodnotu Ano, bude odstraněn doklad pro předchozího roční uzávěrku a bude vytvořen nový doklad pro všechny počáteční zůstatky účtů. Pokud je nastavena na hodnotu Ne, předchozí doklad zůstane a nový doklad bude vytvořen pouze pro opravné položky, které byly zaúčtovány po poslední roční uzávěrce.  
4. Vyberte Ano nebo Ne jako odpověď na dotaz, zda vytvořit transakce uzávěrky během převodu.
    * Pokud je nastavena na hodnotu Ano, budou vytvořeny dvě transakce. Jeden doklad byl vytvořen v uzavíraném fiskálním roce, aby byly vynulovány zůstatky účtů hlavní knihy zisků a ztrát a druhý je vytvořen v dalším fiskálním roce pro počáteční zůstatky. Pokud je nastavena hodnota Ne, jediný doklad je vytvořen pro počáteční zůstatky dalšího fiskálního roku.  
5. Vyberte Ano nebo Ne jako odpověď na dotaz, zda nastavit stav fiskálního roku na trvale uzavřený.
    * Pokud je nastaveno na hodnotu Ano, stav fiskálního roku bude nastaven na Trvale uzavřeno.  Vzhledem k tomu, že trvale uzavřený rok nelze znovu otevřít, je nejvhodnější nastavit tuto možnost na hodnotu Ne.  
6. Vyberte Ano nebo ne pro zda číslo dokladu musí být vyplněno během konce roku zavřete.
    * Pokud bude nastavena na hodnotu Ano, číslo dokladu musí být zadáno ručně během procesu roční uzávěrky. Číselná řada není použita k vygenerování tohoto čísla dokladu. Je doporučeno nastavit ji na hodnotu Ano.  
7. Zavřete stránku.
8. Přejděte na Hlavní kniha > Uzávěrka období > Roční uzávěrka.
9. Kliknutím na tlačítko Nový vytvořte šablonu roční uzávěrky.
    * Šablonu lze vytvořit skupinu právnických osob, pro které se má spustit roční uzávěrka. Tuto šablonu můžete znovu používat každý rok.  
10. Do pole Název skupiny zadejte název šablony roční uzávěrky.
11. Vyberte fiskální rok, pro který bude šablona vytvořena.
    * Pouze právnické osoby, které používají stejný fiskální rok, mohou být seskupeny do šablony roční uzávěrky. Důvodem je, že roční uzávěrka se provádí výběrem fiskálního roku, nikoli data.  
12. Použijte zástupce pro uložení záznamu.
13. Klikněte na tlačítko Přidat a vyberte právnické osoby pro tuto šablonu.
    * Právnické osoby lze přidat výběrem právnické osoby nebo výběrem organizační hierarchie.  Budou přidány pouze právnické osoby s organizační hierarchií se stejným vybraným fiskálním kalendářem.  
14. Vyberte právnické osoby nebo organizační hierarchii.
15. Klikněte na tlačítko OK.
16. Vyberte, zda se bude finanční dimenze převedou do dalšího fiskálního roku.
    * Je nejvhodnější nastavit tuto možnost na hodnotu Ano pro rozvahové účty.  To bude udržovat finanční dimenze v zaúčtovaných transakcích při vytváření počátečních zůstatků rozvahových účtů.  Pro účty zisků a ztrát můžete vybrat možnost zachování finančních dimenzí (Zavřít všechny), když jsou zůstatky přesunuty do Zachovaných zisků, nebo můžete vybrat nahrazení finančních dimenzí hodnotou jiné dimenze (Zavřít jednu). Pokud zvolíte Zavřít jednu, můžete definovat konkrétní hodnotu dimenze pro každou dimenzi nebo toto pole nechat prázdné.  
17. Klikněte na položku Uložit.
18. Spusťte roční uzávěrku výběrem příkazu Spustit fiskální uzávěrku v podokně akcí.
    * Pro vybranou šablonu se spustí roční uzávěrka.  
19. Vyberte všechny právnické osoby nebo jejich podmnožinu ze šablony, pro kterou chcete roční uzávěrku spustit.
    * Při prvním spuštění konci roku zavřít, chcete-li získat počáteční zůstatky, které většina organizací mohou zvolit spuštění Uzávěrka pro všechny právnické osoby v rámci šablony. Pokud jsou potom provedeny úpravy položky, můžete spustit roční uzávěrku pouze pro právnické osoby, které mají úpravy.  
20. Klikněte na tlačítko OK.
21. Vyberte fiskální rok, pro který chcete spustit roční uzávěrku.
22. Zadejte hodnotu do pole Doklad.
    * Platí pravidlo doporučeného postupu zahrnout do čísla dokladu fiskální rok k usnadnění vyhledání dokladu roční uzávěrky, který je vytvořen.  
23. Roční uzávěrka se nastaví na výchozí dávková spouštění.
    * Pro dlouhodobé procesy platí pravidlo doporučeného postupu spouštět je v dávkovém režimu. To je obvykle jeden z těchto procesů, což je důvod pro použití v dávkovém režimu ve výchozím nastavení.  
24. Klikněte na tlačítko OK.


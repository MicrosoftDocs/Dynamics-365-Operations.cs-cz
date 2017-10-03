--- 
title: "Vytvoření nákupní objednávky s plánem dodávek"
description: "Tento postup ukazuje, jak vytvořit plán dodávek pro nákupní objednávku."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 93bd832b4bbb91e6bd0288042098383eb5f4488d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Vytvoření nákupní objednávky s plánem dodávek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak vytvořit plán dodávek pro nákupní objednávku. Plán dodávek se používá, pokud množství z objednávky nebo deníku má být dodáno v podobě vícenásobné expedice. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento postup by obvykle prováděl nákupčí.


## <a name="create-a-delivery-schedule"></a>Vytvoření plánu dodávek
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu US-101 do pole Účet dodavatele.
4. Klikněte na tlačítko OK.
5. V poli Číslo zboží zadejte 'M0001'.
6. Zadejte číslo 10 do pole Množství.
7. Klikněte na Řádek nákupní objednávky.
8. Klikněte na položku Plán dodávek.
    * Stránka Plán dodávek je místo, kde můžete zadat počet dodávek, ve kterých budou dodány celková množství řádku objednávky od dodavatele.  
    * Ve výchozím stavu systém zkopíruje celkové množství a další podrobnosti o původním nákupním řádku na první řádek plánu dodávek. V tomto příkladu vytvoříme plán na dvě dodávky s posunem data druhé dodávky o týden od první.  
9. V poli Množství upravte množství na 4.
10. Klikněte na položku Nová.
11. V poli Množství zadejte zbývající množství 6.
    * V poli Datum dodání vyberte datum, které je týden po datu z prvního řádku dodávky.  
    * Je možné sledovat celkové množství, která je přiděleno na řádky plánu dodávek tím, že si prohlédnete pole Součet a Zbývající. Pokud je zbývající množství nulové, bylo do plánu přiděleno celé množství z původního řádku.  
12. Rozbalte část Převod nákladů.
    * Možnosti zde umožňují řídit způsob, jakým se náklady distribuují na řádcích plánu dodávek. Pokud vyberete Kopírovat hrubé částky, částka nákladů v původním řádku objednávky se zkopíruje do každého dodacího řádku. Možnost Přidělit řádkům dodávek rozděluje náklady z původního řádku podle množství na každém řádku dodávky.  
13. Sbalte část Převod nákladů.
14. Klikněte na tlačítko OK.
    * Plán dodávek nyní byl použit v objednávce.  
    * Původní řádek objednávky, nově označovaný jako obchodní řádek, byl předveden na řádek objednávky s více dodávkami. Je označen jedinečnou ikonou a funguje jako záhlaví pro řádky dodávky.  
15. Vyberte druhý řádek objednávky, který představuje první ze dvou řádků dodávky.
    * Dva nové řádky označované jako řádky dodávky tvoří jeden plán dodávek. Objednávka bude zpracována s ohledem na tyto řádky, nikoli na původní řádek. Pokud jsou vytištěny dokumenty, jako například potvrzení, deníky příjemek produktu nebo faktury, budou zobrazeny pouze řádky dodávky.  

## <a name="change-the-delivery-schedule"></a>Upravte plán dodávek
    * Množství na dodacích řádcích lze změnit. Pokud to provedete, aktualizuje se automaticky obchodní řádek o celkové množství z řádků dodávky.  
1. Do pole Množství na prvním řádku dodávky změňte množství ze 4 na 5.
2. Vyberte první řádek objednávky (obchodní řádek).
    * Množství na obchodním řádku bylo změněno na 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Zpracování příjmu produktu pomocí plánů dodávek
    * Nákupní objednávka musí být potvrzena, než bude možné zpracovat příjemku produktu. V tomto případě je příjem zaznamenán přímo v nákupní objednávce. Příjem může také byly zaznamenány při příjmu zboží ve skladu.  
1. V podokně akcí klikněte na položku Nákup.
2. Klikněte na tlačítko Potvrdit.
3. V podokně akcí klikněte na položku Přijmout.
4. Klikněte na položku Příjemka produktu.
5. Zadejte libovolnou hodnotu do pole Příjemka produktu.
    * Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.  
    * V poli Množství vyberte Objednané množství. Tato možnost znamená, že se během příjmu zpracuje množství, se kterým byly řádky objednávky vytvořeny.  
    * Ujistěte se, že pole Vytisknout příjemku produktu je nastaveno na hodnotu Ne. V tomto příkladu není třeba provádět tisk.  
6. Rozbalte sekci Řádky.
    * Všimněte si, že je vytvořena příjemka produktu pro dva řádky dodávky, ale ne pro původní řádek objednávky. Pokud byl zaznamenán příjem ve skladu, byl také zaznamenán na řádcích plánu dodávky.  
7. Sbalte oddíl Řádky.
8. Klepněte na možnost OK a zaznamenejte příjem.



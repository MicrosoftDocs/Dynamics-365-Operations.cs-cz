--- 
title: "Vytvoření opakované nákupní objednávky"
description: "Tento postup popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 406a59ffdbca4e7a5de54b4cb283a9a46c977ed1
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-repeat-purchase-order"></a>Vytvoření opakované nákupní objednávky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky. Existují dva způsoby vytvoření opakovaných objednávek. Můžete použít akce dostupné na úrovni dokumentů v podokně akcí, nebo můžete použít akce z podrobností o řádku. Akce na úrovni dokumentu jsou určeny především k vytváření nové nákupní objednávky přidáním řádků a informace do záhlaví z jiné objednávky, zatímco akce z podrobností řádku se používá zejména pro přidávání řádků do existující objednávky. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento úkol obvykle provádí nákupčí.


## <a name="create-a-new-repeat-purchase-order"></a>Vytvoření nové opakující se nákupní objednávky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
    * Nejprve vyzkoušíme možnost zkopírovat informace do nové objednávky.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu US-101 do pole Účet dodavatele.
4. Klikněte na tlačítko OK.
5. V podokně akcí klikněte na možnost Nákupní objednávka.
6. Klikněte na Ze všeho.
    * Tato stránka slouží jako zdroj, který můžete kopírovat z existujících objednávek do vaší objednávky. Existují různé možnosti, jak lze řádky kopírovat, a různé typy dokumentů, ze kterých lze kopírovat. Podíváme se nejprve na možnosti, jak kopírovat řádky.   
7. Rozbalte sekci Parametry.
    * Pole Koeficient množství je užitečné, když je nutné použít množství, které se liší od množství v objednávce, ze které kopírujete. Například pokud chcete objednat dvakrát takové množství, než které je v řádcích, ze kterých kopírujete, zadejte do tohoto pole "2" a systém přidá řádky, kde je dvojnásobné původní množství.  
    * Pole Opačné znaménko podporuje také změnu objednaného množství změnou znaménka u množství na přidaných řádcích v objednávce. To může být užitečné v případě, že je nutné stornovat transakci vytvořením řádků objednávky, které negují transakci. Tato možnost je vybrána automaticky při otevření stránky akcí Vytvoření dobropisu.  
    * Možnost Kopírovat náklady umožňuje kopírovat náklady do nové objednávky z dokumentu, ze kterého kopírujete řádky objednávky.  
    * Možnost Přepočítat ceny používá aktuální ceny a slevy namísto jejich kopírování z dokumentu, ze kterého kopírujete ostatní informace.  
    * Možnost Přesná kopie vytvoří přesnou kopii hodnot ve všech polích v záhlaví a na řádcích objednávkového dokumentu. Pokud toto políčko nezaškrtnete, výchozí hodnoty budou použity pro mnoho polí týkajících se dodavatele a produktů, stejně jako byste vytvářeli novou objednávku ručně. Například pokud objednávka, ze které kopírujete, má přepsaný výchozí účet faktury pro dodavatele, tento samý účet faktury bude zkopírován do vaší objednávky. Pokud jste nevybrali možnost Přesná kopie, použije se ve vaší objednávce namísto toho výchozí účet faktury pro dodavatele.  
    * Možnost Odstranit řádky nákupu odstraní všechny řádky nákupní objednávky, které již existují v nákupní objednávce, do které kopírujete, a to před použitím nových řádků. Tuto možnost použijte opatrně, protože odstraní všechny stávající řádky bez dalšího upozornění.  
    * Pokud použijete možnost Kopírovat záhlaví objednávky, nemusíte ručně vytvářet informace o záhlaví v nové objednávce. Všimněte si, že tato možnost bude mít za následek použití výchozích hodnot pro pole související s dodavatelem. Pokud dokument, ze kterého kopírujete, má jiné než výchozí hodnoty, které chcete zkopírovat, použijte také možnost Přesná kopie.  
8. Sbalte oddíl Parametry.
    * Existují různé zdroje dokumentů, ze kterých lze kopírovat, a každý má určenou samostatnou část na této stránce. Například část Nákupní objednávky umožňují kopírovat z existujících nákupních objednávek.  
9. Klepněte na řádek nákupní objednávky s ID 00015. 
10. Klepnutím na toto zaškrtávací políčko vyberte řádek.
11. Zrušte označení pole u řádku, který se nekopíruje do vaší objednávky.
    * 4 řádky byly nyní vybrány a mají být zkopírovány do nákupní objednávky. Je možné vybrat další řádky nákupní objednávky z jiných nákupních objednávek a zkopírovat je také do objednávky. Také je možné přidat řádky z jiných typů dokumentů pro nákup. Dalších několik kroků umožňuje prohlédnout různé možnosti.  
12. Sbalte oddíl Nákupní objednávky.
13. Rozbalte sekci Potvrzení.
    * Zde můžete vybrat potvrzení nákupních objednávek, ze kterých chcete kopírovat. Potvrzení nákupních objednávek jsou označena pomocí ID přidruženého deníku nákupu nebo ID nákupní objednávky.  
14. Sbalte oddíl Potvrzení.
15. Rozbalte část Příjemky produktu.
    * Zde můžete vybrat deníky příjemek produktu, ze kterých chcete kopírovat. Deníky příjemek produktu jsou označeny dokladem produktu dodávky nebo ID nákupní objednávky.   
16. Sbalte část Příjemky produktu.
17. Rozbalte sekci Faktury.
    * Zde můžete vybrat faktury dodavatele, ze kterých chcete kopírovat. Faktury jsou označeny dokladem faktury nebo ID nákupní objednávky.   
18. Sbalte oddíl Faktury.
19. Rozbalte sekci Vybrané řádky nebo záhlaví ke zkopírování.
    * Toto zobrazení obsahuje přehled všech dokladů a řádků, které byly vybrány, a ze kterých budete kopírovat do své objednávky.   
20. Sbalte sekci Vybrané řádky nebo záhlaví ke zkopírování.
21. Klikněte na tlačítko OK.
    * 4 vybrané řádky byly zkopírovány do nové nákupní objednávky.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopírování řádků do existující nákupní objednávky
    * Místo kopírování celé objednávky je běžnější vytvořit novou nákupní objednávku a vyplnit informace v záhlaví nákupní objednávky, a pak jednotlivé řádky kopírovat z existujících objednávek.  
1. Klikněte na Řádek nákupní objednávky.
2. Klikněte na Ze všeho.
    * Nově otevřená stránka je stejná jako stránka otevřená dříve, ale při otevření ze zobrazení řádků objednávky jsou vybrány jiné možnosti. Zkontrolujme si parametry.   
3. Rozbalte sekci Parametry.
    * Možnost Odstranit řádky nákupu není vybrána. To znamená, že můžete kopírovat nové řádky do objednávky bez odstranění existujících řádků.   
    * Možnost Kopírovat záhlaví objednávky také není vybrána, protože pouze přidáváme další řádky do objednávky.   
4. Sbalte oddíl Parametry.
    * V tomto příkladu si zkopírujeme řádky z existující nákupní objednávky.   
5. Klepněte na řádek nákupní objednávky s ID 00034. 
6. Klepnutím na toto zaškrtávací políčko vyberte řádek.
    * Všimněte si, že byl vybrán také jeden řádek objednávky v této nákupní objednávce.  
7. Klikněte na tlačítko OK.
    * Další řádek objednávky byl přidán do nákupní objednávky.  



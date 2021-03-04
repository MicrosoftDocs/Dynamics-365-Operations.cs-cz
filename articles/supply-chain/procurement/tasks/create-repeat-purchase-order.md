---
title: Vytvoření opakované nákupní objednávky
description: Toto téma popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky.
author: mkirknel
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bf5e92ad6bc62dd008a51aacca891cb7253a723
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424164"
---
# <a name="create-a-repeat-purchase-order"></a>Vytvoření opakované nákupní objednávky

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky. Existují dva způsoby vytvoření opakovaných objednávek. Můžete použít akce dostupné na úrovni dokumentů v podokně akcí, nebo můžete použít akce z podrobností o řádku. Akce na úrovni dokumentu jsou určeny především k vytváření nové nákupní objednávky přidáním řádků a informace do záhlaví z jiné objednávky, zatímco akce z podrobností řádku se používá zejména pro přidávání řádků do existující objednávky. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento úkol obvykle provádí nákupčí.


## <a name="create-a-new-repeat-purchase-order"></a>Vytvoření nové opakující se nákupní objednávky
1. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**. Nejprve vyzkoušíme možnost zkopírovat informace do nové objednávky.  
2. Zvolte **Nové**.
3. Do pole **Účet dodavatele** zadejte `US-101`.
4. Vyberte **OK**.
5. V podokně akcí zvolte **Nákupní objednávka**.
6. Vyberte **Ze všeho**. Tato stránka slouží jako zdroj, který můžete kopírovat z existujících objednávek do vaší objednávky. Existují různé možnosti, jak lze řádky kopírovat, a různé typy dokumentů, ze kterých lze kopírovat. Podíváme se nejprve na možnosti, jak kopírovat řádky. 
7. Rozbalte sekci **Parametry**.

    - Pole **Koeficient množství** je užitečné, když je nutné použít množství, které se liší od množství v objednávce, ze které kopírujete. Například pokud chcete objednat dvakrát takové množství, než které je v řádcích, ze kterých kopírujete, zadejte do tohoto pole "2" a systém přidá řádky, kde je dvojnásobné původní množství.  
    - Pole **Opačné znaménko** podporuje také změnu objednaného množství změnou znaménka u množství na přidaných řádcích v objednávce. To může být užitečné v případě, že je nutné stornovat transakci vytvořením řádků objednávky, které negují transakci. Tato možnost je vybrána automaticky při otevření stránky akcí **Vytvoření dobropisu**.  
    - Možnost **Kopírovat náklady** umožňuje kopírovat náklady do nové objednávky z dokumentu, ze kterého kopírujete řádky objednávky.  
    - Možnost **Přepočítat ceny** používá aktuální ceny a slevy namísto jejich kopírování z dokumentu, ze kterého kopírujete ostatní informace.  
    - Možnost **Přesná kopie** vytvoří přesnou kopii hodnot ve všech polích v záhlaví a na řádcích objednávkového dokumentu. Pokud toto políčko nezaškrtnete, výchozí hodnoty budou použity pro mnoho polí týkajících se dodavatele a produktů, stejně jako byste vytvářeli novou objednávku ručně. Například pokud objednávka, ze které kopírujete, má přepsaný výchozí účet faktury pro dodavatele, tento samý účet faktury bude zkopírován do vaší objednávky. Pokud jste nevybrali možnost **Přesná kopie**, použije se ve vaší objednávce namísto toho výchozí účet faktury pro dodavatele.  
    - Možnost **Odstranit řádky nákupu** odstraní všechny řádky nákupní objednávky, které již existují v nákupní objednávce, do které kopírujete, a to před použitím nových řádků. Tuto možnost použijte opatrně, protože odstraní všechny stávající řádky bez dalšího upozornění.  
    - Pokud použijete možnost **Kopírovat záhlaví objednávky**, nemusíte ručně vytvářet informace o záhlaví v nové objednávce. Všimněte si, že tato možnost bude mít za následek použití výchozích hodnot pro pole související s dodavatelem. Pokud dokument, ze kterého kopírujete, má jiné než výchozí hodnoty, které chcete zkopírovat, použijte také možnost **Přesná kopie**.   
    - Existují různé zdroje dokumentů, ze kterých lze kopírovat, a každý má určenou samostatnou část na této stránce. Například část **Nákupní objednávky** umožňují kopírovat z existujících nákupních objednávek.  

8. V části **Nákupní objednávky** vyberte řádky, které chcete zkopírovat do schránky. Je možné vybrat další řádky nákupní objednávky z jiných nákupních objednávek a zkopírovat je také do objednávky. Také je možné přidat řádky z jiných typů dokumentů pro nákup. Dalších několik kroků umožňuje prohlédnout různé možnosti.  
9. Rozbalte sekci **Potvrzení**. Zde můžete vybrat potvrzení nákupních objednávek, ze kterých chcete kopírovat. Potvrzení nákupních objednávek jsou označena pomocí ID přidruženého deníku nákupu nebo ID nákupní objednávky.  
10. Rozbalte část **Příjemky produktu**. Zde můžete vybrat deníky příjemek produktu, ze kterých chcete kopírovat. Deníky příjemek produktu jsou označeny dokladem produktu dodávky nebo ID nákupní objednávky.   
11. Rozbalte sekci **Faktury**. Zde můžete vybrat faktury dodavatele, ze kterých chcete kopírovat. Faktury jsou označeny dokladem faktury nebo ID nákupní objednávky.   
12. Rozbalte sekci **Vybrané řádky nebo záhlaví ke zkopírování**. Toto zobrazení obsahuje přehled všech dokladů a řádků, které byly vybrány, a ze kterých budete kopírovat do své objednávky.   
13. Vyberte **OK**. Vybrané řádky byly zkopírovány do nové nákupní objednávky.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopírování řádků do existující nákupní objednávky  

Místo kopírování celé objednávky je běžnější vytvořit novou nákupní objednávku a vyplnit informace v záhlaví nákupní objednávky, a pak jednotlivé řádky kopírovat z existujících objednávek.  

1. Vyberte **Řádek nákupní objednávky**.
2. Vyberte **Ze všeho**. Nově otevřená stránka je stejná jako stránka otevřená dříve, ale při otevření ze zobrazení řádků objednávky jsou vybrány jiné možnosti. Zkontrolujme si parametry.   
3. Rozbalte sekci **Parametry**.

    - Možnost **Odstranit řádky nákupu** není vybrána. To znamená, že můžete kopírovat nové řádky do objednávky bez odstranění existujících řádků.   
    - Možnost **Kopírovat záhlaví objednávky** také není vybrána, protože pouze přidáváme další řádky do objednávky.   
    - V tomto příkladu si zkopírujeme řádky z existující nákupní objednávky.   

4. Zvolte řádek pro požadovanou nákupní objednávku. Všimněte si, že byl vybrán také jeden řádek objednávky v této nákupní objednávce.  
5. Vyberte **OK**. Další řádek objednávky byl přidán do nákupní objednávky.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
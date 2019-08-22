---
title: Vytvoření nákupní vratky
description: Tento postup popisuje, jak vytvořit nákupní vratku pomocí akce dobropisu a zkopírovat tak řádky z dokumentu faktury dodavatele do nové nákupní objednávky.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c688cc2748b1837ecad060e7f855f7b24b7966d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844410"
---
# <a name="create-a-purchase-return-order"></a>Vytvoření nákupní vratky

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak vytvořit nákupní vratku pomocí akce dobropisu a zkopírovat tak řádky z dokumentu faktury dodavatele do nové nákupní objednávky. Také ukazuje, jak potvrdit objednávku a zpracovat dodávku zboží zpět pro dodavatele. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento úkol obvykle provádí nákupčí.


## <a name="create-a-new-purchase-return-order"></a>Vytvoření nové nákupní vratky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.
    * Prvním krokem je vytvořit novou nákupní objednávku, která bude použita jako nákupní vratka.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu US-102 do pole Účet dodavatele.
4. Klikněte na tlačítko OK.
5. V podokně akcí klikněte na položku Nákup.
6. Klikněte na Dobropis.
    * Tato stránka slouží jako zdroj, který můžete kopírovat z existujících faktur dodavatele do vaší vratky. Toto je stejná stránka, která se používá pro další kopírování. Avšak vzhledem k tomu, že jsme ji teď otevřeli z akce Dobropis, je stránka nakonfigurována tak, aby podporovala vytvoření vratky, která kompenzuje dodavatelské faktury.  
7. Rozbalte sekci Parametry.
    * Možnost Převrátit znaménko je automaticky označena a nelze ji změnit. To zajišťuje, že se znaménko změní pro množství, a že řádky objednávky, které jsou přidány, budou sloužit jako protiúčet k faktuře dodavatele.  
    * Možnost Kopírovat náklady je automaticky označena a nelze ji změnit. To znamená, že náklady z faktury dodavatele jsou přidány do nákupní vratky pro vyrovnání původních nákladů. Upravit změny v záhlaví objednávky a řádky je možné později.  
    * Možnost Přesná kopie je automaticky označena a nelze ji změnit. Tím zajistíte, aby byla vytvořena přesná kopie hodnot ve všech polích na řádcích a v záhlaví faktury dodavatele. To znamená, že je nákupní vratka vytvořena s hodnotami, které odpovídají všem termínům použitým v dokumentu faktury dodavatele.  
    * Možnost Odstranit řádky nákupu odstraní všechny řádky nákupní objednávky, které již existují v nákupní objednávce, a to před přidáním nových řádků. V tomto příkladu jsme zatím nepřidali žádné řádky do nákupní vratky, takže akce nebude mít žádný vliv. Tuto možnost použijte opatrně, protože odstraní všechny stávající řádky bez dalšího upozornění.  
    * Možnost Kopírovat záhlaví objednávky je automaticky označena a nelze ji změnit. Tím se zajistí, že informace jsou zkopírovány z faktury dodavatele a použity v záhlaví nákupní vratky. To je užitečné, protože to pomáhá zajistit, že nákupní vratka vyrovná fakturu za použití podobných podmínek.  
8. Sbalte oddíl Parametry.
9. Rozbalte sekci Faktury.
    * Stránka byla otevřena v akci Dobropis, takže je k dispozici pouze tato možnost kopírovat informace z faktur dodavatelů. Tato karta zobrazí všechny dostupné faktury pro účet dodavatele, který je uveden na nákupní vratce, kterou jste vytvořili dříve.   Faktury jsou označeny dokladem faktury nebo ID nákupní objednávky.  
10. Vyhledejte fakturu dodavatele identifikovanou pomocí čísla faktury AP-0006, a označte daný řádek kliknutím na libovolné pole v tomto řádku.
11. Klepnutím na zaškrtávací políčko pro daný řádek vyberte řádek. 
    * Všimněte si, že řádky, které jsou k dispozici ve faktuře dodavatele, jsou automaticky vybrány spolu s objednávkou. Tato konkrétní faktura dodavatele má 2 řádky objednávky. V tomto příkladu budeme vracet část množství z druhého řádku.  
12. Klepnutím na libovolné pole v tomto řádku označte druhý řádek (řádek se zbožím M0006).
13. V poli Množství upravte množství na 10. To je množství, které bude vráceno dodavateli. 
14. Klepnutím na libovolné pole v tomto řádku označte první řádek (řádek se zbožím M0005).
15. Zrušte označení pole u řádku.
    * Do objednávky budou zkopírovány pouze řádky, které vyberete.  
16. Sbalte oddíl Faktury.
17. Rozbalte sekci Vybrané řádky nebo záhlaví ke zkopírování.
    * Toto zobrazení obsahuje přehled všech dokladů a řádků, které byly vybrány, a ze kterých budete kopírovat do své objednávky.  
18. Sbalte sekci Vybrané řádky nebo záhlaví ke zkopírování.
19. Klikněte na tlačítko OK.
    * Vybrané řádky byly zkopírovány do nákupní vratky. Pole Množství zobrazuje -10.   
20. Klepněte na položku Zásoby.
21. Klikněte na Označení.
    * Řádek objednávky, který byl vytvořen, je označen vůči skladové transakci z faktury dodavatele. To zajišťuje, aby skladové zboží vrácené dodavateli bylo stejné, jako zboží přijaté od něj dříve. Existují situace, ve kterých označení neprobíhá, jako například pokud již byly zásoby označeny jako Spotřebováno, nebo pokud produkt nepoužívá označení.  
22. Klikněte na tlačítko OK.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Ověření a záznam dodávky zboží
1. Klikněte na tlačítko Potvrdit.
2. V podokně akcí klikněte na položku Přijmout.
3. Klikněte na položku Příjemka produktu.
    * Tato stránka slouží k záznamu příjemky produktu pro nákupní objednávky, a také ke zpracování vrácení zboží zpět dodavateli. Řádky objednávky se záporným množstvím značí, že je zboží nutné vrátit dodavateli, a dokument, který lze vygenerovat na této stránce, lze použít jako dodací list pro tuto potřebu.   
    * V poli Množství v tomto příkladu vyberte Objednané množství.   Tím je zajištěno zpracování dodávky pro celé objednané množství, se kterým byly řádky objednávky vytvořeny.   
4. Zadejte hodnotu do pole Příjemka produktu.
    * Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.  
5. Klikněte na tlačítko OK.
    * Zboží bylo zaznamenáno jako expedované v nákupní vratce a byl vytvořen deník příjemek produktů. Akci Příjemka produktu můžete použít ke kontrole deníků vytvořených s nákupní objednávkou a zobrazit tak, co bylo přijato nebo vráceno, a kdy.  


---
title: Zásobování
description: Tohle téma popisuje zásobování v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875544"
---
# <a name="procurement"></a>Zásobování


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V modulu Správa majetku můžete získat přehled o nákupních žádankách a nákupních objednávkách souvisejících s pracovními příkazy. Je rovněž možné vytvořit nákupní objednávku nebo nákupní žádanku z pracovního příkazu.

V seznamu **Nákupních žádanek na pracovním příkazu** (**Správa majetku** > **Společné** > **Zásobování** > **Nákupní žádanka na pracovním příkazu**) se zobrazí seznam nákupních žádanek souvisejících s pracovními příkazy.

- Vyberte úlohu pracovního příkazu v seznamu **Nákupních žádanek na pracovním příkazu** a kliknutím na tlačítko **Nákupní žádanka** otevřete související nákupní žádanku.  
- Vyberte úlohu pracovního příkazu v seznamu **Nákupních žádanek na pracovním příkazu** a kliknutím na tlačítko **Pracovní příkaz** otevřete související pracovní příkaz.  
- Vyberte úlohu pracovního příkazu v seznamu **Nákupních žádanek na pracovním příkazu** a klikněte na tlačítko **Kde byla položka použita** v případě, že chcete získat přehled o tom, zda je položka ve vybraném řádku použita ve Správě majetku ve vztahu k aktivům, výchozím hodnotám typu práce údržby, náhradním dílům a pracovním příkazům. 

![Obrázek č. 1](media/08-work-orders.png)


V seznamu **Nákupních pracovních příkazů** (**Správa podnikového majetku** > **Společné** > **Zásobování** > **Nákupní pracovní příkaz**) se zobrazí seznam nákupních objednávek souvisejících s pracovními příkazy.

- Vyberte úlohu pracovního příkazu v seznamu **Nákupních pracovních příkazů** a kliknutím na tlačítko **Nákupní objednávka** otevřete související nákupní objednávku.  
- Vyberte úlohu pracovního příkazu v seznamu **Nákupních pracovních příkazů** a kliknutím na tlačítko **Pracovní příkaz** otevřete související pracovní příkaz.  
- Vyberte úlohu pracovního příkazu v nákupním seznamu **na pracovním příkazu** a klikněte na tlačítko **Kde byla položka použita** v případě, že chcete získat přehled o tom, zda je položka ve vybraném řádku použita ve Správě majetku ve vztahu k aktivům, výchozím hodnotám typu práce údržby, náhradním dílům a pracovním příkazům. 

![Obrázek č. 2](media/09-work-orders.png)


V výše uvedených seznamech je ikona týkající se řízení data dodání umístěna vpravo na každém řádku. Pokud ikona zobrazuje vykřičník v červeném kruhu, znamená to, že dodávka v související nákupní žádance nebo nákupní objednávce může být zpožděna.

V nákupní žádance se datum použité k výpočtu možného zpoždění nachází ve formuláři **Nákupní žádanky** > pevná záložka **Záhlaví nákupní žádanky** > pole **Požadované datum**. Toto datum se porovnává s dostupným datem na pracovním příkazu nebo na úloze pracovního příkazu stejným způsobem jako datum nákupní objednávky.

Na nákupní objednávce je datum použité k výpočtu možné prodlevy datem souvisejícím s řádkem nákupní objednávky, který je zobrazen ve formuláři **Nákupní objednávka** > výběr řádku nákupní objednávky > pevná záložka **Podrobnosti řádku** > karta **Nastavení** > pole **Potvrzené datum dodání**. Není-li toto pole vyplněno, použije se datum uvedené v poli **Datum dodání** na pevní záložce **Záhlaví nákupní objednávky**. Jedno z těchto dat se porovnává s dostupným datem na pracovním příkazu nebo na úloze pracovního příkazu v následujícím pořadí:

- Skutečné datum zahájení na pracovním příkazu nebo  

- Naplánované datum zahájení na související úloze pracovního příkazu nebo  

- Naplánované datum zahájení na pracovním příkazu nebo  

- Očekávané datum zahájení na pracovním příkazu nebo  


## <a name="create-purchase-order-from-a-work-order"></a>Vytvoření nákupní objednávky z pracovního příkazu

Ve **Všech pracovních příkazech** vyberete úlohu pracovního příkazu a vytvoříte související nákupní objednávku nebo nákupní žádanku. To je prováděno za účelem zajištění vztahů projektů mezi nákupní objednávkou nebo nákupní žádankou a pracovním příkazem.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy** vyberte pracovní příkaz, pro který chcete vytvořit nákupní objednávku, a klikněte na tlačítko **Upravit**.

3. Ve formuláři **Pracovní příkaz** > pevná záložka **Práce údržby na pracovním příkazu** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit nákupní objednávku.

4. Klikněte na **Úlohy položky** > **Nákupní objednávka na základě úlohy pracovního příkazu**.

5. Na stránce se seznamem **Nákupních objednávek projektu** klikněte na položku **Nová**.

6. Vytvořte nákupní objednávku.

>[!NOTE]
>Vytvoření nákupní žádanky je téměř totožné s vytvořením nákupní objednávky. Jediným rozdílem je, že ve výše uvedeném postupu kliknete na **Úlohy položky** > **Nákupní žádanka na základě úlohy pracovního příkazu** v kroku 2.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Vztah projektu mezi pracovním příkazem a nákupní objednávkou nebo nákupní žádankou

Řádek nákupní objednávky nebo řádek nákupní žádanky souvisí s úlohou pracovního příkazu pomocí projektu pracovního příkazu a souvisejícím číslem aktivity projektu. Při vytvoření nákupní objednávky nebo nákupní žádanky z úlohy pracovního příkazu je číslo související aktivity projektu povinné. Číslo aktivity projektu je automaticky vloženo do nákupní objednávky nebo nákupní žádanky, pokud související pracovní příkaz obsahuje úlohy pracovního příkazu, které používají stejný typ úlohy údržby. Pokud úlohy pracovního příkazu obsahují různé typy úloh údržby, musí být číslo aktivity projektu vloženo ručně.

Chcete-li zobrazit nebo vložit číslo aktivity související s řádkem nákupní objednávky, otevřete **Nákupní pracovní příkaz** > vyberte záznam nákupní objednávky > klikněte na nákupní objednávku ve sloupci **Nákupní objednávka** > pevná záložka **Podrobnosti řádku** > karta **Projekt** > pole **Číslo aktivity**.


![Obrázek č. 3](media/10-work-orders.png)


Podobně, chcete-li zobrazit nebo vložit číslo aktivity související s řádkem nákupní žádanky na pracovním příkazu, otevřete **Nákupní žádanka na pracovním příkazu** > vyberte záznam nákupní žádanky > klikněte na nákupní žádanku ve sloupci **Nákupní žádanka** > pevná záložka **Podrobnosti řádku** > karta **Projekt** > pole **Číslo aktivity**.


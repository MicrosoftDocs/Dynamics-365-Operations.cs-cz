---
title: "Vytvoření a zpracování neshody"
description: "Tento postup slouží k provádění správy neshody a je založen na existující objednávce kvality."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a>Vytvoření a zpracování neshody

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup slouží k provádění správy neshody a je založen na existující objednávce kvality. Tento záznam lze spustit v ukázkové společnosti USMF a můžete navrhované hodnoty. Tento postup obvykle provádí úředník řízení kvality.  Nezbytným předpokladem je spuštění záznamu úkolu „Kontrola kvality zboží“. Aby bylo možné zpracovat schválení neshody, uživatel, který spustí záznam úkolu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé. Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.


## <a name="select-a-quality-order"></a>Vyberte objednávku kvality
1. Přejděte do nabídky Objednávky kvality.
2. Označte v seznamu vybraný řádek.
    * Vyberte objednávku kvality, která byla vytvořena na základě záznamu úkolu "Kontrola kvality zboží".  

## <a name="create-a-nonconformance"></a>Vytvoření neshody
1. Klepněte na možnost Dotazy.
2. Klikněte na možnost Neshody.
3. Klikněte na položku Nová.
4. V poli Typ problému kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte problém, který byl zjištěn během procesu kontroly.  
5. V poli Typ problému kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klikněte na tlačítko OK.

## <a name="approvereject-a-nonconformance"></a>Schválení/zamítnutí neshody
1. Klepněte na možnost Funkce.
2. Klikněte na možnost Schválit neshodu.
    * V tomto příkladu to je schválení neshody. Schválené neshody lze přidružit k souvisejícím operacím k zaznamenání práce, která je provedena v průběhu zpracování neshody nebo během zpracování oprav jako v rámci tohoto záznamu úkolu.  
3. Klepněte na tlačítko Ano.

## <a name="create-a-correction-action"></a>Vytvoření akce opravy
1. Klikněte na možnost Opravy.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Číslo pracovníka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klepněte na tlačítko Vybrat.
7. Klikněte na možnost Připojit.
    * Vytvořte poznámku o opravě. V tomto příkladu akce představuje kontaktování dodavatele za účelem diskuze o případu neshody.  
8. Klikněte na položku Nová.
9. Klikněte na možnost Poznámka.
    * Všimněte si, že v závislosti na nastavení sestavy lze vytisknout různé typy dokumentů v sestavách, které se vztahují ke správě neshody.  
10. Zadejte nějakou hodnotu do pole Popis.
11. Zavřete stránku.

## <a name="maintain-a-correction"></a>Údržba opravy
1. Klikněte na možnost Označit jako dokončené.
2. Klikněte na tlačítko OK.
3. Zavřete stránku.

## <a name="close-a-nonconformance"></a>Zavření neshody
1. Klepněte na možnost Funkce.
2. Klikněte na možnost Zavřít neshodu.
3. Klepněte na tlačítko Ano.
4. Zavřete stránku.
5. Zavřete stránku.


--- 
title: "Udržování kusovníku pro model konfigurace produktu"
description: "Spuštění této procedury vyžaduje stávající model konfigurace produktu."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 645d748235935ae67867295a87a84a6539710ab0
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Udržování kusovníku pro model konfigurace produktu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Spuštění této procedury vyžaduje stávající model konfigurace produktu. Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.


## <a name="add-a-bom-line"></a>Přidání řádku kusovníku
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro tuto proceduru vyberte špičkový reproduktor.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Rozbalte sekci Řádky kusovníku.
6. Klepněte na možnost Přidat.
7. Zadejte hodnotu do pole Název.
8. Zadejte nějakou hodnotu do pole Popis.
9. Klikněte na položku Uložit.

## <a name="add-bom-line-details"></a>Přidání podrobností řádku kusovníku
1. Klepněte na podrobnosti řádku kusovníku.
2. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Můžete vybrat zboží M0055.  
    * Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.  
3. Zaškrtněte políčko položky Nastavit.
4. Vyberte možnost Ano v poli Výpočet.
    * Nastavení vlastností výpočtu na hodnotu Ano zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.  
5. Klikněte na záložku Nastavení.
6. Zaškrtněte políčko položky Nastavit.
7. Zadejte číslo do pole Množství.
    * Pole množství určuje množství zboží, které bude zahrnuto v kusovníku. Může se jednat o zřejmého uchazeče pro mapování atributů.  
8. Klepněte na kartu Dimenze.
    * Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.  
9. Klikněte na tlačítko OK.



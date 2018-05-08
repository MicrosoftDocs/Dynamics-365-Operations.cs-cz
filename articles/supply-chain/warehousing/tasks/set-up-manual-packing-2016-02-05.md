--- 
title: "Nastavení ručního balení (jen ve verzi z února 2016 a května 2016)"
description: "Proces balení umožňuje ověřit a zabalit produkty do kontejnerů."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f992a6a1655cd868d79228c490d59b46bfae715
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Nastavení ručního balení (jen ve verzi z února 2016 a května 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Proces balení umožňuje ověřit a zabalit produkty do kontejnerů. V tomto procesu pracovníci skladu vyskladní produkty z umístění úložiště je přesunou je do stanice balení, kde zkontrolují množství a typy položek a přiřadí je k příslušným kontejnerům. Po plném zabalení kontejneru jej mohou uzavřít a přesunout do výstupního překladiště, kde jsou produkty připraveny k expedici. Tato procedura používá ukázkovou společnost USMF.


## <a name="set-up-location-profiles"></a>Nastavit profily skladových míst
1. Přejděte do nabídky Řízení skladu > Nastavení > Sklad > Profily umístění.
2. Klikněte na položku Nová.
    * Profil místa se používá pro stanice balení a obsahuje informace a pravidla pro umístění.  
3. Zadejte hodnotu do pole ID profilu skladového místa.
4. Zadejte hodnotu do pole Název.
5. V poli Formát skladového místa zadejte nebo vyberte hodnotu.
6. V poli Typ místa zadejte nebo vyberte hodnotu.
7. Vyberte možnost Ano v poli Povolit smíšené položky.
8. Vyberte možnost Ano v poli Povolit smíšené stavy zásob.
9. Vyberte možnost Ano v poli Pravidla přepisu pro dny dávky.
10. Zavřete stránku.

## <a name="set-up-warehouse-management-parameters"></a>Nastavení parametrů pro řízení skladu 
1. Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.
2. Klikněte na kartu Balení.
3. V poli ID profilu pro umístění balení zadejte nebo vyberte hodnotu.
    * Vyberte profil umístění, který chcete použít pro balení.  
4. Zavřete stránku.

## <a name="set-up-container-types"></a>Nastavení typů kontejneru
1. Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.
2. Klikněte na položku Nová.
    * Můžete definovat typy kontejnerů, které chcete použít. Můžete zadat fyzické dimenze kontejneru, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a hmotnosti.  Vlastnosti jsou upravená pole, která umožňují přidat další dimenze pro typ kontejneru.     
3. Zadejte hodnotu do pole Typ kódu kontejneru.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Váha obalu zadejte číslo.
6. Zadejte číslo do pole Maximální hmotnost.
7. V poli Objem zadejte číslo.
8. Do pole Délka zadejte číslo.
9. V poli Šířka zadejte číslo.
10. V poli Výška zadejte číslo.
11. Klikněte na položku Uložit.
12. Zavřete stránku.

## <a name="set-up-packing-profiles"></a>Nastavení profilů balení
1. Přejděte do nabídky Řízení skladu > Nastavení > Balení > Profily balení.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID profilu balení.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli ID profilu uzávěrky kontejneru zadejte nebo vyberte hodnotu.
    * ID profilu uzávěrky kontejneru je volitelné a je výchozím profilem uzavřeného kontejneru pro tento profil balení.  
6. Vyberte volbu v poli ID režimu kontejneru.
    * Tato možnost určuje, zda ID kontejneru bude automaticky generováno při vytvoření kontejneru, nebo zda je ID kontejneru vytvářeno ručně.  
7. V poli Typ kontejneru zadejte nebo vyberte hodnotu.
    * Při vytvoření nového kontejneru se typ kontejneru použije jako výchozí.  
8. Označte pole Automaticky vytvořit kontejner při zavření kontejneru.
9. Klikněte na položku Uložit.
10. Zavřete stránku.

## <a name="set-up-container-closing-profiles"></a>Nastavení profilů uzávěrky kontejneru
1. Přejděte na Řízení skladu > Nastavení > Kontejnery > Profily uzávěrky kontejneru.
    * Profily uzávěrky kontejneru definují postup při uzavření kontejneru. Je možné nastavit více profilů pro zavřený kontejner.       
2. Klikněte na položku Nová.
3. V poli ID profilu uzávěrky kontejneru zadejte hodnotu.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte volbu v poli Manifest v.
    * Určete, zda dojde k projevu při uzávěrce kontejneru nebo při potvrzení expedice. Všimněte si, že projev vyžaduje správu přepravy. Projev musí být implementován v modulech přepravy, aby je bylo možné používat.  
6. V poli Sklad zadejte nebo vyberte hodnotu.
7. V poli Výchozí umístění pro konečnou dodávku zadejte nebo vyberte hodnotu.
    * To bude umístění, kam budou přesunuty produkty, jakmile budou kontejnery uzavřené. Toto skladové místo musí mít profil skladového místa definováno v parametrech skladu.  
8. V poli Hmotnost jednotky zadejte nebo vyberte hodnotu.
9. Klikněte na položku Uložit.



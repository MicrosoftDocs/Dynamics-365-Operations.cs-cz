---
title: Vytvoření procesu minimálního nebo maximálního doplňování
description: Tento postup popisuje, jak nastavit nový proces doplnění využívající strategii doplnění metodou min/max.
author: perlynne
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0fbfcceece2883c32a266bcbe659211b0b56ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069719"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Vytvoření procesu minimálního nebo maximálního doplňování

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak nastavit nový proces doplnění využívající strategii doplnění metodou min/max. Pokud zásoby klesnou pod minimální úroveň, vytvoří se práce pro doplnění skladového místa. Postup také popisuje, jak používat pevná výdejní skladová místa a povolit tak doplnění i v případě, že zásoby klesnou pod minimální úroveň, a jak povolit pravidelné spuštění doplnění za pomoci dávkové úlohy. Tyto úkoly obvykle provádějí vedoucí skladu. Tento postup lze spustit s ukázkovými daty společnosti USMF základě vzorových hodnot níže nebo při použití vlastních dat. Jestliže používáte vlastní data, ujistěte se, že používáte sklad, který je povolen pro procesy správy skladu (WMS).


## <a name="create-a-fixed-picking-location"></a>Vytvoření pevně stanoveného výdejního skladového místa
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Pevná umístění**. Tento úkol je volitelný pro doplnění metodou min/max, ale pokud používáte dlouhodobé výdejní skladové místo, úkol umožňuje provést doplnění i v případě, že hodnoty klesnou pod minimální úroveň, protože systém může určit, jaké položky je nutné doplnit, i když nejsou žádné k dispozici.
2. Klepněte na možnost **Nový**.
3. V poli **Číslo položky** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat položku A0001.  
4. V poli **Lokalita** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat pracoviště 2.  
5. V poli **Sklad** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat sklad 24.  
6. V poli **Umístění** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat CP-003.  
7. Zavřete stránku.

## <a name="create-a-replenishment-location-directive"></a>Vytvoření směrnice pro doplnění místa
1. Přejděte do nabídky **Řízení skladu > Nastavení > Směrnice skladového místa**. Směrnice skladového místa slouží k určení toho, kde mají být položky v procesu doplnění vydány.
2. V poli **Typ pracovního příkazu** vyberte možnost Doplnění.
3. V **podokně akcí** klepněte na možnost **Nový**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Typ práce** vyberte „Vybrat“.
6. V poli **Lokalita** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat pracoviště 2.  
7. V poli **Sklad** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat sklad 24.  
8. Klikněte na možnost **Uložit**.
9. V části **Řádky** klikněte na **Nový**.
10. Označte na seznamu vybraný řádek.
11. Zadejte číslo do pole **Do množství**. Například nastavte hodnotu 9999.  
12. Zaškrtněte políčko **Povolit rozdělení**. Pokud vyberete tuto možnost, proces vytváření práce umožní rozdělení množství na řádku práce mezi více umístění.  
13. Klikněte na možnost **Uložit**.
14. V oddílu **Akce směrnice skladového místa** klikněte na **Nová**.
15. Označte na seznamu vybraný řádek.
16. Zadejte hodnotu do pole **Název**.
17. Klikněte na možnost **Uložit**.
18. V **podokně akcí** klikněte na tlačítko **Upravit dotaz**. Můžete tento dotaz upravit a přidat tak omezení, kde mohou být zásoby v procesu doplnění vybrány. Například je možné nastavit, že zásob lze používat pouze ze skladové oblasti ve skladu.
19. Klikněte na tlačítko **OK**.
20. Zavřete stránku.

## <a name="create-a-replenishment-work-template"></a>Vytvoření šablony doplnění
1. Přejděte do nabídky **Řízení skladu > Nastavení > Práce > Pracovní šablony**. Šablona práce se používá jako vodítko pro určení toho, jak musí být doplnění metodou min/max vytvořeno. Jako základ musí existovat řádek šablony práce pro výdej a vložení. Šablona práce například stanoví, že je proces neplatný, až dokud nejsou uvedeny všechny potřebné informace. 
2. V poli **Typ pracovního příkazu** vyberte možnost Doplnění.
3. V **podokně akcí** klepněte na možnost **Nový**.
4. Zadejte hodnotu do pole **Šablona práce**.
5. Klikněte na možnost **Uložit**.
6. V části **Podrobnosti pracovní šablony** klikněte na **Nová**.
7. V poli **Typ práce** vyberte „Vybrat“.
8. V poli **ID pracovní třídy** zadejte nebo vyberte hodnotu. Mělo by se jednat o pracovní třídu související s doplněním. V případě, že používáte USMF, vyberte Doplnění.  
9. V části **Podrobnosti pracovní šablony** klikněte na **Nová**.
10. Označte na seznamu vybraný řádek.
11. V poli **Typ práce** vyberte „Vložit“.
12. V poli **ID pracovní třídy** zadejte nebo vyberte hodnotu.
13. Klikněte na možnost **Uložit**.
14. Zavřete stránku.

## <a name="create-a-new-replenishment-template"></a>Vytvoření nové šablony doplnění
1. Přejděte na **Řízení skladu > Nastavení > Doplnění > Šablony doplnění**. Šablona doplnění se používá k definici položek, množství a místa pro doplnění.
2. V **podokně akcí** klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Šablona doplnění**. Pojmenujte šablonu tak, aby bylo jasné, že je určena pro doplnění metodou min/max.  
4. Zadejte hodnotu do pole **Popis**.
5. Zaškrtněte políčko **Povolit u vlny poptávky použití nerezervovaných množství**. Pokud vyberete tuto možnost, bude doplnění poptávky vlny mít možnost spotřebovat množství, která souvisejí s doplněním metodou min/max. To může být například užitečné, pokud doplnění metodou min/max není zpracováno okamžitě, a aby se tak zabránilo vytvoření nutnosti doplnění nadměrné poptávky.
6. V části **Podrobnosti šablony doplnění** klikněte na **Nová**.
7. V poli **Pořadové číslo** zadejte číslo.
8. Zadejte hodnotu do pole **Popis**.
9. Označte v seznamu vybraný řádek.
10. V poli **Jednotka doplnění** zadejte nebo vyberte hodnotu. Vyberte například ks. Zadání tohoto nastavení je povinné. Umožňuje zadat jiné měrné jednotky pro doplnění ve srovnání s jednotkou zadanou pro minimální a maximální úroveň zásob v této šabloně.
11. V poli **Šablona práce** zadejte nebo vyberte hodnotu. Vyberte šablonu práce, kterou jste vytvořili dříve.  
12. V poli **Minimální množství** zadejte číslo. Výběr minimální množství, které spustí proces doplnění. Nastavte například hodnotu 50. Je možné ponechte nastavenou hodnotu 0, a to pokud se jedná o doplňování pevného skladového místa, a pokud je možnost D **oplnit prázdná pevná skladová místa** nastavena na hodnotu „Ano“. Rovněž kvůli efektivitě doporučujeme vybrat možnost **Doplnit pouze pevná skladová místa**.
13. V poli **Maximální množství** zadejte číslo. Nastavte například hodnotu 100.  
14. V poli **Jednotka** zadejte nebo vyberte hodnotu. Přiřadíte jednotku pro minimální a maximální množství. Nastavte například ks.  
15. Zaškrtněte políčko **Doplnit prázdná pevná skladová místa**. Zaškrtnutím tohoto políčka doplníte pevná skladovací místa, jsou-li prázdná. V opačném případě budou doplněna pouze místa, kde je množství na skladě.
16. Zaškrtněte políčko **Doplnit pouze pevná skladová místa**.
17. Klikněte na **Vybrané produkty**. Jedná se o místo, kde můžete definovat, které produkty mají být doplněny. Pokud je vybrána možnost Pevně stanovené výdejní skladové místo, musíte v tomto dotazu také definovat skladová místa. Dotazy specifické pro varianty jsou k dispozici společně s dotazy specifickými pro produkty.
18. Vyberte řádek **Položky**.
19. Zadejte hodnotu do pole **Kritéria**. Vyberte položky, které mají být doplněny na pevném skladovém místě. Například zadejte A* pro výběr všech položek začínajících na A.
20. Klikněte na tlačítko **Přidat**. Přidáte-li entitu Místo (pokud již neexistuje), můžete omezit doplnění na pevná výdejní skladová místa v rámci určité oblasti skladu.
21. Označte na seznamu vybraný řádek.
22. Nastavte pole **Tabulka** na Umístění.
23. Vyberte ID profilu skladového místa v poli **Pole**.
24. V poli **Kritéria** zadejte nebo vyberte hodnotu.
25. Klikněte na tlačítko **OK**.
26. Zavřete stránku.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Nastavení procesu doplnění tak, aby byl spouštěn jako dávková úloha
1. Přejděte na **Správa skladu > Doplnění > Doplnění.** Na stránce Doplnění můžete nastavit doplnění tak, aby se spustilo jako dávková úloha, nebo aby se vyžadovalo její ruční spuštění.
2. Klikněte na tlačítko **Filtr**.
3. Označte na seznamu vybraný řádek.
4. V poli **Kritéria** zadejte nebo vyberte hodnotu.
5. Klikněte na tlačítko **OK**.
6. Rozbalte sekci **Spustit na pozadí**.
7. Nastavte **Dávkové zpracování** na Ano.
8. Klikněte na **Opakování**.
9. Vyberte možnost **Bez koncového data**.
10. Nastavte **vzor opakování**. V tomto příkladu vyberte Dny.  
11. Klikněte na tlačítko **OK**.
12. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
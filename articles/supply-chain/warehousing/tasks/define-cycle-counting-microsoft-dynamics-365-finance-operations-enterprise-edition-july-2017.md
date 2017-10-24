--- 
title: "Definování cyklické inventury "
description: "Cyklická inventura je skladový proces, který slouží k auditu skladových položek na skladě."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="define-cycle-counting"></a>Definování cyklické inventury  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Cyklická inventura je skladový proces, který slouží k auditu skladových položek na skladě. Toto zaznamenávání úkolu zobrazuje způsob, jak na to: nastavte výchozí prioritu inventury; povolte položku nabídky mobilního zařízení, aby zpracovávala operace výdeje i výpočtu; povolte prahovou hodnotu spuštění inventury když skladové místo bude prázdné; povolte plán cyklické inventury pro konkrétní položku v určitém skladu. Obvykle jsou tyto úlohy prováděny vedoucím skladu. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.


## <a name="set-the-priority-of-counting-work"></a>Nastavení priority inventury
1. Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.
2. Klepněte na kartu Cyklická inventura.
3. V poli Výchozí pracovní priorita pro cyklickou inventuru zadejte číslo.
    * Tento krok změní prioritu práce cyklické inventury ve srovnání s jinými typy práce ve skladu. Zadáním čísla, které je nižší, než je číslo pro jiné typy prací, můžete zvýšit prioritu práce cyklické inventury.  
4. Klikněte na položku Uložit.
5. Zavřete stránku.

## <a name="enable-the-mobile-device"></a>Povolení mobilního zařízení
1. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.
2. Klikněte na položku Nová.
3. Do pole Položky nabídky mobilního zařízení zadejte hodnotu.
4. Zadejte hodnotu do pole Titul.
5. V poli Režim vyberte „Práce“.
6. Nastavte hodnotu možnosti Použít stávající práci na Ano.
    * Pokud vyberete volbu Ano, systém bude hledat existující práci, když je použita položka nabídky mobilního zařízení.  
7. V poli Řídí vyberte „Řízeno systémem“.
    * Pokud je vybráno Řízeno systémem, pracovník skladu bude přesměrován na otevřenou práci v definovaných pracovních třídách. (Tyto pracovní třídy vytvoříme příště.)  
8. Rozbalte nebo sbalte oddíl Pracovní třídy.
    * Dále vytvoříme dvě pracovní třídy pro použití s touto položkou nabídky mobilního zařízení. Při použití položky nabídky budou dotazovány tyto pracovní třídy, a ve výsledku bude uživateli zobrazena práce s nejvyšší prioritou.  
9. Klikněte na položku Nová.
10. Vyberte hodnotu v poli ID pracovní třídy.
11. Klikněte na položku Nová.
12. Vyberte hodnotu v poli ID pracovní třídy.
13. Klikněte na položku Uložit.
14. Zavřete stránku.
15. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení.
16. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
17. Ve stromovém zobrazení vyberte položku nabídky, kterou jste právě vytvořili.
18. Klikněte na položku Upravit.
19. Klepnutím na šipku přidejte položku nabídky do nabídky.
20. Klikněte na položku Uložit.

## <a name="create-a-counting-threshold"></a>Vytvoření prahové hodnoty inventury
1. Přejděte do Správce skladu > Nastavení > Cyklická inventura > Prahové hodnoty cyklické inventury.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID prahové hodnoty cyklické inventury.
4. Nastavte možnost Ihned zpracovat cyklickou inventuru na Ano.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klepněte na tlačítko Uložit.
7. Klepněte na Vybrat umístění.
8. Označte v seznamu vybraný řádek.
9. V poli Kritéria vyberte hodnotu.
10. Klikněte na tlačítko OK.
11. Zavřete stránku.

## <a name="create-a-cycle-count-plan"></a>Vytvoření plánu cyklické inventury
1. Přejděte do Správce skladu > Nastavení > Cyklická inventura > Plány cyklických inventur.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID plánu cyklické inventury.
4. Zadejte hodnotu do pole Popis.
5. Do pole Maximální počet cyklických inventur zadejte číslo.
6. Klepněte na tlačítko Uložit.
7. Klepněte na Vybrat umístění.
8. Označte v seznamu vybraný řádek.
9. V poli Kritéria vyberte hodnotu.
10. Klikněte na tlačítko OK.
11. Do pole Dny mezi cyklickými inventurami zadejte číslo.
    * Pokud je například hodnota zadaná v poli Dny mezi cyklickými inventurami nastavena na 5, práce cyklické inventury bude vytvořena každých pět dní. Pokud je však práce cyklické inventury zpracovávána třetího dne, další práce cyklické inventury bude vytvořen pět dnů po zpracování poslední cyklické inventury, osmého dne.  
12. Klikněte na položku Uložit.
13. Klikněte na položku Nová.
14. V poli Pořadové číslo zadejte číslo.
    * Pořadí je od nejnižšího čísla po nejvyšší číslo. Hodnota musí být větší než 0 (nula).  
15. Označte v seznamu vybraný řádek.
16. Zadejte nějakou hodnotu do pole Popis.
17. Klepněte na tlačítko Uložit.
18. Klikněte na Definovat dotaz na produkt.
19. Označte v seznamu vybraný řádek.
20. V poli Kritéria zadejte nebo vyberte hodnotu.
21. Klikněte na tlačítko OK.
22. Zavřete stránku.



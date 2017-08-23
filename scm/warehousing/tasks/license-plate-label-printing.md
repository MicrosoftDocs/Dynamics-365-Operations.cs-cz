--- 
title: "Povolení tisku popisku registrační značky"
description: "Tento postup umožňuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4ca3cd02a43692cfa9510847b460a318855fd24
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="enable-license-plate-label-printing"></a>Povolení tisku popisku registrační značky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup umožňuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje. Tento postup můžete projít v ukázkových datech společnosti USMF. Pokud jej používáte s použitím vlastních dat, je třeba mít k nastavenou číselnou řadu pro registračních značky vozidla. Je nutné nastavit tiskárnu štítků před zahájením této úlohy. Přejděte do nabídky Správa organizace > Nastavení > Jednotky Síťové tiskárny. V podokně Akce klikněte na Možnosti a poté klepněte na tlačítko Stáhnout instalační program agenta směrování dokumentů. Spusťte instalační program a ujistěte se, že máte nastavenu síťovou tiskárnu na hodnotu Aktivní předtím, než budete pokračovat v postupu.


## <a name="set-up-the-gs1-company-prefix"></a>Nastavení předpony společnosti GS1
1. Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.
2. Do pole Předpona společnosti GS1 zadejte 7 čísel pro vaše číslo společnosti GS1.
3. Klikněte na položku Uložit.
4. Zavřete stránku.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Nastavení číselné řady registrační značky vozidla SSCC
1. Přejděte na Správa organizace > Číselné řady > Číselné řady.
2. Vyberte volbu v poli Oblast.
3. Vyberte volbu v poli Odkaz.
4. Zadejte hodnotu do pole Společnost.
5. Označte na seznamu vybraný řádek.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Rozbalte sekci Segmenty.
8. Klikněte na položku Upravit.
9. V tabulce segmentů vyberte první řádek.
10. Klepněte na tlačítko Odebrat.
11. Klepněte na tlačítko Odebrat.
12. Klikněte na položku Uložit.
13. Zavřete stránku.

## <a name="create-the-document-route-layout"></a>Vytvoření rozvržení směrování dokumentu
1. Přejít na Správa skladu > Nastavení > Směrování dokumentu > Rozložení směrování dokumentů.
    * Povolte rozvržení SSCC.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID rozvržení.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
6. Klikněte na Vložit na konci textu.
7. Klikněte na položku Uložit.
8. Zavřete stránku.

## <a name="set-up-the-document-routing"></a>Nastavení směrování dokumentu
1. Přejít na Správa skladu > Nastavení > Směrování dokumentu > Směrování dokumentů.
2. V poli Typ pořadí pracovních činností vyberte možnost.
3. Klepněte na možnost Nový.
4. Zadejte hodnotu do pole Sklad.
5. Zadejte hodnotu do pole Název.
6. Klepněte na možnost Nový.
7. V poli ID rozvržení zadejte nebo vyberte hodnotu.
8. V poli Název zadejte název tiskárny, kterou chcete použít.
9. Klikněte na položku Uložit.
10. Zavřete stránku.

## <a name="create-mobile-device-menu"></a>Vytvoření nabídky mobilního zařízení
1. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.
2. Klikněte na položku Nová.
3. Do pole Položky nabídky mobilního zařízení zadejte hodnotu.
4. Zadejte hodnotu do pole Titul.
5. Vyberte volbu v poli Režim.
6. Vyberte možnost Ano v poli Použít stávající práci.
7. Vyberte možnost Ano v poli Generovat registrační značku.
8. Rozbalte sekci Pracovní třídy.
9. Klikněte na položku Nová.
10. Zadejte hodnotu do pole ID pracovní třídy.
11. Klikněte na položku Uložit.
12. Zavřete stránku.
13. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení.
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Ve stromové struktuře vyberte "Ve stromu vybrat dříve vytvořenou položku nabídky".
16. Klikněte na možnost Upravit.
17. Klepnutím na šipku přidejte položku nabídky do nabídky.
18. Klikněte na položku Uložit.
19. Zavřete stránku.

## <a name="update-a-work-template"></a>Aktualizace šablony práce
1. Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na položku Upravit.
4. Klepněte na možnost Nový.
5. Označte v seznamu vybraný řádek.
6. V poli Typ práce vyberte „Tisk“.
7. V poli ID pracovní třídy zadejte nebo vyberte hodnotu.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klikněte na Přesunout nahoru.
10. Klikněte na položku Uložit.
11. Zavřete stránku.



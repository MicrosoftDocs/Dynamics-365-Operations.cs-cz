---
title: Nastavení elektronických podpisů
description: Tento postup použijte k nastavení elektronických podpisů.
author: maertenm
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d78ecd0606f3b1d5d7b5f3cd470beecfcdd5077
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747338"
---
# <a name="set-up-electronic-signatures"></a>Nastavení elektronických podpisů

[!include [banner](../../includes/banner.md)]

Tento postup použijte k nastavení elektronických podpisů. Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku. K vytvoření tohoto postupu jsou použita ukázková data společnosti DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Povolení konfiguračního klíče Elektronický podpis
1. Přejděte do nabídky Správa systému > Nastavení > Konfigurace licence.
2. Ve stromu rozbalte možnost Správa.
    * Zkontrolujte, zda je zaškrtnuto políčko Elektronický podpis.  
    * Pokud není zaškrtnuté políčko Elektronický podpis, je nutné povolit režim údržby. Režim údržby lze povolit v tomto prostředí jen provedením úlohy údržby pomocí služeb Lifecycle Services nebo místním použitím nástroje Deployment.Setup.  
3. Zavřete stránku.

## <a name="set-up-electronic-signature-parameters"></a>Nastavení parametrů elektronického podpisu
1. Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Parametry elektronického podpisu.
2. Klikněte na položku Upravit.
3. Zadejte hodnotu do pole Oznámení.
    * Zadejte zprávu, kterou podepisující uživatelé uvidí v případech, kdy je vyžadován podpis. Můžete zadat libovolný text. Tato zpráva uživatele obvykle informuje o významu elektronického podpisu dokumentu.  
    * Pokud chcete zadat text oznámení v dalších jazycích, klikněte na tlačítko Překlady.  
4. Klikněte na položku Uložit.
5. Zavřete stránku.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Nastavení kódů důvodů pro elektronické podpisy
1. Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Kódy důvodů pro elektronický podpis.
2. Klikněte na položku Nová.
    * Kódy důvodů je třeba nastavit dříve, než začnete elektronické podpisy používat. Při podepisování dokumentu je vyžadován platný kód důvodu.     Podepisující uživatel vybere kód důvodu, který bude vyjadřovat účel elektronického podpisu. Jeden z kódů důvodu může například označovat schválení dokumentu právníkem.  
3. Zadejte hodnotu do pole Kód důvodu.
4. Zadejte nějakou hodnotu do pole Popis.
    * Zadejte další kódy důvodů, pokud je to nutné.  
5. Klikněte na položku Uložit.
6. Zavřete stránku.

## <a name="require-electronic-signatures-for-existing-processes"></a>Vyžádání elektronických podpisů pro existující procesy
1. Přejděte do nabídky Správa organizace > Nastavení > Elektronický podpis > Požadavky na elektronický podpis.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte proces vyžadující elektronický podpis.  
3. Zaškrtněte políčko Je požadován podpis nebo jeho zaškrtnutí zrušte.
    * Opakujte tyto kroky pro každý proces, který vyžaduje elektronický podpis.  
4. Klikněte na položku Uložit.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Vytvoření vlastního požadavku na elektronické podpisy
1. Klikněte na položku Nová.
2. Zaškrtněte políčko Je požadován podpis nebo jeho zaškrtnutí zrušte.
3. V poli Název zadejte název procesu, který vyžaduje elektronický podpis.
4. V poli Název tabulky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V seznamu najděte a vyberte tabulku, v níž jsou uložena data, která je třeba podepsat.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Název pole kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. V seznamu najděte a vyberte pole tabulky, které chcete sledovat.
9. Klikněte na odkaz na vybraném řádku v seznamu.
    * Určete, kdy je podpis požadován.     Je-li požadován podpis při každé změně dat v poli, vyberte možnost Vždy.     Vyberte možnost Pouze, pokud je podpis vyžadován pouze za určitých podmínek. Pokud vyberete Pouze, je nutné vybrat také jednu z následujících možností: Při vložení záznamu, Při aktualizaci záznamu nebo Při odstranění záznamu.  
10. Klikněte na položku Uložit.
11. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
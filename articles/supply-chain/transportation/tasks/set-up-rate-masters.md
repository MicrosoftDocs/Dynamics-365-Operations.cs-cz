---
title: Nastavení hlavních sazeb
description: Tento postup popisuje, jak nastavíte hlavní sazby.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77629cbaec4c4d4608b8941e55ab23a106d38727
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233600"
---
# <a name="set-up-rate-masters"></a>Nastavení hlavních sazeb

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak nastavíte hlavní sazby. Hlavní sazby obvykle nastavuje manažer logistiky v závislosti na smlouvách podepsaných s dopravci. V tomto scénáři nastavíte hlavní sazbu pro leteckého dopravce. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

## <a name="set-up-break-master"></a>Nastavení hlavního přerušení

1. Přejděte do nabídky **Správa přepravy > Nastavení > Ohodnocení > Hlavní přerušení**. Hlavní změny slouží k definování struktury cen a použitých zarážek. Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.  
1. Zvolte **Nové**.
1. V poli **Hlavní přerušení** zadejte hodnotu.
1. Zadejte hodnotu do pole **Název**.
1. V poli **Datový typ** vyberte datový typ.
1. V poli **Srovnání** zadejte požadovaný druh srovnání (pomocí operátorů).
1. Do pole **Jednotka přerušení** zadejte jednotku přerušení.
1. V sekci **Podrobnosti** vytvořte tolik přerušení, kolik je potřeba pro strukturu cen.
1. Zvolte **Uložit**.

## <a name="set-up-rate-master"></a>Nastavení hlavní sazby

1. Přejděte do nabídky **Správa přepravy > Nastavení > Ohodnocení > Hlavní sazba**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Hlavní sazba**.
1. Zadejte hodnotu do pole **Název**.
1. V poli **ID metadat sazeb** výběrem rozevíracího seznamu otevřete vyhledávání. ID metadat sazeb určí data potřebná pro hlavní sazbu, protože definuje metadata očekávaná modulem systému přepravy, který používá tuto hlavní sazbu.  
1. V tomto příkladu vyberte možnost P2P. To je již definováno v ukázkových datech.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Zvolte **Uložit**.

## <a name="set-up-rate-base"></a>Nastavení základní sazby

1. Vyberte **základní sazbu**.
    * Nastavení základní sazby určuje sazbu dopravce a slouží k nastavení struktury sazby, protože definuje strukturu kurzů v zarážkách definovaných ve hlavní změně.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Základní sazba**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Hlavní přerušení** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání.
    * Hlavní změny slouží k definování struktury cen a použitých zarážek. Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.  
6. V tomto příkladu použijte hmotnost. To je již definováno v ukázkových datech.
7. Vyberte odkaz na zvýrazněném řádku v seznamu.
8. Rozbalte sekci **Podrobnosti**.
9. Zvolte **Nové**.
10. V poli **PSČ místa vyložení – od** zadejte „30301“.
11. V poli **PSČ místa vyložení – do** zadejte „30318“.
12. V poli **Země/oblast vyložení** zadejte „USA“ .
13. Do pole **<1,00 libry** zadejte hodnotu „100“.
    * Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 1 libra.  
14. Do pole **<5,00 libry** zadejte hodnotu „300“.
    * Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 5 liber.  
15. Do pole **<20,00 libry** zadejte hodnotu „500“.
    * Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 20 liber.  
16. Do pole **<100,00 libry** zadejte hodnotu „1000“.
    * Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 100 liber.  
17. Do pole **<1.000,00 libry** zadejte hodnotu „3000“.
    * Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 1000 liber.  
18. Zvolte **Uložit**.
19. Zavřete stránku.

## <a name="assign-rate-base"></a>Přiřazení základní sazby

1. Rozbalte část **Přiřazení základní sazby**.
2. Zvolte **Nové**.
    * Můžete mít několik přiřazení základní sazby pro jednotlivé hlavní sazby. Díky tomu lze vytvořit několik různých cenových bodů pro každého dopravce v závislosti na cílech, službách nebo jiných základech sazby. V tomto postupu můžete vytvořit pouze jedno přiřazení základní sazby.  
3. Zadejte hodnotu do pole **Název**.
4. V poli **Základní sazba** volbou tlačítka rozevíracího seznamu otevřete vyhledávání.
5. Vyberte odkaz na zvýrazněném řádku v seznamu.
6. V poli **Služba** vyberte tlačítko rozevíracího seznamu a otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Vyberte odkaz na zvýrazněném řádku v seznamu.
9. Do pole **PSČ pro vyzvednutí** zadejte „98052“.
    * Určete, pro které PSČ toto přiřazení základní sazby bude platné.
10. Do pole **Země/oblast pro vyzvednutí** zadejte „USA“.
11. Zvolte **Uložit**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
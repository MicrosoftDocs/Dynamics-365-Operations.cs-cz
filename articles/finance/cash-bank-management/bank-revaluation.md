---
title: Přecenění cizí měny banky
description: Tento článek obsahuje přehled procesu bankovního přecenění cizí měny. Obsahuje informace o nastavení, spuštění procesu, výpočtu proces a stornování transakcí přecenění.
author: angelad116
ms.date: 12/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2d5e8a36d3b4d44c9ad0454db94164adebf80997
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887252"
---
# <a name="bank-foreign-currency-revaluation"></a>Přecenění cizí měny banky

[!include [banner](../includes/banner.md)]


Tento článek obsahuje přehled procesu bankovního přecenění cizí měny. Popisuje, jak nastavit a spustit proces a obsahuje informace o výpočtu pro proces. Vysvětluje také, jak stornovat transakce přecenění, pokud je to nutné.

V rámci uzávěrky období vyžadují účetní konvence přecenění zůstatků účtů v cizích měnách pomocí různých typů směnných kurzů (aktuální, historický, průměrný atd.). Funkce přecenění cizí měny bankovního slouží k přecenění jednoho nebo více bankovních účtů. Tato funkce je také globální funkce. Proto můžete z jediné stránky přecenit banky napříč všemi právnickými osobami, k nimž máte přístup.

> [!NOTE]
> Po spuštění procesu přecenění budou zůstatky na jednotlivých bankovních účtech zaúčtované v cizích měnách přeceněny. Transakce nerealizovaných zisků nebo ztrát, které byly vytvořeny během procesu přecenění, jsou generovány systémem. Mohou být vytvořeny dvě transakce, jedna pro zúčtovací měnu a druhá pro měnu vykazování, pokud je relevantní. Každá účetní položka bude zaúčtována na nerealizovaný zisk nebo ztrátu a přeceňovaný hlavní účet.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Příprava na spuštění přecenění cizí měny

Před spuštěním procesu přecenění je nutné provést následující nastavení.

- Na stránce **Hlavní kniha** zadejte typ směnného kurzu. Pokud není definován typ směnného kurzu pro hlavní účet, použije se tento typ směnného kurzu při přecenění cizí měny.
- Na stránce **Hlavní kniha** zadejte účty pro realizovaný zisk, realizovanou ztrátu, nerealizovaný zisk a nerealizovanou ztrátu k přecenění měny. Účty Realizovaných zisků a ztrát se používají při vyrovnání transakcí pohledávek a závazků. Účet nerealizovaných zisků a nerealizovaných ztrát slouží k vyřazení otevřených transakcí a hlavních účtů hlavní knihy.
- Na stránce **Účty přecenění měny** vyberte různé účty pro přecenění měny pro jednotlivé měny a společnosti. Pokud nejsou definovány žádné účty, budou použity účty ze stránky **Hlavní kniha**.
- Na stránce **Parametry řízení hotovosti a banky** na kartě **Číselné řady** přidejte číselnou řadu pro přecenění cizí měny.


> [!NOTE]
> Používá-li vaší právnická osoba ruský, polský nebo a maďarský kód země nebo oblasti, již lze přecenění cizí měny banky provést. Nebudete moci používat přecenění cizí měny, které používají jiné země nebo oblasti.

## <a name="process-foreign-currency-revaluation"></a>Zpracování přecenění cizí měny

Po dokončení instalace použijte stránku **přecenění cizí měny** v modulu řízení hotovosti a banky k přecenění zůstatků jednoho nebo více bankovních účtů pro všechny právnické osoby. Proces můžete spustit v reálném čase nebo naplánovat jeho spuštění pomocí dávky.

Stránka **Přecenění cizí měny** ukazuje historii každého procesu přecenění. Ukazuje, kdy byl proces spuštěn a jaká kritéria byla definována a obsahuje odkaz na doklad, který byl vytvořen pro přecenění. Také zobrazí, zda bylo stornováno předchozí přecenění. Pokud chcete spustit proces přecenění, vyberte **Přecenění cizí měny** v podokně akcí k otevření dialogového okna **Banka – přecenění cizí měny**.

Pole **Datum přecenění** definuje datum pro výpočet zůstatku cizí měny, který bude přeceněný. Součet všech bankovních transakcí, které se vyskytly až do tohoto data přecenění.

Pole **Datum směnného kurzu** určuje datum směnného kurzu, které bude použito k přecenění zůstatků v měně. Můžete například přecenit zůstatky k datu 31. ledna a použít směnný kurz, který je definován pro 1. února.

Proces přecenění lze spustit pro jednu nebo více právnických osob. Vyhledávání zobrazí pouze právnické osoby, ke kterým máte přístup. Vyberte právnické osoby, pro které chcete vybrat bankovní účty, které mají nárok na přecenění cizí měny. V mřížce zobrazí všechny bankovní účty pro ty právnické osoby.

Nastavte možnost **Náhled před zaúčtováním** na **Ano**, pokud chcete zkontrolovat výsledky přecenění před zaúčtováním. Přecenění cizí měny má náhled, který lze publikovat. Není nutné znovu spustit proces přecenění. Náhled výsledků lze exportovat do aplikace Microsoft Excel, chcete-li uchovat historii způsobu výpočtu částek. Nelze použít dávkové zpracování, pokud chcete zobrazit výsledky přecenění.

Vyberte **OK** ke zpracování přecenění cizí měny. Je vytvořen záznam ke sledování historie každého spuštění. Bude vytvořen samostatný záznam pro každou právnickou osobu a účtovací vrstvu.

## <a name="calculate-unrealized-gainloss"></a>Výpočet nerealizovaných zisků/ztrát

V modulu Řízení hotovosti a banky je bankovní měna považována za základní měnu a není přeceněna. Zůstatek bankovního účtu v zúčtovací měně je přeceněn pomocí směnných kurzů mezi měnou banky a zúčtovací měnou v **datum směnného kurzu**. Zůstatek bankovního účtu v měnjě pro vykazování e přeceněn pomocí směnných kurzů mezi měnou banky a měnou pro vykazování v **datum směnného kurzu**.

Je vytvořena transakce pro rozdíl mezi zůstatkem bankovního účtu a nového zůstatku, který je vypočítán pro zúčtovací měnu. Je vytvořena jiná transakce pro rozdíl mezi zůstatkem bankovního účtu a nového zůstatku, který je vypočítán pro měnu vykazování. Položky pro tyto transakce jsou označeny jako odsouhlasené. 

Pro zúčtovací měnu není vytvořen žádný záznam, pokud jí bankovní měna odpovídá. Podobně není pro měnu pro vykazování vytvořen žádný záznam, pokud jí bankovní měna odpovídá.

Transakce přecenění cizí měny je také rozdělena mezi dimenzemi, které se nacházejí u bankovních transakcí. Rozdělení vychází ze zůstatku pro každou dimenzi. Například Banka celkem je 10 000, ale zůstatek organizační jednotky 001 je 4 000, zatímco zůstatek organizační jednotky 002 je 6 000. V takovém případě je 40 procent částky přecenění zaúčtován do účtu přecenění, který má organizační jednotku 001 a 60 procent je zaúčtována na účet přecenění hlavní organizační jednotky 002. Jestliže účetní struktura neobsahuje organizační jednotku, celá částka je zaúčtována na účet přecenění.

## <a name="reverse-foreign-currency-revaluation"></a>Stornovat přecenění cizí měny

Pokud musíte stornovat transakci přecenění, vyberte tlačítko **Stornovat transakci** v podokně akcí stránky **Přecenění cizí měny**. Nový historický záznam přecenění cizí měny bude vytvořen k udržování historického kontrolního záznamu, kdy bylo přecenění vytvořeno nebo stornováno.

Pokud chcete stornovat několik přecenění, nejprve je nutné stornovat nejnovější přecenění. Poté pokračujte ve stornování staršího přecenění podle data. Poté můžete zpracovat nové přecenění pro období, která jsou stornována.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

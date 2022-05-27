---
title: Přehled konsolidace a eliminace
description: V tomto tématu jsou obecné informace o procesu konsolidace a eliminace. Zahrnuje odpovědi na časté dotazy.
author: panolte
ms.date: 01/11/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13151"
- intro-internal
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670b238580ecf800686324fe664be747c551090d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710691"
---
# <a name="consolidation-and-elimination-overview"></a>Přehled konsolidace a eliminace

[!include [banner](../includes/banner.md)]

V tomto tématu jsou obecné informace o procesu konsolidace a eliminace. Zahrnuje odpovědi na časté dotazy.

Když konsolidujete data, finanční výsledky pro více dceřiných společností se kombinují do výsledků pro jednu konsolidovanou společnost. Dceřiné společnosti mohou pracovat na různých verzích nebo systémech, nemusí být plně vlastněny a pravděpodobně používají různé měny. Existuje několik možností pro konsolidaci dat:

-   **Konsolidovat online** – tato možnost zkonsoliduje denní zůstatky vybraných účtů a dimenzí a uloží je do konsolidované společnosti.
-   **Finanční vykazování** – tato možnost umožňuje konsolidaci transakcí a zůstatků a lze ji generovat kdykoli. Lze vytvořit více úrovní hierarchií a lze zobrazit více měn vykazování.
-   **Konsolidovat s importem** – tato možnost importuje zůstatky do konsolidované společnosti.
-   **Export zůstatků společnosti** – tato možnost dodá soubor exportu zůstatků společnosti. Pak lze soubor importovat do jiných instancí nebo systémů. Finanční vykazování lze také použít k exportu zůstatků do souboru aplikace Microsoft Excel.

Eliminace mohou být hlášeny několika způsoby:

-  Pravidla eliminace lze nastavit v systému a následně zpracovat během procesu konsolidace nebo prostřednictvím návrhu eliminace. Pravidla mohou být zaúčtována do každé společnosti, která má vybranou volbu **Použít pro proces finanční eliminace** v nastavení právnické osoby.
-   Samostatné společnosti lze jej vytvořit a použít k ručnímu určení a zaúčtování transakcí eliminace. Tuto společnost lze použít v procesu konsolidace nebo ve finančním vykazování.
-  Účty a finanční dimenze, které se používají k určení mezipodnikové aktivity, lze filtrovat na definici řádků nebo definici sloupců ve Finančním vykazování a lze zcela využít možnosti rozbalení. Vypočítaný sloupec nebo řádek lze použít k odebrání účtů a finančních dimenzí z konsolidovaného součtu.

Existuje mnoho scénářů konsolidace a každá metoda zpracuje scénáře jinými způsoby.

## <a name="frequently-asked-questions"></a>Časté dotazy
1. Dávám přednost zaúčtování eliminací v databázi. Jaké jsou mé možnosti?

Existuje několik možností. Lze použít možnost **Konsolidace online** a zahrnout eliminace během procesu nebo jako návrh. Transakce se zaúčtují v konsolidované společnosti. Případně lze mít samostatnou společnost, v níž ručně vytvoříte eliminace, a použít tuto společnost ve Finančním vykazování nebo během procesu konsolidace

2.  Potřebujeme naše konsolidované výsledky ve více měnách vykazování.

Možnost **Finanční vykazování** nabízí neomezený počet měn vykazování. Data se převádějí během generování sestav podle typu směnného kurzu a metody převodu měny, které jsou nastaveny v hlavním účtu. Nicméně vzhledem k tomu, že volba **Konsolidace online** má pouze jednu měnu vykazování, konsolidovaná společnost je vyžadována pro každou měnu vykazování při použití této možnosti. Možnost **Finanční vykazování** je doporučena.

3. Chci zobrazit podrobnosti do úrovně transakcí pro jednotlivé společnosti.

Řešením je možnost **Finanční vykazování**, protože podrobnosti do úrovně transakcí lze zobrazit pro tolik společností, kolik je zahrnuto do definice stromu výkaznictví.

4. Používáme plánování rozpočtu nebo kontrolu rozpočtu a je nutné je konsolidovat.

Možnost **Finanční vykazování** je řešení pro konsolidaci veškerého plánování rozpočtu nebo dat kontroly rozpočtu.

5. Naše dceřiné společností jsou umístěny v celém světě a máme více účtových osnov. Která metoda je pro konsolidaci našich dat nejlepší?

Pokud je nutné zpracovat více účtových osnov, máte několik možností. Lze použít možnost **Konsolidace online** a vybrat buď konsolidační účet definovaný v hlavním účtu, nebo skupinu konsolidačních účtů. Můžete také použít možnost **Finanční vykazování**, zahrnout více propojení k finančním dimenzím v definici řádku a namapovat účty.

6. Potřebujeme více úrovní konsolidace. Jinými slovy: nejprve konsolidujeme všechny naše evropské dceřiné společnosti na britskou libru (GBP). Potom vezmeme data převádíme konsolidovanou částku na americký dolar. Jak to lze provést?

Pokud je vyžadováno více úrovní konsolidace a v každé úrovni se používají jiné měny, je třeba použít možnost **Konsolidace online**. Je nutné vytvořit více společností pro konsolidaci, které se liší měnou vykazování a zúčtování. Konsolidace se musí spustit vícekrát. Možnost **Finanční vykazování** vždy převádí ze zúčtovací měny každé zdrojové společnosti na vybranou měnu.

7. Máme dceřiné společnosti v jiném systému. Jak je můžeme konsolidovat?

Použijte možnost **Konsolidovat s importem** k přenesení zůstatků do konsolidované společnosti.

8. Některé naše dceřiné společnosti nejsou plně vlastněny. Která metoda je pro jejich konsolidaci nejlepší?

Pro částečně vlastněné dceřiné společnosti máte několik možností. Pomocí volby **Finanční vykazování** můžete definovat definici stromu výkaznictví a vlastnictví. Také můžete použít vypočtený řádek nebo sloupec k zastoupení částečně vlastněné částky. Lze dokonce zobrazit minoritní podíl jako samostatný řádek v sestavě. Můžete také použít možnost **Konsolidace online**. Karta **Právnické osoby** má sloupec **Vlastnictví**, ve kterém můžete definovat procentuální část vlastněnou mateřskou společností.

9. Naše organizace musí zobrazovat konsolidace podle obchodních jednotek nebo chce použít organizační hierarchie.

Řešení je možnost **Finanční vykazování**. Organizační hierarchie, které v sobě mají právnické osoby nebo finanční dimenze, lze hlásit ve Finančním vykazování. Můžete také vytvoříte vlastní hierarchie s více úrovněmi pomocí definice stromu výkaznictví, která kombinuje právnické osoby a hodnoty dimenze.

10. Máme více instancí systému.

Data můžete konsolidovat pomocí možnosti **Export zůstatků společnosti**, abyste exportovali z jedné instance a použili možnost **Konsolidovat s importem** na ostatních instancích.

11. Mohu provést konsolidaci s rozpočtem ve stavu **KONCEPT**? 
            
V konsolidační společnosti nebudete moci zpracovávat ani vyplňovat rozpočty. Doporučujeme použít Financial Reporting ke konsolidaci konceptů rozpočtů.

Další informace naleznete v tématu [Přecenění měny ve společnosti konsolidace](../general-ledger/currency-revaluation-consolidation-company.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]

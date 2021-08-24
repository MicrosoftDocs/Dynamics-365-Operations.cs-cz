---
title: Pracovní prostor pro správu dlouhodobého majetku
description: Toto téma obsahuje informace o pracovním prostoru Správa dlouhodobého majetku. Tento pracovní prostor zobrazuje informace vztahující se k dlouhodobému majetku, který je zadán v systému. Obsahuje souhrnné a analytické zobrazení.
author: saraschi2
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 597a9a32995d44282c89725e053f6da4643dbb691b1b36ae7c237acbfa2afb70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721796"
---
# <a name="fixed-asset-management-workspace"></a>Pracovní prostor pro správu dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Pracovní prostor **Správa dlouhodobého majetku** zobrazuje informace vztahující se k dlouhodobému majetku, který je zadán v systému. Tento pracovní prostor obsahuje souhrnné a analytické zobrazení. Na kartě **Moje práce** jsou zobrazeny souhrnné dlaždice, podrobnosti o majetku a související informace o dlouhodobém majetku v aktuální společnosti. Přímo v pracovním prostoru také můžete do části analýzy Power BI přidat analýzu. Karta **Analýza – všechny společnosti** zobrazuje pomocí funkcí Microsoft Power BI vizuální prvky související s dlouhodobým majetkem ve všech společnostech.

## <a name="my-work"></a>Moje práce

### <a name="summary"></a>Souhrn

Dlaždice v části **Souhrn** poskytují přehled dlouhodobého majetku. K zobrazeným informacím patří metriky týkající se majetku, který nebyl dosud pořízen, majetku získaném během aktuálního roku a majetku, který byl v aktuálním roce vyřazen. Část **Souhrn** také umožňuje rychlý přechod ke stránce seznamu **Dlouhodobý majetek**, k dávkovému návrhu odpisu a deníku dlouhodobého majetku.

### <a name="find-fixed-assets"></a>Najít dlouhodobý majetek

Část **Najít dlouhodobý majetek** umožňuje rychlé hledání majetku zadáním čísla dlouhodobého majetku, skupiny, názvu, umístění nebo odpovědné osoby. V seznamu se zobrazí veškerý majetek, který odpovídá kritériím vyhledávání.

V seznamu můžete zobrazit následující stránky:

 - Stránku **Podrobnosti** k dlouhodobému majetku
 - Stránku **Knihy** pro všechny knihy, které jsou přiřazeny k položce dlouhodobého majetku
 - Stránka **Ocenění dlouhodobého majetku**

### <a name="valuations"></a>Ocenění

Na stránce **Ocenění dlouhodobého majetku** si můžete prohlédnout nejdůležitější informace o dlouhodobém majetku a podrobnosti o všech knihách s ním spojených. Možnost **Zůstatky** vlevo nahoře zobrazí aktuální ocenění každé knihy spojené s dlouhodobým majetkem. Můžete přejít zpět z uvedených hodnot a zobrazit podrobné transakce, které tvoří souhrnnou hodnotu. Možnost **Profil** vlevo nahoře zobrazí plán odpisu každé knihy spojené s dlouhodobým majetkem.

Stránku **Ocenění dlouhodobého majetku** můžete zobrazit v pracovním prostoru **Správa dlouhodobého majetku** nebo na stránce seznamu **Dlouhodobý majetek**.

### <a name="related-information"></a>Související informace

Můžete přejít přímo na stránku **Nastavení knih**, **Dotaz na transakce dlouhodobého majetku** a několik různých sestav. Stačí použít odkazy v části **Související informace** v pracovním prostoru.

### <a name="analytics--all-companies"></a>Analýza – všechny společnosti

Stránka **Analýza** obsahuje důležité metriky týkající se dlouhodobého majetku u všech právnických osob v systému. Přístup k této kartě je řízen bezpečnostními oprávněními Zobrazit analýzu dlouhodobého majetku pro všechny společnosti.

V následující tabulce jsou uvedeny vizualizace dostupné na stránkách sestav.

| Stránka sestavy            | Vizualizace        |
|------------------------|----------------------|
| Ocenění dlouhodobého majetku | Celková zůstatková účetní hodnota |
| Ocenění dlouhodobého majetku | Zůstatková účetní hodnota podle skupiny dlouhodobého majetku |
| Ocenění dlouhodobého majetku | Pořizovací hodnoty |
| Ocenění dlouhodobého majetku | Hodnoty při vyřazení |
| Ocenění dlouhodobého majetku | Podrobnosti o dlouhodobém majetku |
| Mapy ocenění        | Celková zůstatková účetní hodnota |
| Mapy ocenění        | Umístění dlouhodobého majetku |
| Mapy ocenění        | Podrobnosti o dlouhodobém majetku |

Pokud chcete zobrazit analýzu s daty, je třeba nejprve aktualizovat agregované měření AssetTransactionMeasure na stránce **Obchod s entitami**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Zkopírování vedlejších produktů z existující verze receptury
description: Tato procedura popisuje postup kopírování vedlejších produktů z existující verze receptury do jiné verze receptury pro uvolněný produkt.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbcf2abc37441f9ff23e2b180c261831dfb79369
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829275"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>Zkopírování vedlejších produktů z existující verze receptury

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje postup kopírování vedlejších produktů z existující verze receptury do jiné verze receptury pro uvolněný produkt. Je důležité, aby existovala alespoň jedna verze receptury přidružená k vedlejším produktům. Společnost s ukázkovými daty USP2 slouží k vytváření této procedury.


## <a name="find-a-released-product"></a>Vyhledat uvolněný produkt
1. Přejděte na Uvolněné produkty.
2. Klepněte na tlačítko Zobrazit filtry.
    * Chystáte se v dialogovém okně Filtr přidat pole Výrobní typ.  
3. Klepnutím na tlačítko Přidat pole filtru přidáte pole Typ výroby.
    * V dalším kroku je třeba ručně zadat vzorec do pole Typ výroby předtím, než vyberete možnost Použít. Tím nastavíte filtr na seznamu vydaných produktů.  
4. V poli Typ výroby ručně zadejte vzorec.
5. Klepněte na možnost Použít.

## <a name="select-a-released-product"></a>Vybrat uvolněný produkt
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
2. Klikněte na Verze receptury.
    * V podokně akcí Analýza klikněte na položku Verze receptur.  

## <a name="copy-co-products"></a>Kopírovat souběžný produkt
1. V podokně akcí klikněte na možnost Verze receptury.
2. Klepněte na možnost Souběžné produkty.
3. Klepněte na tlačítko Kopírovat.
4. V poli Číslo zboží zadejte nebo vyberte hodnotu.
5. V poli Verze receptury zadejte nebo vyberte hodnotu.
6. Klikněte na tlačítko OK.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
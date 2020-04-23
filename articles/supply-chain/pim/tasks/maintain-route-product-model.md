---
title: Údržba postupu pro model produktu
description: Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24419cb9bad4b4344fe23789750387de6cca3796
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203503"
---
# <a name="maintain-route-for-a-product-model"></a>Údržba postupu pro model produktu

[!include [banner](../../includes/banner.md)]

Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval. Při provádění celým procesem tento postup používá model špičkový model reproduktoru v ukázkové společnosti USMF.


## <a name="add-a-route-operation"></a>Přidání postupu operace
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro toto cvičení vyberte model špičkového reproduktoru.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Rozbalte sekci Operace postupu.
6. Klepněte na možnost Přidat.
7. Zadejte hodnotu do pole Název.
8. Zadejte nějakou hodnotu do pole Popis.
9. Klikněte na položku Uložit.

## <a name="enter-route-operation-details"></a>Zadání podrobností operace postupu
1. Klepněte na Podrobnosti operace postupu.
2. V poli Operace zadejte nebo vyberte hodnotu.
3. V číslu operace Č. zadejte číslo.
    * Čísla operace určující pořadí v postupu.  
    * Každá vlastnost při operaci postupu může získat statickou hodnotu nebo namapování na atribut. Mapování na atribut způsobí, že hodnota bude nastavena v rámci konfigurace.  
4. V poli Skupina postupů zadejte nebo vyberte hodnotu.
    * Skupina postupů určuje základní chování pro náklady, spotřebu a nastavení.  
5. Klikněte na záložku Nastavení.
6. Klepněte na kartu Časy.
7. Do pole Množství procesu zadejte číslo.
    * Určuje, kolik se zpracuje při jedné operaci.  
8. Do pole Hodiny/čas zadejte číslo.
    * Zadejte časový úsek.  
9. Zaškrtněte políčko položky Nastavit.
10. Do pole Operační čas zadejte číslo.
    * Určete čas zpracování pro množství, které jste zadali.  
11. Klepněte na kartu Požadavky na zdroj.
12. Klepněte na možnost Přidat.
13. Označte v seznamu vybraný řádek.
14. V poli Typ požadavku vyberte možnost.
    * Rozhodněte, zda chcete zadat určité zdroje nebo možností, které musí mít.  
15. V poli Požadavek zadejte nebo vyberte hodnotu.
16. Klikněte na tlačítko OK.


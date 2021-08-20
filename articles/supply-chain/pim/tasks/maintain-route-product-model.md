---
title: Údržba postupu pro model produktu
description: Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 704a6b72c9eb8dc49ba9410ccd3689ba5ccfdd1f03e538b95ad174f6c1ee9796
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746129"
---
# <a name="maintain-route-for-a-product-model"></a>Údržba postupu pro model produktu

[!include [banner](../../includes/banner.md)]

Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval. Při provádění celým procesem tento postup používá model špičkový model reproduktoru v ukázkové společnosti USMF.

## <a name="add-a-route-operation"></a>Přidání postupu operace

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro toto cvičení vyberte model špičkového reproduktoru.  
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Rozbalte sekci **Operace postupu**.
1. Vyberte **přidat**.
1. Zadejte hodnotu do pole **Název**.
1. Zadejte hodnotu do pole **Popis**.
1. Zvolte **Uložit**.

## <a name="enter-route-operation-details"></a>Zadání podrobností operace postupu

1. Vyberte **Podrobnosti operace trasy**.
1. V poli **Operace** zadejte nebo vyberte hodnotu.
1. V poli **Operace č.** zadejte číslo.
    * Čísla operace určující pořadí v postupu.  
    * Každá vlastnost při operaci postupu může získat statickou hodnotu nebo namapování na atribut. Mapování na atribut způsobí, že hodnota bude nastavena v rámci konfigurace.  
1. V poli **Skupina postupů** zadejte nebo vyberte hodnotu.
    * Skupina postupů určuje základní chování pro náklady, spotřebu a nastavení.  
1. Vyberte kartu **Nastavení**.
1. Vyberte kartu **Časy**.
1. Do pole **Množství procesu** zadejte číslo.
    * Určuje, kolik se zpracuje při jedné operaci.  
1. Do pole **Hodiny/čas** zadejte číslo.
    * Zadejte časový úsek.  
1. Zaškrtněte políčko položky **Nastavit**.
1. Do pole **Operační čas** zadejte číslo.
    * Určete čas zpracování pro množství, které jste zadali.  
1. Zvolte kartu **Požadavky na zdroj**.
1. Vyberte **přidat**.
1. Označte na seznamu vybraný řádek.
1. V poli **Typ požadavku** vyberte možnost.
    * Rozhodněte, zda chcete zadat určité zdroje nebo možností, které musí mít.  
1. V poli **Požadavek** zadejte nebo vyberte hodnotu.
1. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
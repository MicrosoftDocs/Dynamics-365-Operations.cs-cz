---
title: Vytvoření prodejní objednávky pro konfigurovatelný produkt
description: Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81e573593fbbb0bf87e53c5cbd985b38a8db89ac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841592"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Vytvoření prodejní objednávky pro konfigurovatelný produkt

[!include [banner](../../includes/banner.md)]

Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce. Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF. Zpracovatel prodejních objednávek obvykle používá tuto proceduru.


## <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku
1. Klikněte na Zpracování a dotaz na prodejní objednávku.
2. Klikněte na položku Nová.
3. Klikněte na Prodejní objednávka.
4. V poli Účet odběratele vyberte US-001. 
5. Klikněte na tlačítko OK.
6. Do pole Číslo položky vyberte „D0006“.
    * Pro tento úkol je nutné vybrat konfigurovatelný produkt.  
7. Klikněte na Produkt a dodávka.
8. Klikněte na Řádek konfigurace.
    * Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole Zahrnout kabel je nyní nastaveno na hodnotu True.  
    * Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.  
9. Klikněte na Šablona nákladu.
    * Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace. Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte klepnout na tlačítko Odemknout.  
10. Klikněte na tlačítko OK.
11. Klikněte na tlačítko OK.
12. Rozbalte sekci Podrobnosti řádku.
13. Klepněte na kartu Produkt.
    * Konfigurace položky je nyní uvedena pod dimenzemi produktu.  
14. Zavřete stránku.

## <a name="select-the-product-configuration"></a>Vyberte konfiguraci produktu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
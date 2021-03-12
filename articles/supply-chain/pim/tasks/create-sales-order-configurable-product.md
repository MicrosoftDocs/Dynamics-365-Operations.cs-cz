---
title: Vytvoření prodejní objednávky pro konfigurovatelný produkt
description: Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992313"
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


---
title: Vytvoření prodejní objednávky pro konfigurovatelný produkt
description: Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570578"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Vytvoření prodejní objednávky pro konfigurovatelný produkt

[!include [banner](../../includes/banner.md)]

Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce. Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF. Zpracovatel prodejních objednávek obvykle používá tuto proceduru.

## <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku

1. Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.
1. Zvolte **Nové**.
1. Vyberte **Prodejní objednávka**.
1. V poli **Účet odběratele** vyberte *US-001*. 
1. Vyberte **OK**.
1. V poli **Číslo položky** zvolte *D0006*.
    * Pro tento úkol je nutné vybrat konfigurovatelný produkt.  
1. Vyberte **Produkt a dodávka**.
1. Vyberte **Nakonfigurovat řádek**.
    * Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole **Zahrnout kabel** je nyní nastaveno na hodnotu *True*.  
    * Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.  
1. Vyberte **Načíst šablonu**.
    * Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace. Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte vybrat tlačítko **Odemknout**.  
1. Vyberte **OK**.
1. Vyberte **OK**.
1. Rozbalte sekci **Podrobnosti řádku**.
1. Vyberte kartu **Produkt**.
    * Konfigurace položky je nyní uvedena pod dimenzemi produktu.  
1. Zavřete stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
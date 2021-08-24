---
title: Vytvoření online sítě a definování atributů kanálu
description: Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98d218a2d4f3b31084adfbc013dd0999f459dc1572e29a6470edc7cb899809c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713359"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Vytvoření online sítě a definování atributů kanálu

[!include [banner](../includes/banner.md)]

Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie. Než budete moci vytvořit nový online kanál, je nutné vytvořit organizační hierarchii. Tato procedura používá data ukázkové společnosti USRT.


## <a name="create-a-new-online-channel"></a>Vytvoření nového online kanálu
1. Přejděte na Retail and Commerce > Kanály > Online obchody.
2. Klikněte na možnost Nový.
3. Zadejte hodnotu do pole Název.
4. V poli Sklad zadejte nebo vyberte hodnotu.
5. V poli Časové pásmo obchodu vyberte požadovanou možnost.
6. V poli Výchozí odběratel zadejte nebo vyberte hodnotu.
7. V poli Adresář odběratele zadejte nebo vyberte hodnotu.
8. V poli Platební podmínky zadejte nebo vyberte hodnotu.
9. V poli Metody platby zadejte nebo vyberte hodnotu.
10. V poli Profil oznámení e-mailem zadejte nebo vyberte hodnotu.
11. Rozbalte část Finanční dimenze.
12. V poli BusinessUnit zadejte nebo vyberte hodnotu.
    * Podobně nastavte hodnotu pro všechny ostatní výchozí dimenze.  
13. Klikněte na položku Uložit.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Přidat online kanál do organizační hierarchie
1. Zavřete stránku.
2. Přejděte do nabídky Správa organizace > Organizace > Organization hierarchies.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na možnost Zobrazit.
5. Klikněte na položku Upravit.
    * Můžete vybrat libovolný uzel hierarchie, pod který chcete vložit nový kanál.  
6. Klepněte na tlačítko Vložit.
7. Klikněte na Kanál Commerce.
8. Klepněte na tlačítko OK.
9. Kliknutím na možnost Publikovat otevřete dialog Zanechat.
10. Do pole Datum platnosti zadejte datum a čas.
11. Klikněte na tlačítko Publikovat.

## <a name="configure-orders-for-near-real-time-notification"></a>Konfigurace objednávek pro blízké oznámení v reálném čase
1. Přejděte na možnost Retail a Commerce > Nastavení centrály > Parametry > Parametry Commerce.
2. Nastavte možnost Použít službu Realtime Service pro vytvoření obejdnávky eCommerce na Ano.
3. Spusťte plán distribuce 1070 k synchronizování změn do databáze kanálů. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
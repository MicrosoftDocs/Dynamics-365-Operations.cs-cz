---
title: Vytvoření online sítě a definování atributů kanálu
description: Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "312363"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Vytvoření online sítě a definování atributů kanálu

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie. Než budete moci vytvořit nový online kanál, je nutné vytvořit organizační hierarchii. Tato procedura používá data ukázkové společnosti USRT.


## <a name="create-a-new-online-channel"></a>Vytvoření nového online kanálu
1. Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Online obchody.
2. Klikněte na položku Nová.
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
7. Klikněte na Maloobchodní síť.
8. Klikněte na tlačítko OK.
9. Kliknutím na možnost Publikovat otevřete dialog Zanechat.
10. Do pole Datum platnosti zadejte datum a čas.
11. Klikněte na tlačítko Publikovat.


---
title: Nastavení dokladů převodu pro pohyb zboží v rámci společnosti
description: Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185674"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Nastavení dokladů převodu pro pohyb zboží v rámci společnosti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje postup vytvoření přepravních dokladů pro pohyb zboží v rámci společnosti. Tato procedura je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Litvě. Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě. Než bude možné tuto proceduru dokončit, je nutné dokončit proceduru "Nastavení převodních dokumentů pro pohyb zboží uvnitř společnosti". Tato procedura je určena pouze pro skladové účetní. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="create-a-transfer-order"></a>Vytvoření převodního příkazu
1. Přejděte na Správa zásob > Příchozí objednávky > Objednávka převozu.
2. Klikněte na položku Nová.
3. V poli Ze skladu zadejte nebo vyberte hodnotu.
4. V poli Do skladu zadejte nebo vyberte hodnotu.
5. Klepněte na možnost Přidat.
6. Označte v seznamu vybraný řádek.
7. V poli Číslo zboží zadejte nebo vyberte hodnotu.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Zadání podrobností přepravy pro převodní příkaz
1. Klikněte na položku Uložit.
2. V podokně akcí klikněte na možnost Expedovat.
3. Klikněte na Podrobnosti přepravy.
4. Vyberte možnost Ano v poli Tisk podrobností o přepravě.
5. V poli Zboží vydal zadejte nebo vyberte hodnotu.
6. Zadejte hodnotu do pole Balík.
7. Do pole Úroveň rizika zatížení zadejte hodnotu.
8. V poli Dopravce zadejte nebo vyberte hodnotu.
9. V poli Model zadejte nebo vyberte hodnotu.
10. Zadejte hodnotu do pole Číslo registrace.
11. Zadejte hodnotu do pole Registrační číslo přívěsu.
12. V poli Řidič zadejte nebo vyberte hodnotu.
13. Do pole Jméno řidiče zadejte hodnotu.
14. Klikněte na položku Uložit.
15. Zavřete stránku.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Zobrazení dodacího listu pro nezaúčtovaný převodní příkaz
1. Klepněte na Dodací list.
2. Klikněte na tlačítko OK.
3. Zavřete stránku.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Zobrazení dodacího listu pro zaúčtovaný převodní příkaz
1. V podokně akcí klikněte na možnost Převodní příkaz.
2. V podokně akcí klikněte na možnost Expedovat.
3. Klikněte na Převodní příkaz expedice.
4. Klikněte na záložku Obecné.
5. Vyberte volbu v poli Aktualizovat.
6. Klikněte na záložku Přehled.
7. Zadejte hodnotu do pole Dodací list.
8. Klikněte na tlačítko OK.
9. V podokně akcí klikněte na možnost Expedovat.
10. Klepněte na Dodací list.
11. Klikněte na tlačítko OK.

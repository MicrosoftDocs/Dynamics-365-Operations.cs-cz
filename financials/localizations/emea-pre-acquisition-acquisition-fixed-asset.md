---
title: "Příspěvek před-pořízení dlouhodobého majetku"
description: "Toto téma vysvětluje, jak vytvořit a zaúčtovat pořízení dlouhodobého majetku před."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264704
ms.assetid: 89218666-7c5e-45ca-aead-a87853d05928
ms.search.region: Czech Republic, Hungary
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c51f041a8287b4623bb8f49bb016c08f7de5b9ae
ms.lasthandoff: 03/31/2017


---

# <a name="post-the-pre-acquisition-of-a-fixed-asset"></a>Příspěvek před-pořízení dlouhodobého majetku

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak vytvořit a zaúčtovat pořízení dlouhodobého majetku před.

**Poznámka:** funkce pro účtování pořízení dlouhodobého majetku před je k dispozici pouze pro právnické osoby, které mají jejich primární adresy do Maďarska a České republiky. Není předběžné pořízení dlouhodobého majetku odpisovaného a nemá žádný vliv, náklady na pořízení nebo zůstatková účetní hodnota dlouhodobého majetku. Při zaúčtování před-pořízení se změní stav dlouhodobého majetku na **získané**. Dlouhodobý majetek, který má **získané** stav není odpisovatelný. Naopak při účtování pořízení, stav se změní na **Open**, a je Odpisovatelný dlouhodobý majetek.

## <a name="set-up-preacquisitions"></a>Nastavit preacquisitions
Před zaúčtováním před-pořízení, musíte provést následující nastavení:

-   Na **dlouhodobého majetku parametry** stránky, nastavte **povolit před-pořízení** možnost na **Ano**.
-   Na **účetní profily dlouhodobého majetku** stránku, nastavit účetní profil pro typ zaúčtování před-pořízení dlouhodobého majetku.

## <a name="post-a-preacquisition-of-a-fixed-asset"></a>Preacquisition dlouhodobého majetku, účtování
1.  Na **dlouhodobého majetku** stránce, vytvořte nový deník a zadejte všechny příslušné údaje podle potřeby.
2.  Deník, který jste právě vytvořili, klepněte na tlačítko **řádky** otevřete **doklad deníku** stránky.
3.  Kliknutím na možnost **Nový** vytvořte řádek.
4.  V **typ transakce** vyberte transakci, která má **před-pořízení** typ transakce.
5.  Zadejte hodnoty pro zbývající pole podle potřeby.
6.  Klepněte na tlačítko **ověřit** a ověřte řádky deníku.
7.  Klepněte na tlačítko **návrhy**&gt;**návrh před-pořízení**.
8.  Klepněte na tlačítko **vyberte** nastavit kritéria pro výběr a klepněte na tlačítko **OK**.
9.  Klepněte na tlačítko **OK** zavřete **návrh před-pořízení** stránky.
10. Klepněte na tlačítko **účtování**&gt;**účtování** k zaúčtování transakce před-pořízení. Na **knihy** stránky, stav dlouhodobého majetku by nyní měly být **získané**.






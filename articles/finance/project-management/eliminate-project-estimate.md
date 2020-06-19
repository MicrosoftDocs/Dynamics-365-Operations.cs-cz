---
title: Eliminace odhadu projektu
description: Toto téma poskytuje informace o odstranění odhadu projektu po jeho dokončení.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410198"
---
# <a name="eliminate-a-project-estimate"></a>Eliminace odhadu projektu

[!include [banner](../includes/banner.md)]

Odhady projektu poskytují finanční pohled na práci, která je odhadována a naplánována na projekt. Chcete-li pracovat s odhady pro určitý projekt, je třeba tento projekt přiřadit k projektu odhadu. Projekt odhadu je vždy založen na stávajícím projektu, ale jednotlivé projekty mohou odkazovat na jeden projekt odhadu. K odhadu projektů lze připojit pouze investiční projekty s pevnou cenou a investiční projekty, které musí patřit do stejné skupiny projektů jako odhadovaný projekt.

Aby bylo možné projekt odhadu vyloučit, musí být kompletní. Následující kroky vysvětlují, jak eliminovat odhad.

1. Přejděte na **Řízení projektu a účetnictví** > **Všechny projekty** a otevřete projekt. 
2. Na kartě **Spravovat** vyberte **Odhady** a na stránce **Odhad** vyberte **Eliminovat**.
3. Na stránce **Eliminujte odhad** na kartě **Všeobecné** nastavte následující možnosti:

   - **Kód období**: Chcete-li vybrat vhodné projekty odhadu, vyberte kód období. 
   - **Datum odhadu**: Vyberte příslušné datum odhadu pro eliminaci.
   - **Eliminovat s varováními WIP** : Povolte tuto možnost, chcete-li poskytovat upozornění, pokud bude eliminován odhad, který je spojen s nedokončenou prací (WIP). Pokud tato možnost není povolena, eliminace nemůže pokračovat, pokud existují neočekávané transakce. 
   > [!NOTE]
   > Tato možnost je k dispozici, pouze pokud je eliminace použita na odhadovaný projekt. Není k dispozici, pokud používáte pravidelné účtování. Toto nastavení pracuje s nastavením na kartě **Odhad** na stránce **Parametry projektu** ve skupině polí **Umožněte odstranění, pokud existují transakce bez odhadu**.
   - **Nastavte fázi na Dokončené**: Povolením této možnosti nastavíte fázi odhadu projektu na **Dokončeno** po spuštění eliminace.
   - **Tisk seznamu odhadu**: Vyberte informace, které mají být zahrnuty při tisku odhadu projektů.
   - **Zobrazit Infolog**: Povolením této možnosti zobrazíte Infolog.
   - **Datum zaúčtování**: Vyberte datum zaúčtování odhadu do účetní knihy.

4.  Vyberte **OK**.
5. Po dokončení procesu eliminace se zobrazí projekt eliminovaného odhadu se zápornou hodnotou. 

Pokud jste nezamýšleli eliminovat odhad, můžete vybrat eliminovaný odhad a vybrat **Storno eliminace**.   

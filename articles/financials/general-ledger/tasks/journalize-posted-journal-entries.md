---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "318527"
---
# <a name="journalize-posted-journal-entries"></a>Zapsání zaúčtovaných položek deníku do deníku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku. Tato procedura používá data ukázkové společnosti USMF.

1. Ověřte nastavení pro deník hlavní knihy v části Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy.
2. Pole Rozšířený deník hlavní knihy lze nastavit na Ano nebo Ne. Pokud ano, bude výstup sestavy jiný.
3. Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku.
    * Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.  
4. Zavřete stránku.
5. Přejděte do hlavní knihy > Periodické úkoly > Zapisování do deníku.
6. Klepněte na tlačítko Filtr.
7. Vyberte řádek obsahující kritéria filtru, která chcete definovat.
8. V poli Kritéria zadejte nebo vyberte kritéria filtrování.
9. Kliknutím na tlačítko OK stránku filtru zavřete.
10. Kliknutím na tlačítko OK spusťte proces zařazení do deníku.
    * Po dokončení procesu se vygeneruje sestava.  


---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5028db1db2359a54d565fc299c9a3353a4cf8297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826147"
---
# <a name="journalize-posted-journal-entries"></a>Zapsání zaúčtovaných položek deníku do deníku

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku. Tato procedura používá data ukázkové společnosti USMF.

1. V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**.
2. Pole **Rozšířený deník hlavní knihy** lze nastavit na Ano nebo Ne. Pokud ano, bude výstup sestavy jiný.
3. Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku. Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.  
4. Zavřete stránku.
5. V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Periodické úlohy > Zapisování do deníku**.
6. Klikněte na tlačítko **Filtr**.
7. Vyberte řádek obsahující kritéria filtru, která chcete definovat.
8. V poli **Kritéria** zadejte nebo vyberte kritéria filtrování.
9. Kliknutím na tlačítko **OK** stránku filtru zavřete.
10. Kliknutím na tlačítko **OK** spusťte proces zařazení do deníku. Po dokončení procesu se vygeneruje sestava.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
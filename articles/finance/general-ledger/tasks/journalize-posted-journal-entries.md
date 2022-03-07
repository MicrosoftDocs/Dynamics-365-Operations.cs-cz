---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca1aed3a77da66ef336942b2c178abdd425d3c25
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240659"
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
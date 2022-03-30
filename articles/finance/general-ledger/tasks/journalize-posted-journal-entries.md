---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400868"
---
# <a name="journalize-posted-journal-entries"></a>Zapsání zaúčtovaných položek deníku do deníku

[!include [banner](../../includes/banner.md)]

Proces zápisu do deníku v hlavní knize poskytuje způsob, jak seskupit a vykazovat zaúčtované položky dokladů pro vaši hlavní knihu. Na základě vámi zadaných kritérií zpracování vygeneruje seznam dokladů, které používají jedinečnou číselnou řadu a mají hodnotu pole **Číslo deníku** hlavní knihu uvedenou jako referenci.

Při zapisování do deníku zaúčtovaných položek deníku postupujte takto. Tato procedura používá data ukázkové společnosti **USMF**.

1. Přejděte k nabídce **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**.
2. V poli **Rozšířený deník hlavní knihy** vyberte hodnotu. Pokud vyberete **Ano**, bude výstup sestavy jiný.
3. Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku. Pokud vyberete **Ano**, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.
4. Zavřete stránku.
5. Přejděte do nabídky **Hlavní kniha** \> **Periodické úkoly** \> **Zapisování do deníku** a vyberte **Filtr**.
6. Vyberte řádek obsahující kritéria filtru, který chcete definovat.
7. V poli **Kritéria** zadejte nebo vyberte kritéria filtrování.
8. Vyberte **OK** a stránku zavřete.
9. Výběrem tlačítka **OK** spusťte proces zápisu do deníku. Po dokončení procesu se vygeneruje sestava.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

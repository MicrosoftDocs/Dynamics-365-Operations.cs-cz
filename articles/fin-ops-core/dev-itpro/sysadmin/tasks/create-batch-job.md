---
title: Vytvoření dávkové úlohy
description: Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191378"
---
# <a name="create-a-batch-job"></a>Vytvoření dávkové úlohy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS). Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil. Dávkovou úlohu můžete nastavit následujícím postupem. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-the-batch-job"></a>Vytvoření dávkové úlohy
1. Přejděte do **navigačního podokna > Moduly > Správa systému > Dotazy > Dávkové úlohy**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Popis práce**.
4. Do pole **Plánované počáteční datum a čas** zadejte datum a čas.
5. Klikněte na možnost **Uložit**.

## <a name="create-a-recurrence"></a>Vytvoření opakování
1. V podokně akcí klikněte na možnost **Dávková úloha**.
2. Klikněte na **Opakování**. Pomocí těchto možností zadejte rozsah a vzor opakování.  
3. Klikněte na tlačítko **OK**.

## <a name="add-alerts"></a>Přidání výstrah
1. V podokně akcí klikněte na možnost **Dávková úloha**.
2. Klikněte na **Výstrahy**. Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení. Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.   
3. Klikněte na tlačítko **OK**.

## <a name="adjust-batch-job-status"></a>Úprava stavu dávkové úlohy
1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Vyberte odpovídající dávkovou úlohu.
3. V podokně akcí klikněte na možnost **Dávková úloha > Funkce > Změnit stav**.
4. Vyberte příslušný stav:
    - **Srážka**: Nastavte dávkovou úlohu jako **srážku** tak, aby byla zadržena plánovačem dávkových úloh. Ekvivalent *zastavení*
    - **Čekání**: Nastavte dávkovou úlohu jako **čekání**, aby čekala na vyzvednutí plánovačem úloh. Ekvivalent *přejít*
5. Klikněte na tlačítko **OK**.
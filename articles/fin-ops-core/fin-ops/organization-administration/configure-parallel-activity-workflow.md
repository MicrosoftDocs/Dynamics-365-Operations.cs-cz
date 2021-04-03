---
title: Konfigurace paralelních aktivit ve workflow
description: Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 450420d44ad4aab233afc5a116369e993aa7a15b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570607"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Konfigurace paralelních aktivit ve workflow

[!include [banner](../includes/banner.md)]

Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.

Paralelní aktivita je tvořena větvemi workflowu, které běží ve stejnou dobu.

## <a name="name-a-parallel-activity"></a>Pojmenování paralelní aktivity

Pomocí následujících kroků zadejte název paralelní aktivity.

1. Klikněte pravým tlačítkem na paralelní aktivitu a poté klikněte na tlačítko **Vlastnosti** k otevření formuláře **Vlastnosti**.
2. V levém podokně klepněte na tlačítko **Základní nastavení**.
3. V poli **Název** zadejte jedinečný název paralelní aktivity.
4. Klepněte na tlačítko **Zavřít**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurace větví paralelní aktivity

Pomocí následujících kroků přidejte a nakonfigurujte větve této paralelní aktivity.

1. Poklikejte na paralelní aktivitu, aby se zobrazily její větve.
2. Pokud chcete přidat pobočku, přetáhněte prvek **Větev** z oblasti **Prvky workflowu** do oblasti vložení na plátně. Následující obrázek znázorňuje oblast vložení.

    ![Oblast vložení](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Pořadí větví není důležité, protože všechny větve paralelní aktivity běží současně.

3. Informace o konfiguraci jednotlivých větví uvádí téma [Konfigurace paralelních větví ve workflow](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
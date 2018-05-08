---
title: "Konfigurace paralelních aktivit ve workflowu"
description: "Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ec1c1d8abc49deb8ef16322370c59d40b01d344c
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurace paralelních aktivit ve workflowu

[!include [banner](../includes/banner.md)]

Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.

Paralelní aktivita je tvořena větvemi workflowu, které běží ve stejnou dobu.

## <a name="name-a-parallel-activity"></a>Pojmenování paralelní aktivity
Pomocí následujících kroků zadejte název paralelní aktivity.
1.  Klikněte pravým tlačítkem na paralelní aktivitu a poté klikněte na tlačítko **Vlastnosti** k otevření formuláře **Vlastnosti**.
2.  V levém podokně klepněte na tlačítko **Základní nastavení**.
3.  V poli **Název** zadejte jedinečný název paralelní aktivity.
4.  Klepněte na tlačítko **Zavřít**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurace větví paralelní aktivity
Pomocí následujících kroků přidejte a nakonfigurujte větve této paralelní aktivity.
1. Poklikejte na paralelní aktivitu, aby se zobrazily její větve.
2. Pokud chcete přidat pobočku, přetáhněte prvek **Větev** z oblasti **Prvky workflowu** do oblasti vložení na plátně. Následující obrázek znázorňuje oblast vložení.![Oblast vložení](./media/workflow_insertionpoint.gif)

   |                                              <strong>Poznámka</strong>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | Pořadí větví není důležité, protože všechny větve paralelní aktivity běží současně. |


3. Informace o konfiguraci jednotlivých větví uvádí téma [Konfigurace paralelní větve](configure-parallel-branch-workflow.md).







---
title: Synchronizace data a času v úlohách importu
description: Použijte časová pásma UTC v úlohách importu, abyste předešli problémům s převody časových pásem.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403834"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Synchronizace data a času v úlohách importu

[!include [banner](../includes/banner.md)]

Je důležité nastavit časové pásmo pro vaši úlohu importu na koordinovaný světový čas (UTC). Pokud použijete jiné nastavení, mohou se v importovaných datech zobrazit neočekávaná data a časy. Bez správného nastavení převede proces importu datum UTC na místní formát a poté jej znovu převede systémové nastavení.

Tato duální konverze způsobí změnu dat mezi aplikacemi. Například duální konverze může způsobit, že se počáteční datum zaměstnance bude lišit mezi Dynamics 365 Human Resources a Dynamics 365 Finance kvůli rozdílům v místních časových pásmech. Nastavení úlohy importu na UTC tento problém řeší.

1. V Dynamics 365 Finance and Operations vyberte **Správa dat**.

2. Vyberte **Importovat projekty** a poté vyberte projekt.

3. V části **Formát data zdroje** vyberte **CSV-Unicode**.

   [![Změna formátu zdrojového data na UTC.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Změňte **Časové pásmo** na **standard UTC (Coordinated Universal Time)** a změňte **Jazyk** na **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

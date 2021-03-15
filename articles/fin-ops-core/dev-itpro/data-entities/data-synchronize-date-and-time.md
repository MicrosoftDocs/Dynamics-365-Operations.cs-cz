---
title: Synchronizace data a času v úlohách importu
description: Použijte časová pásma UTC v úlohách importu, abyste předešli problémům s převody časových pásem.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798712"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Synchronizace data a času v úlohách importu

[!include [banner](../includes/banner.md)]

Je důležité nastavit časové pásmo pro vaši úlohu importu na koordinovaný světový čas (UTC). Pokud použijete jiné nastavení, mohou se v importovaných datech zobrazit neočekávaná data a časy. Bez správného nastavení převede proces importu datum UTC na místní formát a poté jej znovu převede systémové nastavení.

Tato duální konverze způsobí změnu dat mezi aplikacemi. Například duální konverze může způsobit, že se počáteční datum zaměstnance bude lišit mezi Dynamics 365 Human Resources a Dynamics 365 Finance kvůli rozdílům v místních časových pásmech. Nastavení úlohy importu na UTC tento problém řeší.

1. V Dynamics 365 Finance and Operations vyberte **Správa dat**.

2. Vyberte **Importovat projekty** a poté vyberte projekt.

3. V části **Formát data zdroje** vyberte **CSV-Unicode**.

   [![Změna formátu zdrojového data na UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Změňte **Časové pásmo** na **standard UTC (Coordinated Universal Time)** a změňte **Jazyk** na **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
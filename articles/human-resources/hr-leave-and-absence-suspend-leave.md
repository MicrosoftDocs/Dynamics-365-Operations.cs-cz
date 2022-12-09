---
title: Pozastavení pracovního volna
description: U zaměstnance v aplikaci Dynamics 365 Human Resources můžete pozastavit pracovní volno.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805253"
---
# <a name="suspend-leave"></a>Přerušit pracovní volno

>[!Important]
>Funkce uvedené v tomto článku jsou aktuálně dostupné pro zákazníky používající samostatnou verzi aplikace Dynamics 365 Human Resources. Některé nebo všechny funkce budou dostupné jako součást budoucího vydání na infrastruktury Finance po vydání Finance 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete pozastavit pracovní volno pro zaměstnance, abyste zastavili zpracování časového rozlišení pracovního volna u vybraných typů pracovního volna.

## <a name="suspend-leave-and-absence-for-an-employee"></a>Pozastavit pracovní volno a absenci pro zaměstnance

1. V záznamu zaměstnance vyberte možnost **Pracovní volno**.

2. Vyberte **Přerušit pracovní volno**.

3. Zvolte **Nové**.

4. V dialogovém okně **Přerušit časové rozlišení pracovního volna** vyberte **Typ pracovního volna** spolu s **Počátečním datem** a **Koncovým datem** přerušení.

5. Volitelně můžete přidat **Komentář** k přerušení. 

Pokud jsou časové rozlišení zpracovávány i v době, kdy je pracovní volno zaměstnance přerušeno, nebude pro typy přerušeného volna provedeno žádné časové rozlišení.

> [!NOTE]
> Žádosti o pracovní volno pozastaví žádosti o volno, ale žádosti o volno nepozastaví žádosti o pracovní volno.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)
- [Časové rozlišení plánů pracovního volna a absence](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

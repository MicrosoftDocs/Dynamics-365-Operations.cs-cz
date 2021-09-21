---
title: Chyba při opětovném odeslání nákupní objednávky do workflow po změně
description: Chyba při opětovném odeslání nákupní objednávky do workflow po změně
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475843"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Chyba při opětovném odeslání nákupní objednávky do workflow po změně


## <a name="symptoms"></a>Příznaky

Při opakovaném odeslání nákupní objednávky po změně dojde v pracovním postupu k následující chybě:

> Zastaveno (chyba): Výjimka X++: Změny nákupní objednávky PO0000569 jsou povoleny pouze ve stavu Koncept, když je aktivována správa změn na<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

K tomuto problému dochází, pouze pokud byla nákupní objednávka ve stavu *Potvrzeno* před požadováním změn. Pokud požadujete změny, když je objednávka ve stavu *Schváleno*, lze pracovní postup úspěšně zpracovat.

## <a name="resolution"></a>Řešení

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problém bude vyřešen prostřednictvím [tohoto článku znalostní báze Microsoft](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

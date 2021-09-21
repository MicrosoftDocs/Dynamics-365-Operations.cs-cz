---
title: Workflow deníku zásob se nikdy nedokončí a deník nelze zpracovat
description: Po odeslání pracovního postupu schválení deníku přestane zpracování pracovního toku reagovat a vy nebudete moci upravovat ani zpracovávat deníky.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475758"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Workflow deníku zásob se nikdy nedokončí a deník nelze zpracovat

## <a name="symptoms"></a>Příznaky

Po odeslání pracovního postupu schválení deníku přestane zpracování pracovního toku reagovat a vy nebudete moci upravovat ani zpracovávat deníky.

## <a name="resolution"></a>Řešení

Existuje několik důvodů, proč zpracování workflowu nemusí být provedeno. Zkontrolujte následující problémy:

- Jděte na **Řízení zásob &gt; Nastavení &gt; Workflowy správy skladu** a zkontrolujte konfiguraci ovlivněného workflowu. Další informace naleznete v tématu [Workflowy schválení deníku](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Ve workflowu může docházet k výjimce nebo chybě. Zkontrolujte historii pracovní položky ovlivněného workflowu, abyste zjistili, zda obsahuje chybu aplikace, která workflow ukončí.
- Deník zásob lze aktualizovat nebo upravovat, pouze pokud je schválen. Pokud je vyvolání aktivní, můžete se pokusit vyvolat deník. Provádění dávkové úlohy workflowu může být pozastaveno z několika důvodů. Některé z těchto důvodů mohou být způsobeny problémem rámce workflowu.

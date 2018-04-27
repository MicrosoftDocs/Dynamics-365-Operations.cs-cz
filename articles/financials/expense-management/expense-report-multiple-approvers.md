---
title: "Sestavy výdajů a více schvalovatelů"
description: "Toto téma obsahuje informace o sestavách výdajů, které vyžadují schválení více než jednou osobou."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: cs-cz
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>Sestavy výdajů a více schvalovatelů

[!INCLUDE [banner](../includes/banner.md)]

V závislosti na zásadách schvalování výdajů ve vaší organizaci může být zapotřebí ke schválení sestavy výdajů odeslané zaměstnancem více než jedna osoba. Při nastavování procesu workflowu pro schválení sestavy výdajů můžete přidat prvky workflowu, které obsahují úkoly nebo kroky pro jednoho nebo více schvalovatelů sestavy výdajů. Můžete například vyžadovat, aby všechny sestavy výdajů schvaloval nejprve manažer zaměstnance, který sestavu odeslal, a poté koordinátorem závazků.

Pokud se rozhodnete požadovat více schvalovatelů sestav výdajů, můžete přidat prvky workflowu některým z následujících způsobů:

- Přidáte jeden prvek schválení o jednom kroku. Krok může například vyžadovat, aby bylo vyúčtování výdajů přiřazeno do skupiny uživatelů a aby bylo schváleno 50 procenty členů skupiny uživatelů.
- Přidáte jeden prvek s více kroky. Prvek schválení může například obsahovat následující kroky:

    1. Manažer zaměstnance, který odeslal sestavu výdajů, toto vyúčtování schválí.
    2. Úředník závazků ověří účtenky a položky sestavy výdajů.
    3. Vlastník rozpočtu schválí vyúčtování výdajů.

- Přidáte více prvků schválení, z nichž každý obsahuje jeden krok. Například můžete přidat samostatný prvek schválení pro každý z následujících kroků:

    1. Manažer zaměstnance schválí vyúčtování výdajů.
    2. Vlastník rozpočtu schválí vyúčtování výdajů.


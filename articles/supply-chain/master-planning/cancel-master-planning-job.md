---
title: Zrušení hlavní plánovací úlohy
description: Tento článek vysvětluje způsob zrušení aktivní plánovací úlohy, která používá integrovanou funkci plánování.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860776"
---
# <a name="cancel-a-master-planning-job"></a>Zrušení hlavní plánovací úlohy

[!include [banner](../includes/banner.md)]

V aplikaci Microsoft Dynamics 365 Supply Chain Management existuje několik možností zrušení hlavní plánovací úlohy. Hlavní plánovací úlohu můžete například chtít zrušit, pokud byla spuštěna omylem nebo pokud je spuštěna déle, než bylo očekáváno, a chcete ji ukončit. Nejlepší způsob, jak zrušit plánovací úlohu, je ze stránky **nedokončené procesy plánování**. Alternativní možnosti ze stránek **Dávkové úlohy** a **Pokročilé dávkové úlohy** by se měly použít pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** neskončilo během pár minut.

## <a name="preferred-cancel-option"></a>Preferovaná možnost zrušení
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy**
1. Přejděte na **Hlavní plánování > Dotazy a sestavy > Hlavní plánování > Nedokončené plánovací procesy**.
2. Vyberte řádek s plánovacím procesem, který chcete zrušit.
3. Klepněte na možnost **Zrušit**.

## <a name="additional-cancel-options"></a>Další možnosti zrušení
Tyto operace by měly být použity pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** nebylo dokončeno během pár minut.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Odstranění hlavní plánovací úlohy ze stránky **Dávkové úlohy**
1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Vyberte řádek s plánovací úlohou, který chcete odstranit.
3. Klepněte na tlačítko **Odstranit**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Zrušení hlavní plánovací úlohy ze stránky **Pokročilé dávkové úlohy**
1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Pokud není ID úlohy v seznamu zobrazeno, klikněte na tlačítko **Přepnout do rozšířeného formuláře**, jinak pokračujte dalším krokem.
3. Otevřete dávkovou úlohu. Kikněte na **ID úlohy** u dávkové úlohy s úkoly, které chcete ukončit.
4. V okně **Dávkové úkoly** vyberte úkoly, které chcete ukončit.
5. Klikněte na **Změnit stav**, vyberte **Zrušení** a klikněte na **OK**.
6. Na pevné záložce **Dávkové úkoly** klikněte na **Ukončit**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
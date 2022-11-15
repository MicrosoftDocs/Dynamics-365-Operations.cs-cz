---
title: Zrušte úlohu, která byla vytvořena pomocí zastaralého modulu hlavního plánování
description: Tento článek vysvětluje způsob zrušení aktivní plánovací úlohy, která používá zastaralý modul hlavního plánování.
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
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740870"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Zrušte úlohu, která byla vytvořena pomocí zastaralého modulu hlavního plánování

[!include [banner](../includes/banner.md)]

Existuje několik možností pro zrušení úlohy, která byla vytvořena pomocí zastaralého modulu hlavního plánování. Hlavní plánovací úlohu můžete například chtít zrušit, pokud byla spuštěna omylem nebo pokud je spuštěna déle, než bylo očekáváno, a chcete ji ukončit.

Nejlepší způsob, jak zrušit plánovací úlohu, je ze stránky **nedokončené procesy plánování**. Alternativní možnosti ze stránek **Dávkové úlohy** a **Pokročilé dávkové úlohy** by se měly použít pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** neskončilo během pár minut.

## <a name="preferred-cancel-option"></a>Preferovaná možnost zrušení

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Zrušení hlavní plánovací úlohy ze stránky Nedokončené plánovací procesy

1. Přejděte na **Hlavní plánování > Dotazy a sestavy > Hlavní plánování > Nedokončené plánovací procesy**.
2. Vyberte řádek s plánovacím procesem, který chcete zrušit.
3. Vyberte možnost **Zrušit**.

## <a name="additional-cancel-options"></a>Další možnosti zrušení

Tyto operace by měly být použity pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** nebylo dokončeno během pár minut.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Odstranění hlavní plánovací úlohy ze stránky **Dávkové úlohy**

1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Vyberte řádek s plánovací úlohou, který chcete odstranit.
3. Zvolte **Odstranit**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Zrušení hlavní plánovací úlohy ze stránky **Pokročilé dávkové úlohy**

1. Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.
2. Pokud není ID úlohy v seznamu zobrazeno, klikněte na tlačítko **Přepnout do rozšířeného formuláře**, jinak pokračujte dalším krokem.
3. Otevřete dávkovou úlohu. Vyberte **ID úlohy** u dávkové úlohy s úkoly, které chcete ukončit.
4. V okně **Dávkové úkoly** vyberte úkoly, které chcete ukončit.
5. Vyberte **Změnit stav**, vyberte **Zrušení** a klikněte na **OK**.
6. Na pevné záložce **Dávkové úkoly** klikněte na **Ukončit**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
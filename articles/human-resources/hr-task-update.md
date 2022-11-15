---
title: Nastavení úkolů ve správě úkolů
description: Tento článek vysvětluje, jak nastavit úkoly ve Správě úkolů v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745382"
---
# <a name="set-up-tasks-in-task-management"></a>Nastavení úkolů ve správě úkolů

[!INCLUDE [PEAP](../includes/peap-1.md)]

Ve verzích Microsoft Dynamics 365 Human Resources před verzí 10.0.30 museli uživatelé, kteří chtěli upravit úlohu, individuálně upravit tuto úlohu v každém kontrolním seznamu, který ji obsahoval. Od verze Human Resources 10.0.30 si však uživatelé mohou vybrat, jak budou upravené úlohy zpracovávány. Pokud je úkol, který je upravován, na kontrolním seznamu, je nutné vybrat možnosti **Povolit upgrade správy úloh** na kartě **Správa úkolů** na stránce **Sdílené parametry lidských zdrojů**, aby bylo umožněno kontrolnímu seznamu použít upravenou úlohu.

[![Povolte možnost upgradu správy úloh na stránce Sdílené parametry lidských zdrojů.](./media/task-update.png)](./media/task-update.png)

Pokud mají být úpravy úkolů aplikovány na všechny související úkoly kontrolního seznamu, musí již existovat vztah mezi úlohou v knihovně úloh a úlohou v kontrolním seznamu. Byla přidána možnost vytvořit vztah mezi úlohou knihovny a úlohou kontrolního seznamu.

Úkoly můžete vytvářet jednotlivě a poté je znovu použít ve více kontrolních seznamech. Chcete-li vytvořit úkol, na stránce **Nastavení nasazování** na kartě **Úkoly** vyberte **Nový**.

## <a name="set-up-tasks"></a>Nastavení úlohy

Chcete-li vytvořenou úlohu přiřadit k více kontrolním seznamům, vyberte úlohu a následně výberte **Použit na kontrolní seznamy** v nabídce.

Případně můžete úkoly přidat přímo do kontrolního seznamu. Chcete-li přidat úkol do kontrolního seznamu, na stránce **Nastavení nasazování** na kartě **Kontrolní seznam** vytvořte nový kontrolní seznam, do kterého chcete úkol přidat, nebo přidejte úkol do existujícího kontrolního seznamu.

Chcete-li upravit úkol v knihovně, vyberte **Upravit** v nabídce knihovny úloh. Pokud je úkol spojen s nějakými kontrolními seznamy, tyto kontrolní seznamy se zobrazí na stránce **Upravit úkol**. Pokud chcete, aby se úkoly v některém kontrolním seznamu aktualizovaly pomocí úprav, vyberte tyto kontrolní seznamy v části **Použít na kontrolní seznamy**.

Chcete-li odstranit úkoly z knihovny úkolů, vyberte možnost **Odstranit**. Pokud je úkol přidružen k nějakému kontrolnímu seznamu, tato akce neodstraní úkol z tohoto kontrolního seznamu. K odstranění úkolu z kontrolního seznamu je vyžadována samostatná akce.

### <a name="set-up-checklists"></a>Nastavení kontrolních seznamů

Kontrolní seznam je skupina úkolů. Můžete vytvořit tolik kontrolních seznamů, kolik potřebujete, a stejné úkoly můžete přiřadit více kontrolním seznamům. Při vytváření kontrolního seznamu určíte vlastníka a kalendář.

Chcete-li vytvořit nový úkol v kontrolním seznamu, vyberte **Nový** v liště nabídky úkoly. Když vytváříte novou úlohu, můžete volitelně přidat úlohu do knihovny úloh, aby ji bylo možné sdílet ve více kontrolních seznamech. Chcete-li přidat úkol do knihovny, musíte nastavit možnost **Použít úkol na knihovnu** na **Ano**. Pokud úkol přidáte do knihovny úkolů, můžete úkol také přidat do jiných kontrolních seznamů současně výběrem těchto kontrolních seznamů v části **Použít na kontrolní seznamy**. Pokud nepřidáte úlohu do knihovny, úloha bude existovat pouze v kontrolním seznamu, ve kterém ji vytvoříte.

Chcete-li upravit úkol v kontrolním seznamu, vyberte **Upravit** v nabídce úloh. Pokud je úkol spojen s nějakými kontrolními seznamy, tyto kontrolní seznamy se zobrazí na stránce **Upravit úkol**. Pokud chcete, aby se úkoly v některém jiném kontrolním seznamu aktualizovaly pomocí úprav, vyberte tyto kontrolní seznamy v části **Použít na kontrolní seznamy**.

Chcete-li odebrat úkoly z kontrolního seznamu, vyberte **Odstranit**. Tato akce odstraní úkoly z kontrolního seznamu. Neodstraní je však z knihovny úloh. Chcete-li odstranit úkoly z knihovny, otevřete stránku **Knihovna úkolů** a vyberte **Odstranit**.

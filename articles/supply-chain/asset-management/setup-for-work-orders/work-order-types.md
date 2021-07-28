---
title: Typy pracovních příkazů
description: Toto téma vysvětluje typy pracovních příkazů v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d89d7c652837e881f7fcb6014fe017eedc2f876c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351458"
---
# <a name="work-order-types"></a>Typy pracovních příkazů

[!include [banner](../../includes/banner.md)]

 

Typy pracovních příkazů se používají ke kategorizaci pracovních příkazů. Můžete mít například pracovní příkazy, které souvisejí s preventivní údržbou nebo opravnou údržbou.

Typ pracovního příkazu definuje umístění s modelem životního cyklu pracovních příkazů. Model životního cyklu pracovních příkazů definuje stavy životního cyklu pracovního příkazu, které lze nastavit v rámci pracovního příkazu. (Příklady stavů životního cyklu pracovního příkazu jsou **Vytvořeno**, **Zpracovávání** a **Dokončeno**.)

Další informace o stavech životního cyklu pracovního příkazu a fázích projektu naleznete v tématu [stavy životního cyklu pracovního příkazu](work-order-lifecycle-states.md).

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Typy pracovních příkazů**.
2. Zvolte **Nový** pro vytvoření typu pracovního příkazu.
3. V poli **Typ pracovního příkazu** zadejte ID pro typ pracovního příkazu.
4. Do pole **Název** zadejte název.
5. Zvolte model životního cyklu v poli **Model životního cyklu pracovního příkazu**.
5. Nastavte možnost **Jeden pracovník údržby** na **Ano**, chcete-li, aby všechny úlohy pracovních příkazů související s pracovním pořadím tohoto typu byly naplánovány na téhož pracovníka údržby.
6. V poli **Typ nákladů** vyberte **Opravné**, **Preventivní** nebo **Investiční**. Všechny úlohy pracovního příkazu v pracovním příkazu musí mít stejný typ nákladů.
7. V oddílu **Povinné** nastavte příslušné možnosti na **Ano**, chcete-li určit, které informace týkající se poruchy nebo prostoje údržby jsou přidány k pracovnímu příkazu tohoto typu.

    > [!NOTE]
    > Možnosti v oddílu **Povinné** souvisejí s možnostmi na pevné záložce **Ověřit** na stránce **Stavy životního cyklu pracovního příkazu** (**Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Stavy životního cyklu**).

8. Zvolte možnost **Uložit**.

![Typy pracovního příkazu.](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
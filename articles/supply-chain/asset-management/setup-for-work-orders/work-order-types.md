---
title: Typy pracovních příkazů
description: Toto téma vysvětluje typy pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 375b18a4bd37ddadecee03a01b3b2125f5cc8d0a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215417"
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

8. Zvolte **Uložit**.

![Typy pracovních příkazů](media/16-setup-for-work-orders.png)

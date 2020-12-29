---
title: Použití kódů důvodu fáze
description: Pomocí kódu důvodu lze uvést, proč byla zrušena smlouva o úrovni služeb (SLA) nebo proč došlo k překročení časového limitu nastaveného smlouvou SLA.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74594871e9eeed86ae2914d1e5a08c0af28ab643
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423967"
---
# <a name="use-stage-reason-codes"></a>Použití kódů důvodu fáze 

[!include [banner](../includes/banner.md)]


Pomocí kódu důvodu lze uvést, proč byla zrušena smlouva o úrovni služeb (SLA) nebo proč došlo k překročení časového limitu nastaveného smlouvou SLA.

Také můžete vyžadovat zadání kódu důvodu při zrušení smlouvy SLA nebo pokud časový limit překročí čas, který je určen ve smlouvě SLA pro servisní zakázku.

Pokud jste určili, že má být kód důvodu vyžadován, je třeba zadat kód důvodu v následujících situacích:

  - Když je servisní zakázka přesunuta do fáze, v níž je pro danou servisní zakázku pozastaven časový záznam vzhledem ke smlouvě SLA.

  - Pokud je servisní zakázka ukončena.

  - Když je časový záznam zastaven ručně.

## <a name="set-up-reason-codes"></a>Nastavení kódů důvodů

1.  Klepněte na tlačítko **řízení servisu** \> **nastavení** \> **servisní zakázky** \> **kódy důvodu fáze**.

2.  Ve formuláři **Kódy důvodu fáze** klepněte na možnost **nový** k vytvoření nového kódz důvodu fáze.

3.  Do pole **Kód důvodu fáze** zadejte jedinečný kód důvodu fáze.

4.  Do pole **Popis** zadejte popis kódu důvodu fáze.

5.  Uložte změny zavřením formuláře.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Vyžadování kódů důvodů při zrušení smlouvy o úrovni služeb

1.  Klikněte **Správa servisu** \> **Nastavení** \> **Parametry správy servisu**.

2.  Ve formuláři **parametry správy servisu** klepněte na odkaz **Obecné** a poté zaškrtněte políčko **kód důvodu zrušení**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Vyžadování kódu důvodu při překročení časového limitu nastaveného smlouvou o úrovni služeb

1.  Klikněte **Správa servisu** \> **Nastavení** \> **Parametry správy servisu**.

2.  Ve formuláři **parametry správy servisu** klepněte na odkaz **Obecné** a poté zaškrtněte políčko **kód důvodu při překročení času**.

## <a name="see-also"></a>Viz také

[Zahájení a ukončení záznamu času v servisní zakázce](start-and-stop-time-recording-on-a-service-order.md)

  



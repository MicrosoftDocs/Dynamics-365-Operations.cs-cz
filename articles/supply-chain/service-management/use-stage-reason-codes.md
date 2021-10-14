---
title: Použití kódů důvodu fáze
description: Pomocí kódu důvodu lze uvést, proč byla zrušena smlouva o úrovni služeb (SLA) nebo proč došlo k překročení časového limitu nastaveného smlouvou SLA.
author: kamaybac
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac825fe96ee69491953bd50c758dde42744cea85
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573146"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
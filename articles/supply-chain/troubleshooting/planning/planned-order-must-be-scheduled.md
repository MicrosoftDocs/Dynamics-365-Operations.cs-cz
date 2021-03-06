---
title: Plánovaná výrobní zakázka musí být naplánována, než bude možné ji potvrdit
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že objednávku je třeba naplánovat, než bude možné ji potvrdit.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294033"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Plánovaná výrobní zakázka musí být naplánována, než bude možné ji potvrdit

Kód chyby: SYS309802

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:

> Plánovaná výrobní zakázka musí být před potvrzením naplánována.

## <a name="cause"></a>Příčina

Naplánované datum zahájení a ukončení nesmí být prázdné.

## <a name="resolution"></a>Řešení

Chcete-li určit počáteční a konečné datum plánované objednávky, postupujte takto.

1. Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**.
1. Otevřete příslušnou plánovanou objednávku.
1. Na pevné záložce **Všeobecné** v sekci **Naplánováno** uveďte data v polích **Datum začátku** a **Datum ukončení**.

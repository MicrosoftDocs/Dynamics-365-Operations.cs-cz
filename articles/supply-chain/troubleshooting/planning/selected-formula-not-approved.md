---
title: Vybrané číslo receptury není pro dávkovou objednávku schváleno
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že vybrané číslo receptury není pro dávkovou objednávku schváleno.
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
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294025"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Vybrané číslo receptury není pro dávkovou objednávku schváleno

Kód chyby: PRO2614

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:

> Vybrané číslo receptury není pro dávkovou objednávku schváleno.

## <a name="cause"></a>Příčina

Systém ověří potvrzení, aby se ujistil, že pro aktivní položku je k dispozici schválená receptura. Pravděpodobně musíte recepturu schválit.

## <a name="resolution"></a>Řešení

Chcete-li schválit recepturu, postupujte takto:

1. Přejděte do nabídky **Řízení informací o produktech \> Kusovníky a receptury \> Receptury**.
1. Vyberte příslušnou recepturu.
1. V podokně akcí na kartě **Receptura** ve skupině **Spravovat** zvolte **Schválit recepturu**.
1. V dialogovém okně **Schválit kusovník nebo recepturu** okně vyberte schvalovatele a poté vyberte **OK**.

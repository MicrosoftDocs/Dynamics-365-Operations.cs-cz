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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712903"
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

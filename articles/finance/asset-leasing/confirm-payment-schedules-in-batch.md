---
title: Potvrzení platebních kalendářů leasingu majetku v dávce
description: Toto téma vysvětluje, jak potvrdit více platebních kalendářů v dávce.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a3bd7293fed4b8df5d7bd76edacbcae253aa1f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816069"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Potvrzení platebních kalendářů leasingu majetku v dávce

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak potvrdit více platebních kalendářů v dávce. Platební kalendáře se potvrzují buď pro jednotlivé leasingy, nebo prostřednictvím dávkového zpracování. Položku deníku lze zaúčtovat pouze pro leasing, který má potvrzený platební kalendář. Potvrzení platebního kalendáře slouží jako konečné schválení finančních informací o leasingu. Všechny budoucí změny finančních informací o leasingu, jako jsou platby a doba leasingu, představují úpravu leasingu a měly by být zpracovány tímto způsobem.

Chcete-li potvrdit více platebních kalendářů, postupujte takto.

1. Jděte na **Leasing majetku \> Periodicky \> Potvrzení dávky**.
2. Na stránce **Potvrzení dávky** vyberte **Potvrzení dávky**.
3. V zobrazeném dialogovém okně vyfiltrujte knihy, které chcete potvrdit.

    - Chcete-li potvrdit všechny knihy v konkrétní skupině leasingu, vyberte skupinu v poli **Skupina leasingu**.
    - Chcete-li potvrdit konkrétní knihy, vyberte knihy v poli **ID knihy**.
    - Chcete-li potvrdit všechny knihy, zapněte parametr **Pro všechny knihy**.

Informace o nově potvrzených knihách jsou uvedeny na stránce **Potvrzené knihy**. Po potvrzení platebních kalendářů je možné zaúčtovat položky deníku počátečního uznání pro leasingy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
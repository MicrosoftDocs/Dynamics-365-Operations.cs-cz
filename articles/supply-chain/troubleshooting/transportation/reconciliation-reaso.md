---
title: Z důvodu odsouhlasení můžete jako kreditní účet přidat pouze hlavní účet
description: Když ve správě dopravy nastavíte důvod odsouhlasení, můžete jako úvěrový účet přidat pouze hlavní účet.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026323"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Z důvodu odsouhlasení můžete jako kreditní účet přidat pouze hlavní účet

Číslo článku znalostní báze: 4603538

## <a name="symptoms"></a>Příznaky

Když ve správě dopravy nastavíte důvod odsouhlasení, můžete jako úvěrový účet přidat pouze hlavní účet. Jako kreditní účet nemůžete přidat nákladové středisko ani jinou dimenzi. Debetní účet vám však umožňuje vybrat jiné dimenze.

## <a name="resolution"></a>Rozlišení

Pokud se odsouhlasení neprovede za účelem platby prodejci, ale za účelem připsání částky na konkrétní hlavní účet, systém vám při nastavení důvodu odsouhlasení neumožní vybrat finanční dimenzi pro úvěrový účet.

Pokud struktura účtu vyžaduje specifickou hodnotu finanční dimenze pro hlavní úvěrový účet, výsledný deník dodavatele nelze zaúčtovat automaticky, protože chybí hodnota finanční dimenze. Proto musíte nejprve ručně zadat kreditní účet pomocí stránky **Deník faktur**.

Protože u úvěrového účtu je vyžadována hodnota dimenze, nelze deník faktur dodavatele automaticky zaúčtovat. Poté, co ručně přidáte hodnotu dimenze do hlavního účtu pro kreditní hranici, musíte ji zaúčtovat ručně.

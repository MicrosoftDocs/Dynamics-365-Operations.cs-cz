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
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750875"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Z důvodu odsouhlasení můžete jako kreditní účet přidat pouze hlavní účet

Číslo článku znalostní báze: 4603538

## <a name="symptoms"></a>Příznaky

Když ve správě dopravy nastavíte důvod odsouhlasení, můžete jako úvěrový účet přidat pouze hlavní účet. Jako kreditní účet nemůžete přidat nákladové středisko ani jinou dimenzi. Debetní účet vám však umožňuje vybrat jiné dimenze.

## <a name="resolution"></a>Rozlišení

Pokud se odsouhlasení neprovede za účelem platby prodejci, ale za účelem připsání částky na konkrétní hlavní účet, systém vám při nastavení důvodu odsouhlasení neumožní vybrat finanční dimenzi pro úvěrový účet.

Pokud struktura účtu vyžaduje specifickou hodnotu finanční dimenze pro hlavní úvěrový účet, výsledný deník dodavatele nelze zaúčtovat automaticky, protože chybí hodnota finanční dimenze. Proto musíte nejprve ručně zadat kreditní účet pomocí stránky **Deník faktur**.

Protože u úvěrového účtu je vyžadována hodnota dimenze, nelze deník faktur dodavatele automaticky zaúčtovat. Poté, co ručně přidáte hodnotu dimenze do hlavního účtu pro kreditní hranici, musíte ji zaúčtovat ručně.

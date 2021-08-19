---
title: Vlna není způsobilá k vyčištění
description: Vlna není způsobilá k vyčištění
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778499"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Vlna není způsobilá k vyčištění

Kód chyby: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Vlna %1 není pro vyčištění způsobilá.

Data vln nelze vyčistit.  

## <a name="cause"></a>Příčina

Vlna se aktuálně zpracovává, jak naznačuje jedna z následujících podmínek:

- Pole **Stav vlny** je nastaveno na hodnotu *Zpracování*.
- Když vyberete možnost **Dávková úloha** ve skupině **Vlna** na kartě **Vlna** podokna akcí, pole **Stav** není nastaveno na hodnotu *Ukončeno*, *Chyba* nebo *Zrušeno*. Proto je aktuálně spuštěna dávková úloha.

## <a name="resolution"></a>Rozlišení

V podokně akcí na kartě **Vlna** ve skupině **Vlna** vyberte možnost **Dávková úloha** a poté proveďte jeden z těchto kroků:

- Pokud je pole **Stav** nastaveno na hodnotu *Zpracování*: V podoknu akcí na kartě **Dávková úloha** ve skupině **Dávková úloha** vyberte možnost **Zobrazení úkolů**. Průběh můžete sledovat pomocí obnovení stránky **Dávkové úkoly**.
- Pokud není pole **Stav** nastaveno na hodnotu *Zpracování*: V podoknu akcí na kartě **Dávková úloha** ve skupině **Funkce** vyberte možnost **Změnit stav**. V poli **Vyberte nový stav** vyberte možnost *Čekání*. Pak vyberte **OK**.

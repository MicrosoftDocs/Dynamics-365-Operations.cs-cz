---
title: Hmotnost nákladu může obsahovat pouze kladná čísla
description: Při zpracování práce mezi místy se může zobrazit chyba týkající se hmotnosti nákladu a zrušení vaší aktualizace. Chcete-li opravit problém, postupujte následovně.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475784"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Chyba hmotnosti zatížení a aktualizace zrušena při zpracování práce mezi místy

## <a name="symptoms"></a>Příznaky

Pokud existuje otevřená práce při zpracování práce z umístění balení do přechodných skladových míst nebo z přechodných skladových míst do umístění dokovacích míst, zobrazí se následující chybová zpráva.

> Pole Hmotnost nákladu'(=-%1) může obsahovat pouze kladná čísla. Aktualizace byla zrušena

## <a name="resolution"></a>Řešení

Abyste tento problém vyřešili, přejděte na **Správa systému \> Pravidelné úkoly \> Databáze \> Kontrola konzistence** a spusťte proces pro **Kontrola konzistence hmotnosti nákladu skladu**.

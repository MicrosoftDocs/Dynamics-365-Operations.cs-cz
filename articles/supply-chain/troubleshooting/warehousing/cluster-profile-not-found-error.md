---
title: Profil seskupení nebyl nalezen
description: Při práci s operacemi příchozích skladů se může zobrazit chyba, která říká, že profil clusteru nebyl nalezen. Zkontrolujte, zda jsou profily clusteru správně nastaveny.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475840"
---
# <a name="cluster-profile-cant-be-found"></a>Profil seskupení nebyl nalezen

## <a name="symptoms"></a>Příznaky

Při práci s příchozími skladovými operacemi se může zobrazit následující chybová zpráva:

> "Proběhlo generování objednávky kvality %1. Profil seskupení nebyl nalezen. Zkontrolujte prosím svoji konfiguraci."

Tato chybová zpráva souvisí s přijímacím procesem, kde je zapnutá správa kvality (QMS). V závislosti na konfiguracích ve vašem prostředí mohou problém vyřešit další podrobnosti o transakci, která generuje chybovou zprávu.

## <a name="resolution"></a>Řešení

Nejprve zkontrolujte nastavení výdeje v seskupení a ujistěte se, že jsou vaše profily seskupení nastaveny správně. Položku nabídky mobilního zařízení nemůžete použít pro výběr seskupení, pokud nejsou nastaveny profily seskupení. V závislosti na vašem prostředí budete možná muset zkontrolovat další související konfigurace.

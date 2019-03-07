---
title: Potvrzení výdeje kusů
description: Toto téma popisuje, jak nastavit a použít potvrzení výdeje kusů a registrační značky z mobilního zařízení.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b85414dd1385dc3d8c97632eaaeb252759590ff
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "349623"
---
# <a name="piece-picking-confirmation"></a>Potvrzení výdeje kusů

[!include [banner](../includes/banner.md)]

Výdej kusů umožňuje ověřit jednotlivé kusy zásob prostřednictvím výdeje nebo inventury u mobilního zařízení. Pro kusy můžete potvrdit množství práce, které má být zpracováno až do množství, které je specifikováno v práci, která má být dodána. Pro výpočet práce můžete naskenovat zásoby, které započítáváte, a sledovat celkové množství.

Pokud povolíte úkolové práce, potvrzení produktu je vybráno automaticky. Pro výdeje typu práce je povolen maximální počet kusů. To umožňuje nastavit maximální počet kusů, které musí být potvrzeny v pracovním procesu. Maximální množství je založeno na aktuální jednotce zpracovávané práce. Typ práce Inventura nepovoluje maximum.

Můžete také použít množství a měrnou jednotku (MJ) přidružené k naskenovanému čárovému kódu. To bude fungovat u příchozích toků včetně příjmu smíšených registračních značek, položek nákupní objednávky, převodních položek objednávky a položky nákladu. Také funguje u výdeje po kusech, kde skenování čárového kódu přidá množství k celkovému počtu potvrzených kusů při převodu mezi měrnou jednotkou na čárovém kódu a jednotkou práce. Pokud se při započítávání MJ na čárovém kódu potvrdí, že je množství přípustné pro započítání do skupiny klasifikace, bude množství připočteno k celkovému součtu.

## <a name="where-it-applies"></a>Kdy se to používá

Výdej kusů funguje pro všechnu práci při inventuře a pro počáteční výběr u jakéhokoli typu práce. Výdej kusů se nepoužije, pokud je položka řízena sériovými čísly nebo pokud je výrobní zakázka nebo kanban vyskladněn z registrační značky skladového místa a položka je nastavena na Fázování.

## <a name="set-up-piece-picking"></a>Nastavení výdeje kusů

1.  V položce nabídky mobilního zařízení otevřete formulář nastavení pro potvrzení práce: Řízení skladu > **Řízení skladu** > **Nastavení** > **Mobilní zařízení** > **Položky nabídky mobilního zařízení**. 
2. Z položky nabídky mobilního zařízení otevřete Nastavení potvrzení práce.

Následující možnosti budou k dispozici pro výběr, jestliže je typ práce výdej nebo inventura.


|           Parametr           |                                                                            popis                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Potvrzení výdeje kusů | K dispozici pro typy prací Výdej a inventura. Potvrzení produktu je vybráno automaticky. Umožňuje vám potvrdit jednotlivé skladové položky z mobilního zařízení při naskenování. |
|  Maximální počet kusů  |                   K dispozici pro vyskladnění práce, pokud je povoleno potvrzení výdeje kusů. Nastaví limit na počet kusů, které je třeba potvrdit.                   |


---
title: Provedení změny stavu zásob pro práci s dílčím množstvím
description: Tato stránka vysvětluje, jak vytvořit položku nabídky s příslušným nastavením, aby pracovníci mohli provést změnu stavu zásob u částečného množství dávky.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475746"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Povolit změnu stavu zásob pro práci s dílčím množstvím

## <a name="symptoms"></a>Příznaky

Potřebujete provést změnu stavu zásob u částečného množství dávky.

## <a name="resolution"></a>Řešení

Chcete-li pracovníkům umožnit tuto změnu, můžete vytvořit položku nabídky pro mobilní aplikaci Řízení skladu. Na stránce **Položky nabídky mobilního zařízení** vytvořte (nebo upravte) položku nabídky, která má následující nastavení:

- **Režim:** *Práce*
- **Použít existující práci:** *Ne*
- **Proces tvorby práce:** *Pohyb*
- **Zobrazit stav zásob:** *Ano*

Na stránce můžete podle potřeby nastavit další pole.

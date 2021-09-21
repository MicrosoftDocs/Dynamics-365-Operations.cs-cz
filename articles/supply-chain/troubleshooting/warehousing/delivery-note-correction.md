---
title: Opravu poznámky k dodání nelze zpracovat
description: Pokud se pokusíte opravit dodací list po jeho zveřejnění, zobrazí se chyba. Tato stránka vysvětluje, jak opravit zaslané balicí lístky u položek povolených pro WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475822"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Opravu poznámky k dodání nelze zpracovat

## <a name="symptoms"></a>Příznaky

Po vystavení poznámky k dodání ji nemůžete zrušit, protože tlačítko **Zrušení** není k dispozici. Poznámku k dodání také nemůžete opravit. Pokud se o to pokusíte, zobrazí se následující chybová zpráva:

> Poznámku k dodání nelze zpracovat. Poznámka k dodání obsahuje pouze položky, které podléhají procesům správy skladu, protože tyto nejsou opravou poznámky k dodání podporovány.

## <a name="resolution"></a>Řešení

Chcete-li opravit odeslané dodací listy pro položky, které jsou povoleny pro pokročilou správu skladu (WMS), musíte zaúčtování provést z nákladu, nikoli přímo z objednávky.

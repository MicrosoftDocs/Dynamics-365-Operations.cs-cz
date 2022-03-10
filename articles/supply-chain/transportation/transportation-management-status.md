---
title: Stavy správy přepravy
description: Toto téma vysvětluje, jak vytvořit stav přepravy a mapovat tento stav na stav přepravce.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c5570d3b5b436a35bb57d051bc06cde8b78934e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569882"
---
# <a name="transportation-management-statuses"></a>Stavy správy přepravy

[!include [banner](../includes/banner.md)]

Nastavte hlavní kódy pro stavy přepravy k interpretaci kódů poskytovaných vašimi přepravci. To vám umožní integrovat se s přepravci a poskytnout stav. Stav přepravy, který uvedete pro hlavní kód stavu přepravy, může pomoci sledovat stav nákladu, dodávky nebo kontejneru. Konkrétní stav přepravy nákladu, zásilky nebo kontejneru lze aktualizovat pouze prostřednictvím integrace dat, nikoli ručně prostřednictvím uživatelského rozhraní.

## <a name="create-a-transportation-status"></a>Vytvoření stavu přepravy

Chcete-li vytvořit stav přepravy, postupujte dle těchto kroků:

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Hlavní stavy přepravy**.
1. Zvolte **Nový** a vytvořte hlavní stav přepravy.
1. V poli **Hlavní stav přepravy** zadejte jedinečný kód pro stav přepravy.
1. V poli **Typ přepravy** vyberte buď *Přepravce* nebo *Nadřazený uzel* jako typ dopravy.
1. Zadejte název a stav přepravy.
1. Zavřete stránku.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Mapování stavu přepravy na stav přepravce

Pro mapování stavu přepravy na stav přepravce postupujte takto:

1. Přejděte do nabídky **Správa přepravy \> \> Přepravci \> Stav přepravy přepravce**.
1. Vyberte **Nový** a proveďte mapování kódu od dopravce na hlavní kód stavu přepravy.
1. Vyberte jedinečný identifikátor pro dopravce a službu dopravce.
1. Vyberte kód stavu přepravy, který má být mapován na kód vybraného dopravce.
1. Zadejte externí kód, který používá dopravce.
1. Zavřete stránku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
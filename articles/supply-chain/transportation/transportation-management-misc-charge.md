---
title: Vedlejší náklady správu dopravy
description: Toto téma vysvětluje, jak musí být poplatky generované přepravou přidruženy ke kódu poplatku.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6d334a1ac290ab258964df2f146d9cbe30eb766f4002c8bae856cbe5499181b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769508"
---
# <a name="transportation-management-miscellaneous-charges"></a>Vedlejší náklady správu dopravy

[!include [banner](../includes/banner.md)]

Stejně jako u vedlejších nákladů musí být poplatky generované přepravou přidruženy ke kódu poplatku. V opačném případě nebudou přidány zpět k objednávce jako různé poplatky. **Kód poplatku** určuje, jak se účtuje poplatek ve vztahu k objednávce a řádku objednávky, kde je přidána.

Přejděte na **Správa přepravy > Nastavení > Sazby > Vedlejší poplatky** a definujte kvalifikační kritéria, která určují, kdy se konkrétní **Kód poplatku** vztahuje na poplatek.

Měli byste mít alespoň jedno nastavení pro každé relevantní nastavení **Modulu poplatků** (*Zákazník* a *Dodavatel*), kde **Typ vedlejších poplatků** je nastaven na *Žádný*. Pokud toto chybí, vedlejší poplatek *nebude* přidán k objednávce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
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
ms.openlocfilehash: 53c25f204e98a911e9697f5bb950706555749a55
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828297"
---
# <a name="transportation-management-miscellaneous-charges"></a>Vedlejší náklady správu dopravy

[!include [banner](../includes/banner.md)]

Stejně jako u vedlejších nákladů musí být poplatky generované přepravou přidruženy ke kódu poplatku. V opačném případě nebudou přidány zpět k objednávce jako různé poplatky. **Kód poplatku** určuje, jak se účtuje poplatek ve vztahu k objednávce a řádku objednávky, kde je přidána.

Přejděte na **Správa přepravy > Nastavení > Sazby > Vedlejší poplatky** a definujte kvalifikační kritéria, která určují, kdy se konkrétní **Kód poplatku** vztahuje na poplatek.

Měli byste mít alespoň jedno nastavení pro každé relevantní nastavení **Modulu poplatků** (*Zákazník* a *Dodavatel*), kde **Typ vedlejších poplatků** je nastaven na *Žádný*. Pokud toto chybí, vedlejší poplatek *nebude* přidán k objednávce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
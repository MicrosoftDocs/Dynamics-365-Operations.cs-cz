---
title: Vedlejší náklady správu dopravy
description: Tento článek vysvětluje, jak musí být poplatky generované přepravou přidruženy ke kódu poplatku.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849206"
---
# <a name="transportation-management-miscellaneous-charges"></a>Vedlejší náklady správu dopravy

[!include [banner](../includes/banner.md)]

Stejně jako u vedlejších nákladů musí být poplatky generované přepravou přidruženy ke kódu poplatku. V opačném případě nebudou přidány zpět k objednávce jako různé poplatky. **Kód poplatku** určuje, jak se účtuje poplatek ve vztahu k objednávce a řádku objednávky, kde je přidána.

Přejděte na **Správa přepravy > Nastavení > Sazby > Vedlejší poplatky** a definujte kvalifikační kritéria, která určují, kdy se konkrétní **Kód poplatku** vztahuje na poplatek.

Měli byste mít alespoň jedno nastavení pro každé relevantní nastavení **Modulu poplatků** (*Zákazník* a *Dodavatel*), kde **Typ vedlejších poplatků** je nastaven na *Žádný*. Pokud toto chybí, vedlejší poplatek *nebude* přidán k objednávce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
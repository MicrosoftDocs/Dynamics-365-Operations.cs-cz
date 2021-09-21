---
title: Vychystávací práce blokovaná kvůli nedokončeným doplňovacím pracím
description: Výběr práce může být blokován z důvodu práce se závislým doplňováním. Dokončete doplňovací práci a poté zpracujte výdej.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475842"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Práce vyzvedávání nelze odblokovat kvůli nedokončeným doplňovacím pracím

## <a name="symptoms"></a>Příznaky

Při použití doplňování vlnové poptávky lze vychystávací práce zablokovat kvůli závislé doplňovací práci. Pokud je nutné místo pro výdej doplnit, aby byla splněna zdrojový požadavek na objednávku, vytvoří systém práci s doplňováním i výdejem. Zablokuje však vychystávací práce, dokud nebudou dokončeny doplňovací práce a neobdržíte následující chybovou zprávu:

> Práci %1 nelze odblokovat, protože má nedokončenou práci doplnění.

## <a name="resolution"></a>Řešení

Toto chování je záměrné, protože místo výdeje nebude mít dostatek zásob, dokud nebude dokončeno doplňování. Dokončete doplňovací práci a poté zpracujte výdej.

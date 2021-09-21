---
title: Importované nákupní objednávky zobrazují nesprávná čísla řádků
description: Když se nákupní objednávky importují prostřednictvím správy dat, čísla řádků nákupní objednávky nenásledují přírůstek definovaný v systémových parametrech.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475751"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Importované nákupní objednávky zobrazují nesprávná čísla řádků

## <a name="symptoms"></a>Příznaky

Ve výchozím nastavení automaticky generovaná čísla řádků pro řádky nákupní objednávky, které se importují prostřednictvím datové entity *Řádky nákupní objednávky V2* nepoužívají přírůstek čísla řádku systému, který je zadán v systémových parametrech. Pokud ručně vytvoříte nákupní objednávku a přidáte řádky prostřednictvím uživatelského rozhraní, budou čísla řádků správně zvýšena. Pokud však používáte Data management framework (DMF), nejsou správně zvýšena.

K tomuto problému dochází, protože při importu řádků pomocí DMF, pokud čísla řádků již nejsou přiřazena v importované entitě, systém používá k jejich přiřazení metodu DMF. Tato metoda vždy zvyšuje čísla řádků o jedno.

## <a name="workaround"></a>Alternativní řešení

Ujistěte se, že požadovaná čísla řádků jsou již uvedena v polích čísel řádků datové entity při importu řádků nákupní objednávky. V tomto případě DMF nepřepíše čísla řádků.

---
title: Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze
description: Mapováním různých členů dimenze prvku nákladů do sady běžné sady členů dimenze prvku nákladů slučujete data do běžného formátu pro účely analýzy.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176793"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze

[!include [banner](../includes/banner.md)]

Mapováním různých členů dimenze prvku nákladů do sady běžné sady členů dimenze prvku nákladů slučujete data do běžného formátu pro účely analýzy.

Fungujete-li coby globální společnost a řídíte se požadavky účetnictví, můžete používat několik účtových osnov. Při importu členů dimenze prvku nákladů z různých účtových osnov sám může vzniknout směs účtů. Tyto účty však mohou mít stejný ráz a vy pro ně můžete chtít analyzovat a přidělovat náklady pomocí běžného formátu.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Mapovat členy dimenze prvku nákladů do běžného formátu
Následující příklad ukazuje, jak vy, coby správce nákladů, můžete vytvořit nový prvek dimenze nákladů v nákladovém účetnictví, který mapuje členy dimenze prvku nákladů v americké struktuře účtové osnovy a francouzské struktuře účtové osnovy do běžné sady členů dimenze prvku nákladů. Poté můžete použít běžnou sadu členů dimenze prvku nákladů k analýze dat nákladů ze dvou právnických osob v hlavní knize nákladového účetnictví.

| Zdroj: americká účtová osnova                                          | Zdroj: francouzská účtová osnova                                          | Nová běžná sada členů dimenze prvku nákladů                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importované členy dimenze prvku nákladů z americké účtové osnovy | Importované členy dimenze prvku nákladů z francouzské účtové osnovy | Mapovat americké a francouzské členy dimenze prvku nákladů do běžné sady |
| 5001: Prodej                                                           | 5001: Prodej a marketing                                               | 5000: Prodej a marketing                                             |
| 5030: Reklama                                                     | 6390: Skladový nákup\*                                                    | 7000: náklady na úklid                                                 |
| 7001: náklady na úklid                                               | 7001: Cestovní výdaje                                                      | 7001: Cestovné a výdaje                                                   |

\**Skladový nákup francouzského prvku dimenze prvku nákladů není zmapován.

## <a name="currency-conversion"></a>Převod měny
Různé účtové osnovy, které používáte, jsou pravděpodobně nastaveny pro použití v různých měnách. V takovém případě je nutné zadat převod měny tak, aby data nákladů byla zpracovávána ve správné měně do hlavní knihy nákladového účetnictví, kde se používají členy dimenze prvku nákladů. V předcházejícím příkladu, pokud by se používaly americké dolary (USD) v hlavní knize nákladového účetnictví, museli byste vytvořit převod měny z USD do euro (EUR), aby mohlo dojít ke zpracování transakcí pro mapování členů dimenze prvku nákladů.

## <a name="update-mappings-at-any-time"></a>Kdykoli aktualizujte mapování
Kdykoli můžete aktualizovat upřesnění mapování dimenze prvku nákladů. Vzhledem k tomu, že mapování nejsou časově efektivní, změny se projeví, až budete příště zpracovávat transakce nákladů nebo provádět výpočty nákladových.



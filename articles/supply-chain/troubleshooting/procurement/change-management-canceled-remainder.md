---
title: Zrušení zbytku dodávky přesune nákupní objednávku do potvrzeného stavu
description: Pokud je zbytek dodávky zrušen u nákupní objednávky, kde je zapnuta správa změn, přejde nákupní objednávka do stavu Potvrzeno
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475808"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Zrušení zbytku dodávky přesune nákupní objednávku do potvrzeného stavu

## <a name="symptoms"></a>Příznaky

Pokud je u nákupní objednávky, která podléhá správě změn, jedinou požadovanou změnou zrušení zbytku dodávky na jednom nebo více řádcích, přejde nákupní objednávka přímo do stavu *Potvrzeno*, když je schválena, a nebude vytvořen žádný deník.

## <a name="resolution"></a>Řešení

Zrušení zbytku dodávky nemá vliv na obsah deníku potvrzení. Tato funkce by měla být použita, když byl řádek částečně přijat, a zbývající kvalita by měla být zrušena v kroku procesu po potvrzení nákupní objednávky u dodavatele.

Pokud by se to mělo projevit v potvrzení nákupní objednávky, mělo by být množství upraveno na řádku nákupní objednávky tak, aby bylo vyžadováno potvrzení. Popřípadě pokud na řádku nic nebylo přijato, lze množství odebrat. V takovém případě bude vyžadováno opětovné potvrzení.

---
title: Text se přepíše, když je položka nakonfigurována na řádku prodejní objednávky
description: Když je produkt nakonfigurován na řádku prodejní objednávky, modifikovaný text se přepíše standardním. Změňte text po nakonfigurování řádku, ne dříve.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475750"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Text položky se přepíše, když je produkt nakonfigurován na řádku prodejní objednávky

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když vytvoříte řádek prodejní objednávky pro konfigurovatelnou položku a poté upravíte text položky. Když položku konfigurujete a vyberete **OK**, text je přepsán standardním textem.

## <a name="resolution"></a>Řešení

Toto chování se očekává. Textové pole obsahuje název varianty, který se vyplní až po konfiguraci řádku. Proto musíte změnit text po nakonfigurování řádku, ne dříve.

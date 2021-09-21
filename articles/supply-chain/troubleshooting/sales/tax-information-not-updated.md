---
title: Daňové informace se neaktualizují, pokud se změní umístění prodejní objednávky
description: Pokud se pracoviště, sklad nebo adresa dodání změní buď v záhlaví prodejní objednávky, informace o dani případu se na řádcích automaticky neaktualizují. Musíte to udělat ručně.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475800"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Daňové informace se neaktualizují, pokud se změní umístění v hlavičce prodejní objednávky

## <a name="symptoms"></a>Příznaky

Pokud se pracoviště, sklad nebo adresa dodání změní buď v záhlaví prodejní objednávky, informace o dani případu se na řádcích automaticky neaktualizují.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. K problému dochází, protože ani doručovací adresa, pracoviště a sklad se na úrovni řádku automaticky nezmění. Musíte je aktualizovat ručně.

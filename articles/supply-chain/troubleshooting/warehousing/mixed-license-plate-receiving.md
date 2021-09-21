---
title: Přijímání smíšených registračních značek nefunguje pro všechny dispoziční kódy
description: Když je pole Akce pro kód dispozice je nastaveno na Kredit nebo Odpad, můžete použít pouze položku nabídky Přijetí smíšené registrační značky ke zpracování vrácených položek.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475821"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Přijímání smíšených registračních značek nefunguje pro žádný dispoziční kód kromě kreditu

## <a name="symptoms"></a>Příznaky

Když je pole **Akce** pro kód dispozice je nastaveno na *Kredit* nebo *Odpad*, můžete použít pouze položku nabídky [Přijetí smíšené registrační značky](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) ke zpracování vrácených položek.

## <a name="resolution"></a>Řešení

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době jsou pro příjem smíšených registračních značek podporovány pouze [dispoziční kódy](/dynamics365/supply-chain/service-management/set-up-disposition-codes), kde je pole **Akce** nastaveno na *Kredit* nebo *Odpad*.

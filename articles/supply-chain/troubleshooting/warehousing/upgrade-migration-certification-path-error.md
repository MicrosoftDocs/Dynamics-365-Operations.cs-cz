---
title: Chyba certifikační cesty při upgradu nebo migraci na WMS
description: Pokud aplikace při upgradu nebo migraci na WMS zobrazí chybu „Důvěryhodná kotva pro certifikační cestu nebyla nalezena“, tato stránka obsahuje informace o tom, jak problém vyřešit.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475770"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Při aktualizaci a migraci do WMS nebyla nalezena důvěryhodná kotva pro certifikační cestu

## <a name="symptoms"></a>Příznaky

Při upgradu a migraci na rozšířenou správu skladu (WMS) vám aplikace Warehouse Management může zobrazit následující chybovou zprávu:

> Nebyla nalezena důvěryhodná kotva pro certifikační cestu.

## <a name="cause"></a>Příčina

K tomu dochází, protože certifikáty podepsané samy sebou nejsou důvěryhodné v systému Android 8+ v místních prostředích.

## <a name="resolution"></a>Řešení

Použijte externí (veřejný) certifikační autoritu (CA). Oprava tohoto problému je k dispozici ve verzi 1.9.0.0 aplikace Warehouse Management. Další informace o tomto problému a jeho řešení najdete v článku [Při nastavování připojení aplikace nebyla nalezena důvěryhodná kotva pro certifikační cestu](certification-path-app-connection-error.md).

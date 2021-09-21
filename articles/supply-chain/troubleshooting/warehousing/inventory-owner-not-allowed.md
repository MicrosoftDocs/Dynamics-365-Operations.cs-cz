---
title: Vlastník zásob není povolen při zpracování pohybů
description: Může se zobrazit chyba „Vlastník zásoby %1 není povolen." Procesy správy skladu podporují pouze zásoby, které jsou ve vlastnictví právnické osoby.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475772"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Vlastník zásob není povolen při zpracování pohybů ve skladové aplikaci

## <a name="symptoms"></a>Příznaky

Když zpracováváte pohyby v mobilní aplikaci Warehouse Management, může se zobrazit následující chybová zpráva:

> Vlastník zásob %1 není v tomto procesu povolen.

## <a name="cause"></a>Příčina

To nastává proto, že sledovací dimenze **Vlastník** chybí, když se mobilní aplikaci Řízení skladu používá k provádění přesunů. Pravidelný deník přesunů zásob od klienta Supply Chain Management nejspíš funguje podle plánu a lze ho zaúčtovat, pouze pokud je vyplněna dimenze **Vlastník**.

## <a name="resolution"></a>Řešení

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době procesy správy skladu podporují pouze zásoby, které jsou ve vlastnictví právnické osoby.

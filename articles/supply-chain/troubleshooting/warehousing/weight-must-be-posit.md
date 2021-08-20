---
title: Hmotnost musí být kladná
description: Hmotnost musí být kladná
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776769"
---
# <a name="weight-must-be-positive"></a>Hmotnost musí být kladná

Kód chyby: WeightMustBePositive

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Hmotnost musí být kladná.

## <a name="cause"></a>Příčina

Pole **Hrubá hmotnost** je nastaveno na hodnotu *0* (nula) nebo na zápornou hodnotu.

## <a name="resolution"></a>Rozlišení

Chcete-li zadat hmotnost, proveďte jeden z následujících kroků.

- V poli **Hrubá hmotnost** nastavte hodnotu. Poté vyberte jednotku z rozevíracího seznamu.
- Výběrem možnosti **Získat systémovou hmotnost** vypočítejte hodnotu **Hrubá hmotnost**.

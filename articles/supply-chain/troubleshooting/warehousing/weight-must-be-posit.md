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
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924296"
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

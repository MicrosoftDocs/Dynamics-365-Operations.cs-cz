---
title: Potvrzení dávky a poznávací značky
description: Toto téma popisuje, jak nastavit a použít potvrzení dávky a registrační značky z mobilního zařízení.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c309061b31f10209c22cb90cc08c971b697f6dc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233120"
---
# <a name="batch-and-license-plate-confirmation"></a>Potvrzení dávky a poznávací značky

[!include [banner](../includes/banner.md)]

Potvrzení dávky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná dávka. Při počátečním vyskladnění práce pro dávku pouze nad položkami, kde dávka nad označuje rozsah dávek vyšší než umístění v hierarchii vyhledávání, musíte ověřit, že vyskladněná dávka se shoduje dávkou na řádku práce.

Potvrzení registrační značky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná registrační značka. Při vyskladnění práce ze skladového místa fáze musíte ověřit, že vyskladněná registrační značka odpovídá registrační značce, která je přidružena k práci. Pokud práce začala naskenováním poznávací značky, tento krok potvrzení bude přeskočen.

## <a name="where-it-applies"></a>Kdy se to používá

Potvrzení platí v následujících situacích:

- Potvrzení dávky se týká počátečního vyskladnění práce pro dávku nad položky.
- Potvrzení poznávací značky platí pro vyskladnění ze skladových míst fáze.

> [!IMPORTANT]
> U potvrzení registrační značky není doplňování podporováno. Při provádění doplňovacích prací není vytvořen žádný krok potvrzení registrační značky.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Nastavení potvrzení dávky a poznávací značky

Můžete nakonfigurovat potvrzení dávky a poznávací značky z položek nabídky mobilního zařízení.

1. Z položek nabídky mobilního zařízení vstupte do nastavení potvrzení práce.  
1. Vyberte možnost pro potvrzení dávky nebo registrační značky. Obě možnosti jsou k dispozici pro vyskladnění typu práce, které nemají povolené automatické potvrzení.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
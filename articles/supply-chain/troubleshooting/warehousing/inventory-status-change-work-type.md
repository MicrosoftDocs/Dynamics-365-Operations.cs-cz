---
title: Jako typ práce nelze vybrat změnu stavu zásob
description: Nelze vytvořit řádek pracovní šablony pro změnu stavu zásob, protože typ práce používají pouze systémové procesy. Vyberte jiný typ práce.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475830"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Ve sloupci Typ práce nelze vybrat změnu stavu zásob

## <a name="symptoms"></a>Příznaky

Při konfiguraci Microsoft Dynamics 365 Supply Chain Management se může zobrazit následující chybová zpráva:

> Nelze vytvořit řádek pracovní šablony pro změnu stavu zásob, protože typ práce není platný. Vyberte jiný typ práce.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Typ práce *Změna stavu zásob* používají pouze systémové procesy. Tento údaj nelze nakonfigurovat. Vzhledem k tomu, že seznam typů práce je opraven jako výčet, nelze nadbytečné položky odfiltrovat z rozevírací nabídky **Typ práce**.

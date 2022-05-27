---
title: Fáze servisních zakázek
description: Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e748afbd159d7a8fca1372676872cc02dd7ea57
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671723"
---
# <a name="service-order-stages"></a>Fáze servisních zakázek   

[!include [banner](../includes/banner.md)]


Můžete nastavit fáze pro servisní zakázku a definovat tak úkoly, které musí být dokončeny, pořadí, ve kterém jsou dokončeny, a zaměstnance, kteří odpovídají za toto dokončení. Definováním fází servisní zakázky a jejich přiřazením k zaměstnancům můžete řídit tok servisní zakázky pomocí jednotlivých úloh, které provádějí různé osoby v rámci servisní organizace. Posloupnost fází musí obsahovat počáteční fázi.

Můžete také definovat akce, které jsou povoleny v každé fázi. Příklad zrušením zaškrtnutí políčka **Zaúčtovat** ve všech fázích mimo konečné fáze zabráníte zaúčtování servisních zakázek dříve, než projdou celou úplnou posloupností fází.

## <a name="branching-in-service-order-stages"></a>Větvení fází v servisní zakázce

Při nastavování servisní fáze můžete vytvořit více možností nebo větví dostupných pro výběr v další fázi služby. Všechny větve, které jste vytvořili, lze vybírat při dokončení počáteční fáze. Například můžete nastavit **Plánování** jako počáteční fázi. Vytvořte dvě fáze s názvem **Probíhá** a **Zrušeno** a poté vyberte **Plánování** jako jejich nadřazenou fázi. Přiřaďte fázi **Plánování** k prodejní objednávce. Po dokončení fáze plánování pro prodejní objednávku můžete vybrat fázi **Probíhá** (pokud je prodejní objednávka připravena pro práci), nebo se můžete rozhodnout vybrat fázi **Zrušeno** (pokud je prodejní objednávka zrušena).

## <a name="see-also"></a>Viz také

[Nastavit fáze servisních zakázek](set-up-service-order-stages.md)

[Změna fáze servisní zakázky](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
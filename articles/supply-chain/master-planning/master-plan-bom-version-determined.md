---
title: Určení verze kusovníku
description: Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efc980e3a3dfff6d163812396613a1493f4428a4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213784"
---
# <a name="determine-the-bom-version"></a>Určení verze kusovníku

[!include [banner](../includes/banner.md)]

Pokud má položka při rozpadu poptávky výchozí typ plánované objednávky Výroba, modul plánování najde platnou verzi kusovníku na základě pracoviště. 

Dimenze pracoviště je vždy známa a je uvedena v transakci poptávky. K určení použité verze kusovníku se využívá následující proces:

-   Pokud pro položku existuje verze kusovníku definovaná na pracovišti uvedeném v poptávce, bude použit kusovník specifický pro pracoviště.
-   Pokud pro položku neexistuje verze kusovníku definovaná pro pracoviště uvedené v poptávce, bude použit obecný kusovník. Obecný kusovník není vázán na pracoviště a platí pro více pracovišť. Pokud existuje obecný kusovník, bude použit.
-   V případě, že neexistuje žádná obecná verze kusovníku, kterou by bylo možné použít, rozpad poptávky se v tomto bodě zastaví.

Platná verze kusovníku, bez ohledu na to, zda se jedná o specifický kusovník pracoviště nebo obecný kusovník, musí splňovat vyžadovaná kritéria data a množství.






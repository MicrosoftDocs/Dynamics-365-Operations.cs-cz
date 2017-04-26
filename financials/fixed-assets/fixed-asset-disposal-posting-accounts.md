---
title: "Účty pro zaúčtování likvidace dlouhodobého majetku"
description: "V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 670a67de2287fa5d0be29463f6f456b27fd88000
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Účty pro zaúčtování likvidace dlouhodobého majetku

[!include[banner](../includes/banner.md)]


V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.

Na stránce Účetní profily dlouhodobého majetku na pevné záložce Účty hlavní knihy výběrem Vyřazení – prodej a Vyřazení – likvidace nastavte zaúčtování do hlavní knihy.

U obou typů transakcí je účet hlavní knihy pro hodnotu vyřazení dlouhodobého majetku zaúčtován na stranu Dal. Částka MD je zaúčtována na protiúčet, který může být například bankovní účet. Byl-li dlouhodobý majetek prodán zákazníkovi, použije se místo protiúčtu účet zákazníka.

Klepněte na tlačítko Vyřazení a poté klepněte na Prodej nebo Likvidace a poté nastavte podrobné účty pro vrácení zůstatkové účetní hodnoty dlouhodobého majetku. Také můžete zadat informace v polích Zaúčtovat hodnotu a Hodnota prodeje na stránce Parametry vyřazení. 

Transakce vyřazení pro položku dlouhodobého majetku ve fondu majetku s nízkou hodnotou snižuje čistou účetní hodnotu fondu majetku s nízkou hodnotou pouze o vyřazenou částku. Pokud je však hodnota prodeje položky majetku vyšší než čistá účetní hodnota fondu majetku s nízkou hodnotou, je hodnota fondu majetku s nízkou hodnotou snížena na nulovou hodnotu.







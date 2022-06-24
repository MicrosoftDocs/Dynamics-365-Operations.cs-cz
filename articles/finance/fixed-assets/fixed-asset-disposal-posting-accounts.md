---
title: Účty zaúčtování dlouhodobého majetku
description: V tomto článku je vysvětleno nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1272cdb16396d24b5495f023e7b9fe3dee341507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871326"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Účty zaúčtování dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje nastavení účtů pro zaúčtování do hlavní knihy pro účely vyřazení majetku.

Chcete-li nastavit účetní účty hlavní knihy, které se použijí při likvidaci majetku, vyberte **Likvidace – prodej** a **Likvidace – odpad** v pevné záložce **Hlavní účty** na stránce **Profily zaúčtování dlouhodobého majetku**.

U obou typů transakcí (likvidace majetku prodejem nebo vyhozením do odpadu) je účet hlavní knihy pro hodnotu vyřazení dlouhodobého majetku zaúčtován na stranu Dal. Částka MD je zaúčtována na protiúčet, který může být bankovní účet (například). Byl-li dlouhodobý majetek prodán zákazníkovi, použije se místo protiúčtu účet zákazníka. Více informací viz [Likvidace dlouhodobého majetku jako odpadu](dispose-of-a-fixed-asset-as-scrap.md).

Klepněte na tlačítko **Likvidace** a poté klepněte na **Prodej** nebo **Odpad** a poté nastavte podrobné účty pro vrácení zůstatkové účetní hodnoty dlouhodobého majetku. Také můžete zadat informace v polích **Zaúčtovat hodnotu** a **Hodnota prodeje** na stránce **Parametry likvidace**. 

Transakce vyřazení pro položku dlouhodobého majetku ve fondu majetku s nízkou hodnotou snižuje čistou účetní hodnotu fondu majetku s nízkou hodnotou pouze o vyřazenou částku. Pokud je však hodnota prodeje položky majetku vyšší než čistá účetní hodnota fondu majetku s nízkou hodnotou, je hodnota fondu majetku s nízkou hodnotou snížena na nulovou hodnotu.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

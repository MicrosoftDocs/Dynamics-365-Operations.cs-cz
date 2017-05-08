---
title: "nezdokumentovaný"
description: "Zpráva opatření je návrh vygenerovaný systémem na změnu existující plánované nebo potvrzené objednávky."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>nezdokumentovaný

Zpráva opatření je návrh vygenerovaný systémem na změnu existující plánované nebo potvrzené objednávky.

### <a name="introduction"></a>Úvod

Zprávy akcí jsou generovány při výpočtu hlavního plánování jako reakce na změněné požadavky. Na prodejní objednávce, pro kterou jste již vytvořili nákupní objednávku, se mohlo změnit například datum expedice nebo množství, aby byl splněn požadavek. V tomto případě se při výpočtu hlavního plánování vygeneruje jedna nebo více zpráv akcí, aby se aktualizovala nákupní objednávka. Můžete se rozhodnout, zda navržené změny provést.

Můžete nastavit způsob, jakým se zprávy akcí vypočítávají pro skupinu disponibility, kterou připojíte k položce.

 <a name="selecting-action-messages"></a> Volba zpráv akcí
==========================

Na stránce **Skupiny disponibility**můžete vybrat zprávy akcí, které má sytém vygenerovat, a skupiny disponibility nebo položky, na které se mají zprávy použít. Vybrat můžete následující zprávy akcí:

| Zpráva             | Popis                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Posunout**         | Pokud vyberete tuto zprávu, systém v případě potřeby vygeneruje zprávy akcí, aby se objednávka přesunula na dřívější datum. V poli **Doba posunutí** můžete nastavit také maximální počet dní mezi příjmem a výdejem bez posunutí. |
| **Odložit**        | Pokud vyberete tuto zprávu, systém v případě potřeby vygeneruje zprávy akcí, aby se objednávka přesunula na pozdější datum. V poli **Doba odkladu** můžete nastavit také maximální počet dní mezi příjmem a výdejem bez odkladu.       |
| **Snížení**        | Pokud vyberete tuto zprávu, výrobní zakázky, nákupní objednávky a jiné příjmové transakce se sníží tak, aby se zabránilo přebytku zásob.                                                                                                   |
| **Zvýšit**        | Pokud vyberete tuto zprávu, výrobní zakázky, nákupní objednávky a jiné příjmové transakce se zvýší tak, aby se zabránilo nedostatku zásob.                                                                                                    |
| **Odvozené akce** | Pokud vyberete tuto zprávu, zprávy akce se vytvoří pro odvozené požadavky, jako například akce pro objednávky komponent splňující výrobní požadavek.                                                                                                   |




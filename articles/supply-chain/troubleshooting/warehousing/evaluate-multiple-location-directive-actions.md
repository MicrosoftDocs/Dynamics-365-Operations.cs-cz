---
title: Vyhodnocení všech akcí pro směrnice umístění více SKU
description: Byla přidána nová funkce k vyhodnocení všech akcí pro více směrnic místa SKU. Tato stránka vás provede informacemi o tom, jak ji zapnout.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea265166902f85c2c09cae08ee6de5cd7094e1b4
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778395"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Možnost více SKU nevyhodnocuje více akcí direktivy umístění

## <a name="symptoms"></a>Příznaky

Směrnice skladového místa typu pracovního příkazu *Prodejní objednávky* a typu práce *Vložení* nehodnotí více akcí směrnic skladového místa, když je vybrána možnost **Vícenásobné SKU**. Vyhodnocuje se pouze první akce směrnice skladového místa.

## <a name="resolution"></a>Řešení

Ve verzi 10.0.15 byla přidána nová funkce *Vyhodnocení všech akcí pro směrnice skladového místa vícenásobného SKU* (viz [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Tato funkce vyhodnocuje všechny akce pro směrnice skladového místa vícenásobného SKU. Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Správci mohou pomocí stránky [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit či zakázat ji v případě potřeby.

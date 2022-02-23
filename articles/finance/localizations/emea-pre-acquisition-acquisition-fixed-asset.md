---
title: Účtování předpořízení dlouhodobého majetku
description: Toto téma vysvětluje, jak vytvořit a zaúčtovat předpořízení dlouhodobého majetku.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264704
ms.search.region: Czech Republic, Hungary
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26eaf0b1cfb504e241f2f171fb79cbe6aed794c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407623"
---
# <a name="post-the-pre-acquisition-of-a-fixed-asset"></a>Účtování předpořízení dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit a zaúčtovat předpořízení dlouhodobého majetku.

**Poznámka:** Funkce pro účtování předpořízení dlouhodobého majetku je k dispozici pouze pro právnické osoby, které mají své primární adresy v Maďarsku a České republice. Předpořízení dlouhodobého majetku se neodpisuje a nemá vliv na náklady na pořízení nebo zůstatkové účetní hodnoty dlouhodobého majetku. Při účtování předpořízení, stav dlouhodobého majetku se změní na **Získáno**. Dlouhodobý majetek, který má stav **Získáno**, není odpisovatelný. Naproti tomu, při účtování pořízení se stav změní na **Otevřeno** a dlouhodobý majetek je odpisovatelný.

## <a name="set-up-pre-acquisitions"></a>Nastavení předpořízení
Předtím, než budete moci zaúčtovat předpořízení, je třeba dokončit toto nastavení.

-   Na stránce **Parametry dlouhodobého majetku** nastavte možnost **Povolit předpořízení** na **Ano**.
-   Na stránce **Účetní profily dlouhodobého majetku** nastavte účetní profil dlouhodobého majetku na typ zaúčtování předpořízení dlouhodobého majetku.

## <a name="post-a-preacquisition-of-a-fixed-asset"></a>Účtování předpořízení dlouhodobého majetku
1.  Na stránce **Dlouhodobý majetek** vytvořte nový deník a zadejte všechny příslušné údaje podle potřeby.
2.  U deníku, který jste právě vytvořili, klikněte na **Řádky** k otevření stránky **Doklad deníku**.
3.  Kliknutím na možnost **Nový** vytvořte řádek.
4.  V poli **Typ transakce** vyberte transakci typu **Předpořízení**.
5.  Podle potřeby zadejte hodnoty pro zbývající pole.
6.  Kliknutím na možnost **Ověřit** ověřte řádky deníku.
7.  Klikněte na **Návrhy** &gt; **Návrh předpořízení**.
8.  Kliknutím na **Vybrat** nastavte kritéria výběru a klikněte na **OK**.
9.  Kliknutím na tlačítko **OK** zavřete stránku **Návrh předpořízení**.
10. Kliknutím na **Zaúčtovat** &gt; **Zaúčtovat** zaúčtujte transakci předpořízení. Stav dlouhodobého majetku na stránce **Knihy** by teď měl být **Pořízené**.





---
title: Vytvoření účetních struktur
description: Tento průvodce úkoly vás provede vytvořením účetní struktury.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93cc2e9ceb15070491bb3d0a790367e6d5bf8c4a30cd7efa690fd825963165b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779534"
---
# <a name="create-account-structures"></a>Vytvoření účetních struktur

[!include [banner](../../includes/banner.md)]

Tento průvodce úkoly vás provede vytvořením účetní struktury. Kroky používají ukázková data společnosti USMF.

1. Přejděte na **navigační podokno > Moduly > Hlavní kniha > Účetní osnovy > Struktury > Konfigurovat účetní struktury**.
2. V **podokně akcí** klikněte na **Nové** a otevřete rozbalovací dialogové okno.
3. Do pole **Účetní struktura** zadejte název popisující účel účetní struktury.
4. Do pole **Popis** zadejte popis specifikující účel účetní struktury.
5. Klepněte na volbu **Nový**.
6. V části **Segmenty a povolené hodnoty** klikněte na **Přidat segment**.
7. V seznamu dimenzí vyberte dimenzi k přidání do účetní struktury.
8. Na konci seznamu klikněte na možnost **Přidat segment**.
9. Podle potřeby zopakujte kroky 6 až 9.
10. V části **Podrobnosti povolené hodnoty** vyberte segment k úpravě povolených hodnot.
    Klikněte například na pole **Hlavní účet**.  
11. V poli **Operátor** vyberte možnost, jako je „mezi“ a „zahrnuje“.
12. Zadejte hodnotu do pole **Hodnota**. Například 600 000.  
13. Zadejte hodnotu do pole **prostřednictvím**. Například 699 999.  
14. V části **Podrobnosti povolené hodnoty** klikněte na **Použít**.
15. Podle potřeby zopakujte kroky 10 až 15.  
16. V části **Podrobnosti povolené hodnoty** klikněte na **Přidat nová kritéria**.
17. V poli Operátor vyberte možnost, jako je „mezi“ a „zahrnuje“.
18. Zadejte hodnotu do pole **Hodnota**. Například 033.  
19. Zadejte hodnotu do pole **prostřednictvím**. Například 034.  
20. Klikněte na **Použít**.
21. V mřížce vyberte segment k úpravě povolených hodnot. Například Nákladové středisko.  
22. Zadejte hodnotu do pole **Nákladové středisko**. Například 007…021.  
23. V části **Segmenty a povolené hodnoty** klikněte na **Přidat**.
24. Zadejte hodnotu do pole **Hlavní účet**. Například 600 000…699 999.  
25. V mřížce vyberte segment k úpravě povolených hodnot. Například Oddělení.  
26. Zadejte hodnotu do pole Oddělení. Například 032.  
27. Zadejte hodnotu do pole Nákladové středisko. Například 086.  
28. V **podokně akcí** klikněte na možnost **Ověřit**.
29. V **podokně akcí** klikněte na možnost **Aktivovat**.
30. Klepněte na tlačítko **Aktivovat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
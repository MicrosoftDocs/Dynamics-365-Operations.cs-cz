---
title: Vytvoření kusovníku pro základní produkt založený na dimenzích
description: V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715764"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Vytvoření kusovníku pro základní produkt založený na dimenzích

[!include [banner](../../includes/banner.md)]

V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů. První 4 záznamy jsou věnovány nastavení data potřebného k dokončení tohoto postupu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento úkol obvykle zpracovává návrhář produktu.

## <a name="select-the-product"></a>Výběr produktu

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Označte na seznamu vybraný řádek.
    * Vyhledejte uvolněný základní produkt s konfigurací založenou na dimenzích, kterou jste vytvořili v rámci příručky pro první úlohy v tomto pořadí.  
1. V podokně akcí zvolte **Technik**.
1. Vyberte **Verze kusovníku**.

## <a name="create-new-bom-and-bom-version"></a>Vytvoření nového kusovníku a verze kusovníku

1. Zvolte **Nové**.
1. Vyberte **Kusovník a verze kusovníku**.
1. Zadejte hodnotu do pole **Název**.
    * Nastavení pracoviště  
    * V tomto postupu nebudeme nastavovat konkrétní pracoviště pro kusovník.  
1. Vyberte **OK**.
1. Zvolte **Nové**.
    * V tomto postupu přidáme čtyři řádky do kusovníku. Dva řádky představují možnosti pro kabel a dva řádky představují možnosti pro kabinet.  
1. Označte v seznamu vybraný řádek.
1. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
    * Vyberte číslo položky A0001, kabely HDMI 6'.  
1. V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabelu vytvořenou v příručce 4 v tomto pořadí.  
1. Zvolte **Nové**.
    * Vyberte číslo položky A0002, kabely HDMI 12'.  
1. Označte na seznamu vybraný řádek.
1. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
1. V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.
    * Vyberte znovu skupinu konfigurace kabelu.  
1. Zvolte **Nové**.
1. Označte na seznamu vybraný řádek.
1. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
    * Výběr číslo položky D0002 kabinet.  
1. V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabinetu pro tento řádek kusovníku.  
1. Zvolte **Nové**.
1. Označte na seznamu vybraný řádek.
1. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
    * Vyberte číslo položky M0007 standardní kabinet jako poslední řádek kusovníku.  
1. V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.
    * Vyberte skupinu konfigurace kabinetu pro poslední řádek kusovníku.  

## <a name="approve-and-activate"></a>Schválit a aktivovat

1. Zavřete stránku.
1. Vyberte **Schválit**.
1. V poli **Schválil(a)** zadejte nebo vyberte hodnotu.
1. Vyberte *Ano* v poli **Chcete kusovník také schválit?**.
1. Vyberte **OK**.
1. Vyberte **Aktivovat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
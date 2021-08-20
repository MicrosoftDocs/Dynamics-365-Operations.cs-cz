---
title: Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby
description: Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1288867dbfee12f0fd50550aa8974d692ac271bb4b6bdbbd1e2423cd8d3413a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756019"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby

[!include [banner](../../includes/banner.md)]

Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce. Je nutné nastavit index paliva dopravce před spuštěním tohoto průvodce. K tomu můžete použít postup "Nastavení indexu paliva dopravce". Tyto úlohy nastavení jsou obvykle prováděny manažerem logistiky. Jako ukázková data pro tento postup slouží data USMF.


## <a name="create-an-accessorial-master"></a>Vytvoření hlavní dodatečné služby
1. Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Hlavní dodatečná služba.
4. Zadejte hodnotu do pole Název.
5. Klikněte na položku Uložit.

## <a name="create-a-carrier-accessorial-charge"></a>Vytvoření nákladů na dodatečné služby dopravce
1. Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Náklady na dodatečné služby dopravce.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID dodatečné služby dopravce.
4. V poli Dopravce dodávky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V tomto příkladu vyberte Dopravce s nákladními vozy.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Služba dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V tomto příkladu vyberte nově vytvořenou hlavní dodatečnou službu.  
11. Klikněte na položku Uložit.

## <a name="create-an-accessorial-assignment"></a>Vytvoření přiřazení doplňkové služby
1. Klikněte na možnost Přiřazení dodatečných služeb.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Přepněte rozšíření oddílu Kritéria.
    * U kritéria můžete zvolit, aby se vždy použil palivový příplatek, nebo v tomto příkladu zvolte, aby byl použit jen v určité oblasti.  
5. V poli PSČ původního místa zadejte hodnotu.
6. V poli PSČ místa určení zadejte hodnotu.
7. Přepněte rozšíření oddílu Výpočet.
    * V části pro kalkulaci můžete určit způsob výpočtu palivového příplatku. Tento výpočet závisí na jednotce dodatečné služby, kterou jste vybrali jako základ výpočtu.  
8. V poli Typ poplatku za dodatečné služby vyberte „Palivový příplatek“.
9. Vyberte možnost Vzdálenost v poli Jednotka dodatečné služby.
10. V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. Klikněte na položku Uložit.

## <a name="update-the-carrier-rating-profile"></a>Aktualizace profilu hodnocení dopravce
1. Přejděte do nabídky Správa přepravy > Nastavení > Dopravci > Dopravci.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Rozbalte oddíl Profily sazeb.
4. Klikněte na možnost Upravit.
5. V poli Index paliva dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
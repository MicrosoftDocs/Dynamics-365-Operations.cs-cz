---
title: Konfigurace přístupových práv pro kontrolora objektu nákladů
description: Pomocí tohoto postupu proveďte konfiguraci přístupových práv pro kontroloru objektu nákladů.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b62e5765964a13357e0e7b663be1c7fd2cc19037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208792"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigurace přístupových práv pro kontrolora objektu nákladů

[!include [banner](../../includes/banner.md)]

Pomocí tohoto postupu proveďte konfiguraci přístupových práv pro kontroloru objektu nákladů. Tento záznam používá v ukázkových datech společnost USP2.


## <a name="assign-the-cost-object-controller-role"></a>Přiřazení role kontrolora objektu nákladů
1. Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Uživatelské jméno pomocí hodnoty „alicia“.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost Přiřadit role.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
6. Klikněte na tlačítko OK.

## <a name="enable-access-list-security"></a>Povolení zabezpečení přístupového seznamu
1. Přejděte na Nákladové účetnictví > Dimenze > Hierarchie dimenzí.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte organizaci.  
3. Klikněte na položku Upravit.
4. V poli Hierarchie přístupového seznamu vyberte možnost Ano.
5. Klikněte na Zobrazit hierarchii.

## <a name="assign-access-rights-to-user"></a>Přiřazení přístupových práv uživateli
1. Klikněte na položku Nová.
2. Označte v seznamu vybraný řádek.
3. V poli ID uživatele zadejte nebo vyberte hodnotu.
    * Vyberte správce.  
4. Ve stromovém zobrazení vyberte 'Organization\CEO\CFO\FIM'.
5. Klikněte na položku Nová.
6. Označte v seznamu vybraný řádek.
7. V poli ID uživatele zadejte nebo vyberte hodnotu.
    * Vyberte Alicia.  
8. Klikněte na položku Uložit.

## <a name="enable-access-rights-in-cost-accounting"></a>Povolení přístupových práv v nákladovém účetnictví
1. Přejděte na Nákladové účetnictví > Nastavení > Parametry.
2. Klikněte na záložku Obecné.
3. Zvolte parametr Ano v poli Povolit přístup k zobrazení pro členy dimenze objektu nákladů.
4. Klikněte na položku Uložit.
5. Zavřete stránku.
6. Přejděte na Nákladové účetnictví > Nastavení > Konfigurace pracovního prostoru pro řízení nákladů.
7. Klikněte na položku Upravit.
8. Vyberte možnost Ano v poli Publikováno.
    * Pokud vyberete Ano, uživatel s přiřazenou některou z následujících čtyř rolí si může zobrazit sestavy v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní, úředník na pozici nákladového účetního nebo kontrolor objektu nákladů. Pokud vyberete Ne, pouze uživatel s přiřazenou některou z následujících rolí si může zobrazit sestavy: manažer nákladového účetnictví, nákladový účetní a úředník na pozici nákladového účetního.    
9. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]